深入了解机器学习 (Descending into ML)
---

线性回归 Linear Regression 是一种找到最适合一组点的直线或超平面的方法。
本模块会先直观介绍线性回归，为介绍线性回归的机器学习方法奠定基础。


- 从数据中学习
    - 您可以使用很多种复杂的方法从数据中学习 There are lots of complex ways to learn from data
    - 但我们可以从简单且熟悉的内容入手 But we can start with something simple and familiar
    - 从简单的内容入手可打开通往一些广泛实用方法的大门 Starting simple will open the door to some broadly useful methods

- 例子

![某个例子](/img_for_md/QQ20180307-234329@2x.png)


#### - 方差 A Convenient Loss Function for Regression
- 给定样本的 L2 损失也称为平方误差
- L2 Loss for a given example is also called [ squared error ]

= 预测值和标签值之差的平方
= (观察值 - 预测值)^2
= (y - y')^2
= the square of the difference between the label and the prediction
= (observation - prediction(x))^2
= (y - y')^2


着眼于最大限度地 减少整个数据集的误差 minimizing loss across our entire data set
![](/img_for_md/QQ20180307-234543@2x.png){:height="50%" width="50%"}


#### - 线性回归

```
Ruth 阿姨将她喜爱的蟋蟀数据库作为生日礼物送给您，并邀请您自己利用该数据库训练一个模型，从而预测鸣叫声与温度的关系。
```
![大概是基础概念](/img_for_md/QQ20180307-235050@2x.png)

```
where:

 is the temperature in Celsius—the value we're trying to predict.
 is the -slope of the line-.
 is the number of chirps per minute—the value of our input feature.
 is the y-intercept.
By convention in machine learning, you'll write the equation for a model only slightly differently:

where:

 is the predicted label (a desired output).
 is the bias (the y-intercept). In some machine-learning documentation, it is instead referred to as .
 is the weight of feature 1. Weight is the same concept as "slope" written with  above.
 is a feature (a known input).
To infer (predict) the temperature  for a new chirps-per-minute value , just plug the  value into this model.

The subscripts (for example,  and ) foreshadow more sophisticated models that rely on multiple features. For example, a model that relies on three features would use the following equation:
```

#### - 训练Training 模型 a model
- 表示通过有标签样本来学习（确定）所有权重和偏差 the weights and the bias 的理想值。
- 在监督式学习中，机器学习算法通过以下方式构建模型：检查多个样本并尝试找出可最大限度地减少损失的模型；
- 这一过程称为 经验风险最小化 empirical risk minimization。


#### - 损失是对糟糕预测的惩罚 Loss is the penalty for a bad prediction.
- 也就是说，损失是一个数值，表示对于单个样本而言模型预测的准确程度。
-  loss is a number indicating how bad the model's prediction was on a single example.
- 如果模型的预测完全准确，则损失为零，否则损失会较大。
- If the model's prediction is perfect, the loss is zero; otherwise, the loss is greater.
- 训练模型的目标 是从所有样本中找到 一组平均损失“较小”的权重和偏差。


#### 均方差
![](/img_for_md/QQ20180307-235436@2x.png){:height="50%" width="50%"}
- 不记得n-1的那个叫啥了


~~瞎bibi~~

怎么这么多叫法,方差原来是叫l2误差....
诶我不记得大学概率论的时候叫l2误差啊.....

我不要蟋蟀数据库做生日礼物啊,谷歌你是不是傻
线性回归这个真很像多元的那个分析

嗯 目前还是在捡起来老本的状态.

我觉得我还是想设置一下截图的大小,太大了.