## What Bootstrap.sh does
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
