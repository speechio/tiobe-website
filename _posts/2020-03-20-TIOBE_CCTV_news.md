---
layout: article
title: TIOBE 场景测试:新闻联播
permalink: /tiobe/cctv_news/
key: TIOBE_cctv_news
tags: TIOBE-Benchmark
lang: zh
author: SpeechIO
---

# 场景素材来源
YouTube CCTV中央电视台 官方频道

我们爬取了该频道新闻联播2019年全年视频内容。分12个月，每个月抽取2期，共计24期节目，并抽取音频，共计时长约12小时

# 场景特点
* 环境
  * 主体为密闭录音棚，安静，无背景噪声
  * 穿插少量会场、户外采访
* 拾音设备
  * 专业高保真麦克风，等同于近场，声音质量极好
* 说话人
  * 主体为专业播音员，穿插少量领导人讲话，记者及被采访对象
* 说话方式
  * 主体为朗读式，中等语速，几乎无口误、重复、停顿等现象
* 方言
  * 极标准普通话
* 内容领域
  * 国家时政新闻

新闻联播场景的以上特点，接近语音识别的理想场景，基本可以代表现有的中文语音识别系统性能上限，因此我们选择该场景作为 TIOBE Benchmark 的第一个测试领域。

# 测试结果
测试时间：2020.03

|    | 字错误率CER(Charactor Error Rate) %   | 
|:----:|:----:|:----:|:----:|
| 阿里   | 1.41   | 
| 百度   | 2.42   | 
| 谷歌   | 4.68   | 
| 讯飞   | 1.16   | 
| 腾讯   | 2.2   | 
| 创Y   | 1.09   | 

# 简评
* 除 Google 外，上述测试对象的错误率已经达到1%～2%水平，即100个字中只发生1到两个字的错误。举一个不完全准确，但直观例子来说明：语音识别中的核心模块，完成从声音到拼音序列的转化，之后的过程与拼音输入法无异。大家可以回想一下自己在使用拼音输入法过程中的错字率，来更直观的对比这里1%～2%的字错误率。可以说，该场景在现有的语音识别技术水平下，已经是一个已解决的问题。
* Google 的识别率明显低于国内厂商。毋庸置疑，Google 在语音技术上处于全球前列，引领技术进步路线。国内企业**整体更好的原因**，主要应在于中文领域的数据积累和资源打磨，相反，相信若测试切换到英文场景，会有类似反转。这种优势，应该会持续体现在我们下面的各个领域测试中，留待我们后续验证。该例子说明，除算法外，领域数据的积累和打磨，对最终系统的性能表现也至关重要。