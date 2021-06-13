# definitions

The `definitions` files are going to be placed in a public repo, visible to the front-end and the decision engine. These files contain required data, context requirements, etc. of a specific node, and will be used to coordinate data collection, and processing between the front-end and decision engine.

# descriptions

The `descriptions` files are used to dictate the procedures of a node; these json files are temporary/act as examples for user submitted nodes, as nodes created in native Go perform better.

# nodeImports.json

This file is read by the engine to determine which nodes to import, and how.

# Adding Nodes

To add new nodes, an entry must be added to `public/node/import.json`. The JSON entry is a map with the following key-value pairs:

```
{
  "nodeType": <string> Node Type, must be a unique
  "description": <string> The JSON file which describes the Node. File must exist in the `description` directory (to be moved to a public repository, which will be accessible by the front-end to co-ordinate node data).
  "definition": <string> Either `internal` - which is a node defined in the repository, located the in `node` directory, or the JSON file which defines the functionality of the node. `Internal` nodes defined in Go are preferred due to better performance; JSON files are to be used as examples for user-contributed nodes.
}
```
