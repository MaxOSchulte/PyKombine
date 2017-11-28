# PyKombine
Projekt for the combination of skeletal data of multiple, over the network distributed, Kinect v2 devices

---

# PyKombine

This project attempts to combine the skeletal data of several Kinect devices. These devices can be distributed over the network. Each client that has a kinect connection (Klient) processes the data in a minimal way and sends it to OSC bundles via zmq to the server (Kombine / Kombiner).
The Kombiner than merges all connected Kinect device data into on single skeleton and publishes it in OSC-Bundles via zmq. 

## Known Bugs, Issues

 * Only one Person can be tracked.
 * A Persson should only show its front to the sensors
 * A Klient-PC must run Windows.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

#### Install python3.5+ (32-Bit)

**Python3.5 (32-Bit)** or higher must be installed. Please see the official Python documentation for install instructions ([Download Pyhton official](https://www.python.org/downloads/))

Windows user can also use **Anaconda** ([Anaconda Home](https://anaconda.org/)).

#### Installing Virtualenv (optional)

Installing Virtualenv ([Documentation](https://virtualenv.pypa.io/en/stable/)). has following advantages:

 * Dependency isolation
 * no root required for pip packages

**Install instructions can be seen below**
    
### Installing

**pyhton3 references here to the install python3 version (3.5 or 3.6 atm.) if your system uses a different python3 version by default replace the python3 command with python3.5 or python3.6 (depending on what you installed)**

**The python command differs on Windows, it can be python3, py3 or py**

---


*(optional)* Install and activate Virutalenv

```
python3 -m pip install virtualenv

python3 -m virtualenv -p python3.5 env
```


**Linux / Max-OS**

```
. ./env/bin/activate
```

**Windows**

```
.\env\Scripts\activate.bat
```

---

Install all requirements to run this project. 

```
python3 -m pip install -r misc/requiremnts
```


## Usage

### Server (Kombine)

**Windows:** Run `server.bat`  or `python3 src\server.py`
**Max-Os / Linux:** Run `server` or `python3 src/server.py`


### Client (Klient)

**Windows:** Run `klient.bat` or `python3 src\klient.py`. append `_dummy.bat`  for testing purpose.
**Max-Os / Linux:**  Run `klient` or `python3 src/klient.py`. append `_dummy` for testing purpose.




### Display Kombine output
**TODO**

## Built With

* Python3.5+
* Pykinect2 - Python3 wrapper for the Kienct2 SDK

## Authors

* **Max Schulte**

## Acknowledgments

**TODO**

* Hat tip to anyone who's code was used
* Inspiration
* etc

