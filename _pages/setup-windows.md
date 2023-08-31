---
layout: page
title: CIS 5650 - Setup instructions for your Windows PC
description: >
  This page provides instructions for setting up your Windows PC for CIS 5650
hide_description: true
permalink: /setup-windows/
---

## Setup your Windows 10 Computer

Follow this guide to setup your personal Windows computer.

This guide assumes that you have admin access to your computer.

1. Click **Start**, type `winver`, and hit enter. This will open a window with information about your Windows version. Check that the version is **1809 or newer**. Run Windows Update if necessary.
    ![winver](/assets/images/screenshots/winver.jpg)
2. Download and install the latest [**NVIDIA GPU Driver**](https://www.nvidia.com/download/index.aspx?lang=en-us) for your GPU.
3. Download and install [**Git**](https://git-scm.com/download/win).
    * Shehzan's preferred installation options (other than defaults):
        * Adjusting your Path environment: Select `Use Git and optional tools from Command Prompt`. This option allows you to use Git from both Git Bash and Command Prompt.
        * Configuring the line ending conversion: Select `Checkout as-is, commit as-is`. Shehzan uses this option because he also changes all his preferred editors to use Unix line endings. If you do not want to change your editors, select `Checkout as-is, coming Unix-style line endings`.
        * Configuring the terminal emulator to use with Git Base: `Use Windows' default console window`.
        * Configuring extra options: Select `Enable symbolic links` in addition to default options.
        * Configuring experimental options: Select `Enable experimental support for pseudo consoles`.
    * After installation, follow the [**First Time Git Setup**](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup) Guide if this is the first time you are using Git.
4. Install **Visual Studio 2019**. We recommend (but not require) that you wipe out any old versions of Visual Studio (2017 and below). See [Visual Studio Uninstaller](https://github.com/Microsoft/VisualStudioUninstaller/releases) for help.
    * Visit [http://www.seas.upenn.edu/cets/software/msdn/](http://www.seas.upenn.edu/cets/software/msdn/).
    * Once you're in the Microsoft Azure download page, look for `Visual Studio 2019 Community` and download it.
    * Make sure this ends up installing the `Visual Studio Installer` so you can select the packages you want.
    * Once in the installer, do the following
        * Under the `Workloads` tab, select `Desktop Development with C++`. This will select almost everything you will need.
        * Under the `Individual Components Tab`, make sure these packages are selected. **DO NOT uncheck** everything else.
            * Visual Studio 2019:
                * Git for Windows (optional)
                * Github Extension for Visual Studio (optional)
                * MSVC v141 - VS 2017 C++ x64/x86 build tools (v14.16) - Allows you to build VS 2017 projects using 2019 (used for the DXR project later on)
                * C++ ATL for v141 build tools (x86 & x64)
                * Windows 10 SDK (10.0.17763.0)
                * Windows 10 SDK (10.0.18362.0)
                * Windows 10 SDK (10.0.19041.0)
            * Visual Studio 2022 (in addition to above components for 2019 which are available for VS 2022):
                * MSVC v142 - VS 2019 C++ x64/x86 build tools - Allows you to build VS 2019 projects using VS 2022
                * Windows 10 SDK (10.0.22621.0)
                * Windows 10 SDK (10.0.22000.0)
                * Windows 10 SDK (10.0.20348.0)
5. Install Nsight Compute, Nsight Graphics, and Nsight Systems from [https://developer.nvidia.com/nsight-tools-visual-studio-integration](https://developer.nvidia.com/nsight-tools-visual-studio-integration).
6. Install the latest version of [**CUDA**](https://developer.nvidia.com/cuda-downloads) (minimum version 11.6).
    * Use the `Custom Installation` and select only `CUDA` (do not install the display driver and other components).
    ![cuda-11-custom-installation](/assets/images/screenshots/cuda-11-custom-installation.jpg)
7. Install [**CMake**](http://www.cmake.org/download/). Windows binaries are under `Binary distributions`.
8. Install [Visual C++ Redistributable 2015/17/19 and 2013](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads). Note: there are 2 different install files for 2015/17/19 and for 2013 - you need to install both.
9. (_Optional_) Download [**GPU-Z**](https://www.techpowerup.com/download/techpowerup-gpu-z/). You can either install it, or run it as a portable executable. This provides useful information about your GPU and technologies it supports.
    ![gpu-z](/assets/images/screenshots/gpu-z.jpg)

### Enable GPU Performance Counters

When running profiling, the Nsight tools need access to systems level counters to trace the performance. There are two options to do this:

1. Run the program as admin, which is tedious to set up each time.
2. Enable Performance counters using NVIDIA Control Panel (Recommended).

The steps to enable this are:

1. Open NVIDIA Control Panel. This can be done from the start menu, the taskbar NVIDIA icon, or Control Panel.
2. On the menu bar (top), select `Desktop -> Enable Developer Settings`.
3. On the left side panel, you will now see `Developer -> Manage GPU Performance Counter`. Change the option to `Allow access to the GPU performance counters to all users`.

See [NVIDIA Documentation](https://developer.nvidia.com/nvidia-development-tools-solutions-err_nvgpuctrperm-permission-issue-performance-counters) for more.

[Back to Setup](/setup/)