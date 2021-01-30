# Node Cheat Sheet
## What is node.js?
Node.js is a runtime environment that allows us to execute JavaScript code outside a web browser. It is particularly useful in running server-side scripts in the backend environment.
## npm Commands
Creating a package.json file for your project
```
npm init
```
Installing project dependencies
```
npm install <node package>
```

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
