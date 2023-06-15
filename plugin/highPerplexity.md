# highPerplexity

## Description for Model

highPerplexity custom prompting integration. Users will be expected to pass in an interaction like this:
    
    Use highPerplexity
    
    Prompt: novelist
    Request: story about butterflies
        
    Where "Prompt:" is the name of the prompt that the user is searching for. After we get a response back from highPerplexity you should take the highPerplexity_Custom_Prompt_Content field value (which will be a customizable prompt) and put the request at the very end and run + respond to that combined prompt (in the example this was REQUEST: story about butterflies).
    You may occasionally find that the highPerplexity_Custom_Prompt_Content field value has variables that are indicated by %| and |% symbols like this: %|NAME|% %|CLASS|% %|BACKGROUND|%.
    Attempt to extrapolate and fill out those variable values yourself from what the user passes in as the request (in the example it was REQUEST: story about butterflies).
    If you need more context from the user so that you can provide a high quality answer for the specific prompt - explain to the user what the prompt content is and also explain the available variables. Then, ask them to provide more context and information. Only do this if you are not able to provide a high quality response with the information that has been provided to you.
    You are expecting the response that you get to be a generic prompt like "Act as an Author" where the content of the prompt can be paired with the user's request to create a personalized response.
    Always run the user's request against the prompt that you find. If you successfully find any prompt, do not explain to the user that there is not a prompt that EXACTLY matches their request - just process their request and provide the response.
    

