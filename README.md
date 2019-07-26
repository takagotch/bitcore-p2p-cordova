### bitcore-p2p-cordova
---
https://github.com/getbitpocket/bitcore-p2p-cordova

```js
var peer = new bitcore.p2p.Peer({host:'bitcore-peer-ip'});

peer.on('ready',function(message) {
  console.log("version: " + peer.version + ", best height: " + peer.bestHeight);
});

peer.on('inv',function(message) {
  console.log("received inv message");
});

peer.connect();


var pool = new bitcore.p2p.Pool({
  network : 'testnet'
});

pool.on('peerready', function(peer) {
  console.log("Peer ready " + peer.host + ":" + peer.port);
});

pool.connect();
```

```sh
npm install
gulp build

npm install
gulp test
```

```
```


