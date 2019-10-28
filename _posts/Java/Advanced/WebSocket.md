---
layout: post
title:  "基于TCP/UDP的“仿微信聊天室”"
categories: Java
tags:  项目 
---



**主要功能：**用户注册登入，查询用户，添加好友，发送消息，视频聊天，发送表情包。
**设计思路：**客户端显示聊天界面，服务器提供多线程处理来自不同客户端的消息，数据库存储用户信息（用户账号，密码，好友列表等）。
**技术方案：**使用Socket实现客户端和服务器之间的连接，客户端配置连接服务器的IP地址和端口号。数据传递使用IO流来实现





TCP 通讯

先写下最简单的服务器怎么搭建



```
ServerSocket ssocket = new ServerSocket(14000);  // 服务器和端口号
Socket socket = ssocket.accept();  //服务器接受的套接字
//获取的数据和输出的数据
InputStream inputStream = socket.getInputStream; //套接字获取输入流
OutputStream outputStream = socket.getOutStream; //套接字 输出流
//可以把输入，输出流转成各种流，调用不同流的方法





```





