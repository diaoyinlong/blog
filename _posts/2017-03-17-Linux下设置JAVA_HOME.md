---
title: Linux下设置JAVA_HOME
layout: post
categories: 环境部署
tags: JAVA
---
__编辑/etc/profile__  
export JAVA_HOME=/usr/java/jdk1.8.0_101  
export JRE_HOME=${JAVA_HOME}/jre    
export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib    
export PATH=${JAVA_HOME}/bin:$PATH