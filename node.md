# Node Cheat Sheet
## What is Node.js?
Node.js is a runtime environment that allows us to execute JavaScript code outside a web browser. It is particularly useful in running server-side scripts in the backend environment.
## Node Modules
- Libraries supported by Node
### Native Modules
- Visit nodejs.org/api for available modules.
Example using file system module:
```javascript
//jshint esversion:6

const fs = require('fs');
// require('<module name>');

fs.copyFileSync("file1.txt", "file2.txt");
// Copies content from one file to another.
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
- process.argv[2] represents the first argument passed to program run in node
  ```javascript
  const argument = process.argv[2];
  ```
