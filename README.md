# Jasper

<1> Hardware
============

1. Check earphone
---------------------------
<pre><code> pi@raspberrypi:~$sudo raspi-config </code></pre>

2. Confirm sound output
----------------
<pre><code> pi@raspberrypi:~$aplay /usr/share/sounds/alsa/Front_Center.wav </code></pre>


<2> Software
============

1. Before install Jasper
------------------------
* Before installing Japer, we will install some tools to need.
<pre><code> pi@raspberrypi:~$sudo apt-get update
 pi@raspberrypi:~$sudo apt-get upgrade --yes
 pi@raspberrypi:~$sudo apt-get install git-core python-dev bison libasound2-dev libportaudio-dev python-pyaudio --yes
 
 pi@raspberrypi:~$vi~/.bashrc
 pi@raspberrypi:~$source ~/.bashrc </code></pre>

2. Install Jasper
-----------------
* You will install Jasper through Git.
<pre><code> pi@raspberrypi:~/work $git clone https://github.com/jasperproject/jasper-client.git jasper </code></pre>

* Install library additionally because Jasper uses various python librarie.s
<pre><code> pi@raspberrypi:~/work $sudo pip install --upgrade setuptools
 pi@raspberrypi:~/work $sudo pip install -r jasper/client/requirements.txt </code></pre>
 
* Change 'jasper.py' to executable file. 
<pre><code> pi@raspberrypi:~/work $chmod +x jasper/jasper.py </code></pre>

* Install 'Google STT' and 'TTS'.
<pre><code> pi@raspberrypi:~/work $sudo apt-get update
 pi@raspberrypi:~/work $sudo apt-get install python-pymad
 pi@raspberrypi:~/work $sudo pip install --upgrade gTTS </code></pre>
 
* If error occurs while installing 'gTTS', Reinstall pip.
<pre><code> pi@raspberrypi:~/work $sudo apt-get remove python-pip
 pi@raspberrypi:~/work $sudo apt-get install python-setuptools
 pi@raspberrypi:~/work $sudo easy_install -U pip </code></pre>
 
