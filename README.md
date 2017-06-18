# 游戏策划
> 2014145139 袁臻

## 1 概述
### 1.1 名称
涂鸦跳跃网络版(Doodle Jump Online)

### 1.2 定位
一款网络休闲类游戏；较原版新增在线系统，玩家可以团队合作。

## 2 设计理念
### 2.1 玩法阐述
角色是一个在危险的地面上跳跃的绿色的小外星人Doodle，你的任务是要避免它坠落，并尽可能跳得越高。火箭筒能使Doodle飞得更快，但危险的是，它的时间有限，并且会消失在背上，必须小心；此外还有移动的地面，蓝色的，你需要选定合适的时机通过它们，而不是踩空导致游戏结束；还有棕色地面只能通过一次。
在这过程中，有奖励积分可以收集。相比较原版的单机模式，我们新开发了网络功能，这样你可以和朋友一起来探索天空之旅。

### 2.2 主要特色
* 玩家只有一种游戏方式：“联网”，首次登录需要注册账户；
* 登录后进入队伍进行游戏
* 以队伍为单位进行游戏
* 游戏中队员之间交流
* 使用游戏中获得的分数兑换金币
* 使用金币为队友建立绿色地面
* 使用金币使队友原地复活
* 使用金币使蓝色地面移动变慢
* 与队友交换道具

### 2.3 游戏系统简述
分为客户端和服务端两个部分：
#### 2.3.1 客户端
与玩家交互、执行游戏逻辑：
* 注册登录
* 查看当前所有队伍/创建队伍
* 开始游戏
* 团队交流

#### 2.3.2 服务端
* 账户：注册登录；
* 生成地图；
* 统计：最高分、排名处理；
* 队伍：创建、加入、删除队伍：
* 即时通信：聊天；

### 2.4 技术要点
主要技术要点有：
* 队伍算法设计实现
* 数据库设计实现
* 即时通信实现

### 2.5 设备需求
* 客户端：画面素材较简单，对设备要求较低，具有Java运行环境；
* 服务端：较高数据库性能、CPU性能，内存初步为2GB，具有Java运行环境；
* 网络：客户端、服务端具备良好互联网访问能力；

## 3 世界构架
### 3.1 故事主线
旅行者Doodle来到X星球，这里没有陆地，只有漂浮的地面，Doodle开始了他的旅途。

### 3.2 地理架构
* 二维地理环境，地理环境纵向延伸；
* 有固定或者运动的地面；
* 绿色地面固定，多次经过；
* 蓝色地面横向运动，多次经过；
* 棕色地面固定，只能经过一次；

### 3.3 NPC
主要由怪物组成：
* 怪物：玩家撞到它后结束生命（范围较小）；
* 飞碟：玩家进入其吸引范围后结束生命（范围大小居中）；
* 黑洞：玩家进入其吸引范围后结束生命（范围较大）；

### 3.4 任务系统
## 4 游戏系统
### 4.1 角色系统
只有一种角色，玩家控制旅行者；

### 4.2 技能系统
技能不累计，玩家每次开始都是零技能，通过游戏高度获得技能；

### 4.3 道具装备
游戏场景中按照预先设计的概率出现道具，玩家可获取它：
* 金币：可购买地面、生命；
* 弹簧：垂直上升一小段距离；
* 火箭筒：垂直上升一大段距离；
* 蘑菇：反转控制方向；
* 爱心：生命

### 4.5 成就系统
根据玩家的最高成绩，给予玩家不同等级的头衔，保存在玩家的信息里。

## 5 界面与操作
### 5.1 操作模式
* 键盘方向键（左、右）控制Doodle左右方向运动；
* Doodle上下跳动由程序控制（向上跳动）；

### 5.2 界面设计
* 二维界面，漫画的风格；
* 使用图片资源绘制画面；

### 5.3 界面引导流程
以动画的方式演示游戏如何入门：
* 开始；
* 注册账户并且登录；
* 开始游戏；
* 控制Doodle左右移动；
* 控制Doodle获得道具；
* 结束；

### 5.4 帮助
提供游戏图文说明；

## 6 人际互动
### 6.1 排行榜
服务端对所有用户的游戏记录：
* 总共高度
* 最高高度
进行存储和排名，用户可查看：
* 本玩家的队伍内、世界排名；
* 所在队伍的世界排名；

### 6.2 互动方式
* 每个客户端访问互联网，与服务端联机；
* 玩家可通过内置的即时消息系统在队伍、世界的范围内发言；

### 6.3 组队系统
* 加入已经存在的队伍
* 创建队伍，邀请玩家加入

<<<<<<< HEAD
## 7 关卡与数值
### 7.1 战斗数值
* 得分由当前玩家高度决定；
* 用户每次游戏的分数都会保存在服务端；

### 7.2 关卡设计
游戏只有单一的关卡，此关卡高度没有限制；
按照高度高低分为不同等级，如下：
* 0 - 19999
* 20000 - 39999
* 40000 - 59999
* 60000 - 79999
* 80000 - 89999
根据等级变换场景风格；

=======
>>>>>>> 完成左右超出位移
## 8 其他
### 8.1 音效
音效采用原版游戏的音效。