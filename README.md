# Matter-Workshop
Setting up a complete Matter network using Nordic SoCs &amp; a Raspberry Pi.

> **Note**
> This guide uses the nRF Connect for Desktop Tools and nRF Connect SDK v2.3.0 !

## Prefix - Setting up the Development Environment
> **Note**
> A recommended setup video can be found online under: [nRF Connect for VS Code - Installation](https://www.youtube.com/watch?v=zcMCaODyISo)

We will follow the guided, and automated installation through nRF Connect for Desktop and will use the recommended IDE: Microsoft's VS Code.

**Step 1**: Download and install the following tools:
1. [nRF command line tools](https://www.nordicsemi.com/Products/Development-tools/nrf-command-line-tools/download)
   - This should also install the required J-Link drivers for programming + debugging any Nordic Development Kits (DKs). Do so, if you don't have any previous J-Link drivers installed. If you cancel/abort the step, please install the latest J-Link driver manually (can be found [here](https://www.segger.com/downloads/jlink/)).
2. [nRF Connect for Desktop](https://www.nordicsemi.com/Products/Development-tools/nRF-Connect-for-Desktop/Download)
   - The main desktop application acts as an umbrella for several tools, including the Toolchain Manager to install the SDK or the nRF Programmer to use for flashing an image to a Nordic device.
3. [Visual Studio Code](https://code.visualstudio.com/Download)
   - VS Code will be our preferred IDE. It will be extended with Nordic's plugins/extension to enable a fully featured coding and debugging environment for Nordic + Zephyr RTOS projects.
  
**Step 2**: After installation of all three applications, please open nRF Connect for Desktop. **Install the Toolchain Manager** that is used for downloading and installing the nRF Connect SDK.

**Step 3**: Run the Toolchain Manager, **install the nRF Connect SDK v2.3.0** (as this version will be used in this workshop).
> **Newer SDK version available** You may use a newer SDK version, but keep in mind to then refer to the latest documentation and hyperlinks!

> **Warning**
> Ensure to use a basic directory name (no special characters!) and keep the installation directory close to the file system root! <br> This will ensure no further issues with scripts and the toolchain on heavily nested projects. I am using ***C:/Nordic/SDK***

**Step 4**: Open VS Code through the Toolchain Manager to detect missing extensions/plugins. **Install Nordic's VS Code extensions** (nRF Connect, nRF Terminal, nRF Konfig etc.) by clicking on install missing extensions. Note that you can also install those through the VS Code extensions tab when searching the extensions marketplace for nRF Connect for VS Code extension pack. Also note that you should be aware of conflicting extensions if you have used VS Code previously with other extensions.

**Step 5**: Run VS Code and **perform the Quick Setup on the nRF Connect extension**. Select the nRF Connect SDK and toolchain that matches your setup.

## [Chapter 1 - Matter End Device (e.g. Nordic DK as Matter Light Bulb)](./1_Matter_End_Device.md)
