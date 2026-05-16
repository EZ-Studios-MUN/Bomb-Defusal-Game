# Bomb-Defused-Game

This is the code for our project Bomb Defusal Game, which is heavily inspired by the game Keep Talking and Nobody Explodes, as this is an attempt to make the game in real life. This is the source code, 3D model, and wiring for our project.

V1 of this project are running on 2 Grove Beginner Arduino Kit, and we are currently working on V2 which will be fully hotswappable and alos will be based on custom PCB and STM32 platform

## Description V1

This project is the final project for our ENGI 1020 course at Memorial University. In this project we are using 2 grove beginner kit to achieve all 6 modules: Morse Code, Simon Says, Passwords, Mazes, Wires, and the Timer module. for Morse Code, Simon Says, we only uses buzzer, LEDs, and buttons to make this module, but for the Passwords module, we used a I2C LCD, and 6 buttons to make it work. For the Timer module, we used a 4 pin clock segmented display to achieve the timer effect. For both Mazes and Wires, we are using 2 OLED screens with SPI connections to achieve the functionality of the module. Thus, we make a split between the modules, where all modules without an OLED screen will be runned on one of the Grove Kit, and other modules with an OLED will be runned on the other Grove Kit. Now, since there is no good firmware and driver for an OLED screen with SPI connection with grove kit, we went and made our own firmware, called SPI_ARDUINO.ino. then we upload this firmware onto the Grove Kit, afterwards, we also coded a library that works with this firmware, called LCDDriver, This is called an LCDDriver because OLED is technicalled an LCD, so we named it more broad, hoping to put more into this firmware later. We have also used the engi1020 firmware and library to make the other games, though we need to change and modify the firmware ourselves to make the timer module work, it is still mostly engi1020 firmware and library, thus we will acknowledge this later in the acknowledge section. All code, 3D model, and wiring diagrams are in this github, at different sections with corresponding folder names.

## Description V2

Since this version is outside of the scope of the final project of ENGI1020 class, We decided to change to a better solution for this new version. We will be using custom built PCB along side with STM32 chip per module to make this whole project fully like the original game where you can swap different modules out live without closing the game. Also since we need a lot of pins and power to drive all the game at the same time. We decided to go with a main chip in the box as well thus we can achieve this hotswapping mechanism. We will try to make everything fully 3D printable and also put out a BOM for all parts we are going to use. Firmware and code will be in C/C++ instead of Python.

## Authors

Yicheng (Abner) Zhang
yichengz@mun.ca

Eric Guzzwell
ejguzzwell@mun.ca

## Donations

If you want to support us, please use link: https://buymeacoffee.com/yichengz

## Acknowledgments

* Keep Talking and Nobody Explodes
* Memorial University engi1020 firmware