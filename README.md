linconnect-server
=================

Mirror Android notifications on a Linux desktop.

LinConnect Client: https://github.com/hauckwill/linconnect-client/

Introduction
------------
LinConnect is a project to mirror *all* Android notifications on a Linux desktop using LibNotify.

*Please note that this is my first time using Python (though I do have experience in other languages), so the code may still be messy. It's a WIP.*

Installation
------------

**Requirements**

* python2
* python-pip
* python-gobject
* libavahi-compat-libdnssd1
* cherrypy (python package)
* pybonjour (python package)

**Running**

Simply run linconnect_server.py to start the server, then start the Android application. The Android application will detect the server and display it in the server list. Selecting it will send a test notification to the server.

**Simple Setup**

Enter the following command into a console to install the server, set it to autostart, and run LinConnect. The server will be automatically updated daily.

```bash
$ wget --quiet https://raw.github.com/hauckwill/linconnect-server/master/LinConnectServer/install.sh; \
chmod +x install.sh; \
./install.sh
```

If you recieve an error about pybonjour, you may have to install libavahi-compat-libdnssd1
```bash
apt-get install libavahi-compat-libdnssd1
```
Then download the latest pybonjour from Google Code :
https://code.google.com/archive/p/pybonjour/downloads

Unpack the downloaded file :
```bash
tar zxf pybonjour-1.1.1.tar.gz
```
Install the module
```bash
cd pybonjour-1.1.1
sudo python setup.py install
```

And finally retry the setup.

To remove LinConnect, delete the ~/.linconnect directory.

**Tested with :**

* Ubuntu 13.10
* Ubuntu 15.10
        
Client Download
---------------

![alt text](https://upload.wikimedia.org/wikipedia/commons/c/cd/Get_it_on_Google_play.svg "Google Play")

A binary of the client may be downloaded from the Google Play Store.

https://play.google.com/store/apps/details?id=com.willhauck.linconnectclient
