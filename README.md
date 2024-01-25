# DBAI 2024

This data contains 2-3 KMs each of morning, afternoon, evening and night. This data was collected via drivebuddyai's device installed in multiple vehicles, that has sensors namely a road monitoring camera, a driver monitoring camera, GPS and IMU. 

The `sensor_data` folder contains the dataset in `.json` format files named on with the format `{vehicle type}_{day time}.json`. 

The corresponding video files can be downloaded from the below links.

[morning](https://drivebuddyai.sharepoint.com/:f:/s/drivebuddyAI/EiYe9ZZGw1RHtmz3C1ST4c4Bw4--6_NbREMnwtKjEeZY7A?e=D6zZta) <br>
[afternoon](https://drivebuddyai.sharepoint.com/:f:/s/drivebuddyAI/EsgstvH98shBmWxy4b-hmlQBcpTTWxRKwmAvEvILy3yOfg?e=bgrhpE) <br>
[evening](https://drivebuddyai.sharepoint.com/:f:/s/drivebuddyAI/EnrcWesfRINBm-S8XFbHQhcBJwm4ejBXblMAGkwqFe_K0Q?e=TpObKc) <br>
[night](https://drivebuddyai.sharepoint.com/:f:/s/drivebuddyAI/EiQWYtvJthNFuvANCtE67fEBhkBITL1Kgo5llsb69dRINQ?e=xbMLv0) <br>


## Dataset Structure

#### Directory Structure
```
+-- sensor_data (folder contains .json files) 
    | 
    +-- morning.json 
    +-- afternoon.json 
    +-- evening.json 
    +-- night.json 

 
+-- morning (folder contains .mp4 files of both roadside and driver side)  
    | 
    +-- video_rms_[YYYY]-[MM]-[DD]_[HH]-[MM].mp4 
    +-- video_dms_[YYYY]-[MM]-[DD]_[HH]-[MM].mp4 

+-- afternoon (folder contains .mp4 files of both roadside and driver side)  
    | 
    +-- video_rms_[YYYY]-[MM]-[DD]_[HH]-[MM].mp4 
    +-- video_dms_[YYYY]-[MM]-[DD]_[HH]-[MM].mp4 

+-- evening (folder contains .mp4 files of both roadside and driver side)  
    | 
    +-- video_rms_[YYYY]-[MM]-[DD]_[HH]-[MM].mp4 
    +-- video_dms_[YYYY]-[MM]-[DD]_[HH]-[MM].mp4 

+-- night (folder contains .mp4 files of both roadside and driver side)  
    | 
    +-- video_rms_[YYYY]-[MM]-[DD]_[HH]-[MM].mp4 
    +-- video_dms_[YYYY]-[MM]-[DD]_[HH]-[MM].mp4 

```

#### Data Format
```
timestamp (UTC Time) 
| 
+--orientation (IMU Data) 
   | 
   +--heading (degree) 
   +--roll (degree) 
   +--pitch (degree) 
   +--xAccel (m/s^2) 
   +--yAccel (m/s^2) 
   +--zAccel (m/s^2) 
   +--xAngRate (deg/s) 
   +--yAngRate (deg/s) 
   +--zAngRate (deg/s) 
   +--height (mm) 
+--gnss 
   | 
   +--speedData 
       | 
       +--speed (KM) 
       +--speedMeter (meter) 
   +--location 
       | 
       +--coordinates ([latitude, longitude]) 
       +--gnssFixType (State of gnss) 
   +--distanceData 
       | 
       +--distanceStd (m) 
       +--distance (m) 
       +--totalDistance (m) 
+--dmsVideo (path to driver side video) 
+--rmsVideo (path to roadside side video) 

```