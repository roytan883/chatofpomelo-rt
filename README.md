## Chatofpomelo-rt

### A simple chat room experiment using pomelo framework and html5.

### 这是个人维护版本，原版来自于chatofpomelo-websocket，但是原版已经不再维护
### 此版本配合pomelo-rt使用

## install(node v4 or v6)
```
git clone https://github.com/roytan883/chatofpomelo-rt
cd game-server && npm install && cd ../web-server && npm install && cd ..
```

## run
### pm2 run  
```
cd game-server && pm2 start pm2/pm2-dev.json && cd ../web-server && pm2 start pm2/pm2-dev.json && cd ..
```
### or use nodejs run it directly 
```
cd game-server
node app.js env=development id=master-server-1 host=127.0.0.1 port=13005 type=master
node app.js env=development id=connector-server-1 host=127.0.0.1 port=14050 clientPort=13050 frontend=true serverType=connector
node app.js env=development id=chat-server-1 host=127.0.0.1 port=16050 serverType=chat
node app.js env=development id=gate-server-1 host=127.0.0.1 clientPort=13014 frontend=true serverType=gate
cd web-server
node app.js
```

## use

http://serverIP:3001/

serverIP should be your server ip




