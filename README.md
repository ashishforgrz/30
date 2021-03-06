# 30/05/2022

Express JS -
Express is a minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications

Node.js NPM -
package manager for Node.js packages
hosts thousands of free packages to download and use
syntax: npm install <package_name>

Get -
app.get() function lets you define a route handler for GET requests to a given URL
eg:
const app = require('express')();

// If you receive a GET request with `url = '/test'`, always
// send back an HTTP response with body 'ok'.
app.get('/test', function routeHandler(req, res) {
  res.send('ok');
});

Post -
Post method facilitates you to send large amount of data because data is send in the body
app.post() function routes the HTTP POST requests to the specified path with the specified callback functions
eg: 
var express = require('express');
var app = express();
var PORT = 3000;
  
app.post('/', (req, res) => {
  res.send("POST Request Called")
})
  
app.listen(PORT, function(err){
    if (err) console.log(err);
    console.log("Server listening on PORT", PORT);
}); 

Put -
The app.put() function routes the HTTP PUT requests to the specified path with the specified callback function
var express = require('express');
var app = express();
var PORT = 3000;
  
app.put('/', (req, res) => {
  res.send("PUT Request Called")
})
  
app.listen(PORT, function(err){
    if (err) console.log(err);
    console.log("Server listening on PORT", PORT);
}); 

Delete -
The app.delete() function is used to route the HTTP DELETE requests to the path 
var express = require('express');
var app = express();
var PORT = 3000;
 
app.delete('/', (req, res) => {
  res.send("DELETE Request Called")
})
 
app.listen(PORT, function(err){
    if (err) console.log(err);
    console.log("Server listening on PORT", PORT);
});


Middleware - 
Middleware functions are functions that have access to the request object, the response object , and the next function in the application's request-response cycle
eg: 
const express = require('express');
const app = express();

app.get('/', (req, res, next) => {
  res.send('Welcome Home');
});

app.listen(3000);

Routing -
Routing refers to how an application???s endpoints (URIs) respond to client requests
eg:
// GET method route
app.get('/', (req, res) => {
  res.send('GET request to the homepage')
})

// POST method route
app.post('/', (req, res) => {
  res.send('POST request to the homepage')
})

Request & Response -
request object represents the HTTP request and contains properties for the request query string
response specifies the HTTP response when an Express app gets an HTTP request
