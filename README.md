# tcp.js

tcp.js is a Node.js project making TCP communication easy in node.js. It tries to level out the difference between and a client, making the communication more simple. It also has built-in JSON encoding/decoding.

## How to Install

```bash
$ npm install tcp.js
```

## How to use

### Server

```js
var sockets = require('tcp.js').server(1337);

sockets.on('connection', function (socket) {
  socket.send('news', { hello: 'world'});
  socket.on('myEvent', function (data) {
    console.log(data);
  });
});
```

### Client

```js
var sockets = require('tcp.js').client('127.0.0.1', 1337);

sockets.on('connection', function(socket) {
  socket.on('news', function (data) {
    console.log(data);
    socket.send('myEvent', { my: 'data'});
  });    
});
```

## Author
This library is developed by kasmura

His website is www.kasmura.com

<<<<<<< HEAD
## License
NO RIGHTS RESERVED / ANTI-COPYRIGHT / UNLICENSE
=======
## (un)License
This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org/>
>>>>>>> Added underscore.js to dependencies
