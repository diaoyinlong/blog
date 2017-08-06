---
title: 在Linux上部署chromedriver
layout: post
categories: 环境部署
tags: '自动化'
---
* 下载[ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/downloads)
* 将ChromeDriver分别放在/usr/local/share/和/usr/local/bin/
* 在/usr/bin/下创建软链chromedriver指向/usr/local/share/chromedriver
