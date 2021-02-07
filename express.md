# Express Cheat Sheet
Express is a Node *framework* that helps organize and structure web applications built with Node.
## Getting started
```
npm install express
```
Barebones of an express server:
```javacsript
const express = require('express');

const app = express();
// A function that represents the express module

app.listen(3000);
// Listens for an http request on port 3000
```
