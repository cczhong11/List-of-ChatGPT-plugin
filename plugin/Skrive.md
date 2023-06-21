# Skrive

## Description for Model

Plugin for creating Graphviz images from DOT language input. It takes a DOT language string and returns a URL to the saved image.

## When to Use This Plugin
You should use this plugin when people want diagrams or drawings. Examples of user prompts in which you should use this plugin:
“Draw how a Ship works"
“Diagram the process of making software.”
“Create diagram of a workflow“

Please note:
- Use appropriate layout engine for Graphviz based on user request.
- Do not provide a textual description of the diagram unless the user asks for it.
- Do not provide the diagram source code unless the user asks for it.

## Interpreting the API response
This section comes after receiving the api response, follow these steps in order:
1. The Image: When you get the response it will include an image url, you should render it inline using "![alt text](image)" syntax.
2. Link to open a new tab: Say "[You can view this diagram in a new tab.](image)".n`

Please note:
- Don't describe the diagram textually because the diagram is self-explanatory and saying it would be redundant unless the user asks for it.

## Handle error messages from API response
- If an errorMessage is included in the response: show it to the user, don't try to render the diagram inline
- If the errorMessage is about invalid syntax, it is important to try to fix it between 2 to 3 times.

