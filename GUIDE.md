# How to assemble and setup PiRacer

## Assemble the PiRacer
https://www.waveshare.com/wiki/JetRacer_Assembly_Manual

![falcon](/falcon.jpeg)

<br>

## Setup

**1. Install Raspberry PI OS**
**2. clone piracer_py repo**

```bash
git clone https://github.com/SEA-ME/piracer_py
```

**3. Install dependencies:**

```bash
sudo apt update
sudo apt install \
	gcc \
	v4l-utils \
	i2c-tools \
	raspi-config \
	python3-dev \
	python3-setuptools \
	python3-venv \
	libopencv-dev
```

**4.Enable i2c and camera**
```
ifconfig
```
Use the **ifconfig** tool to enable the following peripherals:

- i2c: Interface Options > I2C
- Camera: Interface Options > Camera

**5. Reboot**

```bash
sudo reboot
```

**6. Install piracer-py package**

```bash
$ cd ~
$ mkdir piracer_test/
$ cd piracer_test/
$ python3 -m venv venv 
$ source venv/bin/ativate

$ pip install -r requirements.txt
$ pip install piracer-py
```

**7. Test**
```bash
$ cd example
$ python shanwan_gamepad_control.py
```