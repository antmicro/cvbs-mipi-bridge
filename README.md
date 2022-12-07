# Composite Video (CVBS) to MIPI CSI-2 bridge

Copyright (c) 2022 [Antmicro](https://www.antmicro.com)

![Baseboard visualization](img/cvbs-mipi-bridge-black.png)

## Overview

This repository contains open hardware design files for a video bridge converting the analog composite video (CBVS) standard into MIPI CSI-2.
The video conversion is handled with Analog Devices [ADV7828-M](https://www.analog.com/media/en/technical-documentation/data-sheets/ADV7282.pdf) 10-bit 4x Oversampled SDTV Video Decoder.
The design files were prepared in KiCad.

## Repository structure

The main repository directory contains KiCad PCB project files, a LICENSE and README.
The remaining files are stored in the following directories:

* `lib` - contains the component libraries
* `img` - contains graphics for this README

## Key Features

* Analog Devices ADV7282-M CVBS-to-MIPI video converter
* 6 analog video input channels exposed on RCA connectors
* A single 1-lane MIPI CSI-2 digital output interface

Please note that according to the datasheet the ADV7282-M includes an embedded analog multiplexer and processes only one analog input channel at a time.

This video accessory is electrically compatible with several video processing platforms created by Antmicro, such as:
 
* [Jetson Nano Baseboard](https://github.com/antmicro/jetson-nano-baseboard) supporting NVIDIA Jetson Nano, Jetson Xavier NX, Jetson TX2 NX
* [Google Coral Baseboard](https://github.com/antmicro/google-coral-baseboard)
* [Snapdragon 625 Baseboard](https://github.com/antmicro/snapdragon-625-baseboard)
* [Snapdragon 845 Baseboard](https://github.com/antmicro/snapdragon-845-baseboard)
* [AMD-Xilinx Kria K26 DevBoard](https://github.com/antmicro/kria-k26-devboard)

It can also be used with NVIDIA AGX Xavier and NVIDIA AGX Orin with a dedicated [adapter](https://github.com/antmicro/jetson-agx-csi-adapter).

## License

[Apache-2.0](LICENSE)
