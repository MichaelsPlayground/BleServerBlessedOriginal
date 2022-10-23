# Manual to use the nRF Connect app with a BLE device

1) download the app here https://play.google.com/store/apps/details?id=no.nordicsemi.android.mcp&hl=de&gl=US

2) start the app and the BLE server on a second device, press "scan" if the server is not found 

![found server](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server01.png?raw=true)

3) press connect to start the connection with the server and see the services that are published by the server:

![published_services](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server02.png?raw=true)

4) The BleServerBlessedOriginal server is providing the general services like **General Attribute**,  
**Generic Access** and **Device Information** and 2 data services like the **Current Time Service** and   
a **Heart Rate Service**. Note: sometimes a service is duplicated shown. 

Now click on the **Heart Rate** entry and we see the Heart Rate Measurement **characteristic** with the "short" UUID 0x2A37:

![heart_rate_service](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server03.png?raw=true)

5) The properties for this characteristic show "INDICATE" and "READ" and 2 symbols behind. The "down arrow" is for reading the data, 
the "up and down arrows" are for the INDICATE option, means you can get updates when the value is changing. Here I pressed the "read" 
(= the "down arrow") and get the actual value for the heart rate (64 bpm).

![heart_rate_data](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server04.png?raw=true)

6) 

![heart_rate_data](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server05.png?raw=true)



![heart_rate_data](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server06.png?raw=true)


![heart_rate_data](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server07.png?raw=true)

