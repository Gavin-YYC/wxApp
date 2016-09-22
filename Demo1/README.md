# 一、小程序项目目录结构

该项目的目录结构即为小程序的基本目录结构，一般形式如下：

    ├── app.js    // 小程序逻辑
    ├── app.json  // 小程序公共配置
    ├── app.wxss  // 小程序公共样式表
    ├── pages     // 用于存放页面模块
    │   ├── index
    │   │   ├── index.js
    │   │   ├── index.json
    │   │   ├── index.wxml
    │   │   └── index.wxss
    │   ├── logs
    │   │   ├── logs.js
    │   │   ├── logs.json
    │   │   ├── logs.wxml
    │   │   └── logs.wxss
    │   └── main
    │       ├── main.js
    │       ├── main.wxml
    │       └── main.wxss

其中：`app.js`、`app.json`、`app.wxss`是项目的主体文件，这三个文件必须放到项目的根目录下，微信小程序会读取这些文件，并生成小程序实例。

## 1、主体文件

### app.js

`app.js`是项目的入口文件，在该组件中可以监听小程序的生命周期，声明全局变量、提供公共API，以及就像在例子中看到的同步的存取本地数据等等。

    // app.js
    // 创建小程序
    App({

      // 小程序的生命周期
      onLaunch: function () {
        console.log('App Launch');
      },
      onShow: function () {
        console.log('App Show');
      },
      onHide: function () {
        console.log('App Hide');
      },

      // 提供一些公共方法
      getUserInfo: function () {
        wx.login({
          // ...
        })
      },
      // 获取位置信息
      getLocation: funtion () {
        wx.getLocation({
          // ...
        });
      },

      // 全局变量
      globalData: {
        userInfo: null
      }
    })

### app.json

`app.json`是对小程序的全局配置，主要配置：决定页面文件的路径、窗口表现、设置网络超时时间、设置多tab等。



### app.wxss

## 2、页面
