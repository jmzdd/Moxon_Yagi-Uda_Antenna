# <center>Moxon-Yagi-ntenna

⚠实验性：天线尚未经过矢量网络分析仪测量，未实际使用测试，仅通过MMANA-GAL仿真。

## 1、项目背景

&emsp;&emsp;本天线设计参考了“Moxo n-Yagi Satelli te Antenna by DUIAU (based LY3LP's design)”，感谢DU1AU和LY3LP两位前辈的贡献，原设计图如下：

<div align=center> <img src="https://raw.githubusercontent.com/jmzdd/Moxon_Yagi-Uda_Antenna/main/Raedme/design.jpg" width = 40%/> </div>

&emsp;&emsp;由于本人手上只有直径1.25mm的铜线作为振子，因此需要对天线的尺寸重新设计。这里我选择使用MMANA-GAL软件对天线进行仿真。花了一两天时间在B站熟悉和理解软件的使用，最后根据软件的仿真结果制作出了成品。

## 2、设计过程
&emsp;&emsp;因为是UV双段天线，因此要求天线的中心频率在常用的两个频段：145MHz与435MHz。使用软件对该天线进行仿真，在结构不变的前提下，我修改了振子的长度与各振子之间的间距，最终得出了想要的结果。

&emsp;&emsp;由于理论知识实在欠缺，在设计过程中遇到的问题大多交给Gemini帮忙给出建议，例如：要解决天线阻抗偏小的问题，可以采取以下措施：
+ 增加天线的尺寸。天线的尺寸越大，天线的输入阻抗就越高。
+ 缩短馈电点的长度。馈电点的长度越短，天线的输入阻抗就越高。
+ 添加串联电感。串联电感可以提高天线的输入阻抗。

&emsp;&emsp;经过调整后，软件显示天线在145MHz的时候，其阻抗为51.46欧姆，驻波比为1.03;当频率为435MHz时，其阻抗为51.1欧姆，驻波比为1.13。

<div align=center> <img src="https://raw.githubusercontent.com/jmzdd/Moxon_Yagi-Uda_Antenna/main/Raedme/size.png" width = 40%/> </div>
&emsp;
<div align=center> <img src="https://raw.githubusercontent.com/jmzdd/Moxon_Yagi-Uda_Antenna/main/Raedme/ant.jpg" width = 40%/> </div>

## 3、说明
&emsp;&emsp;仓库内包含了我所使用的仿真软件安装包以及所有的仿真结果，软件资源来源自互联网。现对仿真文件进行说明：

| 文件名 | 说明  |
|:--------:| :---------:|
| moxon+yagi_d1.25mm.maa | 振子直径为1.25mm |
| moxon+yagi_d2mm.maa | 振子直径为2mm |
| moxon+yagi_d3mm.maa | 振子直径为3mm |

&emsp;&emsp;软件在使用过程中可能会出现“点击仿真不出结果”的情况，我没有找到原因。如果有知道原因的同学，欢迎联系我~

## 4、测试过程

&emsp;&emsp;由于手上没有设备，因此使用了RTL-SDR进行测试，其中145MHz不明显，435MHz瀑布图如下：
<div align=center> <img src="https://raw.githubusercontent.com/jmzdd/Moxon_Yagi-Uda_Antenna/main/Raedme/435MHz.png" width = 40%/> </div>


## 5、参考资料
### 仿真软件学习
+ <a href="https://www.qsl.net/bv3fg/ant/MMANA-GAL_manual_zh-TW_20211206-01.pdf">【MMANA-GAL_manual_zh-TW.pdf】</a>
+ <a href="https://www.bilibili.com/video/BV14J411Q7TQ/?vd_source=4c90b194142aa9512e6e97d2155ada5d">【宅台长】天线设计软件MMANA-GAL介绍</a>
+ <a href="https://www.bilibili.com/video/BV12Z4y1B7dj/?vd_source=4c90b194142aa9512e6e97d2155ada5d">【业余无线电·天线仿真】MMANA-GAL仿真：莫克森天线应该怎样调整</a>
### 天线计算器
+ <a href="https://upall.cn/example/moxon/">【天线计算器】</a>
### 调试与制作
+ <a href="https://www.hellocq.net/forum/read.php?tid=374264">DIY“莫克森+八木”UV双段天线</a>
+ <a href="https://www.bilibili.com/video/BV19v411T7gT/?vd_source=4c90b194142aa9512e6e97d2155ada5d">自己做一根UV段八木天线连接国际空间站转发器能成功吗？</a>

希望能够对看到这份文档的朋友提供一些小帮助，73~
