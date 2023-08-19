---
layout: page
title: CIS 5650 - Setup instructions for CETS Virtual Lab
description: >
  This page provides instructions for setting up CETS Virtual Lab for CIS 5650
hide_description: true
permalink: /setup-cets/
---

## Using CETS Virtual Lab for CIS 5650

The Virtual Lab connects you remotely to computers available to CETS. The Virtual Lab consists of computers with **NVIDIA Quadro RTX T1000** GPUs.

## Connecting to the Virtual Lab

1. You need to first connect to the Penn VPN: [https://www.isc.upenn.edu/how-to/university-vpn-getting-started-guide](https://www.isc.upenn.edu/how-to/university-vpn-getting-started-guide)
2. Once installed and connected, you can connect to the Virtual Lab:
[https://cets.seas.upenn.edu/answers/virtuallab.html](https://cets.seas.upenn.edu/answers/virtuallab.html)
3. When you log in you can open a command prompt window and run `nvidia-smi`.
    ![nvidia-smi-quadro-rtx-t1000](/assets/images/screenshots/nvidia-smi-quadro-rtx-t1000.jpg)
4. Great thing about CETS Virtual Lab computers is that they come with all the required software installed. You do not need to do anything else.

## Developing Software in Virtual Lab PCs

Using the Virtual Lab PCs is similar to using Moore Lab - unless you use the correct directories and network drives, your data will be wiped with each use.

When you directly compile and build projects stored on network drives, you may run into Visual Studio compilation issues.

If you have been using Moore Lab for previous projects and have workarounds for this, feel free to continue using those practices.

Otherwise, you can either copy projects to-and-from the network drives to local storage, or you can use git to push and clone your work. If you are copying your projects, make sure to use consistent paths because of CMake, otherwise you will need to delete the CMake cache and regenerate it.

[Back to Setup](/setup/)