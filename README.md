# douyu-hongbao

#### 介绍
斗鱼自动抢礼物红包工具<img src="https://images.gitee.com/uploads/images/2020/1116/165713_916299e5_2268103.png" width = "24" height = "24"/>

#### ![更新v1.1](https://www.easyicon.net/api/resizeApi.php?id=1143807&size=24) v1.1更新信息
1. 优化同一个房间短时间（20秒）内有多个红包的情况下，执行多次关注取关操作问题。

	- v1.0版本中，如果每20秒（内）左右有一个红包（同一房间），假设一分钟内有5个红包，那么最终导致可抢红包可能只有两个。 这是由于延迟取关机制引发的问题。该问题导致抢最后三个红包（假设）时，关注主播的条件已经被前两个红包线程取关了，而后三个红包线程无法感知，导致无法正确抢到红包。

2. 当获得到办卡（开启小礼物自动赠送），飞机（开启大礼物自动赠送）时，且粉丝牌没有满，则直接加入到粉丝团列表中。
	
	- 有些房间会在发出【关注主播】的红包后，继而发出【关注+粉丝团】的红包，这次更新让在第一个红包中抢到办卡及以上的同学，能够在第一时间内快速获得满足下一个红包的参与条件。【v1.0版本中，需要等五分钟更新一次粉丝徽章，有时会错过红包】

#### ![下载](https://www.easyicon.net/api/resizeApi.php?id=1225445&size=24) 下载

1. 蓝奏云地址：[下载](https://yijianguanzhu.lanzous.com/isYQrim0zuf)
2. 百度网盘：[下载](https://pan.baidu.com/s/1gi_auk-mGf8Ep5qw2N1qWQ "提取码: f2mg")

#### ![安装教程](https://www.easyicon.net/api/resizeApi.php?id=1211336&size=24) 安装方式

1. 与正常程序安装方法一致，根据提示操作即可

#### ![说明](https://www.easyicon.net/api/resizeApi.php?id=1215091&size=24) 使用说明
    本程序属于绿色软件，不包含任何破坏计算机系统程序。

1. 注意事项：<font color=red>安装路径不能包含中文名，否则无法启动</font>
2. 使用步骤：启动程序 -> 扫描二维码

![启动程序](https://images.gitee.com/uploads/images/2020/1117/133300_4cdb1d85_7859954.png "启动程序")
![扫描二维码](https://images.gitee.com/uploads/images/2020/1117/133423_493a7593_7859954.png "扫描二维码")
3. core目录核心配置文件，logs目录下存放每日运行日志文件，cookie.txt账号信息，hongbao.log文件只单独记录礼物赠送信息

![新生成配置](https://images.gitee.com/uploads/images/2020/1117/135119_c9f3acca_7859954.png "新生成文件")
4. 运行日志展示：强悍的抢红包速度，速度快的30~40ms一次请求（1H2G的服务器），cookie过期自动续期。

![运行日志](https://images.gitee.com/uploads/images/2020/1117/135626_f2375e9b_7859954.png "运行日志")
5. 礼物赠送日志展示

![赠送日志](https://images.gitee.com/uploads/images/2020/1117/140106_344dfbce_7859954.png "赠送日志")

#### ![配置](https://www.easyicon.net/api/resizeApi.php?id=1183257&size=24) 自定义配置
    在/core/config.ini文件中，可自定义特定参数（首次运行会自动生成）:
        [monitor-thread]
          # 每隔多少秒检测一次红包（默认：10秒）
		  period=10
		[handler-thread]
		  # 抢红包线程启动偏移量，取值范围：[-2.00,2.00]（单位秒）（保留两位小数）（默认：0）
		  leftshift=0
		[broker-thread]
		  # 小礼物是否自动赠送（大气、666和办卡）（默认：true）
		  small=true
          # 大礼物是否自动赠送（飞机、火箭）（默认：false）
		  precious=false

#### ![交流](https://www.easyicon.net/api/resizeApi.php?id=550214&size=24) 交流

1. QQ群 250097154