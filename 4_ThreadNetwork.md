# Chapter 4 - Running the OTBR to create a Thread network

Running the OTBR to create a Thread network, e.g. to build the underlying layer for Matter over Thread operation. <br> 
For Matter over WiFi applications, this chapter can be skipped. <br>

We are using the OTBR command line interface (ot-ctl commands).

You may search through the commands and usage interactively by adding the parameter help to the respective command.<br> Examples:

```
sudo ot-ctl help
sudo ot-ctl dataset help
```

### Step 1: Create a new Thread network configuration

Set up a new Thread dataset / network config.

```
sudo ot-ctl dataset init new
```

### Step 2: Commit the dataset to active operational dataset in non-volatile storage

```
sudo ot-ctl dataset commit active
```

### Step 3: Bring up the network interface
```
sudo ot-ctl ifconfig up
```

### Step 4: Start the Thread operation
```
sudo ot-ctl thread start
```

### Step 5: Verify that Thread network is running
The device should act as Thread leader.

```
sudo ot-ctl state
```

Expect:
```
leader
Done
```

### Step 6: Retrieve the Thread network credentials in HEX format

> **Note**
 The Thread network configuration and network credentials are stored in the Thread dataset that has just been created. The dataset needs to be given to the Matter controller/Chip Tool to perform the commissioning for a Matter over Thread end device.

List the active dataset in HEX format, save the output.
```
sudo ot-ctl dataset active -x
```

## Next Chapter
Switch to [Chapter 5 - Commissioning the End Device](./5_Commissioning.md)
