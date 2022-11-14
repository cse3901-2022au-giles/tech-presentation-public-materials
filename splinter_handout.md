# Splinter Handout

## Presentation
[Link to Presentation](https://docs.google.com/presentation/d/15gvJLGxGktgb-KgyH5_OsRGgxxXO2A2_jAQtBo_ti7s/edit#slide=id.g1925d817904_0_33)

## Learning Objectives

* Be competent in distinguishing when to/not to utilize Node.js
* Be familiar with Node.js Modules
* Be familiar with advantages versus disadvantages of a single threaded asynchronous runtime environment
* Be familiar with common Node.js functions
* Be familiar with how Node.js is used in a Tech Stack
* Be familiar with common Node.js Frameworks
* Be familiar with Node Package Manager

## Knowledge Check

1. **Would a collection of libraries that help establish communication between a web client and server most likely be considered a tech stack or a framework?**

2. **What is a runtime environment? Can you think of other examples of runtime environments?**

3. **True or False: Node.js is a multi-threaded platform**

4. **What is NPM?**

5. **Node.js runs on the**
    1. Browser
    2. Server
    3. Both Browser and Server

6. **How do you expose a Node.js Module?**

7. **Would it make sense to use Node.js for applications with intensive server-side computations? Why or why not?**

## Common Node.js Modules
 
### HTTP
 
The `http` module provides support for the Hypertext Transfer Protocol (HTTP).  Import the `http` module with:
 
```js
const http = require('http');
```
 
The `http` module includes functions to create an HTTP server,
 
```js
const server = http.createServer( (req, res) => { … } );
```
 
get the request header,
 
```js
const headers = req.getHeaders();
```
 
set the response header,
 
```js
res.setHeader('Content-Type', 'text/html');
```
 
and listen on a specified hostname and port number.
 
```js
server.listen( port, hostname, () => { … } );
```
 ---
### URL
 
The `url` module provides support for Universal Resource Locator (URL) address resolution.  Import the `url` module with:
 
```js
const url = require('url');
```
 
The `url` module includes functions to parse a URL from a string,
 
```js
const myURL =url.parse('http://www.google.com');
```
 
set the protocol portion of the URL,
 
```js
myURL.protocol = 'http';
```
 
set the hostname portion of the URL,
 
```js
myURL.hostname = 'google.com';
```
 
set the port number portion of the URL,
 
```js
myURL.port = '80';
```
 
and set the pathname portion of the URL.
 
```js
myURL.pathname = ‘/search?q=port+80’;
```
--- 
### Domain Name System (DNS)
 
The `dns` module provides support for Domain Name System (DNS) naming resolution.  Import the `dns` module with:
 
```js
const dns = require('dns');
```
 
The `dns` module includes functions to resolve a hostname, such as `’google.com’` into an array of resource records.
 
```js
dns.resolve('google.com', (err, records) => { … } );
```
 ---
### File System (FS)
 
The `fs` module provides support for interacting with the file system.  Import the `fs` module with:
 
```js
const fs = require('fs');
```
 
The `fs` module includes functions to open a file and set the file descriptor `fd`,
 
```js
fs.open(‘example.txt', (err, fd) => { … } );
```
 
read from a file into a buffer,
 
```js
fs.read(‘example.txt’, buffer, (err, bytesRead, buff) => { … } );
```
 
write a buffer to a file,
 
```js
fs.write(‘example.txt’, buffer, (err, bytesWritten, buffer) => { … } );
```
 
and close a file.
 
```js
fs.close(fd);
```

## Node.js Installation

### Windows Installation
To install Node for Windows, you should download the .msi file listed on the [Node.js](https://nodejs.org/en/download/) website. Run the file, and choose your desired path to install Node.js. The default setting should now include npm package manager (you will probably want this; see the NPM tab for more information), but just make sure it is set to install on in the Custom Setup section of your installer.
![Window Installation](/images/WindowsInstallation.JPG)

### Macintosh Installation
Download .pkg file for Mac from [Node.js](https://nodejs.org/en/download/) website and run installer.

Update NPM version by running following command:
```
$ sudo npm install npm --global
```
Also need to set NODE HOME by running the following commands:
```
$ echo ‘export PATH=/usr/local/bin:$PATH’ >>~/.bash\_profile
$ source ~/.bashrc
```

