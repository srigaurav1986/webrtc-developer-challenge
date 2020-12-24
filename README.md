# The Multi-room audio-video conferencing tool with Socket.IO and Node.JS

It's a simple solution to connect anyone over a simple room name, without any additional plugins

So, this utility attempts to handle everything. It:

- Simplifies the communication process, with rich user experience
- Users can chat
- accounts for the latest Chrome release's getUserMedia() function to run without ssl, So fake keys added.


## Installation

#### Download

Simply clone or download the zip of the project,

#### Using with [Node.js](http://nodejs.org) via [npm](https://www.npmjs.org/):

Command Line:

```shell
npm install
```

## Usage

```shell
node app.js
```

- This should start your chat app at port 5000.We are running it on HTTP as application is deployed behind Load balancer which is acting as SSL terminator with valid certificates. Codebase also contains fake SSL keys if one wants to run it on local or with uncertified SSL keys.In later case we need to start "https" server with "option" json in app.js.   
- Any two users can chat over https://<your domain>/any+room+name
  
- For NAT traversal we can use COTURN server which acts as both STUN and TURN. We can limit opened UDP port by specifying port range.
- Regarding Security its DTLS over UDP, signaling is protected using valid SSl certificate and LB as SSL terminator.For NAT traversal TURN server credentials are used for TURN allocations. 
  
 App is deployed at 
 https://quilled-rose-anteater.glitch.me/
 To create room, press "CLICK" button and unique room url will be created next to it like https://quilled-rose-anteater.glitch.me/836958
  

