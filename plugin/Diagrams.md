# Diagrams

## Description for Model

You should use this plugin when users request visualizations or ask follow-up questions about a diagram or any modifications thereof.
Examples of user prompts to use this plugin include:
"Explain how a computer works using a visual diagram."
"Describe the process of create a REST API on AWS."
"How does a jet engine work?"
"Show me how ... works."
"Show me a network diagram of ... ."

This plugin is also useful when a you receive a question about how something works, requires an explanation about an idea or process, summarization, or asks for a description of a process. Any prompt that can be effectively summarized or explained in the format of a state diagram, UML diagram, graph or other types of diagrams can be visualized using this plugin.  We will talk more about the types of diagrams which are supported in a bit.

To create a request to the plugin API, create the diagram based on what the user asked and pass it to the plugin API to render. Kroki supports a wide range of syntaxes including Mermaid, GraphViz, PlantUML, and many more.  Neo4J uses Cypher to create network graph diagrams.

When creating diagrams:

Prefer hierarchical layouts for diagrams, and avoid linear diagrams.
If there are multiple options, choose the best one and let the user know about the other options available.
Here is a list of symbols which should not be used, for what purpose and what to use instead, delimited by commas:

- ampersand &, label, "and"
- round brackets (), node identifiers node labels edge labels, comma ,
- empty text "", edges, use a label if it is not the same as the target node

Each type of diagram has a different syntax.  If you do not know the syntax, do not use that type.

Things to always do:

Use short node identifiers, for example, P for Patient or AI for Artificial Intelligence.
Use double-quotes for all labels, nodes and edges.

Things to never do:
Referring to a subgraph root node from within a subgraph itself is a syntax error and will fail so don't do it ever.
This is wrong:

digraph G {
  subgraph cluster_A {
    label="X";
    T [label="Y"];
    A -> A0;
  }

  subgraph cluster_A0 {
    label="Z";
  }
}

The correct way to do it:
digraph G {
  subgraph cluster_A {
    label="X";
    T [label="Y"];
  }

  A -> A0;

  subgraph cluster_A0 {
    label="Z";
  }
}


Examples of invoking the plugin API:

User asks: "Show me how to design an N-tier architecture."
Your call to the api:

{
  "diagram_type": "graphviz",
  "diagram_source": "digraph G {\n rankdir=TB;\n node [shape=box];\n subgraph cluster_0 {\n label=\"Presentation Layer\";\n color=blue;\n P [label=\"Web Server (e.g., Apache, Nginx)\"];\n }\n subgraph cluster_1 {\n label=\"Application Layer\";\n color=green;\n A [label=\"Application Server (e.g.,{
}

User asks: "Draw me a mindmap for a luxury cosmetics rollout of a new product.  Use a maximum of 6 nodes."
Your call to the api:
```
{
  "diagram_type": "mermaid",
  "diagram_source": "graph TB\n  NP[\"New Product Rollout\"]\n  NP --> R[\"Research\"]\n  NP --> PD[\"Product Development\"]\n  NP --> M[\"Marketing\"]\n  NP --> D[\"Distribution\"]\n  NP --> S[\"Sales\"]"
}```

User asks: "Show me how a product reviewer can interact with amazon.com using plantuml."
Your call to the api:
```
{
  "diagram_type": "plantuml",
  "diagram_source": "@startuml\n left to right direction\n actor \"Product Reviewer\" as pr\n rectangle Amazon {\n usecase \"Browse Products\" as UC1\n usecase \"Purchase Product\" as UC2\n usecase \"Write Review\" as UC3\n usecase \"Rate Product\" as UC4\n }\n pr --> UC1\n pr --> UC2\n pr --> UC3\n pr --> UC4\n @enduml"
}```


User asks: "Show me a network graph with the relationships between the members of the karate club."
Your call to the api:
```
{
  "diagram_type": "network",
  "diagram_source": "{\"directed\": false, \"multigraph\": false, \"graph\": {}, \"nodes\": [{\"id\": \"Member 1\"}, {\"id\": \"Member 2\"}, {\"id\": \"Member 3\"}, {\"id\": \"Member 4\"}, {\"id\": \"Member 5\"}, {\"id\": \"Member 6\"}, {\"id\": \"Member 7\"}, {\"id\": \"Member 8\"}, {\"id\": \"Member 9\"}, {\"id\": \"Member 10\"}], \"links\": [{\"source\": \"Member 1\", \"target\": \"Member 2\"}, {\"source\": \"Member 1\", \"target\": \"Member 3\"}, {\"source\": \"Member 1\", \"target\": \"Member 8\"}, {\"source\": \"Member 2\", \"target\": \"Member 4\"}, {\"source\": \"Member 2\", \"target\": \"Member 5\"}, {\"source\": \"Member 2\", \"target\": \"Member 9\"}, {\"source\": \"Member 3\", \"target\": \"Member 6\"}, {\"source\": \"Member 3\", \"target\": \"Member 10\"}, {\"source\": \"Member 4\", \"target\": \"Member 7\"}, {\"source\": \"Member 5\", \"target\": \"Member 8\"}, {\"source\": \"Member 6\", \"target\": \"Member 9\"}, {\"source\": \"Member 7\", \"target\": \"Member 10\"}]}"
}```


When the user requests revisions to the diagram, for example, they ask to draw the crossover node in green then call the api with the same `diagram_type` parameter and the modified `diagram_source` text.

Interpreting the API response:

When you get the response, it will either include an image URL or an image. Render either of these inline using the alt text syntax.
You should create the response in this order: first the image, then suggestion to edit using words, then the edit link, then the textual explanation.

Important Tips:

Do not repeat the same link.
If an errorMessage is included in the response, show it to the user, don't try to render the diagram inline, still suggest they can edit it online or try again.
Add textual explanation of the diagram contents in the end of the message. Keep it brief unless the user asks for more details.
Do not use alias names in the textual explanation such as "Food_Critic" or "fc", just use the displayed name like "Food Critic".
Don't show the diagram block unless the user asks for it.


