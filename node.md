# Node Cheat Sheet
## What is Node.js?
Node.js is a runtime environment that allows us to execute JavaScript code outside a web browser. It is particularly useful in running server-side scripts in the backend environment.
## Node Modules
- Libraries supported by Node
### Installed Modules
- `require` is the equivalent of `import`. But, Node and V8 Chrome Engine existed before ES6. The import keyword works for Node. However, current best practices recommend continuing to use require.
- Visit nodejs.org/api for available modules.
Example using file system module:
```javascript
//jshint esversion:6

const fs = require('fs');
// require('<module name>');

fs.copyFileSync("file1.txt", "file2.txt");
// Copies content from one file to another.
```
### Internal Modules
Exporting Modules
- `module.exports` is an object created by a specific `module`. This object specifies whether a module can be exported to be used in other JavaScript files.
  ```javascript
  module.exports = {
    <module name>: <module name>
  };
  ```
- `exports` is a shorthand for `module.exports` that can't be used interchangably.
- `exports` is assigned `module.exports` prior to the module being evaluated.

Importing Modules
- Use require keyword to import modules:
  ```javascript
  const <module name> = require('./<module name>.js');
  
  const value = <module name>.<module method>();
  ```

### External Modules
Use npm:
1. `npm init` (If starting without a package.json file)
2. `npm install <package name>` (This downloads module and creates a dependency)
3. require the module `const <variable name> = require('<module name>')` inside the script file
4. use the module `<variable name>.<method>();`

## Useful Node Packages
### lite-server
- Creates a development server that can auto-update the page as files change.
- `--save-dev` option specifies that package is for development purpose only.
```
npm install --save-dev lite-server
```
Add script to package.json
```
"scripts": {
  "start": "lite-server"
}
```
Run development server
```
npm start
```
## Node Commands
### Node REPL
- Allows code to be written directly in terminal
- `Tab` enables smart selection of available commands
- Exit REPL using `.exit` or `Ctrl + c`
  
Starts node REPL (Read Evaluate Print Loop)
```
node
```

## Node Arguments in Terminal
- process.argv[0] represents the node binary
- process.argv[1] represents the javascript file
- process.argv[2] represents the first argument passed to program run in Node
  ```javascript
  const argument = process.argv[2];
  ```
  
  ## Environment
  ### Browser vs. Node
  The global object for the browser is
  ```
  window
  ```
  The global object for Node is
  ```
  global
  ```
  ### process.env
  process.env is a global object injected by Node at runtime.
  - Useful during deployment (e.g. server address change from development to production).
   
