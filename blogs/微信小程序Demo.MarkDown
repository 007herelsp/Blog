## 建立微信小程序工程

打开微信开发者工具，可以直接去官网下载。

> ![img](/img/wxDemo/img1.png)

新建一个工程。

这里没有内侧或者公测资格（只有企业公众号才有）可以选择无AppID模式，此模式下部分功能受限，但是不影响我们“尝鲜”微信小程序。

![img](/img/wxDemo/img2.png)

![img](/img/wxDemo/img3.png)

<br />

<br />

## 目录结构及文件

新建好的工程代码目录如下。

app.js为整个微信小程序的入口文件，里面提供了一些全局方法以及全局变量。

app.json是整个项目的配置，里面以json格式提供配置（注：不能写注释）。

wxss为样式文件，类似css的作用。

pages是一个文件夹，里面包含了每个单页面，单页面也是一个单独的文件夹存放在pages下面，里面可以包含wxml、wxss、js以及json四个格式的文件，每个文件的命名规范都跟文件夹名字一致。

![img](/img/wxDemo/img4.png)

<br />

<br />

## 添加一个页面

首先要在pages文件夹下面新建一个文件夹，如新加一个名为map的页面。

新建map文件夹，在下面加入map.js、map.wxss、map.wxml、map.json（可选）。

然后在app.json配置文件中pages数组中加入相应数据。

wxss相当于css，wxml相当于html，json是一些配置，前端er很容易上手。

<br />

<br />

## 开发页面

微信小程序开发文档

[https://mp.weixin.qq.com/wiki?t=resource/res_main&id=mp1474632113_xQVCl&token=&lang=zh_CN/](https://mp.weixin.qq.com/wiki?t=resource/res_main&id=mp1474632113_xQVCl&token=&lang=zh_CN/)

wxss相当于css，wxml相当于html，json是一些配置。

有了前端基础开发微信小程序上手非常快，就是wxml中组建需要用官方提供的，比如a标签没有了，没法直接访问外部链接了（个人认为这是接入商家会觉得比较蛋疼的一个地方）。

还有一些基础API，简单易用，快速上手。

<br />

关于tabBar。

![img](/img/wxDemo/img5.png)

我做了一个跟微信比较类似的效果。

只需在app.json配置文件中加入相应的代码即可。

pagePath对应相应页面，iconPath与selectedIconPath代表选中与不选中的时候的图片。

```json
"tabBar": {
"color": "#dddddd",
"selectedColor": "#21BB32",
"borderStyle": "white",
"navigationBarTitleText": "",
"backgroundColor": "white",
"list": [
  {
    "pagePath": "pages/index/index",
    "text": "Home",
    "iconPath": "images/home1.png",
    "selectedIconPath": "images/home2.png"
  },
  {
    "pagePath": "pages/map/map",
    "text": "Map",
    "iconPath": "images/map1.png",
    "selectedIconPath": "images/map2.png"
  },
  {
    "pagePath": "pages/game/game",
    "text": "Game",
    "iconPath": "images/player1.png",
    "selectedIconPath": "images/player2.png"
  }
]
```
  }

<br />

<br />

## Demo

最后附上我的Demo。

[https://github.com/answershuto/wxDemo](https://github.com/answershuto/wxDemo)

