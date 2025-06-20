**从任何平台过来的朋友们请先阅读此说明（除了下方的英文）！**

**This is a project for someone who wants to send morning greeting to his/her girlfriend/boyfriend but without programming experience. It's just a simple python script taking advantage of Wechat Official Test Platform. It may be useless for people outside China. Please ignore this project if you are not using Wechat or you are a programmer.**

# 每日早安推送给别人家的女朋友

这里有[更新说明](./UPGRADE.md)


## 使用说明

不想看文字的可以看下面的视频教程：

https://www.bilibili.com/video/BV1ke4y1o7Wd/

在我刚想构思这个教程怎么让不懂编程的朋友很快入门的时候，我考虑到：避免服务器搭建，避免定时任务，避免接触代码。在经历过各种思考后，觉得可以用 Github Actions 来白嫖。。

效果如图。当然，文字是可以修改的。
<img src="https://user-images.githubusercontent.com/9566402/183242263-c93517a2-5377-435d-8386-8d47252c9e07.jpg" width="300px" />

首先，按图搜索，测试号，进来之后微信扫码登录！
![cf7dbd4502df44765ed3506f55caea5](https://user-images.githubusercontent.com/9566402/183242272-134e37e7-718d-42dd-9ed7-fca2810e94e6.png)

按图点击 Fork，创建到自己的仓库下！
<img width="1471" alt="image" src="https://user-images.githubusercontent.com/9566402/186087195-d1f2c124-1b59-4ea8-93dc-0b1e31a2e754.png">

按下图，创建模板，设置变量，把微信公众平台上的各种字符串按说明创建到 GitHub -> Settings -> Secrets -> Actions 中。
![71bf9d11a876d23ef0f0728645a8ba0](https://user-images.githubusercontent.com/9566402/183242301-fd6ab30e-bfe5-4245-b2a9-f690184db307.png)
![381e8ee4a7c5ec6b8c09719f2c7e486](https://user-images.githubusercontent.com/9566402/183242295-4dcf06bb-2083-4883-8745-0af753ca805c.png)
![48c60750cec7adc546e0ad99e3082b3](https://user-images.githubusercontent.com/9566402/183242320-18500adc-14e5-4522-a3ad-ae19cc4479bf.png)

启用自己项目下的 Action！
![30a5b1b2b06ba4a40a3d8ef01652409](https://user-images.githubusercontent.com/9566402/183242334-9943c538-ba3d-4d01-8377-d040143b7560.png)

如果运行出现错误，按以下方法可以看到错误，在这里 issue 提问也可以，在小红书群里问也可以
![6b0da6f44e18c2bfd94910c377d13e6](https://user-images.githubusercontent.com/9566402/183242349-1aa5ada6-2ee7-4cf9-a542-4b2dad88b8fe.png)

启用后可以直接运行，看看女朋友的手机有没有收到推送吧！
这个定时任务是每天早晨8点推送，如果会编程的同学可以自己自定义一些东西～

图中的操作，除了各种英文字符串不一样，模板消息中的中文不一样，其他的应该都是一样的，不然程序跑不通的～

Github 的右上角可以点击 star 给我点鼓励吧亲

小红书/抖音上点点关注，点点赞，有什么好玩的东西可以at我，我来教你们做

ps. 有一些注意事项在此补充

1. 第一次登录微信公众平台测试号给的 app secret 是错误的，刷新一下页面即可
2. 生日的日期格式是：`05-20`，纪念日的格式是 `2022-08-09`，请注意区分。城市请写到地级市，比如：`北京`，`广州`，`承德`
3. 变量中粘贴的各种英文字符串不要有空格，不要有换行，除了模板之外都没有换行
4. Github Actions 的定时任务，在 workflow 的定义是 `0 0 * * *`，是 UTC 时间的零点，北京时间的八点。但是由于 Github 同一时间任务太多，因此会有延迟
5. 我会偶尔优化一下代码，emm 但现在我自己在做一个完整的平台项目，想让大家更加便捷地上手

## 版权相关

更新：2022.08.22

再更新一下，之前说的最火的那个视频的作者联系我了，我加以下这些限制协议不是因为这位作者，因为她确实有标明出处。只不过当时我的抖音号不叫这个名字，所以找不到罢了。。

(啊其实是因为有很多人在抖音上发我这个教程，但完全没有标出处，都说是自己男朋友给做的，我什么时候有那么多女朋友了请联系我让我认识一下)

当初做这个项目的时候，其实没有想到会被这么多人喜欢，因此没有加任何的开源协议、版权声明、代码加密等措施。说实在的，这个功能很简单，但是有朋友告诉我很多人都在用我的代码和教程去自己发抖音集赞，甚至还有人进行盈利骗钱的操作。让我比较心烦的是，大家给别人的视频点赞，然后跑过来问我怎么用，我？？？

因此，这个项目我会继续更新（本来都不打算更新了），首先更新协议如下：

1. 根据 Github [默认版权协议](https://docs.github.com/cn/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository#choosing-the-right-license)，在未发布开源许可协议时，遵循默认版权法，即任何人无法修改、复制本项目。但由于本项目使用说明解读，因此在 2022年8月22日23:00 之前对本项目的复制、修改不做严格限制。（收费除外）
2. **增加 [GPLv3](https://www.gnu.org/licenses/gpl-3.0.txt) 协议：凡使用本项目，其代码必须公开；如由此项目衍生的收费服务，必须提前告知终端用户此项目是可以免费获得及收费的理由；在本项目基础上 Fork、修改后的代码，必须采用 GPLv3 协议。此协议受全世界版权法律保护，本人保留对一切违反本协议行为诉诸法律的权力。**
3. **版权声明：凡是在世界范围内各平台（包括但不限于抖音、微博、小红书、Github、Gitee、微信公众平台、微信小程序、Youtube、Instagram、Twitter 等）使用本项目（包括但不限于展示、发布使用说明等）时，必须在明显的位置（内容、评论区等）表明出处（在已知账号的情况下，提及原作者；未知账号的情况下，展示本项目的地址）。**
4. 文件保护声明：如果复制、修改本项目，衍生后的项目可以添加本文件的内容，但禁止删除本文件中的任何内容。

其次，我会偶尔增加新功能。

## 自我介绍

首发在小红书，但是有大家说字看不清，因此在这里搞一篇使用说明。

> 我一脸懵逼地在小红书新建的群里听说有网友在抖音帮推我这个项目..
>
> 在此表示十分感谢，因为我懒得做视频。。当时也是一时兴起，所以就只发了小红书。。
>
> 大家喜欢我的项目我真的十分感谢，不过有朋友说找不到我本人。对于涨粉丝这件事情我还是很感兴趣的。。


## 自我推广

本人在维护一套全新的闭源平台，不过要收费。

可以让大家完善地自定义各种字段，模板内容。如果大家愿意，可以通过查但请注意，此群只解答新版推送平台相关的内容，与本项目相关的内容请勿进群。

下方是开源版的QQ群，有需要可以添加。

我才知道微信群上限是200人，过了还要邀请。
<img src="https://github.com/user-attachments/assets/d639d7b2-bbd8-4213-aaff-158dd34fce63" width="300px" />
<img src="https://github.com/user-attachments/assets/a8c86692-5679-4a34-bee9-f7467b132cd7" width="300px" />
<img src="https://github.com/user-attachments/assets/e2cde89f-944e-4ed2-a9a7-419a683c995d" width="300px" />

如果觉得这个项目对你有用，欢迎给我买杯咖啡

