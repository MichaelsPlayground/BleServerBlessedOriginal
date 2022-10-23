# Manual to use the nRF Connect app with a BLE device

1) download the app here https://play.google.com/store/apps/details?id=no.nordicsemi.android.mcp&hl=de&gl=US

2) start the app and nthe BLE server on a second device, press "scan" if the server is not found 
3) 
![found server](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server01.png?raw=true)

3) press connect to start the connection with the server and see the service that is published by the server:
4) 
![published_services](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server02.png?raw=true)

4) The BleServerBlessedOriginal server is providing the general services like **General Attribute**,  
**Generic Access** and **Device Information** and 2 data services like the **Current Time Service** and   
a **Heart Rate Service**. Note: sometimes a service is duplicated shown. 

Now click on the **Heart Rate** entry:

![heart_rate_service](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server03.png?raw=true)

5) 

![heart_rate_data](https://github.com/MichaelsPlayground/BleServerBlessedOriginal/blob/master/docs/server04.png?raw=true)


