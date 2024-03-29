# douyu-hongbao

#### 介绍
斗鱼自动抢礼物红包工具<img src="https://images.gitee.com/uploads/images/2020/1116/165713_916299e5_2268103.png" width = "24" height = "24"/>

#### 下载

1. 蓝奏云地址：[下载](https://yijianguanzhu.lanzout.com/if1gB1hntvgd)

#### 2.0.1更新信息
1. 修复近期斗鱼服务器TLS疑因版本回溯导致无法使用问题

#### 2.0更新信息
1. 版本换新，初步提供可视化操作界面。
	- 2.0使用示例
		- 启动程序
		![启动程序](https://foruda.gitee.com/images/1699716441608073124/728da954_7859954.png "启动程序")
		- 扫描二维码
		![扫描二维码](https://foruda.gitee.com/images/1699716522310976289/41c8cdae_7859954.png "扫描二维码")
		- 成功登录账号
		![登录成功](https://foruda.gitee.com/images/1699718611373545829/f3e7fbe7_7859954.png "登录成功")
		- 查看站内信
		![查看站内信](https://foruda.gitee.com/images/1699716978516316976/f2ccb61c_7859954.png "查看站内信")
		- 账号设置
		![账号设置](https://foruda.gitee.com/images/1699717320759365979/4742fdde_7859954.png "账号设置")
		- 关于
		![关于](https://foruda.gitee.com/images/1699717390539039232/fc0d8924_7859954.png "关于")	
		- 选择账号
		![选择账号](https://foruda.gitee.com/images/1699718069843642937/4ad9a9c2_7859954.png "选择账号")
		![选择账号](https://foruda.gitee.com/images/1699718226175882203/f4210f05_7859954.png "选择账号")				
	- 新功能
		- 账号设置增加了【指定抽奖直播间】属性，设置后，如果抽奖直播间符合设置的房号，将直接参与抽奖，不受其他抽奖属性限制。（注：同其他属性一样，多个房号用英文半角","分隔）
		- 新增每日任务自动领取功能，只领取奖励，不自动做任务。

---
#### 下载

1. 蓝奏云地址：[下载](https://yijianguanzhu.lanzout.com/isqOH1hnuqwf)	

#### 1.5.1更新信息
1. 修复近期斗鱼服务器TLS疑因版本回溯导致无法使用问题

#### 1.5更新信息
1. 常规更新
2. 修复删除粉丝牌异常问题

#### v1.4更新信息
1. 增加挂机直播间功能（可做斗鱼看直播的活动），详见[自定义配置](#custom)
2. 增加斗鱼弹幕抽奖功能，详见[自定义配置](#custom)
	- 弹幕抽奖配置示例，描述：只参与鱼翅,Q币,QB,Qb,qb的奖品且金额在20（包含）以上的弹幕抽奖
			
			  # 是否开启弹幕抽奖（默认：true）
	          lottery=true
	          # 只参与想要的弹幕抽奖奖品，多个使用英文半角","分隔，如鱼翅,Q币,QB,Qb,qb（无默认值）
	          lottery_want=鱼翅,Q币,q币,QB,Qb,qb
	          # 只参与大于等于该值的弹幕抽奖金额，结合lottery_want属性使用，如=6时，只有鱼翅价值在6以上才参与（无默认值）
	          lottery_profit=20
	- 警示：建议设置自己喜欢的奖品，否则参与的抽奖过多，弹幕发言功能会遭到禁封。
	- 通常弹幕发言被禁封，过个几天也会恢复正常。
3. 现在 `config.ini` 配置文件支持动态读取内容改变，以后修改配置文件属性，再也不需要重启程序了。

#### v1.3更新信息
1. 增加自动删除粉丝牌功能，详见[自定义配置](#custom)
    - 程序启动会先保存已有的粉丝牌，以免误删。
    - 新得到的粉丝牌，删除策略根据账号7天内是否赠送过价值礼物和其他免费礼物结算，如7天内没有赠出过其他道具，粉丝牌将会删除，如7天内赠出过其他道具，粉丝牌将会保留。
    - 其他道具包含价值礼物和其他免费礼物，不包含礼物红包的礼物。
2. 增加每日自动领取荧光棒、周日自动赠送荧光棒功能，详见[自定义配置](#custom)
	- 荧光棒为均衡赠送策略，假设本周共400个荧光棒，如设置了三个直播间，第一个直播间赠出134个，第二个直播间赠出133个，第三个直播间赠出133个；如设置了两个直播间，第一个直播间赠出200个，第二个直播间赠出200个；如设置了一个直播间，就将荧光棒全部赠送给这个直播间。
	- 房间号为实际房间号，不可设置靓号/vip房间号，否则荧光棒可能无法领取或赠出。

#### v1.2更新信息
1. 修复BUG。
2. 修复礼物码错误导致无法自动赠送火箭问题。
3. 优化关注取关机制，保证同一个房间在可见的红包雨情况下，不再重复关注取关。

	- 此次改善能够降低斗鱼风险用户侦测系统对账号的风险评估

#### v1.1.2更新信息
1. 新增拾起红包功能。

	- 当满足粉丝团参与条件时，会重新拾起被丢弃的红包，仅限于非立即开启的红包。 
2. 修复抢红包时，用户登录信息过期导致的循环BUG。

#### v1.1更新信息
1. 优化同一个房间短时间（20秒）内有多个红包的情况下，执行多次关注取关操作问题。

	- v1.0版本中，如果每20秒（内）左右有一个红包（同一房间），假设一分钟内有5个红包，那么最终导致可抢红包可能只有两个。 这是由于延迟取关机制引发的问题。该问题导致抢最后三个红包（假设）时，关注主播的条件已经被前两个红包线程取关了，而后三个红包线程无法感知，导致无法正确抢到红包。

2. 当获得到办卡（开启小礼物自动赠送），飞机（开启大礼物自动赠送）时，且粉丝牌没有满，则直接加入到粉丝团列表中。
	
	- 有些房间会在发出【关注主播】的红包后，继而发出【关注+粉丝团】的红包，这次更新让在第一个红包中抢到办卡及以上的同学，能够在第一时间内快速获得满足下一个红包的参与条件。【v1.0版本中，需要等五分钟更新一次粉丝徽章，有时会错过红包】

#### v1.0初版
1. 支持斗鱼app扫码登录，登录认证信息过期自动续期。
2. 自动监控红包，默认十秒监测一次。
3. 自动关注，自动取关，自动抢红包，自动赠送礼物。
4. 支持自定义参数配置，详见[自定义配置](#custom)
5. 新号或等级太低的小号容易抢不到红包，充值就可解决或将账号升级到15级以后再使用。

#### 安装方式

1. 与正常程序安装方法一致，根据提示操作即可

#### 使用说明
    本程序属于绿色软件，不包含任何破坏计算机系统程序。

1. 注意事项：<font color=red>安装路径不能包含中文名，否则无法启动</font>
2. 使用步骤：启动程序 -> 扫描二维码

![启动程序](https://images.gitee.com/uploads/images/2020/1117/133300_4cdb1d85_7859954.png "启动程序")
![扫描二维码](https://images.gitee.com/uploads/images/2020/1117/133423_493a7593_7859954.png "扫描二维码")
3. core目录核心配置文件，logs目录下存放每日运行日志文件，barrage.log文件记录荧光棒领取信息，clear_fans_card.log文件记录删除粉丝牌信息，cookie.txt账号信息，hongbao.log文件只单独记录礼物赠送信息

![新生成配置](https://images.gitee.com/uploads/images/2021/0925/131613_e5769a03_7859954.png "新生成文件")
4. 运行日志展示：强悍的抢红包速度，速度快的30~40ms一次请求（1H2G的服务器），cookie过期自动续期。

![运行日志](https://images.gitee.com/uploads/images/2020/1117/135626_f2375e9b_7859954.png "运行日志")
5. 礼物赠送日志展示

![赠送日志](https://images.gitee.com/uploads/images/2020/1117/140106_344dfbce_7859954.png "赠送日志")
6. 删除粉丝牌日志展示

![删除粉丝牌日志](https://images.gitee.com/uploads/images/2021/0925/132207_e4a7ff34_7859954.png "删除粉丝牌日志")
7. 领取荧光棒日志展示 

![领取荧光棒日志](https://images.gitee.com/uploads/images/2021/0925/132325_c95106d3_7859954.png "领取荧光棒日志")
#### 自定义配置 <a name="custom"></a>
    在/core/config.ini文件中，可自定义特定参数（首次运行会自动生成）:
        [monitor-thread]
          # 每隔多少秒检测一次红包（默认：10秒）
          period=10
          # 想挂机的直播间，多个使用英文半角","分隔，如1111,2222（无默认值）
          hang=
          # 是否开启弹幕抽奖（默认：true）
          lottery=true
          # 只参与想要的弹幕抽奖奖品，多个使用英文半角","分隔，如鱼翅,Q币,QB,Qb,qb（无默认值）
          lottery_want=
          # 只参与大于等于该值的弹幕抽奖金额，结合lottery_want属性使用，如=6时，只有鱼翅价值在6以上才参与（无默认值）
          lottery_profit=
        [handler-thread]
          # 抢红包线程启动偏移量，取值范围：[-2.00,2.00]（单位秒）（保留两位小数）（默认：0）
          leftshift=0
        [broker-thread]
          # 小礼物是否自动赠送（大气、666和办卡）（默认：true）
          small=true
          # 大礼物是否自动赠送（飞机、火箭）（默认：false）
          precious=false
        [fans-card-thread]
          # 是否开启删除粉丝牌功能（默认：true）
          clear=true
        [barrage-thread]
          # 每周日自动赠送荧光棒的直播间，多个使用英文半角","分隔，如1111,2222 （无默认值）
          roomId=
#### 交流

1. QQ群 250097154