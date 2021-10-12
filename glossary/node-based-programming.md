# Node-Based Programming

Things to know about node-based programming:

### Each node is like a step in a process

Nodes will usually be connected from the output of one node to the input of the next and each changes the values, audio, visuals, etc. Sometimes, you could have nodes go on their own path and get reincorporated into the main path.

### Outputs and inputs generally have to match

In some languages, a node could have multiple output data types - they should connect to a matching input type (an RGB color connecting to an input expecting RGB color). Some programs will take whatever info is available in the output to make it fit. TouchDesigner separates nodes based on types and can be converted to other types.

### Each node will have parameters

Depending on what the node is, each will have controllable aspects (speed, file to use, volume, etc.) and usually, there is a way to access values outside the node to use in these situations.

