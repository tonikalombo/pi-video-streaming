### raspivid Example
<br> To listen on a TCP port (IPv4) and wait for an incoming connection: <code>raspivid -l -o tcp://0.0.0.0:3333</code>
<br> To record a 10 second long video with arbitray file name: <code>raspivid -o /path/filename.h264 -t 10000</code>
<br> To convert raw h264 video into MP4 format, install MP4Box:
<br> <code>sudo apt-get install -y gpac</code>
<br> Capture raw video with raspivid and wrap it in an MP4 container:
<br> Capture 30 seconds of raw video at 640x480 and 150kB/s bit rate into a pivideo.h264 file:
<br> <code>raspivid -t 30000 -w 640 -h 480 -fps 25 -b 1200000 -p 0,0,640,480 -o pivideo.h264 </code>
<br> Wrap the raw video with an MP4 container: 
<br><code>MP4Box -add pivideo.h264 pivideo.mp4</code>
