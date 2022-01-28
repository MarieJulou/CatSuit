# CatSuit
CatSuit is an easy-to-make e-textile platform. Fully integrated textile-based sensors detect touch, position, and meshes deformation. This project presents playful applications of e-textile. CatSuit aims to make e-textile technology more accessible to non-professionals.


The manual on the **full manufacturing process** of Catsuit is on the Technical report-Catsuit.pdf file.

To launch a **demo of Catsuit** : 

## Installation

Install node.js for your operating system.
Download or clone the repo of https://github.com/pandrr/osc2ws into a folder. 
Open a terminal in the osc2ws directory and type:
```
npm i
```

## Start

Before starting anything, make sure you have a Cables.gl account.
### Launch server
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

### Prepare Catsuit


Then connect the alimentation cord in the back of the Catsuit to its battery.
The 3 Wemos will send OSC data to your local IP address and use port 9000

eg : 192.168.1.169:9000

Soon the server should be receiving messages from the Wemos.

If the **server doesn't receive any messages** the Wemos are not connected to the right wifi and/or server

in this case
You should change and upload the Wemos code accordingly to IP adress and port server.

eg : 
```
const char* host = "172.21.72.110";
const int recv_port = 8000;
const int send_port = 9000;

```
if it doesn't work check the wifi connection variable: 
eg : 
```
const char* ssid = "PoleDeVinci_DVIC"; 
const char* pwd = "8PfURsp!dvic"; 
const IPAddress ip(172, 21, 72, 201);
const IPAddress gateway(172, 21, 72, 1);
const IPAddress subnet(255, 255, 255, 0);
```

### Launch Cables.gl
Go to the Cables.gl patch : https://cables.gl/p/FQQsDO

You should be seeing the 3 triangle moving.

