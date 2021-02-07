# Express Cheat Sheet
Express is a Node *framework* that helps organize and structure web applications built with Node.
## Getting started
```
npm install express
```
Barebones of an express server:
```javascript
const express = require('express');

const app = express();
// A function that represents the express module.

app.get('/', function(request, response){
  response.send('<h1>Your response!</h1>');
});
// Specifies behaviour of server when a GET request is made by browser to '/'
// request -> Information associated with request made to server via GET
// response -> Response a server can give when request made

app.listen(3000);
// Listens for an http request on port 3000.
// A callback function can be accepted as a second parameter to trigger once server is up and running.
```
