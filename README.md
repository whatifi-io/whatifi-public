# definitions

The `definitions` files are going to be placed in a public repo, visible to the front-end and the decision engine. These files contain required data, context requirements, etc. of a specific node, and will be used to coordinate data collection, and processing between the front-end and decision engine.

# descriptions

The `descriptions` files are used to dictate the procedures of a node; these json files are temporary/act as examples for user submitted nodes, as nodes created in native Go perform better.

# nodeImports.json

This file is read by the engine to determine which nodes to import, and how.
