---
title: EM算法
date: 2016-11-27 09:03:04
tags:
---

EM算法是一种迭代算法，用于含有有隐变量的概率模型参数的极大似然估计，或极大后验概率估计。
EM算法的每次迭代由两步组成：E步，求期望;M步，求极大。

极大似然估计：
极大后验概率估计：
期望：

最大似然估计提供了一种给定观察数据来评估模型参数的方法，即：“模型已定，参数未知”。
最大似然估计中采样需满足一个很重要的假设，就是所有的采样都是独立同分布的。

http://blog.csdn.net/upon_the_yun/article/details/8915283

似然函数：在数理统计学中，似然函数是一种关于统计模型中的参数的函数，表示模型参数中的似然性。
“似然性”与“或然性”或“概率”意思相近，都是指某种事件发生的可能性，但是在统计学中，“似然性”和“或然性”或“概率”又有明确的区分。概率用于在已知一些参数的情况下，预测接下来的观测所得到的结果，而似然性则是用于在已知某些观测所得到的结果时，对有关事物的性质的参数进行估计。

条件概率：P(A|B)表示在B事件发生的情况下，A事件发生的概率。
联合概率：P(AB)表示AB事件同时发生的概率。



贝叶斯公式：
    P(y|x) = ( P(x|y) * P(y) ) / P(x)
这里：
P(y|x) 是后验概率，一般是我们求解的目标。
P(x|y) 是条件概率，又叫似然概率，一般是通过历史数据统计得到。一般不把它叫做先验概率，但从定义上也符合先验定义。
P(y) 是先验概率，一般都是人主观给出的。贝叶斯中的先验概率一般特指它。
P(x) 其实也是先验概率，只是在贝叶斯的很多应用中不重要（因为只要最大后验不求绝对值），需要时往往用全概率公式计算得到。

先验概率：P(头痛｜感冒) ，感冒会导致头痛的概率。P(头痛）P(感冒）都是先验概率。
后验概率：P(感冒｜头痛) ，头痛是由感冒引起的概率。

事件发生前的预判概率。可以是基于历史数据的统计，可以由背景常识得出，也可以是人的主观观点给出。一般都是单独事件概率，如P(x),P(y)。

先验概率（prior probability）是指根据以往经验和分析得到的概率，如全概率公式，它往往作为"由因求果"问题中的"因"出现的概率·
后验概率是指依据得到"结果"信息所计算出的最有可能是那种事件发生,如贝叶斯公式中的,是"执果寻因"问题中的"因".


后验概率在实际中一般是很难直接计算出来的，相反先验概率就容易多了。因此一般会利用先验概率来计算后验概率。（根据贝叶斯公式）


http://www.cnblogs.com/washa/p/3222109.html
极大似然估计，与最大后验概率，与最大熵估计 都可以用来估计概率分布参数；

最大后验估计是根据经验数据获得对难以观察的量的点估计。与最大似然估计类似，但是最大的不同时，最大后验估计的融入了要估计量的先验分布在其中。故最大后验估计可以看做规则化的最大似然估计。

MAP与MLE最大区别是MAP中加入了模型参数本身的概率分布，或者说。MLE中认为模型参数本身的概率的是均匀的，即该概率为一个固定值。

函数y=f(x)，x0= argmax(f(x)) 的意思就是参数x0满足f(x0)为f(x)的最大值；换句话说就是 argmax(f(x))是使得 f(x)取得最大值所对应的变量x。arg即argument，此处意为“自变量”。

