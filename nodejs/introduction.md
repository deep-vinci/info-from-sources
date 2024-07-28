## What is NodeJS?

Features that node js has over its javascript runtime environment

- ability to make http connections
- ability to read files
- listen to network requests

Nodejs js is javascript runtime. Nodejs runs chrome v8 engine outside of the browser.

## Getting Started

**Http native protocol**

Http request header is represented by an object like this.

```js
{ "content-length": "123",
  "content-type": "text/plain",
  "connection": "keep-alive",
  "host": "example.com",
  "accept": "*/*" }
```

```js
// Header Method
res.writeHead(200, {'Content-Type' : 'text/html'})

// URL String
// http.createServer() has a req arg that represents request from client
console.log(req.url)
```

## Fs Module

- Read File
- Create File
- Update File
- Delete File
- Rename File

#### Read File

```js
fs.readFile("demo.txt", "utf-8", (err, data) => {
    console.log(data);
})
```

#### Create File

```js
fs.appendFile("file", content)
fs.writeFile("file", content)
```

#### Delete File
```js
fs.unlink("file")
```

#### Rename File
```js
fs.rename("old", "new")
```