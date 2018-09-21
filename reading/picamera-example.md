### Picamera Example
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
