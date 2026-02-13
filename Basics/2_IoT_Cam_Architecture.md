# Introduction 

Before applying STRIDE , we have to understand the basic architecture of the cloud based iot camera , in this document . we'll be defining  the following :

1. Components
2. Data flow
3. Trust boundary
4. Assets

Defining the above are important because STRIDE threat model works on system components.

## Data flow of a Cloud connected IOT camera :

![Cloud IoT Camera Data Flow](https://github.com/ricktor0/cloud-iot-camera-threat-modeling/blob/d1394b4f8f2c285ed9498f6dcea85beb25371422/Basics/cloudbasedcam.png)

Your 10-step flow:

1. Camera captures video
2. Encodes (H.264/H.265)
3. Connects to router
4. Sends stream (RTSP/HTTPS/etc.)
5. Data reaches cloud
6. Cloud authenticates & stores/relays
7. User opens app
8. App requests access
9. Cloud verifies token    
10. Cloud relays video


