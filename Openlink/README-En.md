# How to use openrtk as a base station

Openlink download：<https://github.com/Aceinna/openrtk_core/releases>

Select a path to save log file.

![avatar](./img/1.png)

Connect openrtk330 serial port to computer, click the first [config] button of [Input] [Stream] open the configuration dialog.

![avatar](./img/2.png)
 
Check the [Input-1], select [Serial Port] for [Stream], select the second serial port, select 460800 for [Bitrate], finally, click the [OK] button.

![avatar](./img/3.png)

Click the first [config] button of [Output] [Stream] open the configuration dialog.

![avatar](./img/4.png)

Check [Output-1], select [NTRIP Client/Caster] for [Stream] , input [Host], [Port] , [Mountpoint] and so on, click the [OK] button.

![avatar](./img/5.png)

Click [Options] to open the station’s configuration dialog window.

![avatar](./img/6.png)

Check the [Station ID] and input station id，input latitude, longitude and height when selected [Lat/Lon/Height] or input x , y and z when selected [X/Y/Z], if [use pos in type(999)] is checked, the position in type 999 will be used.

![avatar](./img/7.png)

Click [start] to upload data as a base station.

![avatar](./img/8.png)