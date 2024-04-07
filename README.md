# Getting Started with Node.js

Node.js is a runtime environment that allows you to run JavaScript on the server side. It is built on Chrome's V8 JavaScript engine and is used for building scalable network applications. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient, perfect for data-intensive real-time applications that run across distributed devices.

## Installation

To get started with Node.js, first, download and install Node.js from the [official website](https://nodejs.org/en/download/).

Node.js comes with npm (Node Package Manager), which is used to install Node.js packages.

## Usage

### Creating a Simple Server

Here's a basic example of creating a server using Node.js:

```javascript
const http = require('http');

const server = http.createServer((req, res) => {
 res.statusCode = 200;
 res.setHeader('Content-Type', 'text/plain');
 res.end('Hello World\n');
});

server.listen(3000, '127.0.0.1', () => {
 console.log('Server running at http://127.0.0.1:3000/');
});
```
This code creates a simple HTTP server that listens on port 3000 and responds with "Hello World" for every request.
