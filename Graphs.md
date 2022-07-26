# Graphs

When i think of a Graph, i probably think of those long vertical bars that represent a numeric value, the kind you used to see in 
your Math book in school (and maybe still do).
But those aren’t the graphs we’re talking about here; instead, think of a spider web-shaped structure with interconnected parts 
that represent a whole.
So, let’s delve into what graphs are; usually, a graph has two basic components called Nodes and Edges. Nodes are connected using 
Edges; the first two Nodes are connected using Edges; then, Nodes can be connected in any number.

Thus, graphs are excellent because of how they are structured when you want to represent a relationship between certain concepts 
or entities. You have different representation types, algorithms, and data structures to work with.

most efficient use of graphs. The most important factors for deciding what data structures to use are Memory and Time complexity.

### Tools Used in Graphs

1.Query & Mutate Using Algorithms
2.Serialize / Deserialize
3.Visualize

### QuickGraph Library

QuickGraph is a .NET library of graphs structures and algorithms for C#. It provides direct/indirect graph data structures.
Its algorithms are depth-first search, breath-first search, A* search, shortest path, k-shortest path, and maximum flow.
QuickGraph is free and open-source software that allows you to construct data structures and algorithms in .NET. It also provides 
basic serialization/deserialization support and some visualization features, though they are not stable.

QuickGraph’s algorithm library is quite versatile and includes practically anything you would need; it seldom falls short in 
terms of usability, and the data structures cover a lot of territories and will supply you with what you need in most 
circumstances.

QuickGraph’s major flaw is its extremely improper documentation; it is scarcely useable and, in some cases, simply incorrect, 
very simple and lacking in diversity. The API changes while the docs do not adhere to this change in many cases.

This will complicate the process by making you rely on manually checking the library source; hence it is quite frustrating.

The major reason for this is probably the poor maintenance, as the project is still stuck at its version 3.6, and this update 
came in mid-2011, which is more than a decade ago! Many appreciations to the developer; however, upkeep has to be better.

### Deserialization
Deserialization means changing the format of the graph from one to the other; this is important when you need to export the graph 
to some other application, updating its context and use according to your needs.
Although QuickGraph gives you the option to serialize to GraphML, you will need to code the serialization on your own for many 
other formats as there are many formats such as XML and CSV.

### GraphDB
GraphDB allows you to treat nodes and edges as records or values instead of implicit relationships between tables, as in the case 
of a relational DB.
This gives you a more natural and more functional graph data processing.

### Visualization
Visualization is one of the most vital aspects of any process, as giving a graphical representation to a code makes it much more easily understandable and interactive. It makes work much more fluid and quicker.

There are various visualization tools available, one of which is the yEd Graphic Editor. This application is fantastic, and it’s 
even better because it’s available for free!

Its layout engine, as well as the customization tools that come with it, are fantastic.

Then there’s GraphViz, which is open-source and widely used in academic circles for graph visualization; DOT language scripts are 
used. It allows you to save schematics as pictures (SVG, for example).

Then there is Microsoft Automatic Graph Layout. This is similar to GraphViz but more basic and compatible with the Windows and .
NET ecosystem.

Finally, Gephi is an extremely sophisticated tool that can be used for much more than just visualization. It’s also free and 
open-source.
It offers extensive plug-in support. It is the most effective visualization tool.



