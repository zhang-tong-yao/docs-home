# Wall

<div align="center">

![](https://camo.githubusercontent.com/f9095c0db982b668c03349722093ae6a0a6e2ce83c4ef7f78fd3bbc5b1c67e11/68747470733a2f2f696d672d626c6f672e6373646e696d672e636e2f31383432343632646131333134376665613163343866386333386663363132352e706e67)

![Vue](https://img.shields.io/badge/Vue-3.2.13-brightgreen.svg) &nbsp; 
![Spring Boot 2.2.6](https://img.shields.io/badge/Spring%20Boot-2.2.6-brightgreen.svg)

</div>

Wall是一款快速分享资源应用程序。俗称“照片墙、视频墙”，基于Vue3 + Spring Boot开发的云共享资源应用系统。快速分享发布照片和视频平台。兼容PC端和移动端，支持端对端跨平台上传资源文件。

- 演示地址：[https://demo-wall.ityao.cn](https://demo-wall.ityao.cn)

- 后台管理：[https://demo-wall.ityao.cn/login](https://demo-wall.ityao.cn/login)，账号密码：admin/123456

🌟如果这个项目让你有所收获，记得 Star 关注哦，这对我是非常不错的鼓励与支持。

## 演示截图

![](https://camo.githubusercontent.com/e680070d160ceaa7172cf2520f97a0cce195c64f7bdc93a5ba9e7206b670fa24/68747470733a2f2f696d672d626c6f672e6373646e696d672e636e2f6469726563742f66656538313065623365373834366563386332633632303762343930393361352e706e67)

![](https://camo.githubusercontent.com/5c66847dfa9d850d18aa55ed2e25c28f6f1288be90b2b37fcfa3b007e6297419/68747470733a2f2f696d672d626c6f672e6373646e696d672e636e2f6469726563742f63363035326563333230353734363538616363343861303065636465383031642e706e67)

![](https://camo.githubusercontent.com/05b7f4c72c985f07f9f1248f5337c090c60137efda4ebc4e24be0e5612b01aff/68747470733a2f2f696d672d626c6f672e6373646e696d672e636e2f6469726563742f62643263366439323361336334633936393330376630363563623062333538362e706e67)

![](https://camo.githubusercontent.com/b080792198ab1173702182a554f1ff071bdfe303ec7e402c2ebf4595c7d0c899/68747470733a2f2f696d672d626c6f672e6373646e696d672e636e2f6469726563742f34323034636264343666636634346464616338643831396631646463386563372e706e67)

![](https://camo.githubusercontent.com/224f21ef31e3322d80986128cd2cb168c571edf37c04e4ac04aee1a570ffef2d/68747470733a2f2f696d672d626c6f672e6373646e696d672e636e2f6469726563742f34396165636536663264313634653437386133653738316134396161363763312e706e67)

![](https://camo.githubusercontent.com/9bb3d7a1707f39d030d639cd33e15dfe9ac2b376f6f2f51424d231e6245d0214/68747470733a2f2f696d672d626c6f672e6373646e696d672e636e2f6469726563742f32376331633338356366323334343836616163663166333939356438653831652e706e67)

![](https://camo.githubusercontent.com/bc30933f0fc7d04d02f26031b337f0fcfdd886bd2f1bcc85f68865c9f9263a36/68747470733a2f2f696d672d626c6f672e6373646e696d672e636e2f6469726563742f66653336656133363037333534353062616362306639373238633139613261322e6a706567)

## 开发者名单

Wall还有很多不足之处，比如部分移动端机型兼容等相关问题，或许你可以加入Wall团队，我们一起贡献代码。[申请加入](#共同协作)

下面表格中出现你的名称及主页地址，视为Wall团队成员。

| 名称          | Github                           |
| ------------- | -------------------------------- |
| Tongyao       | https://github.com/zhang-tong-yao |
| 期待你的入... | 期待你的入...                    |

## 安装教程

1、下载地址：[https://github.com/zhang-tong-yao/wall/releases](https://github.com/zhang-tong-yao/wall/releases)，以最新版为准。

2、解压缩包，如下图展示文件目录内容。

![](https://img-blog.csdnimg.cn/direct/f158faad18c34107aafb6e1c69a0e040.png)

- startup.bat：Wall启动脚本。
- wall-3.0.0.sql：后端数据库。

### 程序安装

注：3.0.0版本以上为收费版本（29元，永久使用）。[2.0.0（3.0.0的旧版）以下为免费开源版本，点我跳转2.0.0安装文档。](/2.0.0.md)


注：自3.0.0版本以上起，只需导入数据库SQL，在Wall目录下执行start脚本均可一键启动，无需其他操作。

1、导入```Wall.sql```文件到MySQL数据库，`注：MySQL为5.7版本`。

```
mysql> source wall-3.0.0.sql
```

2、修改config/application.yml配置文件，并修改你本地的MySQL数据库连接端口及账号密码。

```
# project prot
server:
  port: 9999

# database config
mysql:
  database: wall
  port: 3306
  ip: 127.0.0.1
  username: root
  password: root
```

3、后端服务支持两种环境下快捷启动。

- Windows：双击```startup.bat```文件启动。

- Linux：执行根目录```./startup.sh```文件启动。


在Linux下，如果你想关闭会话后继续运行Wall，那么可以搭配nohup使用。

```
nohup ./startup.sh r> /dev/null 2> /dev/null &
```

4、浏览器访问Wall程序。

浏览器输入：```http://localhost:9999```，正常显示页面及操作数据，至此完成安装。

后台管理：```http://localhost:9999/login```，默认账号密码：admin/123456，如有问题，请提交Issues。

### 拓展配置（可选）

主要简化Wall安装程序后的一些基本配置，如暂不需要，无需配置。

1、修改后端服务端口

默认端口为9999，修改config/application.yml配置文件。并修改你的后端端口，本文设置为8080。

```
# project prot
server:
  port: 8080
  
......
```

2、修改Wall上传文件大小限制

修改config/application.yml配置文件，暂改为2048（2GB）。

```
# spring config
spring:
  ......

# file upload size
  servlet:
    multipart:
      max-file-size: 2048MB
      max-request-size: 2048MB
```

## 更新日志
#### 2024－06 - 12（v3.0.0）

> 1. 全新首页瀑布流布局展示
> 2. 全新资源UI展示界面
> 3. 全新安装启动程序及脚本，实现一键安装
> 4. 新增VR全景展示功能
> 5. 新增系统欢迎初始页
> 6. 新增对资源文件密码验证功能
> 7. 新增批量上传资源功能
> 8. 新增批量上传图床URL资源功能
> 9. 新增自定义设置封面压缩比例
> 10. 新增自定义设置首页布局展示
> 11. 支持资源文件标题默认为空
> 12. 优化上传封面识别算法功能
> 13. 优化处理上传资源文件算法功能
> 14. 优化修复首页加载慢效率问题
> 15. 优化修复资源列表修改资源等字段问题
> 16. 优化修复后台表单及自适应等问题
> 17. 优化修复首页瀑布流展示及自适应等问题
> 18. 优化修复删除资源文件本地资源不删除问题
> 19. 重构资源查看器和图片、视频、VR全景一并轮播展示功能
> 20. 支持以Linux为内核系统如：Cent OS、Ubuntu、Debian等系统

#### 2023－04 - 03（v2.0.3）

> 1. 修复后端默认配置文件信息
> 2. 优化前端相应提示文字

#### 2023－03－22（v2.0.2）

> 1. 修复封面图片压缩算法。

#### 2023－03－15（v2.0.1）

> 1. 修复Linux系统下启动时相关小问题。

#### 2023－03－14（v2.0.0）

> 1. 修复并兼容Linux操作系统。
> 1. 修复图片视频资源上传路径相关小问题。
> 1. 简化安装配置及实现一键启动Wall程序。

#### 2023－03－10（v1.0.1）

> 1. 修复上传点击标签归类时会唤起软键盘问题。
> 2. 修复上传选择图后又删除或重新选择时选不了相册问题。
> 3. 优化设置页面相应提示语。
> 4. 优化部分页面样式效果。
> 5. 优化上传选中标签时可见1个问题。

#### 2023－03－07（v1.0.0）

> 1. 初始版本发布

## 共同协作

参与共同协作会得到什么？

- 你会出现在Wall开源人员贡献列表。
- 扎实的应用技术。
- 为求职简历加分。

根据下列模板修改并回答问题：

- 擅长技术：你熟悉和擅长的技术。

- 主页地址：你的GitHub主页地址或其他主页地址（用于展示跳转你的主页）。

- 如何理解开源？：你如何理解开源思想和想法。


并发送至邮箱：super_tongyao@163.com，留意邮箱回信，让我们一起把Wall变的更好。

## 技术讨论

Wall 技术问题交流群：

| <img src="https://store.ityao.cn/api/image/friend/qrcode.png" alt="二维码加载失败，请手动添加微信号入群。"  style="zoom:100%;" /> | <span style="font-weight:200px">如二维码不展示，请手动添加微信号：zhangtygz（备注：wall交流群，否则不会通过）</span> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |


## GitHub

[https://github.com/zhang-tong-yao/wall](https://github.com/zhang-tong-yao/wall)
