目前进度只完成了基础功能，为每个满足收藏数限制的作品创建文件夹，保存缩略图和data信息，包括作品名，作者名，地址等。
未完成：自定义存储文件夹，自定义收藏数限制，自定义用户名密码
未完成：使用代理IP相关（获取，动态变换）
未完成：web端显示
使用了8个多线程同时抓取
使用config文件存储cookies和用户密码，登录时抓取post_key
使用requests获取网页
使用正则匹配获取关键字
实现了直接存大图，但目前应对反爬能力有限，故未采用消耗流量之方法，
另为支持P站发展，只提供缩略图也属合理需求

bug：部分作品出现大量创建多个文件夹

*重要*编码问题解决方案：
pixiv包含大量特殊字符、中文、日文、韩文、emoji符号，
需要修改python默认IO为utf-8并且控制台编码也为utf-8
推荐使用Python自身IDLE或pycharm