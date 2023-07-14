# Chapter 5 - Commissioning the End Device

Once all previous steps are completed, we are now ready to commission a Matter over Thread (or also Matter over WiFi) end device.

### Step 1: Start the Matter End Device and log the output

Note down the Setup Piun Code and the Setup discriminator. On all Nordic examples, these are pre-configured to:

1. Setup pin code: ```20202021```
2. Setup Discriminator: ```3840 (0xF00)```

### Step 2: Start the BLE Advertising (if not started by default) on the Matter End Device

For the Matter Light bulb example, the BLE advertising is automatically started. Press Button 4 to enable advertising / validate this.

### Step 3: Commissioning into Thread network over BLE
To commission the device to the existing Thread network, use the following command pattern:

```
./chip-tool-debug pairing ble-thread <node_id> hex:<operational_dataset> <pin_code> <discriminator>
```

Where node id can be freely selected. <br>
As this is our first Matter node, we will issue node id 0. The Pin code and discriminator are given from the end device configuration. The Thread dataset comes from the Thread Border Router.
This simplifies the command to:

```
./chip-tool-debug pairing ble-thread 0 hex:<operational_dataset> 20202021 3840
```
