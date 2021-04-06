# media-server-demo-node
Demo application for the Medooze Media Server for Node.js

## Intallation
```
npm install
```

## Run
You need to run the demo passing as argument the public IP address of the media server that will be included in the SDP. This IP address is the one facing your clients.
```
node index.js <ip>
```

The demo will open an HTPPS/WSS server at port 8000. 

## HOW TO USE A RTSP/RTP stream into webrtc
FFMPEG command - generate a ffmpeg video streaming and push stream to your server ip
```
ffmpeg -rtsp_transport tcp -i 'rtsp://wowzaec2demo.streamlock.net/vod/mp4:BigBuckBunny_115k.mov' -c:v copy -an -f rtp rtp://<ip>:5004
```

The demo will open an HTPPS/WSS server at port 8000. 

## Conclusion
i fork a branch from medooze media-server-demo-node, some syntax are depreciated, and i amended it
, also mark some code about setDirection ( i have not idea why yet )  , then the demo works....

https://github.com/medooze/media-server-demo-node

## Demos
### SVC Layer selection

To run this demo just open `https://ip:8000/svc/` on a Chrome browser and follow instructions.

### Recording

To run this demo just open `https://ip:8000/rec/` with Chrome or Firefox.

### Broadcasting

To run this demo just open `https://ip:8000/broadcast/` with Chrome or Firefox and follow instructions.

### Simulcat

To run this demo just open `https://ip:8000/simulcast/` with Chrome or Firefox and follow instructions.




