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
