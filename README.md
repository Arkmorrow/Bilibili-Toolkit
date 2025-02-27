<p align="center">
<img src="https://cdn.kagamiz.com/Bilibili-Toolkit/bilibili.png" width="300">
</p>

<h1 align="center">- Bilibili Toolkit -</h1>

<p align="center">
<img src="https://img.shields.io/badge/version-2020.7.20-green.svg?longCache=true&style=for-the-badge">
<img src="https://img.shields.io/badge/license-SATA-blue.svg?longCache=true&style=for-the-badge">
<img src="https://img.shields.io/travis/com/Hsury/Bilibili-Toolkit?style=for-the-badge">
</p>

<h4 align="center">🛠️ 哔哩哔哩（B站）辅助工具箱，支持Cookie/Token/Password融合持久化登录与多用户操作</h4>

<p align="center">
<img src="https://cdn.kagamiz.com/Bilibili-Toolkit/demo.png" width="750">
</p>

## 功能

|组件                |版本           |描述                          |
|--------------------|---------------|------------------------------|
|login               |2020/7/4       |登录                          |
|get_user_info       |2019/9/15      |获取用户信息                  |
|set_privacy         |2018/7/24      |修改隐私设置                  |
|silver_to_coin      |2018/8/8       |银瓜子兑换硬币                |
|watch               |2020/7/20      |观看                          |
|like                |2020/7/20      |点赞                          |
|reward              |2020/7/20      |投币                          |
|favour              |2020/7/20      |收藏                          |
|combo               |2020/7/20      |三连推荐                      |
|share               |2020/7/20      |分享                          |
|follow              |2018/7/8       |关注                          |
|follow_batch        |2020/7/2       |批量关注                      |
|ban                 |2021/2/19      |拉黑                          |
|ban_batch           |2021/2/19      |批量拉黑                      |
|danmaku_post        |2020/7/20      |弹幕发送                      |
|comment_like        |2018/6/27      |评论点赞                      |
|comment_post        |2019/8/3       |评论发表                      |
|dynamic_like        |2018/6/29      |动态点赞                      |
|dynamic_repost      |2019/3/11      |动态转发                      |
|dynamic_purge       |2019/3/11      |动态清理                      |
|system_notice       |2019/8/3       |系统通知查询                  |
|mall_rush           |2019/9/15      |会员购抢购                    |
|mall_coupon         |2019/3/3       |会员购优惠卷领取              |
|mall_order_list     |2019/9/15      |会员购订单列表查询            |
|mall_coupon_list    |2019/8/4       |会员购优惠卷列表查询          |
|mall_prize_list     |2019/8/3       |会员购奖品列表查询            |
|live_prize_list     |2019/8/3       |直播奖品列表查询              |

## 使用指南

### 二进制版本

从[Release页面](https://github.com/Hsury/Bilibili-Toolkit/releases)下载并解压与您的平台适配的压缩包，修改默认配置文件config.toml后运行可执行文件bilibili即可

*若要加载非默认配置文件，将其路径作为命令行参数传入即可*

### 源代码版本

1. 克隆或[下载](https://github.com/Hsury/Bilibili-Toolkit/archive/master.zip)本代码仓库，并修改默认配置文件config.toml

```
git clone https://github.com/Hsury/Bilibili-Toolkit.git
cd Bilibili-Toolkit
nano config.toml
```

2. 安装Python 3.6或更高版本，并使用pip安装依赖

```
pip install -r requirements.txt -U -i https://pypi.tuna.tsinghua.edu.cn/simple
```

3. 启动脚本

```
python bilibili.py
```

### Docker版本

1. 安装Docker

2. [下载](https://raw.githubusercontent.com/Hsury/Bilibili-Toolkit/master/config.toml)默认配置文件config.toml并根据需求修改

3. 启动容器，并挂载配置文件

```
docker run --rm -it -v [YOUR PATH TO CONFIG.TOML]:/app/config.toml zsnmwy/bilibili-toolkit
```

*若要加载代理池，补充参数`-v [YOUR PATH TO PROXY.TXT]:/app/proxy.txt`以挂载代理列表文件*

## 图形验证码识别API

使用CNN卷积神经网络构建，已实现对**登录、评论**验证码的自适应识别

```
requests.post("https://bili.dev:2233/captcha", json={'image': base64.b64encode(image).decode("utf-8")})
```

## 鸣谢

本项目的灵感与使用到的部分API来自以下项目：

> [czp3009/bilibili-api](https://github.com/czp3009/bilibili-api)

## 许可证

Bilibili Toolkit is under The Star And Thank Author License (SATA)

本项目基于MIT协议发布，并增加了SATA协议

您有义务为此开源项目点赞，并考虑额外给予作者适当的奖励 ∠( ᐛ 」∠)＿
