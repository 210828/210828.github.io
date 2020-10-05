---
layout:     post                    # 使用的布局（不需要改）
title:      Myeclipse工具搭建Hibernate开发环境            # 标题 
#subtitle:   Hello World, Hello Blog    #副标题
date:       2020-10-05                  # 时间
author:     Mrs.白                      # 作者
header-img: img/wallhaven-39d3yd.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - 学习
---

**首先下载数据库的驱动程序包，创建一个普通的Java项目（自拟名称），在MySQL中创建数据库，并创建相关的数据表（自拟名称）。**

一.创建数据库的连接

 1. 打开MyEclipse Database Explorer

 		![在这里插入图片描述](https://img-blog.csdnimg.cn/20200518081622350.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
2.	在打开窗口的右侧，选择New
		![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410141935556.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
	
3. 在弹出的对话框中进行数据库连接驱动设置
  （添加数据库的驱动程序包，添加驱动程序后，系统会自动生成Driver Classname）

  ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410142155854.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70) 

 4. 单击Test Driver测试连接是否成功，勾选Save password。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410142240422.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
 5. 就创建了一个名为myconn的连接
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410142357978.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)

二.添加Hibernate Capabilities.....

 1. 右键单击项目，选择MyEclipse——Add Hibernate Capabilities.....
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410142441304.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
 2. 点击next
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410135357131.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
 3. 设置配置文件的路径及名称，点击下一步
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410135403122.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
 4. 进行数据库连接的设置，点击next
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020041014274683.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
 5. 进行Session Factory的创建，点击new
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410142858625.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
 6. 在src下创建一个新包，点击Finish
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410142951117.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
 7. 工程中会增加一个配置文件和一个HibernateSessionFactory类
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410143021702.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)


三.创建实体类 编写实体类，包括： 实体的相关属性 公有无参构造方法 相应属性的setter和getter方法

创建包，并在包中创建User类，类中描述基本的属性及相应属性的setter和getter方法
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410135823195.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)

四.创建映射文件

 1. 打开MyEclipse Datebase Explorer，找的myconn连接，找的自定义的数据库，然后在TABLE找到自定义的数据表

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410135952516.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)

2. 在表名上单击右键，选择方向工程Hibernate Reverse Engineering
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410143223616.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
3. 设置映射文件存放包，点击Browse
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410143321854.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
4. 点击src——com.my.vo,点击OK
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410143418145.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
5. 勾选第一个，点击next
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410143451651.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
6. 设置映射类型和主键生成策略，选择Navicat，点击next
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410143525752.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
7. 设置映射相关的实体类，点击Finish
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410143614309.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
8. 在实体类的包下则创建了一个映射文件
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200410143649317.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)