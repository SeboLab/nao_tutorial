# nao_tutorial

## How To Download naoqi Package

When you git clone this repository to a new ubuntu laptop (e.g. Intro Robo L05), your environment may not be ready to run naoqi to control NAO. If you find that your ubuntu laptop does not recognize naoqi package, you should do the following steps.

1. Go to NAO's website (https://www.aldebaran.com/en/support/nao-6/downloads-softwares) to download NAO's SDKs. Click the download button for ``SDKs 2.8.6 - Python 2.7 SDK``
<img width="1308" alt="Screen Shot 2023-10-17 at 8 21 33 PM" src="https://github.com/tinghanlin/nao_tutorial/assets/66953378/14f5d0bf-a620-4493-a0c4-b9b31cc09e8d">

2. On the ubuntu laptop, extract the downloaded SDK to this repository, and make sure you see that ``pynaoqi-python2.7-2.8.6.23-linux64-20191127_152327`` is in this repository. 
3. In the terminal, set the pythonpath to access the naoqi package, by running ``export PYTHONPATH=~/nao_tutorial/pynaoqi-python2.7-2.8.6.23-linux64-20191127_152327/lib/python2.7/site-packages``. To see what is in pythonpath, ``echo $PYTHONPATH``. Note that the path will be dependent on where you store this repository. For example, if this ``nao_tutorial`` is stored in Desktop, then your path will be ``export PYTHONPATH=~/Desktop/nao_tutorial/pynaoqi-python2.7-2.8.6.23-linux64-20191127_152327/lib/python2.7/site-packages``. 
5. You might also want to write this command in the ``~/.bashrc`` file, by running ``echo 'export PYTHONPATH=~/nao_tutorial/pynaoqi-python2.7-2.8.6.23-linux64-20191127_152327/lib/python2.7/site-packages' >> ~/.bashrc``. To see what is in ``~/.bashrc``, run ``nano ~/.bashrc`` and exit by doing ``CTRL + X``. Note again, if you download this repository in Desktop, then your path will be ``echo 'export PYTHONPATH=~/Desktop/nao_tutorial/pynaoqi-python2.7-2.8.6.23-linux64-20191127_152327/lib/python2.7/site-packages' >> ~/.bashrc`` 
6. naoqi is properly downloaded when you compile a file that calls ``import naoqi`` and no error message is shown.

The above steps are modified and references from: http://wiki.ros.org/nao/Tutorials/Installation and http://doc.aldebaran.com/2-5/dev/python/install_guide.html

## How To Set Up NAO
1. NAO: Plug in the power source (charge to the back), NAO ethernet cable to its head and to the port of the router (the port).
2. Wifi + Laptop: Open laptop using password: XXXXXX, connect the laptop's wifi to the same router (Router Password: is XXXXXX), and connect power to your laptop.
3. NAO is powered up: press the button on NAO, and you will hear onagu. NAO will likely go-to sitting position, so make sure to hold it.

## Check NAO's Setting
1. Get his IP address: press his chest button, and NAO will say its IP address (e.g. “192.168.1.4”).
2. Open an internet browser (such as Internet Explorer, Chrome, Firefox, etc).
3. Type the IP address that NAO has just spoken into the address bar and press Enter. NAO’s webpage opens.
4. Type in the default login and password: “nao” for both.

<img width="1236" alt="NAO-setting" src="https://github.com/tinghanlin/nao_tutorial/assets/66953378/3fdbcba3-4455-4366-8f27-0e81d538998a">

## How To Run NAO With hello_world.py

1. Set the correct IP address for NAO in `hello_world.py`. NAO should always have an IP address number starting `192.168.X.XXX`. If you don't know NAO's IP address, press its power button and it will verbally tell you. After you hear the IP address, update it in the code in `hello_world.py`. Note that you only need to do this once whenever you power NAO on.
2. Open a terminal, cd to this repository, and run `python2 hello_world.py` because NAO is using python version 2.7.

## Acknowledgment
This tutorial is written by Timmy Lin. If you encounter any questions, please reach out to him via tinghan@uchicago.edu. We thank Sarah for the original source code in ``hello_world.py``.
