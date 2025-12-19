# ESP32 Guide for beginners

A basic esp32 guide for those who wanna delve into esp32 work and understand how and what makes an ESP32 tick :)

## How to read this

This guide is intended to help the user understand how an ESP32 works at a low level, and also to bridge the gap between beginners with ESP-IDF, and not intended to just be a copy paste bin repository. We hope you are able to follow along aslong as you have the following knowledge;

- Basic knowledge in C based language (Mainly Syntax and OOP)
- Basic knowledge of Git
- Basic knowledge of Linux and commands (This tutorial is written on a linux based system)

This is v0.0.1d of the documentation, please refer to the github for the latest docs [here](https://github.com/Mervinpais/ESP32-Guide-for-beginners/)

---

## Introduction

<details>
<summary>What is an ESP32?</summary>
The ESP32 is a powerful, low-cost microcontroller with integrated Wi-Fi and Bluetooth capabilities. It's developed by Espressif Systems and is widely used in both hobbyist and professional projects.

Key features of the ESP32 include:

- Dual-core processor running at up to 240 MHz
- Low-power sleep modes for battery-operated devices
- Multiple GPIO pins for input/output control
- Support for ADC (analog-to-digital conversion), DAC (digital-to-analog conversion), PWM (pulse-width modulation), SPI, I2C, UART, and more
- Small footprint and easy integration into compact designs

It can be used for a variety of projects such as IoT devices, home automation, wearable electronics, robotics, sensor networks, and even small web servers.

</details>
<details>
<summary>Why use an ESP32?</summary>
The ESP32 is extremely versatile and popular for many reasons:

- **Connectivity:** Built-in Wi-Fi and Bluetooth allow devices to communicate with the internet or with each other without extra modules.
- **Performance:** Its dual-core processor and hardware acceleration make it fast enough for demanding tasks, like audio processing, sensor fusion, and even small ML inference.
- **Analog and Digital Control:** With multiple ADC, DAC, PWM, and GPIO pins, you can read sensors, control motors, LEDs, and actuators.
- **Low Power:** It has multiple sleep modes, making it ideal for battery-powered devices.
- **Community & Support:** Huge ecosystem of libraries, tutorials, and open-source projects makes development easier.
- **Cost-effective:** Very cheap compared to other microcontrollers with similar features.
- **Flexibility:** Can be programmed using ESP-IDF (native SDK), Arduino framework, MicroPython, or even JavaScript (Espruino), making it accessible to beginners and professionals alike.

In short, it’s a tiny chip with massive potential, capable of powering smart home devices, wearables, robotics, and any IoT project you can think of.

</details>

## How to start using your ESP32?

### Prerequisites

1. An esp32 board (Wroom-32, Wrover-E, etc.)
2. A USB C/Micro B cable (Most Esp32's nowadays use USB C but some older ones use micro B)
3. A Computer running either Windows, macOS, or Linux (We will be using Debian 12 for this tutorial)

### Main steps

1. Go to [Standard toolchain setup for linux and macOS](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/linux-macos-setup.html) for Linux/macOS and [Standard toolchain setup for Windows](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/windows-setup.html) for Windows and follow the steps

> [!NOTE] We will also be using Nvim for the majority of this tutorial, note that you can use the eclipse or vscode extension if you prefer to install esp-idf but I recommened using Neovim mainly for the speed and fun of it, else you can go ahead with the following links
>
> - [Eclipse Plugin](https://github.com/espressif/idf-eclipse-plugin/blob/master/README.md)
> - [VSCode Plugin](https://github.com/espressif/vscode-esp-idf-extension/blob/master/README.md)

2. After installation, Ensure you can access `idf.py` easily in your terminal

### How to's

### Create a project

```esp-idf
idf.py create-project PROJECT-NAME
```

### Set target
