# level-net-server

> LevelDB database exposed as a TCP server.

## Install

Install the level server and the `level` modules if you haven't.

```bash
$ npm i level-net-server level --save
```

## Require

```javascript
var Server = require('level-net-server')
```

## Create DB

```javascript
var level = require('level');

var db = level('/path/to/leveldb/dir', {createIfMissing: true});
```

## Create Server

```javascript
var server = Server(db);
```

## Make server listen on port

```javascript
server.listen(port, host, cb);
```

## Interact with it

You can use the [level-net-client](https://npmjs.org/package/level-net-client) to interact with this server.

## Close the server

```javascript
server.close(cb);
```