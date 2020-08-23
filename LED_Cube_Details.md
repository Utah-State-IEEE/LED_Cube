# Project Details: USU IEEE LED Cube

**Note:** This guide contains the full details on the build for the USU IEEE LED Cube.  If you want a faster read so you can quickly start programming animations, see the **README.md** file in this repository.

## Introduction and Purpose

The USU IEEE LED cube was designed and built to provide real-world design and prototyping experience for the students of USU.  As students designed and built the project, it provided them opportunities to see real-world applications for the concepts they learned in class.  By continuing to program and improve the LED cube, it is our hope that many more students will continue learning and applying technical knowledge. In this way, the IEEE branch funds used to construct the cube will continue empowering and educating students for years to come.

This document provides full details on the construction of the cube for others to learn about and make improvements or repairs.  This document should be updated as necessary, but should never be completely deleted.  Without this document, the LED cube will quickly fall into neglect and disrepair and the funds and time devoted to its construction will be wasted.

## Design Overview

This document will outline all of the design components of the LED cube, from the hardware and construction methods to the controlling software.  We first list the resources that helped us in our design to thank them for their work, but also because they provide additional support and explanation to this documentation.

The most heavily used resource was Hari Wiguna's _8x8x8 Blue LED Cube_ project on hackaday.io  This project write-up provided important guidance on circuit design, and the circuitry of the USU IEEE LED Cube is nearly identical to Hari's. Thanks for sharing your build! A link to the resource is found here: https://hackaday.io/project/1243-8x8x8-blue-led-cube

The other valuable resource was _LED Cube 8x8x8_ by chr on Instructables.  This provided some handy tips on cube construction, as well as giving additional insight into coding the cube.  This resource can be found here: https://www.instructables.com/id/Led-Cube-8x8x8/

### Hardware Design

The LED cube hardware consists of 3 major subsystems: the LED matrix itself, control circuitry, and power supply circuitry.  A list of the components used will be provided, then these subsystems will be explained below.

#### Electronics Used

A list of important part numbers is provided here so that datasheets and replacement information can be obtained.

- Nichia Blue LED NSPB346LS (x 448)
- 100 Ohm resistors (x 64)
- 3000 Ohm resistors (x 14)
- Texas Instruments Power Shift Register TPIC6B595 (x 8)
- 0.1 uF ceramic capacitors (x 8)
- NPN Amplifier Transistors P2N2222A (x 7)
- P-Channel MOSFET FQP27P06 (x 7)
- Arduino Nano (x 1)
- 1000 uF electrolytic capacitor (x 1)

#### LED Matrix

Since no microcontroller provides 448 outputs, the first challenge of an LED cube is to managing to individually address each LED without a dedicated GPIO.  This is overcome using multiplexing and relying on human persistence of vision.  In this multiplexing configuration, LEDs are aligned so as to be individually addressable using only a few GPIO pins.

![Multiplexing Example](https://github.com/Utah-State-IEEE/LED_Cube/blob/Erik-C-55-documentation1/Multiplexing.png)

#### Control Hardware

![Layer Select Circuit](https://github.com/Utah-State-IEEE/LED_Cube/blob/Erik-C-55-documentation1/Layer_Select.png)

Another image is seen below.

![Shift Register Circuit](https://github.com/Utah-State-IEEE/LED_Cube/blob/Erik-C-55-documentation1/shift_register.png)

Below is the pinout for the Arduino Nano.

![Arduino Nano Pinout](https://github.com/Utah-State-IEEE/LED_Cube/blob/Erik-C-55-documentation1/Nano_pinout.png)


#### Device Enclosure

### Software Design
