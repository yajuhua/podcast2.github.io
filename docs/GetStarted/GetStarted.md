# 快速开始
## 使用Docker部署Podcast2

#### 1.安装并启动Docker

````shell
curl -fsSL https://get.docker.com -o get-docker.sh && sh get-docker.sh && systemctl start docker
````

#### 2.创建并启动容器

````shell
docker volume create podcast2
docker run -id --name=podcast2 \
-p 8088:8088 \
--restart=always \
--mount source=podcast2,destination=/data \
yajuhua/podcast2:latest
````

#### 3.防火墙放行8088端口

````shell
#以下是centos7，其他系统自行搜索。
firewall-cmd --add-port=8088/tcp --permanent
firewall-cmd --reload
````

#### 4.进入面板

> 默认访问地址 [http://你的IP地址:8088]()
>
> 默认用户名：admin <br>
> 默认密码：123456

![登录](../images/login.png)

## 安装插件
> 项目默认是没有添加插件的，自行按需添加
#### 支持网站
| 网站 <img width=200/>                          |                                                                                            
|:---------------------------------------------|
| [干净世界](https://ganjing.com/)                 |
| [vimeo](https://vimeo.com.com/)              |
| [ntdm](https://www.ntdm.tv)                  |
| [girigirilove](https://www.girigirilove.com) |
| [youtube](https://www.youtube.com)           |
| [bilibili](https://www.bilibili.com)         |
| [抖音](https://www.douyin.com/)                |

#### 1.安装插件
![安装插件](../images/installPlugin.png)

#### 2.设置插件，如果有的话
![设置插件](../images/setting.png)

## 添加订阅
> 以干净世界为例
#### 1.复制主页链接
![复制主页链接](../images/channelUrl.png)

#### 2.粘贴并点击Add
![添加订阅](../images/add.png)

#### 3.点击二维码
![二维码](../images/QRcode.png)

#### 4.扫描二维码添加到播客APP（如：AntennaPod）

<img src="../images/AntennaPod-1.jpg" alt="链接地址" style="zoom:25%;" /><img src="../images/AntennaPod-2.jpg" alt="AntennaPod-2" style="zoom:25%;" />

## 播客APP

<a href="https://www.apple.com/apple-podcasts/" target="_blank">
              <img src="https://www.apple.com/v/apple-podcasts/c/images/overview/hero_icon__c135x5gz14mu_large.png" width="35" alt="Apple Podcasts">
            </a><a href="https://podcastaddict.com/" target="_blank"><img title="Podcast Addict" alt="Podcast Addict" src="https://pod.link/assets/apps/podcastaddict.svg" width="35"></a>  <a href="https://antennapod.org/" target="_blank">
              <img src="https://antennapod.org/assets/branding/logo-full-horizontal-dynamic.svg" width="230" alt="AntennaPod">          </a>
          

          
## Star History
![Star History](https://api.star-history.com/svg?repos=yajuhua/podcast2)
## 使用到的项目
- [https://github.com/yt-dlp/yt-dlp](https://github.com/yt-dlp/yt-dlp)
- [https://github.com/nilaoda/N_m3u8DL-RE](https://github.com/nilaoda/N_m3u8DL-RE)
- [https://github.com/aria2/aria2](https://github.com/aria2/aria2)
- [https://github.com/SocialSisterYi/bilibili-API-collect](https://github.com/SocialSisterYi/bilibili-API-collect)

## 使用的加速站
- [https://github.moeyy.xyz](https://github.moeyy.xyz)
## 参考
- [https://github.com/mxpv/podsync](https://github.com/mxpv/podsync)

## 免责声明              

**此项目仅供研究、学习和交流，请勿用于商业或非法用途， 开发者与协作者不对使用者负任何法律责任， 使用者自行承担因不当使用所产生的后果与责任。**

