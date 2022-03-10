# 测试培训课件-Chales的功能使用（一）
## 一、学习目标：

<font color=#999AAA >学习Chales的基本原理，安装、激活、简单抓包分析
<hr style=" border:solid; width:100px; height:1px;" color=#000000 size=1">

## 二、学习内容：
 ### 1.  Charles的基本介介绍
 

> 是一个HTTP代理服务器,HTTP监视器,反转代理服务器，当浏览器连接Charles的代理访问互联网时，Charles可以监控浏览器发送和接收的所有数据。它允许一个开发者查看所有连接互联网的HTTP通信，这些包括request, response和HTTP headers （包含cookies与caching信息）。是常用的网络封包截取工具，在做移动开发时，我们为了调试与服务器端的网络通讯协议，常常需要截取网络封包来分析。

　　Charles 通过将自己设置成系统的网络访问代理服务器，使得所有的网络访问请求都通过它来完成，从而实现了网络封包的截取和分析。
　　除了在做移动开发中调试端口外，Charles 也可以用于分析第三方应用的通讯协议。配合 Charles 的 SSL 功能，Charles 还可以分析 Https 协议。

 - 支持SSL代理。可以截取分析SSL的请求。
 - 支持流量控制。可以模拟慢速网络以及等待时间较长的请求。
 - 支持AJAX调试。可以自动将json或xml数据格式化，方便查看。
 - 支持AMF调试。可以将Flash Remoting 或 Flex Remoting信息格式化，方便查看。
 - 支持重发网络请求，方便后端调试。
 - 支持修改网络请求参数。
 - 支持网络请求的截获并动态修改。
 - 检查HTML，CSS和RSS内容是否符合W3C标准。
**注意：该软件在特殊情况下会出现劫持浏览器导致无法浏览网页的问题(请谨慎使用)。**

### 2.  关于Charles的安装
Charles下载地址：[https://www.charlesproxy.com/download/](https://www.charlesproxy.com/download/)
通过官网下载对应电脑系统的Charles的安装包
![在这里插入图片描述](https://img-blog.csdnimg.cn/c5d49d506d484c6d8d32f948f8b4acaf.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6Z2e6Iqx6Z2e6Zu-LS0=,size_20,color_FFFFFF,t_70,g_se,x_16)
Charles的安装相对简单，双击安装包即可，直接下一步直到安装完成（window安装时建议安装到D盘或者其他非系统盘）

> 安装完成后打开Charles即可

![在这里插入图片描述](https://img-blog.csdnimg.cn/c97310ba128947b68414a7dffe3cd23b.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6Z2e6Iqx6Z2e6Zu-LS0=,size_20,color_FFFFFF,t_70,g_se,x_16)


 ### 3.  Charles激活工具
 

> 因Charles为收费软件，所以想要使用完整的Chrles功能，需要通过秘钥进行激活，以下为激活流程

 

 - 访问激活码生产地址：[https://tools.zzzmode.com/mytools/charles/](https://tools.zzzmode.com/mytools/charles/)
![在这里插入图片描述](https://img-blog.csdnimg.cn/e8c22115478440fdbc8a7405fa4a72db.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6Z2e6Iqx6Z2e6Zu-LS0=,size_20,color_FFFFFF,t_70,g_se,x_16)
 - 输入任意信息即可生产激活码（最好输入姓名或者其他昵称信息），然后点击生产
 - ![在这里插入图片描述](https://img-blog.csdnimg.cn/3ba0b7869b02477bb9506fec00cd393d.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6Z2e6Iqx6Z2e6Zu-LS0=,size_20,color_FFFFFF,t_70,g_se,x_16)

 - 复制name 以及”License Key:“对应的 激活码数据
 
 - 打开Charles激活码配置页面
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/d7890acb120844739ab982bf90c99479.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6Z2e6Iqx6Z2e6Zu-LS0=,size_20,color_FFFFFF,t_70,g_se,x_16)

 - 输入对应激活码数据，点击Register即可
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20c1089ef3504b7fb40bf57fd9a8c48e.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6Z2e6Iqx6Z2e6Zu-LS0=,size_20,color_FFFFFF,t_70,g_se,x_16)

 - 配置完成后重启即可

 
 ### 4. Charles工具栏介绍
 

> Charls的工具栏主要为菜单栏、工具栏
> 
![在这里插入图片描述](https://img-blog.csdnimg.cn/013da54502c84420bd84da838cb74b18.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6Z2e6Iqx6Z2e6Zu-LS0=,size_20,color_FFFFFF,t_70,g_se,x_16)
#### 菜单栏：

 1. Chrles ：Charles的一些官网信息，版本信息等
 2. File：与Session(会话)相关的功能，导入、导出、关闭、打开等
 3. Edit：对数据进行基本操作的功能
 4. View：接口详细信息相关的功能
 5. Proxy：端口相关功能，只需要重点掌握几个配置的功能点即可
 6. Tools：工具相关功能，关于Charles高级功能的使用
 7. Window：Charles窗口配置
 8. Help：帮助使用Charles的功能
 
#### 工具栏（目前显示在首页的工具栏按钮是所有使用最频繁的工具）
 9. Structure（结构）：以列表形式显示抓取的接口信息，抓取的数据会以域名进行分类
 10. Sequence（顺序）：以接口的请求时间进行显示
 11. OverView（概况）：描述接口的请求的概况，包括接口请求的类型，参数、耗时、协议等等信息
 12. Content （内容）：接口请求的实际的请求参数、header、response等
 13. Sumary（总结）：关于请求的一个总结性数据，一般不太需要关注
 14. Chart：以图表形式展示的数据
 15. Notes：关于接口的备注信息

 ### 5. Charles抓包数据简单学习
基于以上的知识、就可以简单的抓取数据包
![在这里插入图片描述](https://img-blog.csdnimg.cn/b5aa3181338944e088ad082e388b7f29.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6Z2e6Iqx6Z2e6Zu-LS0=,size_20,color_FFFFFF,t_70,g_se,x_16)

> 1、练习抓取百度搜索的数据
> 2、尝试http、https的请求抓取

# 学习时间：

<font color=#999AAA >学习时间规划：
1、 周一至周五晚上 8 点—晚上10点
2、 周六上午 9 点-上午 11 点
3、 周日下午 2 点-下午 4 点
<hr style=" border:solid; width:100px; height:1px;" color=#000000 size=1">

# 学习产出：

<font color=#999AAA >掌握Charles的基本知识

1、熟悉工具栏对应功能
2、熟练掌握安装、激活流程
3、 可以简单抓取http或者其他未加密的数据，并查看
