# pi-video-streaming
This project setups a video streaming server and initiation of streaming on a raspberry pi
<br> First connect your raspberry pi to a picamera: https://www.raspberrypi.org/documentation/usage/camera/README.md
## Enabling the camera
<br> Open the raspi-config tool from the Terminal:

<code> sudo raspi-config </code>
<br> select <code>interfacing options</code>
<br> Select the <code>camera</code> option and select <code>yes</code> to enable, then go to Finish and you'll be prompted to reboot.

### Short and simple setup guide

<br><code> git clone https://github.com/tonikalombo/pi-video-streaming.git </code>
<br><code> cd pi-video-streaming/ </code>
<br><code> sh bootstrap.sh </code>
