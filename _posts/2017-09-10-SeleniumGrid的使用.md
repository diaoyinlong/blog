---
title: Selenium Grid的使用
layout: post
categories: 自动化
tags: selenium
---

- 启动hub

		java -jar selenium-server-standalone-3.5.3.jar -role hub
		
- 启动node

		java -jar selenium-server-standalone-3.5.3.jar -role node -hub http://192.168.0.108:4444/grid/register
		
- python客户端调用

		from selenium.webdriver.remote.webdriver import WebDriver
		from selenium.webdriver.common.desired_capabilities import DesiredCapabilities

		driver=WebDriver('http://192.168.0.108:4444/wd/hub',DesiredCapabilities.CHROME)
		driver.get('http://www.baidu.com')