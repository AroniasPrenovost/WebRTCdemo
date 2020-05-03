Multi-Client WebRTC Video
=========================

Based on https://github.com/shanet/WebRTC-Example, see [https://shanetully.com/2014/09/a-dead-simple-webrtc-example/](https://shanetully.com/2014/09/a-dead-simple-webrtc-example/) for a description of WebRTC basics.

## Usage

The signaling server uses Node.js and `ws` and can be started as 
follows:

```
$ npm install
$ npm start
```

With the server running, open Chrome and go to to `https://[server]` from any client on the LAN.

Optionally, use a URL parameter to specify the client display name, e.g. `https://[server]/?displayName=Boston`

You may have conflicting tasks already using the default HTTP and/or 
HTTPS ports (80 and 443), which will result in an error on startup. 
Change the constants in server.js and go to 
https://localhost:[HTTPS_PORT]

For production, the server can be deployed as a Windows service using 
node-windows, which can be installed as follows:

```
npm install -g node-windows
node install_service.js
```
