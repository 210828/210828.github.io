#### MySQL数据库：JDBC8.0.18------jar包的下载（百度网盘）及导入java-web中的过程
链接: https://pan.baidu.com/s/1I-iWo49zzw6nlx-TqgmJVQ 
提取码: ksqu 
复制这段内容后打开百度网盘手机App，操作更方便哦
1. 下载压缩包bingjieya
2. 解压后找到mysql-connector-java-8.0.18.jar文件
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191205143309252.PNG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
3. 在eclipse的项目中找到WebContent下的WEB-INF中的lib文件，将mysql-connector-java-8.0.18.jar拖到该文件下面
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191205143823753.PNG)
4. 右击项目名称，点击Build Path，再点击Configure Build Path
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191205144930304.png)
5. 点击Libraries，然后点击Add JARs，找到WebContent下的WEB-INF中的lib文件下的mysql-connector-java-8.0.18.jar点击，然后点击ok，再点击Apply and Close就好了
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191205145810365.PNG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTk2ODcyNA==,size_16,color_FFFFFF,t_70)
6. 最后出现Referenced Libraries，如图：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191205145958642.PNG)