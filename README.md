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

### Reading and Writing Files

Node.js provides the fs (File System) module to interact with the file system on your computer.

Reading Files

To read a file, you can use the fs.readFile method:

```javascript
const fs = require('fs');

fs.readFile('./path/to/your/file.txt', 'utf8', (err, data) => {
 if (err) {
    console.error('Error reading file:', err);
    return;
 }
 console.log('File content:', data);
});
```
Writing Files

To write to a file, you can use the fs.writeFile method:

```javascript
const fs = require('fs');

fs.writeFile('./path/to/your/file.txt', 'Hello, World!', (err) => {
 if (err) {
    console.error('Error writing file:', err);
    return;
 }
 console.log('File has been written');
});
```

### Working with JSON Files

Node.js makes it easy to work with JSON files. You can read and write JSON data using the fs module.

Reading JSON Files

```javascript
const fs = require('fs');

fs.readFile('./path/to/your/data.json', 'utf8', (err, data) => {
 if (err) {
    console.error('Error reading JSON file:', err);
    return;
 }
 const jsonData = JSON.parse(data);
 console.log('JSON data:', jsonData);
});
```
