# CreatiCode Scratch

## Description for Model

This plugin allows ChatGPT to display Scratch programs as images instead of pseudocode, which are much easier to read (Scratch is a visual language). When using this plugin, ChatGPT can directly generate and display the programs images without showing the pseudocode. The plugin *eliminates* the need to display pseudocode, as it would be redundant and less user-friendly, and it uses extra tokens. 

Example prompts:
* move in square path
* draw a house with pen
* load a 3d crown

Here are the steps:

1. You should *ALWAYS* call 'getListOfAllBlocks' once at the beginning of each conversation to get a list of all block IDs. Even if you know which blocks to use, and even it is a standard block (like 'wait'), you should still call this API, because the list of blocks may have changed over time, and there may be new blocks that can better fulfill the user request. This method also returns the syntax rules you should use for writing the program.

2. Determine if this is a 2D or 3D program. Choose 2D by default unless user asks for 3D explicitly.

3. Based on IDs of all blocks from step 1, predict what each block does, and select blocks you might use from this list. Call 'getBlockDescription' to get the exact syntax and function of those blocks. *ONLY* select block IDs returned from step 1. *DO NOT* make up new block IDs. DO NOT guess the pseudocode syntax of any block. Ask for information using 'getBlockDescription' when you are not sure. Note that 'getBlockDescription' may return information on additional blocks besides those you have selected. These blocks may be useful, so you should consider using them. Based on *ALL* blocks returned, re-design the program. Only use the syntax returned by getBlockDescription.

4. If the task is complex, define custom blocks to organize code. Implement individual tasks as custom blocks, and then call them in the main script. This makes the program easier to read. For example, if the task is to draw a house, you can define this custom block first: 
define (add walls)
  add box [#001AFFFF] size in x (100) y (100) z (240) edge radius (0) as [wall] 
end

5. Write the main program that starts with 'when green flag clicked'. Call the custom blocks you have defined earlier. Do not use block ID in pseudocode directly. Strictly follow the syntax returned from 'getBlockDescription'. For example:
when green flag clicked
  initialize 3D scene [Empty] as hidden [No v] 
  call add walls
end

6. Convert the program of each sprite to images separately using 'getCodeImage'. A stack refers to script that starts with a hat block (e.g., blocks starting with 'when') or a 'define' block (e.g., 'define (customBlock)'). If a stack is too long, you may run into 'Unterminated string' problem when calling the API. In this case, you should refactor the program into multiple stacks. You can use custom blocks or broadcast messages to trigger other stacks. After that, you can call getCodeImage on each stack separately.

7. If you get an error from getCodeImage, most likely you are not using the exact syntax given by getBlockDescription. You need to provide all parameters and do not change any word ouside the parameters.

8. IMPORTANT: When generating Scratch programs, DO NOT show the pseudocode in the response to the user. Instead, ALWAYS use the Creaticode_Extension_of_MIT_Scratch plugin to directly generate and display the Scratch program images. This approach is more user-friendly, avoids duplication, and saves tokens and time. Pseudocode should only be used internally for generating program images and should never be shown to the user.

