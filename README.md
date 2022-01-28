# CatSuit
CatSuit is an easy-to-make e-textile platform. Fully integrated textile-based sensors detect touch, position, and meshes deformation. This project presents playful applications of e-textile. CatSuit aims to make e-textile technology more accessible to non-professionals.


The manual on the full manufacturing process of Catsuit is on the --- file.

To launch a demo of Catsuit : 
Installation

Install node.js for your operating system.
Download or clone the repo of https://github.com/pandrr/osc2ws into a folder. 
Open a terminal in the osc2ws directory and type:
```
npm i
```
start

Open a terminal in the osc2ws directory and type:
```
node main.js
```
After starting up it should look like this 
```
local ip: 172.21.72.110
starting websocket server on port 8000
starting osc receiver on port 9000
```

Now connect your websocket to ws://localhost:8000

With the Wemos send OSC data to your local IP address and use port 9000
eg : 192.168.1.169:9000

You should change and upload the Wemos code accordingly to IP adress and port server.

eg : 
```
const char* host = "172.21.72.110";
const int recv_port = 8000;
const int send_port = 9000;

```

Then connect the alimentation cord in the back of the Catsuit to its battery 
