---
title: VirtualBox无法识别USB设备的解决方案
layout: post
categories: Linux
tags: Virtual Box
---

 - 问题描述  
 最近想将iPhone上的照片和视频导出到电脑上，可是Apple并没有提供Linux版iTunes，所以只好借助虚拟机来做中转。使用Virtual Box安装好Win7后在控制台->设置->usb设备->添加usb筛选里无法识别任何usb设备。  
	
 - 解决方案  
 将当前用户添加到virtual box用户组，添加成功后即可设置usb筛选器。
	
		sudo usermod -G vboxusers -a your_account_name
	

	> 注：最好使用usb3.0控制器否则虚拟机无法识别usb3.0设备
