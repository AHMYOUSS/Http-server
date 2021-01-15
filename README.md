What is Node.js?
let http = require('http')

let server = http.createServer(function(req, res) {

    // req: methods and properties for request
    // res: method and properties for response

    // Request & Response:
    // HEADER: information about the body, and info about destination, and source.
    // BODY (payload): data

    // Response Headers
    let responseHeaders = {
        'Content-Type': 'text/plain'
    }
    // Status Code:
    // 200 -> OK
    // 404 -> Not Found
    res.writeHead(200, responseHeaders)

    // Response Body
    res.write("Hello world")
    res.end()

})

let port = 8080

server.listen(port, function() {
    console.log(`Server listening on port ${port}...`)
})

Node.js is an open source server framework
Node.js is free
Node.js runs on various platforms (Windows, Linux, Unix, Mac OS X, etc.)
Node.js uses JavaScript on the server
Node.js is great for real-time services
Node.js is a JavaScript runtime built on Chrome's V8 JavaScript engine. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient.

V8 is Google's open source high-performance JavaScript engine, written in C++ and used in Chromium, Node.js and multiple other embedding applications.

npm is the package manager for Node.js, and it is the largest ecosystem of open source libraries in the world. Check out modulecounts.com.

Basically, Node.js enables JavaScript to run on the server/PC rather than the browser. Think of it as an alternative to PHP, C# .NET, and Java on the server.

With just this, node creates an HTTP server:
let http = require('http');

http.createServer(function (req, res) {
    res.writeHead(200, {'Content-Type': 'text/plain'});
    res.end('Hello World!');
}).listen(8080);
