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
### Python Example
<br><code>from picamera import PiCamera</code>
<br><code>from time import sleep</code>
<br><code>camera = PiCamera()</code>
<br><code>camera.resolution = (2592, 1944)</code>
<br><code>camera.framerate = 15</code>
<br><code>camera.start_preview()</code>
<br><code>camera.annotate_text = "Hello world!"</code>
<br><code>sleep(10)</code>
<br><code>camera.capture('/home/pi/Desktop/max.jpg')</code>
<br><code>camera.stop_preview()</code>

## Let's get started
<br> Install pip
<br><code>sudo apt-get install python-pip</code>
<br>Install the picamera library:
<br><code>pip install picamera</code>
<br>Install the flask Python library:
<br><code>sudo pip install flask</code>
<br> Download Miguel’s Flask video streaming project:
<br><code>git clone https://github.com/miguelgrinberg/flask-video-streaming.git</code>
<br> In the project folder edit the app.py file. Comment the following:
<br><code> #from camera import Camera </code>
<br> Un-comment the following line:
<br><code>from camera_pi import Camera</code>

 <br> Start the Flask server:
<br><code> python app.py </code>
<br> Output
<br><code> * Running on http://0.0.0.0:5000/ </code>
