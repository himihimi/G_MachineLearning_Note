问题构建 Framing
---
https://developers.google.com/machine-learning/crash-course/framing/video-lecture
// 20180307


- 什么是 监督式机器学习？ Supervised Machine Learning
    * 机器学习系统
    * 通过学习如何组合 输入信息 
    * 来对 从未见过的数据 做出有用的预测
```
机器学习系统通过学习如何组合输入信息来对从未见过的数据做出有用的预测。
ML systems learn how to combine input to produce useful predictions on never-before-seen data.
```


术语 fundamental machine learning terminology
---

## - 标签 Labels = 输出 (仿佛是)

- 标签是指我们要预测的真实事物 !要预测的目标!!!：y
- 基本线性回归中的 y 变量

```
在简单线性回归中，标签是我们要预测的事物，即 y 变量。标签可以是小麦未来的价格、图片中显示的动物品种、音频剪辑的含义或任何事物。
A label is the thing we're predicting—the y variable in - simple linear regression.-
```


## - 特征 Features = 输入 (仿佛是返回值)

- 指用于描述数据的 输入变量 ：xi
- 基本线性回归中的 {x1, x2, ... xn} 变量
> 各种能拿来提供给机器学习的信息都算, 就有点像多元分析的中的因素, 可以拿来分析的都可以

```
- 在简单线性回归中，特征是输入变量，即 x 变量。简单的机器学习项目可能会使用单个特征，而比较复杂的机器学习项目可能会使用数百万个特征，按如下方式指定：
A feature is an input variable—the x variable in simple linear regression.

        在垃圾邮件检测器示例中，特征可能包括：
        电子邮件文本中的字词
        发件人的地址
        发送电子邮件的时段
        电子邮件中包含“一种奇怪的把戏”这样的短语。
```

＞特征不能光看脸
![](/img_for_md/QQ20180307-231035@2x.png)


## - 样本 Examples = 一份数据,包含输入输出 (仿佛是一次运行in和out)
- 样本是指数据的特定实例：x
- 有标签样本具有 {特征, 标签}：(x, y)
    - 用于训练模型
> 有输入有输入的

- 无标签样本具有 {特征, ?}：(x, ?)
    - 用于对新数据做出预测
>只有输入无输出的?

```
样本是指数据的特定实例：x。（我们采用粗体 x 表示它是一个矢量。）
我们将样本分为以下两类：
    有标签样本
    无标签样本
An example is a particular instance of data, x. 
(We put x in boldface to indicate that it is a vector.) We break examples into two categories:
    labeled examples
    unlabeled examples    

有标签样本同时包含特征和标签。即： 
``` 
`labeled examples: {features, label}: (x, y) `

**我们使用有标签样本来训练模型。Use labeled examples to train the model **

在我们的垃圾邮件检测器示例中，有标签样本是用户明确标记为“垃圾邮件”或“非垃圾邮件”的各个电子邮件。

`unlabeled examples: {features, ?}: (x, ?) `


## - 模型 Models = (仿佛是函数function)
- 可将样本映射到预测标签：y'
- 由模型的内部参数定义，这些内部参数值是通过 学习 得到的
- 学习规律 创建模型
```
模型定义了特征与标签之间的关系。
A model defines the relationship between features and label.

例如，垃圾邮件检测模型可能会将某些特征与“垃圾邮件”紧密联系起来。
```
    我们来重点介绍一下模型生命周期的两个阶段：
    1. 训练表示创建或学习模型。
    -Training- means creating or learning the model.
    也就是说，您向模型展示有标签样本，让模型逐渐学习特征与标签之间的关系。
    
    2. 推断表示将训练后的模型应用于无标签样本。 
    -Inference- means applying the trained model to unlabeled examples. 
    也就是说，您使用训练后的模型来做出有用的预测 (y')。例如，在推断期间，您可以针对新的无标签样本预测 medianHouseValue。


1. 回归模型可预测连续值。
A regression model predicts continuous values
例如，回归模型做出的预测可回答如下问题：
    - 加利福尼亚州一栋房产的价值是多少？
    - 用户点击此广告的概率是多少？

2. 分类模型可预测离散值。
A classification model predicts discrete values. 
例如，分类模型做出的预测可回答如下问题：
    - 某个指定电子邮件是垃圾邮件还是非垃圾邮件？
    - 这是一张狗、猫还是仓鼠图片
    
    
    
    
~~瞎bibi时间~~
---
感觉有点像以前学的多元分析的一个什么分析
就是很多的因素,然后算一个值,可以最终知道这个因素到底是否和结果有关,或者什么是最相关
百度了一下貌似叫 相关分析(correlation analysis)
但是又百度了一下
包括3类:
①多元方差分析、多元回归分析和协方差分析，称为线性模型方法，用以研究确定的自变量与因变量之间的关系；
②判别函数分析和聚类分析,用以研究对事物的分类；
③主成分分析、典型相关和因素分析，研究如何用较少的综合因素代替为数较多的原始变量。

感觉我是学过主成分,多元方差分析 大概.

然后大概还有一个 正交试验设计(Orthogonal experimental design)
研究多因素多水平的又一种设计方法，它是根据正交性从全面试验中挑选出部分有代表性的点进行试验.

但是都记不起来了


