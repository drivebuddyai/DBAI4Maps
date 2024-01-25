# DBAI 2024

This data contains 2-3 KMs each of morning, afternoon, evening and night. This data was collected via drivebuddyai's device installed in multiple vehicles, that has sensors namely a road monitoring camera, a driver monitoring camera, GPS and IMU. 

The `sensor_data` folder contains the dataset in `.json` format files named on with the format `{vehicle type}_{day time}.json`. 

The corresponding video files can be downloaded from the below links.

[morning](https://drivebuddyai-my.sharepoint.com/:f:/g/personal/kanaksvi_drivebuddyai_co/EpNZDD6pFrJDrxxFE93gYIgBUzDrOsE2LsODad-38hiMPA?e=AqIbFY) <br>
[afternoon](https://drivebuddyai-my.sharepoint.com/:f:/g/personal/kanaksvi_drivebuddyai_co/EnBv6RP6axxDlr7e43qqVYYBG8_FObE-DiKL2FSRTthJOA?e=BkaLHH) <br>
[evening](https://drivebuddyai-my.sharepoint.com/:f:/g/personal/kanaksvi_drivebuddyai_co/EkKa3ABUhRxKmhWXONd9XIQBlDdXmaFXZrJ6jthMn1By_w?e=Y2nA8Z) <br>
[night](https://drivebuddyai-my.sharepoint.com/:f:/g/personal/kanaksvi_drivebuddyai_co/Ei1lAHVo5nZGhEXaqk9jvPUBkLFhM5bd_8wUt9whNA5Y7g?e=xJfo4o) <br>


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
