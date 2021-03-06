[English](https://github.com/xingliuhua/easyserver/blob/master/README.md)
# easyserver

一个轻巧但是功能强大的模拟服务器桌面程序。


## 背景
作为前端开发或者APP开发者，经常会遇到服务端未开发部署完毕，但是我们想要提前看下网络请求的效果。想要模拟服务端返回的数据目前我们可以用抓包工具
来实现，比如：fiddler、charles等等，大致流程都是拦截请求和服务端返回的响应。

市面上的抓包工具有很多优点：
* 我们电脑上基本都有安装。
* 使用方便，bug较少。

但是我们也发现有些缺点：
* 开启占用内存多。
* 有些工具每次请求都要改返回响应信息，比较麻烦。
* 有些工具虽然能设置请求自动返回的数据，但是数据是自己保存文件，时间长了自己都忘了放哪里了，容易丢。
* 工具都是针对请求路径，如果要模拟不同参数返回的数据，就要不停的改。
* 同组人员虽然也能连同一个抓包工具，但是想到别人电脑上改动比较麻烦。


## 功能
* 能对请求设置返回信息，自动返回信息。
* 返回信息自动保存到磁盘，下次启动自动加载。
* 请求方式 + 接口地址 + 所有参数 这些都完全相同才认为是同一请求。
* 同时支持GUI操作和文件配置，使用简单。
* 支持多人在线配置并使用。
* 小巧轻便，占用内存少。
* 支持mac、window，linux。

## 安装
1. 下载对应平台的zip包。

[mac](https://github.com/xingliuhua/easyserver/blob/master/easyserver_mac_v1.0.tar.gz)

[windows-64](https://github.com/xingliuhua/easyserver/blob/master/easyserver_windows_v1.0.zip)

2. 解压缩即可，不需要安装任何依赖。

## 使用
以mac为例，
1. 命令行启动
解压后运行
```tex
./easyserver
```
2. 设置端口并启动
<img src="https://github.com/xingliuhua/easyserver/blob/master/easyserver_pic_run.png"  >

我们看到会出现一个对话框出来了，我们可以改动要监听的端口。
比如我们想要模拟：http://test:8888/login 接口，我们就输入8888即可。
点击Run按钮（点击后鼠标离开即可看到按钮状态变化）

3. 浏览器打开 http://localhost:8888/easyserver/index

<img src="https://github.com/xingliuhua/easyserver/blob/master/easyserver_pic_index.png">

前端或app请求http://xxxx:8888/login接口，刷新网页，我们就可以看到请求记录了,其中"xxxx"是本机的IP地址,
点击右边的修改图标进入到添加页面，修改返回信息提交，这样我们就设置了一个请求的返回信息。后面再次请求登录接口就返回了想要的信息。

`注意：app请求的时候url要写easyserver所运行的电脑IP地址，只有这样你才能访问得到`
4. 点击index页面的config链接，我们可以看到以前配置的请求列表，支持修改，删除。

5. 不想使用可直接点击关闭，想暂时关闭请点击"Stop"按钮。

## 优化
在使用的过程中发现还有很多需要优化的地方，后期会一一优化。
* APP请求后，首页不会自动刷新请求记录。
* 页面丑陋。
* 同一个请求只是参数改变就需要配置，过于麻烦，既是优点又是缺点。

### 维护者

[@xingliuhua](https://github.com/xingliuhua).

### 如何贡献

非常欢迎你的加入! 提一个Issue 或者提交一个 Pull Request.
