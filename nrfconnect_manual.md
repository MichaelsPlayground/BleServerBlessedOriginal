# Manual to use the nRF Connect app with a BLE device

1) download the app here https://play.google.com/store/apps/details?id=no.nordicsemi.android.mcp&hl=de&gl=US

2) start the app and the BLE server on a second device, press "scan" if the server is not found 

[nRFConnect_manual](nrfconnect_manual.md)

![found server](docs/server01.png?raw=true)

![found server](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server01.png?raw=true)

3) press connect to start the connection with the server and see the services that are published by the server:

**Important notice when working with a emulated device running on a Smartphone (e.g. the BleServerBlessedOriginal): 
For security reasons the address the server can get connected is changing very often so when using the nRF Connect-app 
it is often necessary to (re)run a scan AND choose the newest entry (mostly the most bottom down one).**

![published_services](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server02.png?raw=true)

4) The BleServerBlessedOriginal server is providing the general services like **General Attribute**, 
**Generic Access** and **Device Information** and 2 data services like the **Current Time Service** and 
a **Heart Rate Service**. Note: sometimes a service is duplicated shown. 

Now click on the **Heart Rate** entry and we see the Heart Rate Measurement **characteristic** with the "short" UUID 0x2A37:

![heart_rate_service](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server03.png?raw=true)

5) The properties for this characteristic show "INDICATE" and "READ" and 2 symbols behind. The "down arrow" is for reading the data, 
the "up and down arrows" are for the INDICATE option, means you can get updates when the value is changing. Here I pressed the "read" 
(= the "down arrow") and get the actual value for the heart rate (64 bpm). A note on INDICATION - sometimes you see a 
"NOTIFICATION" instead - it is similar to "INDICATE" but the server does not await a confirmation.

![heart_rate_data](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server04.png?raw=true)

6) Pressing the "INDICATE" arrow will activate a continuous sending of the heart rate (this server is running an update every second).   
In the "Descriptors" section you see that "Indications enabled" shows up. A second press on the "INDICATE" button will stop the 
indication.

![heart_rate_data](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server05.png?raw=true)

7) The **Device Information** should give some information about the device, the Server will use the information from the Smartphone it 
is running on.

![heart_rate_data](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server06.png?raw=true)

8) The last service exposed by the Server is the **Current Time Service** that allows to READ, NOTIFY and WRITE ("arrow up" symbol). 
I activated the notification and now I'm getting the actual time provided by Server's (= Smartphones) time. 

![heart_rate_data](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server07.png?raw=true)

A note on writing data to the server: you need to know what the format is the server accepts for this 
characteristic. Giving a wrong (=not accepted) value or not the necessary amount of data will result in a failure.
 
