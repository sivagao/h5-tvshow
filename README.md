
control tv show by phone app

tv 访问 地址（BE 生成随机码的二维码照片给它，区别 socket.io 连通）
手机 scan 二维码发送给 BE, BE 查找到目标 device socket.io resure 
- 两者联通

手机开始浏览资源
（豌豆荚 oscar api）
选择电影，获得影片地址，发送给 BE
BE 转发给 tv

tv
h5 播放器

手机手势监听
（播放，暂停，快进，聊天，评论等）

tv
监听手势动作来响应


其他扩展 - 
如何展示手机里的歌曲，照片等？！ 短距离传送（红外，蓝牙？！）
快速连接（建立 socketId 和 deviceId 关系 ）


socket.io 状态机设置

```
sync - 是否断开 心跳保持

connection negotiating
确定转发关系（A-B connnecting）

gateway -》 根据 user-agent 自动跳转

gateway/phone
scanner页面
1 -connect:<deviceIdTV>
 
gateway/tv
二维码页面
2 -connected:<deviceIdPhone>
 

choose film
browser/
phone 浏览页面等
1 -play:<videoUrl>
 
waiting/
tv 等待页面
2 -played:<videoUrl>


看片控制
controller/
phone 控制器页面
- pause
- play
- go-progress -> 拖拽改变进度条
- back
- go-volume
- synced-progress -> 动态改变进度条
- 截图分享（tv 截图通过中转到手机上，发朋友圈~）
 

player/xxx
tv 播放页面 
- goed-volume
- goed-progress -> 改变播放进度
- sync-progress -> 同步播放进度

```

Todo: 

https://github.com/soldair/node-qrcode
https://github.com/videojs/video.js
播放器:
被调起来（传入 url）
play/pause/goTo进度设置查询/volume 设置查询/截图 base64
