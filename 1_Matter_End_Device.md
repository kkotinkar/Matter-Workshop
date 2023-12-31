# Chapter 1 - Matter End Device
Firstly, we will compile the firmware for a Matter end device which is our Nordic development kit / SoC. <br>

You can find all available Matter samples of the nRF Connect SDK under: [Matter samples](https://developer.nordicsemi.com/nRF_Connect_SDK/doc/2.3.0/nrf/samples/matter.html).

<img src="images/1_Matter_samples.PNG" alt="Matter Samples" width="700"/>

The complete app code of a Matter weather station is available under nRF Connect SDK [Applications](https://developer.nordicsemi.com/nRF_Connect_SDK/doc/2.3.0/nrf/applications/matter_weather_station/README.html). It is intended to showcase an actual Matter application with sensors running on the Thingy:53.

## Step 1: Select a Matter sample application (e.g. Matter Light bulb)

Ensure that you have a compatible DK at hand. A nRF5340-DK, a nRF52840-DK or a nRF7002-DK will work.<br>

We will select the nRF52840-DK as device platform and the [Matter Light bulb](https://developer.nordicsemi.com/nRF_Connect_SDK/doc/2.3.0/nrf/samples/matter/light_bulb/README.html) example code. 

## Step 2: Create a new application under VS Code

Within VS Code, use the nRF Connect Extension to create a new freestanding application in your workspace directory of choice.

![](images/1_create_new_app.png)

## Step 3: Add a build configuration

Add a build configuration to your newly created project to link the source code to the applicable hardware / Nordic Development Kit. <br>
Select the nRF52840-DK and keep the remaining settings on default for now. <br>
Hit **Build Configuration**, this will build the configuration and compile the source code.
> **Note**
> When using the nRF5340-DK or the nRF7002-DK, use the application core of the nRF5340 as build target (nrf5340dk/nrf7002dk_nrf5340_cpuapp).

![](images/1_add_build_config.png)

## Step 4: Flash the compiled project to your nRF52840-DK

Connect your nRF52840 DK, a serial number should appear under Connected Devices within nRF Connect for VS Code. <br>
Hit **Flash** to program the kit.

![](images/1_flash_process.png)

## Step 5: Validate the firmware on the DK's terminal output
Expect a terminal / shell output via the Virtual COM port of your connected DK as follows.

![](images/1_DK_output.png)

> **Note**
> The Setup Pin Code and Setup Discriminator will be required for the commissioning process at the Matter controller later on.

## Next Chapter
Switch to [Chapter 2A - Setup of a Thread RCP](./2A_Thread_RCP.md)