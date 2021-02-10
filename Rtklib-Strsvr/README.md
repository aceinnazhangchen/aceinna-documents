[English](README-En.md)
# Strsvr 采集Ins2000数据说明
strsvr.exe 下载地址：<https://github.com/Aceinna/rtklib_aceinna/releases>
## 1. 使用strsvr保存Ins2000数据同时解码

1.1. 【Input】的【Type】选择【Serial】，然后点击其右侧的【Opt】按钮。

![avatar](./img/1.png)

1.2. 在【Serial Options】对话框中【Port】选择Ins2000的串口，【Bitrate】选择460800，点击【OK】保存退出。

![avatar](./img/2.png)

1.3. 点击【Cmd】按钮，打开【Serial/TCP Commands】对话框。

![avatar](./img/3.png)

1.4. 在【Serial/TCP Commands】对话框中勾选【commands at startup】，在文本框中输出配置参数。
```
unlogall
NTRIPCONFIG NCOM1 client V1 47.116.1.17:2201 WX02 AceinnaRTK SIGEMZOOMQ1JDJI3
SETINSTRANSLATION ANT1 -0.28 1.43 1.0 0.20 0.20 0.20
SETINSTRANSLATION DUALANT 0.7 0.0 0.0 0.20 0.20 0.20
SETINSROTATION RBV 0.0 0.0 0.0 0.5 0.5 1.0
SETINSTRANSLATION USER -0.28 1.43 1.0 0.20 0.20 0.20
INSCOMMAND ENABLE
LOG RANGECMPB ONTIME 1
LOG RAWEPHEMB ONCHANGED
LOG GLOEPHEMERISB ONCHANGED
LOG GALEPHEMERISB ONCHANGED
LOG BDSEPHEMERISB ONCHANGED
LOG QZSSEPHEMERISB ONCHANGED
LOG INSCONFIGB ONCHANGED
LOG versionb once
LOG rxstatusb once
LOG inspvaxb ontime 0.1
LOG bestgnssposb ontime 0.1
LOG bestgnssvelb ontime 0.1
LOG headingb ontime 0.1
LOG heading2b ontime 1
LOG RAWIMUSXB ONNEW
LOG gpgga ontime 0.1
LOG NCOM1 gpgga ontime 1
SAVECONFIG
```
![avatar](./img/4.png)

1.5. 【(1)Output】选择【File】，然后点击其右侧的【Opt】按键。

![avatar](./img/5.png)

1.6. 在打开的【File Options】对话框中选择保存文件的路径。

![avatar](./img/6.png)

1.7. 点击左下角的小方块按钮。

![avatar](./img/7.png)

1.8. 在弹出的【Input Stream Monitor】对话框中，选择【Ins2000】。

![avatar](./img/8.png)

1.9. 点击【Start】开始采集数据。

![avatar](./img/9.png)

1.10. 采集数据的数据同时实时解码产生的文件。

![avatar](./img/10.png)

1.11. 如果忘记在【Input Stream Monitor】中选择【Ins2000】导致没有实时解码，可以使用文件解码工具解码。 

文件工具下载：<https://github.com/aceinnazhangchen/Ins2000_deocder/releases>