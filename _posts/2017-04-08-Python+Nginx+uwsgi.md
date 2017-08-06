---
title: Python+Nginx+uwsgi
layout: post
categories: 环境部署
tags: 'Django'
---

- 在Django项目的wsgi.py目录下添加django.xml文件
- 修改Nginx配置
- 安装uwsgi

***
    <uwsgi>
    <socket>127.0.0.1:8081</socket>
    <chdir>/home/diao/Projects/hello_django/hello_django</chdir>
    <pythonpath>..</pythonpath>
    <module>wsgi</module>
    </uwsgi>

***
    server {
        listen       8080;
        server_name  127.0.0.1;
        
        location / {            
            uwsgi_pass  127.0.0.1:8081;
            include  uwsgi_params;
        }
    }
    
***
    sudo apt install uwsgi

    sudo apt install uwsgi-plugin-python3

    uwsgi -x /home/hysia/website/blog/django.xml
