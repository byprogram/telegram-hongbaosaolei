# 电报红包扫雷机器人
[![](https://img.shields.io/badge/Author-byprogram-orange.svg)](https://github.com/byprogram)
[![](https://img.shields.io/badge/version-1.0-brightgreen.svg)]([https://github.com/byprogram/telegram-kuaisan-bot])<br>
<br>
![video_2023-01-23_01-21-41](https://user-images.githubusercontent.com/121013897/213930238-c64e31dd-0138-40f7-aa34-5648d21288ca.gif)

## 付费版本，可直接运营（仅售200USDT）
- 支持后台管理系统，可以查看各类数据<br>
- 支持人工充值提现
- 支持尾号扫雷玩法，也可以对接其他玩法
- 赠送免费搭建、更新和维护服务
- Demo预览
    - [后台管理系统演示](http://ksadmin.byprogram.xyz/) `账号:admin 密码:admin`<br>
    - [红包扫雷tg群演示](https://t.me/+nXgsczko7F03NzBl)
## 使用方法
1.[申请](https://t.me/BotFather)一个telegram机器人,获取token<br>
2.新建telegram群组，邀请机器人进群，给予管理员权限<br>
3.安装[Node.js](https://nodejs.org/en/)和[MySQL](https://www.mysql.com/)<br>
4.新建MySQL数据库，导入telegram.sql文件<br>
5.修改index.js文件中配置，在根目录终端输入 `node index` 启动程序<br>
``` javascript
/*配置区开始*/
var pool = mysql.createPool({
    port:3306, //mysql端口
    user     : 'telegram', //mysql用户名
    password : 'telegram', //mysql密码
    database : 'telegram', //mysql数据库
});
var token = '你的token'; //机器人的token
var chatid = 123456; //发送群或用户的id
var periodTime = 10; //每一期开奖的间隔，默认10秒
var inline_keyboard = [ //内联键盘
    [{ text: '点数统计', callback_data: '1' },{ text: '长龙统计', callback_data: '2' }], 
    [{ text: '项目介绍', callback_data: '3' ,url:"https://github.com/byprogram/telegram-kuaisan-bot-v1.0"}],
    [{ text: '联系作者', callback_data: '4' ,url:"https://t.me/byprogram"}]
]
/*配置区结束*/
```
## 技术疑问交流
Telegram：[@byprogram](https://t.me/byprogram)<br>
个人主页：https://www.byprogram.xyz/
## 声明
本项目仅供技术研究，请勿用于任何商业用途，请勿用于非法用途，如有任何人凭此做非法事情，均于作者无关，特此声明。
