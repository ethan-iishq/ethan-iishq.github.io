---
layout: post
title: linux下解压tar.xz文件的命令
key: 20161103
tags: jar
---

假设更改test.jar中的jdbc.properties文件

### 1、列出该配置文件：

` $jar -tf test.jar | grep jdbc.properties`

`METF-INF/jdbc.properties`

### 2、加压处该配置文件：
` $jar -xf test.jar METF-INF/jdbc.properties`

### 3、编辑配置文件，保存。
` $vim METF-INF/jdbc.properties`

### 4、更新配置文件到jar包中
` $jar -uf test.jar METF-INF/jdbc.properties`
` $rm -f METF-INF/jdbc.properties`

### 5、完毕
