---
layout: post
category: "linux"
title:  "centos防火墙"
tags: [Linux]
---



> centos6防火墙


进入防火墙配置命令  

	vim /etc/sysconfig/iptables

光标放到一行上，按yy,再按P，复制一行，开放端口

<!-- more -->

防火墙打开、关闭、重启、查看状态  

	service iptables start
	service iptables stop
	service iptables restart
	service iptables status



> centos7防火墙

开发端口，<zone>里加入  

	vim /etc/firewalld/zones/public.xml
	<port protocol="tcp" port="80"/>
	<port protocol="tcp" port="443"/>

防火墙打开、关闭、重启、查看状态 

	systemctl start firewalld
	systemectl restart firewalld
	systemctl stop firewalld
	systemctl status firewalld