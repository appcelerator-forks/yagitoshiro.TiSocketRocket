TiSocketRocket
===========================================

SocketRocket wrapper for Titanium(iOS)

* Android, Windows, and Mobileweb are not supported.

INSTALL
-----------------------------

Copy iphone/ro.toshi.ti.mod.tisocketrocket-iphone-1.0.0.zip in your project.
See http://docs.appcelerator.com/platform/latest/#!/guide/Using_a_Module for details.

EXAMPLE
------------------------------------
  
```javascript
var ws = require('ro.toshi.ti.mod.tisocketrocket');
ws.addEventListener('open', function(e){
  Ti.API.info("Socket opened");
});

ws.addEventListener('error', function(e){
  Ti.API.info(e);
});

ws.addEventListener('message', function(e){
  Ti.API.info("You got a message!: " + e);
});

ws.createWebSocket({
  url: 'wss://example.com/'
});

ws.send(JSON.stringify({
  message: "Hello Websocket"
}));

```


