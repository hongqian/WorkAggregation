# WorkAggregation
基于数据技术的招聘信息聚合系统
本系统以Python为核心，依托web展示，所有功能在网页就可以完成操作，爬虫、分析、可视化、互动独立成模块，互通有无。具体依托python的丰富库实现，爬虫使用Requests爬取，使用lxml、beautifulsoup4解析。使用numpy、pandas分析数据，使用pyecharts做可视化，使用Flask进行web后台建设。数据通过csv、MySQL、配置文件来进行存储互通。  
为了拓展功能编写了定时器，微信推送，为了适应团队合作编写了函数注册器，参数迭代器。  
提供大约50万条数据，来自前程无忧、齐鲁人才网、猎聘网、拉勾网等等网站，需要的基本数据一应俱全。

## 环境
- Windows 
- Linux 未测试
- Python 3.6 
- MySQL 8.0.11  
- Chrome（内核版本60以上）

## 安装
1. 运行 install_package.bat（出错管理员权限下尝试）  
2. 解压MySQL 8.0.11 并将 my.ini移到MySQL软件目录    
如图配置好mysql目录和mysqldata目录  
3. 初始化mysql   
4. 点击 server.py 来运行web服务器  
5. 使用Chrome访问 http://127.0.0.1:5000/  

## 架构
系统大致结构如下图，spider目录存放爬虫代码，analysis目录承担了导入、分析、渲染图表、交互等功能，data目录存放原始数据，conf目录存放图表、mysql配置文件。导入处理分析入口统一由analysis_main控制，由server调用，其他功能直接由server调用，所有功能在主页就可以启动。
![](https://github.com/xming521/picture/blob/master/job2.png)
![](https://github.com/xming521/picture/blob/master/job1.jpg)

## 鸣谢
鸣谢 server酱、 pyechart 、腾讯云等的产品或技术支持