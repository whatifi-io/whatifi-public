# Adding Nodes

To add new nodes, an entry must be added to `nodeImports.json`. The JSON entry is a map with the following key-value pairs:

```
{
  "nodeType": <string> Node Type, must be a unique
  "description": <string> The JSON file which describes the Node. File must exist in the `description` directory (to be moved to a public repository, which will be accessible by the front-end to co-ordinate node data).
  "definition": <string> Either `internal` - which is a node defined in the repository, located the in `node` directory, or the JSON file which defines the functionality of the node. `Internal` nodes defined in Go are preferred due to better performance; JSON files are to be used as examples for user-contributed nodes.
}
```
