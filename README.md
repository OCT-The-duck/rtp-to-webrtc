# rtp-to-webrtc
Stream from the RTP H264 videos to WebRTC



## Usage

```bash
go build
vi SDP # (paste out the browser's offer here)
cat SDP | ./rtp-to-webrtc <RTP port> # (then copy the program's offer)

ffmpeg -i <video stream> -c:v libx264 -pix_fmt yuv420p .. (more arg stuffs) -f rtp rtp://127.0.0.1:<RTP port>
```

