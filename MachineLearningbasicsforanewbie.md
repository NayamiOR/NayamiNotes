# Machine Learning basics for a newbie

# 原文

## **Overview**

- Get introduced to the world of machine learning with some basic concepts
- Statistics, Artificial Intelligence, Deep Learning and Data mining are few of the other technical words used with machine learning
- Learn about the different types of machine learning algorithms

## **Introduction**

There has been a renewed interest in machine learning in last few years. This revival seems to be driven by strong fundamentals – loads of data being emitted by sensors across the globe, with cheap storage and lowest ever computational costs!

However, not every one around understands what machine learning is. Here are a few examples:

- [What is Machine Learning and how is it different from Big Data and Business Analytics?](http://discuss.analyticsvidhya.com/t/what-is-machine-learning-and-how-is-it-different-from-big-data-and-business-analytics/306)
- [What is the difference between machine learning, data analysis, data mining, data science and AI?](http://discuss.analyticsvidhya.com/t/what-is-the-difference-between-machine-learning-data-analysis-data-mining-data-science-and-ai/572)

Here was a little funny (but immensely true) take on the topic we circulated on our [Facebook page](http://www.facebook.com/analyticsvidhya) recently.

![https://www.analyticsvidhya.com/wp-content/uploads/2015/06/10945756_10202550638602268_6848260291113352290_n.jpg](https://www.analyticsvidhya.com/wp-content/uploads/2015/06/10945756_10202550638602268_6848260291113352290_n.jpg)

Coming to the point, given the amount of confusion on the topic, we thought to create an awesome introductory series of articles on machine learning. The idea is to do away with all the jargons, which might have intimidated you in past and create something which can be read by a 5 year old (ok…sorry, may be a high school pass out)!

## **So what exactly is machine learning? My small experiment…**

Just to make sure I don’t over-estimate (or under-estimate) the capability of the target audience, I got hold of 10 people who were completely new to analytics. None of them had heard about machine learning before (yes, there are people like that!). Here is what they said:

- I don’t know, may be learning from machines?
- Making machines learn something a.k.a. programming machine software
- Learning with help of computers
- Learning through online courses (!!!)

That was fun! Perfect group to explain machine learning to. Here is how I started explaining to these people:

*Machine Learning refers to the techniques involved in dealing with vast data in the most intelligent fashion (by developing algorithms) to derive actionable insights.*

By this time, they were looking at me as if I have spoken a few things in front of people from Mars! So, I stopped and then asked them a question in return, which they could relate to more:

***KJ:** What do you think happens when you search for something on Google?*

***Group:** Google shows up the most relevant web pages related to that search.*

***KJ:** That’s good! but what really happens so that Google can show these relevant pages to you?*

This time it looked like they were thinking a bit more. Then some one from the group spoke

***Group member:** Google looks at the past clicks from the people to understand which pages are more relevant for those searches and then serves those results on top of search.*

This was a far better attempt. I also had to control my urge to preach that how Google does this is far more smarter way than this simple concept. But, I thought I had a good hook to explain machine learning here. So, I continued:

***KJ:** OK, that sounds like a good approach. But, how many searches and what all kind of searches would Google handle regularly?*

***Group:** Must be a real big number – may be a trillion searches every year*

***KJ:** So, how do you think Google can serve so many requests with such accuracy? Do you think there are people sitting in Google offices and continuously deciding which search result is relevant and which is not?*

***Group member:** Haven’t really thought about it, but no, that sounds humanly impossible to do.*

***KJ:** You are right. This is where machine learning comes into play. **Machine learning is a set of techniques, which help in dealing with vast data in the most intelligent fashion (by developing algorithms or set of logical rules) to derive actionable insights (delivering search for users in this case).***

A logical nod from the group, looks like mission accomplished…yay! But wait…

## **Now the common question – How is machine learning different from X?**

The minute you start reading about machine learning, you see various rockets bombarding you with high velocity. These are jargons used loosely in the industry. Here are some of them: Artificial Intelligence, Deep Learning, Data Mining and Statistics.

For your clear understanding, I have explained these terms below in the simple manner. You will also understand the importance of these terms in context of machine learning:

### **X = Artificial Intelligence(AI):**

It refers to the procedure of *programming* a computer (machine) to take *rational**.*** Ah! what is rational? Rational is the basis of taking a decision.

I mentioned ‘rational’ instead of intelligence (as expected) because we human beings tend to take decisions which are high on being rational and feasible rather than being explicitly intelligent. This is because *all intelligent decisions needn’t be rational and* feasible ***(***my hypothesis***)**.* Hence, the central motive behind using AI is to achieve the computer (machine) behave in a dandy fashion in lieu of human guidance instead of being doltish!

AI may include programs to check whether certain parameters within a program are behaving normally. For example, the machine may raise an alarm if a parameter say ‘X’ crosses a certain threshold which might in turn affect the outcome of the related process.

### **Use of Artificial Intelligence in Machine Learning**

*Machine Learning is a subset of AI* where the machine is trained to learn from it’s past experience. The past experience is developed through the data collected. Then it combines with algorithms such as Naïve Bayes, Support Vector Machine(SVM) to deliver the final results.

### **X = Statistics:**

At this high level stage, I assume you would know about statistics. If you don’t, here’s a quick definition, Statistics is that branch of mathematics which utilizes data, either of the entire population or a sample drawn from the population to carry out the analysis and present inferences. Some statistical techniques used are regression,variance, standard deviation, conditional probability and many others. To know about this topic, read [How to understand population distributions using statistics?](https://www.analyticsvidhya.com/blog/2014/07/statistics/)

### **Use of Statistics in Machine Learning**

Let’s understand this. Suppose, I need to separate the mails in my inbox into two categories: ‘spam’ and ‘important’. For identifying the spam mails, I can use a machine learning algorithm known as Naïve Bayes which will check the frequency of the past  spam mails to identify the new email as spam. Naïve Bayes uses the statistical technique Baye’s theorem( commonly known as conditional probability). Hence, we can say machine learning algorithms uses statistical concepts to execute machine learning.

Additional Information: The main difference between machine learning and statistical models come from the schools where they originated. While machine learning originated from the department of computer science and statistical modelling came down from department of mathematics. Also any statistical modelling assumes a number of distributions while machine learning algorithms are generally agnostic of the distribution of all attributes.

### **X = Deep Learning:**

Deep Learning is associated with a machine learning algorithm (Artificial Neural Network, ANN) which uses the concept of human brain to facilitate the modeling of arbitrary functions. ANN requires a vast amount of data and this algorithm is highly flexible when it comes to model multiple outputs simultaneously. ANN is more complex topic and we may do justice to it in an altogether separate article.

### **X = Data Mining:**

During my initial days as an analyst, I always used to muddle the two terms: Machine Learning and Data Mining. But, later I learnt, Data Mining deals with searching specific information. And Machine Learning solely concentrates on performing a given task. Let me cite the example which helped me to remember the difference; Teaching someone how to dance is Machine Learning. And using someone to find best dance centers in the city is Data Mining. Easy!

Also Read: [Introduction to Online Machine Learning](https://www.analyticsvidhya.com/blog/2015/01/introduction-online-machine-learning-simplified-2/)

## **But, How exactly do we teach machines?**

Teaching the machines involve a structural process where every stage builds a better version of the machine. For simplification purpose, the process of teaching machines can broken down into 3 parts:

![https://www.analyticsvidhya.com/wp-content/uploads/2015/06/teach-ML.png](https://www.analyticsvidhya.com/wp-content/uploads/2015/06/teach-ML.png)

I shall be covering each of these 3 steps in detail in my subsequent write-ups. As of now, you should understand, these 3 steps ensures the holistic learning of the machine to perform the given task with equal importance. Success of machine depends on two factors:

1. *How well the generalization of abstraction data take place.*

*2. How well the machine is able to put it’s learning into practical usage for predicting the future course of action.*

Also Read: [Learn about Scikit-Learn – Machine Learning tool in Python](https://www.analyticsvidhya.com/blog/2015/01/scikit-learn-python-machine-learning-tool/)

## **What are the steps used in Machine Learning?**

There are 5 basic steps used to perform a machine learning task:

1. **Collecting data**: Be it the raw data from excel, access, text files etc., this step (gathering past data) forms the foundation of the future learning. The better the variety, density and volume of relevant data, better the learning prospects for the machine becomes.
2. **Preparing the data**: Any analytical process thrives on the quality of the data used. One needs to spend time determining the quality of data and then taking steps for fixing issues such as missing data and treatment of outliers. [Exploratory analysis](https://www.analyticsvidhya.com/blog/2015/02/data-exploration-preparation-model/) is perhaps one method to study the nuances of the data in details thereby burgeoning the nutritional content of the data.
3. **Training a model**: This step involves choosing the appropriate algorithm and representation of data in the form of the model. The cleaned data is split into two parts – train and test (proportion depending on the prerequisites); the first part (training data) is used for developing the model. The second part (test data), is used as a reference.
4. **Evaluating the model**: To test the accuracy, the second part of the data (holdout / test data) is used. This step determines the precision in the choice of the algorithm based on the outcome. A better test to check accuracy of model is to see its performance on data which was not used at all during model build.
5. **Improving the performance**: This step might involve choosing a different model altogether or introducing more variables to augment the efficiency. That’s why significant amount of time needs to be spent **in data collection and preparation.**

Be it any model, these 5 steps can be used to structure the technique and when we discuss the algorithms, you shall then find how these five steps appear in every model!

Also Read: [Getting Smart with Machine Learning – Ada Boost and Gradient Boost](https://www.analyticsvidhya.com/blog/2015/05/boosting-algorithms-simplified/)

## **What are the types of Machine Learning algorithms?**

![https://www.analyticsvidhya.com/wp-content/uploads/2015/06/machine-learning-types.png](https://www.analyticsvidhya.com/wp-content/uploads/2015/06/machine-learning-types.png)

### **Supervised Learning / Predictive models:**

Predictive model as the name suggests is used to predict the future outcome based on the historical data. Predictive models are normally given clear instructions right from the beginning as in what needs to be learnt and how it needs to be learnt. These class of learning algorithms are termed as **Supervised Learning.**

For example: Supervised Learning is used when a marketing company is trying to find out which customers are likely to churn. We can also use it to predict the likelihood of occurrence of perils like earthquakes, tornadoes etc. with an aim to determine the Total Insurance Value. Some examples of algorithms used are: Nearest neighbour, Naïve Bayes, Decision Trees, Regression etc.

### **Unsupervised learning / Descriptive models:**

It is used to train descriptive models where no target is set and no single feature is important than the other. The case of unsupervised learning can be: When a retailer wishes to find out what are the combination of products, customers tends to buy more frequently. Furthermore, in pharmaceutical industry, unsupervised learning may be used to predict which diseases are likely to occur along with diabetes. Example of algorithm used here is: K- means Clustering Algorithm

### **Reinforcement learning (RL):**

It is an example of machine learning where the machine is trained to take specific decisions based on the business requirement with the sole motto to maximize efficiency (performance). The idea involved in reinforcement learning is: The machine/ software agent trains itself on a continual basis based on the environment it is exposed to, and applies it’s enriched knowledge to solve business problems. This continual learning process ensures less involvement of human expertise which in turn saves a lot of time!

An example of algorithm used in RL is Markov Decision Process.

Important Note: There is a subtle difference between Supervised Learning and Reinforcement Learning (RL). RL essentially involves learning by interacting with an environment. An RL agent learns from its past experience, rather from its continual trial and error learning process as against supervised learning where an external supervisor  provides examples.

A good example to understand the difference is self driving cars. Self driving cars use Reinforcement learning to make decisions continuously – which route to take? what speed to drive on? are some of the questions which are decided after interacting with the environment. A simple manifestation for supervised learning would be to predict fare from a cab going from one place to another.

## **What are the applications of Machine Learning?**

It is very interesting to know the applications of machine learning. Google and Facebook uses ML extensively to push their respective ads to the relevant users. Here are a few applications that you should know:

- **Banking & Financial services**: ML can be used to predict the customers who are likely to default from paying loans or credit card bills. This is of paramount importance as machine learning would help the banks to identify the customers who can be granted loans and credit cards.
- **Healthcare**: It is used to diagnose deadly diseases (e.g. cancer) based on the symptoms of patients and tallying them with the past data of similar kind of patients.
- **Retail**: It is used to identify products which sell more frequently (fast moving) and the slow moving products which help the retailers to decide what kind of products to introduce or remove from the shelf. Also, machine learning algorithms can be used to find which two / three or more products sell together. This is done to design customer loyalty initiatives which in turn helps the retailers to develop and maintain loyal customers.

These examples are just the tip of the iceberg. Machine learning has extensive applications practically in every domain. You can check out a few Kaggle problems to get further flavor. The examples included above are easy to understand and at least give a taste of the omnipotence of machine learning.

## **End Notes**

In this article, we started by developing a basic understanding of what machine learning is. We also looked at how it gets confused with several other terms. We also covered the process to teach a machine, the essential steps used in machine learning, the algorithms used in machine learning followed by the applications of machine learning.

I hope this article helped you to get acquainted with basics of machine learning. We would love to hear about it from you. Did you find it useful? What aspects of machine learning confuse you the most? Feel free to post your thoughts through comments below.

# 翻译

## 介绍

在过去的几年里，人们对机器学习产生了新的兴趣。这种复苏似乎是由强大的基本因素推动的 - 全球各地
的终端都在释放出的大量数据，并且这些数据的成本非常低廉，计算成本是有史以来是最低的！
然而，并非每个人都了解机器学习是什么。这里有几个例子：
什么是机器学习？它与大数据和业务分析有何不同？
机器学习，数据分析，数据挖掘，数据科学和AI之间有什么区别？
最近，我们发布了一个有趣的（但非常真实的）主题。
说道这一点，考虑到这个话题上的混乱程度，我们打算写一篇关于机器学习的介绍性文章。这个想法是去
掉所有可能在过吓唬人的术语，创造一些可以被5岁的孩子轻松了解的东西（emmmmmmm............好吧,
对不起，可能需要高中毕业）！
机器学习究竟什么是？我的一个小实验......
为了确保我不会高估（或低估）目标受众的能力，我找到了10个对分析完全陌生的人。他们之前都没有听
说过机器学习（是的，真的有这样的人！！！！！）。他们是这样说的：
我不知道，可能是向机器中学习？
让机器学习一些东西，也就是编程机器软件
借助计算机帮助我学习？
通过在线课程学习（!!!）
这很有趣！完美的解释了他们认为的机器学习。以下是我向这些人解释机器学习的概念：
机器学习是指以最智能的方式处理大量数据（通过开发算法）以获得可操作的见解的技术。
这时，他们看着我，就好像我是火星人一样对他们说话！所以，我停止了愚蠢的术语讲解，然后反过来问
他们问题，方便他们可以更深入的了解：
KJ：当你在谷歌搜索某些东西时，你认为会发生什么？
组员：Google会显示与该搜索相关的网页。
KJ：那很好！但究竟是什么让Google可以向你显示这些相关页面呢？
这次看起来他们想的比较多。然后组内的一些人开始发言
组员：Google会查看用户过去的点击次数，了解哪些网页与这些搜索更相关，然后在搜索结果上提供这些
结果。
这是一个很好的尝试。但我还必须控制住自己的冲动，告诉他们Google做到这一点要比他们这个简单的概
念复杂的多。但是，我想我有一个更好的方法来解释机器学习。所以，我继续说：
KJ：好的，这听起来不错。但是，Google会定期处理多少次搜索以及所有搜索的类型？
组员：这一定是一个很大的数字 - 可能每年是一万亿次搜索2021/7/13 机器学习前需要哪些预备知识？ - 知乎
https://www.zhihu.com/question/283702958 2/5
KJ：那么，你们认为Google如何准确地满足如此多的请求？你们是不是认为有人坐在Google办公室并不
断处理哪些搜索结果是跟搜索的问题是相关的呢?
小组成员：我还没有想过，但是不会有人去处理这些，因为这好像听起来不像是人类可以处理的。
KJ：你是对的。这是机器学习发挥作用的地方。机器学习是一组技术，以最智能的方式处理大量数据（通
过开发算法或一组逻辑规则）， 来获得可操作的结果（在我们讨论的问题中是为用户提供搜索）。
这个时候小组成员们按照意料之中的点了点头，看起来像我已经完成任务......耶！可是总觉得哪里不对呢…
现在有一些常见的问题 - 比如机器学习与X有什么不同？
你开始学习有关机器学习的那一刻，你会看到各种知识好像火箭一样在高速的轰炸着你。这些是术语在行
业内使用的比较多。以下是其中一些：人工智能，深度学习，数据挖掘和统计。
为了让你更加清楚理解，我以简单的方式解释了这些术语。你还会了解到这些术语在机器学习中的重要
性：
什么是人工智能（AI）：
它指的是一台计算机（机器）进行编程使得自己变得合理的程序。啊! 什么是理性的？理性是做出决定的基
础。
我提到“理性”而不是智力（如预期的那样），因为我们人类倾向于做出高度理性和可行的决策而不是明
确的智慧。这是因为所有智能决策都不需要理性和可行（我的假设）。因此，使用人工智能背后的核心动
机是以一种时髦的方式实现计算机（机器）的行为，而不是由愚蠢的人类指导！
人工智能可以包括用于检查程序中的某些参数是否正常运行的程序。例如，如果参数说“X”超过某个阈
值，机器可能会发出警报，而该阈值反过来可能又会影响相关过程的结果。
人工智能在机器学习中的应用
机器学习是人工智能的一个子集，其中机器经过培训，可以从中学习过去的经验。过去的经验是通过收集
的数据制定的。然后它结合朴素贝叶斯，支持向量机等算法来提供最终结果。
什么是统计：
在这个高水平的阶段，我假设你已经了解了统计学。如果没有的话，这里有一个可以让你快速了解统计学
的定义，统计学是数学的一个分支，它利用数据，或者是整个群体的数据，或者从群体中抽取一个样本，
来进行分析并给出推论。使用的技术统计有回归、方差、标准差、条件概率等等。
在机器学习中使用统计学
让我们理解这一点，首先需要假设，我需要将收件箱中的邮件分为两类：“垃圾邮件”和“重要邮件”。
为了识别垃圾邮件，我可以使用称为朴素贝叶斯的机器学习算法，该算法将检查过去垃圾邮件的频率，从
而将新邮件识别为垃圾邮件。朴素贝叶斯使用统计技术贝叶斯定理（通常称为条件概率）。因此，我们可
以说机器学习算法使用统计概念来执行机器学习。2021/7/13 机器学习前需要哪些预备知识？ - 知乎
https://www.zhihu.com/question/283702958 3/5
PS：机器学习和统计模型之间的主要区别来自它们的发源地。机器学习起源于计算机科学系，统计建模来
自数学系。此外，任何统计建模都假设许多分布，而机器学习算法通常不知道所有属性的分布。
什么是深度学习：
深度学习与机器学习算法（人工神经网络，ANN）相关联的，该算法使用人脑的概念来促进任意函数的建
模。神经网络需要大量数据，并且该算法在同时对多个输出进行建模时具有高度灵活性。神经网络是一个
更复杂的主题，我们可以在完全独立的文章中对其进行讨论。
什么是数据挖掘：
在我刚开始做数据分析师的日子里，我总是习惯于混淆两个术语：机器学习和数据挖掘。但是，后来我了
解到，数据挖掘处理的是搜索特定信息。机器学习专注于完成一项特定的任务。让我举一个帮助我记住差
异的例子; 教别人如何跳舞是机器学习。利用某人在城市中寻找最佳的舞蹈中心是数据挖掘。是不是超级简
单！
但是，我们究竟如何教机器？
教机器涉及到一个结构化过程，这个过程中，每个阶段都可以构建更好的机器版本。为简化起见，教学机
器的过程可分为三个部分：
我将在随后的文章中详细介绍这3个步骤中的每一个。到目前为止，你应该明白，这3个步骤确保机器的整
体学习能够同等重要地执行给定的任务。机器的成功取决于两个因素：
抽象数据的泛化效果如何。
这台机器如何把它的学习应用到预测未来的实际应用中。
机器学习的步骤是什么？
有5个基本步骤用于执行机器学习任务：
收集数据：无论是来自excel，access，文本文件等的原始数据，这一步（收集过去的数据）构成了未来学
习的基础。相关数据的种类，密度和数量越多，机器的学习前景就越好。
准备数据：任何分析过程都会依赖于使用的数据质量如何。人们需要花时间确定数据质量，然后采取措施
解决诸如缺失的数据和异常值的处理等问题。探索性分析可能是一种详细研究数据细微差别的方法，从而
使数据的质量迅速提高。
训练模型：此步骤涉及以模型的形式选择适当的算法和数据表示。清理后的数据分为两部分 - 训练和测试
（比例视前提确定）; 第一部分（训练数据）用于开发模型。第二部分（测试数据）用作参考依据。
评估模型：为了测试准确性，使用数据的第二部分（保持/测试数据）。此步骤根据结果确定算法选择的精
度。检查模型准确性的更好测试是查看其在模型构建期间根本未使用的数据的性能。
提高性能：此步骤可能涉及选择完全不同的模型或引入更多变量来提高效率。这就是为什么需要花费大量
时间进行数据收集和准备的原因。
无论是任何模型，这5个步骤都可用于构建技术，当我们讨论算法时，您将找到这五个步骤如何出现在每个
模型中！2021/7/13 机器学习前需要哪些预备知识？ - 知乎
https://www.zhihu.com/question/283702958 4/5
机器学习算法有哪些类型？
监督学习/预测模型：
顾名思义,预测模型用于根据历史数据预测未来结果。预测模型通常从一开始就给出明确的指示，如需要学
习的内容以及如何学习。这类学习算法被称为监督学习。
例如：当营销公司试图找出哪些客户可能会流失时，就会使用监督学习。我们还可以用它来预测地震，龙
卷风等危险发生的可能性，目的是确定总保险价值。使用的算法的一些示例是：最近邻算法，朴素贝叶斯
算法，决策树算法，回归算法等。
无监督学习/描述性模型：
它用于训练描述模型，其中没有设置目标，并且没有一个特征比另一个重要。无监督学习的情况可以是：
当零售商希望找出产品组合时，顾客往往会更频繁地购买。此外，在制药工业中，可以使用无监督学习来
预测哪些疾病可能与糖尿病一起发生。这里使用的算法示例是：K-均值聚类算法
强化学习（RL）：
这是机器学习的一个例子，其中机器被训练根据业务需求做出特定的决定，唯一的座右铭是最大化效率
（性能）。强化学习所涉及的理念是：机器/软件代理根据其所处的环境不断地自我训练，并应用它丰富的
知识来解决业务问题。这种持续的学习过程可以减少人类专业知识的参与，从而节省大量时间！
RL中使用的算法的示例是马尔可夫决策过程。
PS：监督学习和强化学习（RL）之间存在细微差别。RL主要涉及通过与环境交互来学习。RL代理从其过去
的经验中学习，而不是从其持续的试验和错误学习过程中学习，而是外部主管提供示例的监督学习中学
习。
了解差异的一个很好的例子是无人驾驶汽车。自驾车使用强化学习来不断做出决策 - 走哪条路？速度是是
多少？这些问题都是与环境互动后决定的。监督学习的一个简单表现是预测出租车从一个地方到另一个地
方的车费。
机器学习有哪些应用？
了解机器学习的应用是非常有趣的。Google和Facebook广泛使用ML将其各自的广告推送给相关用户。以
下是你应该了解的一些ML应用：
银行和金融服务：ML可用于预测可能违约支付贷款或信用卡账单的客户。这是至关重要的，因为机器学习
将帮助银行识别那些是可以获得贷款和信用卡的客户。
医疗保健：它用于根据患者的症状诊断致命疾病（例如癌症），并根据类似患者的过去数据对其进行统
计。
零售：它用于识别销售频繁（快速移动）的产品和缓慢移动的产品，帮助零售商决定从货架上引入或移除
哪种产品。此外，机器学习算法可用于查找哪两个/三个或更多产品一起销售。这样做是为了设计客户忠诚
度计划，从而帮助零售商开发和维护忠诚的客户。2021/7/13 机器学习前需要哪些预备知识？ - 知乎
https://www.zhihu.com/question/283702958 5/5
这些例子只是冰山一角。机器学习在每个领域都有广泛的应用。可以查看一些Kaggle问题以获得更多知
识，上面包含的例子很容易理解，至少可以体验机器学习的无所不能。
随着人工智能的热潮，人们开始逐渐的对机器学习产生了兴趣，而这种兴趣也是全球化，虽然人们对机器
学习有很大的兴趣，但是人们对机器学习似乎并没有真正的了解，而文章的作者借由向一些非数据科学行
业内的小白科普机器学习的过程中，用非常白话的语言向我们介绍了什么是机器学习，一些机器学习中的
专业术语，机器学习的步骤和机器学习的类型与应用。并且通过一些小案例向我们解释了各种算法的作
用，在我认为，机器学习是进入人工智能领域一块很好的垫脚石，至少不会再未来的浪潮中使我们迷失了
方向。