[中文](README.md)

# OpenRTK Dirver Instructions

## Burn firmware

1. Connect OpenRTK330LI to the computer with a usb cable.

2. Burn the firmware to OpenRTK330LI.

## Data collection

(You can also use python-openimu to collect data.)

1. Open OpenRTK_Dirver.exe and select the three serial ports corresponding to OpenRTK330LI. If the serial ports are not displayed, you can click [Refresh] to try.

![avatar](./img/01.png)

2. Click [Open] without checking [replay file] to collect the data of OpenRTK330LI into a local file.

![avatar](./img/02.png)

3. Click [Log Path] to open the collection folder. The three files in the folder correspond to the data collected by the three serial ports.

![avatar](./img/03.png)
![avatar](./img/04.png)

4. After a period of time, click [Close] to stop collecting data.

![avatar](./img/05.png)

5. Serial_1_COMX_XXXX-XX-XX_XX-XX-XX.bin collected by the first serial port is the result data and IMU raw data file,if you use python-openimu to collect data, this file same as the user_XXXX-XX-XX-XX_XX-XX-XX.bin file collected by python-openimu.

![avatar](./img/06.png)
![avatar](./img/06-1.png)

6. Serial_3_COMX_XXXX-XX-XX_XX-XX-XX.bin collected by the third serial port is the original rtcm data file,if you use python-openimu to collect data, this file same as the rtcm_base_XXXX-XX-XX_XX-XX-XX.bin file collected by python-openimu.

![avatar](./img/07.png)
![avatar](./img/07-1.png)

## Decode data

1. Click the [Tools] menu and select [Decoder] to open the [Decoding Tool].

![avatar](./img/08.png)

2. Select [openrtk], and select the file collected by the first serial port, and click [decode].

![avatar](./img/09.png)

3. The files in the folder are the decoded data, and the files with the suffix _s1.bin are the raw data of imu.

![avatar](./img/10.png)

## Merge data

1. Click the [Tools] menu, select [Merger] to open [Merge Tool].

![avatar](./img/11.png)

2. The rtcm file selects the file collected by the third serial port, and the imu file selects the imu raw data decoded before.

![avatar](./img/12.png)

3. Click [merge] to merge the files into one raw data file.

![avatar](./img/13.png)

## Replay

1. Power off and restart OpenRTK330LI, you need to restart the device every time before replaying data.

2. Select the three serial ports corresponding to OpenRTK330LI.

![avatar](./img/01.png)

3. Check [replay file], and select the merged raw data file.

![avatar](./img/14.png)

4. Click [Open] to start replay.

![avatar](./img/15.png)

5. The first serial port still outputs the result data file, you can use [Decode Tools] to decode it.

![avatar](./img/16.png)
![avatar](./img/17.png)


