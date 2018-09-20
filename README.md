# pi-video-streaming
This project setups a video streaming server and initiation of streaming on a raspberry pi
<br> First connect your raspberry pi to a picamera: https://www.raspberrypi.org/documentation/usage/camera/README.md
## Enabling the camera
<br> Open the raspi-config tool from the Terminal:

<code> sudo raspi-config </code>
<br> select <code>interfacing options</code>
<br> Select the <code>camera</code> option and select <code>yes</code> to enable, then go to Finish and you'll be prompted to reboot.
### raspivid
<br> To listen on a TCP port (IPv4) and wait for an incoming connection: <code>raspivid -l -o tcp://0.0.0.0:3333</code>
<br> To record a 10 second long video with arbitray file name: <code>raspivid -o /path/filename.h264 -t 10000</code>
<br> To convert raw h264 video into MP4 format, install MP4Box:
<br> <code>sudo apt-get install -y gpac</code>
