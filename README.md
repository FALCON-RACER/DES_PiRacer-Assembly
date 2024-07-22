# [DES Project - PiRacer Assembly](https://github.com/SEA-ME/DES_PiRacer-Assembly)

- [**DES Project - PiRacer Assembly**](#des-project---piracer-assembly)
  - [Introduction](#introduction)
  - [Project Description](#project-description)
  - [Project Goals and Objectives](#project-goals-and-objectives)
- [**GUIDE**](#guide)
  - [Assemble the PiRacer](#assemble-the-piracer)
  - [Setup](#setup)


## Introduction

The purpose of this project is to provide students with hands-on experience in assembling and testing a PiRacer, a small, single-board computer-based racing car. The project will cover the basics of electronics, programming, and robotics, and will provide students with a foundation in these important areas of technology.  
</br>

## Project Description

The PiRacer is a compact, single-board computer-based racing car that uses the Raspberry Pi computer as its brain. In this project, students will be working together in teams to assemble and test their PiRacers. The project will require students to use a variety of tools and technologies, including soldering irons, multimeters, and programming languages like Python.  
</br>

## Project Goals and Objectives

* To gain hands-on experience in assembling and testing a PiRacer
* To develop basic skills in electronics, programming, and robotics
* To learn about the Raspberry Pi computer and its capabilities
* To work as part of a team to complete a complex project  
</br>

---

# GUIDE

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