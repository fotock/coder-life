# 十大常用机器学习算法

源自: [towardsdatascience.com](https://towardsdatascience.com/a-tour-of-the-top-10-algorithms-for-machine-learning-newbies-dde4edffae11)

## 1 线性回归

线性回归可能是统计学和机器学习中最知名且易于理解的算法之一。

预测建模主要关注最小化模型的误差或使可能性最准确的预测，但代价是可解释性。我们将从许多不同的领域借用，重用和窃取算法，包括统计数据并将其用于这些目的。

线性回归的表示是通过查找称为系数（B）的输入变量的特定权重来描述最符合输入变量（x）和输出变量（y）之间关系的线的等式。

![ ](/assets/ml-algorithm-1.jpg)

线性回归

例如：y = B0 + B1 * x

我们将在给定输入x的情况下预测y，并且线性回归学习算法的目标是找到系数B0和B1的值。

可以使用不同的技术从数据中学习线性回归模型，例如用于普通最小二乘的线性代数解和梯度下降优化。

线性回归已经存在了200多年，并且已经被广泛研究。使用此技术时，一些好的经验法则是删除非常相似（相关）的变量，并尽可能消除数据中的噪声。这是一种快速而简单的技术和良好的第一种算法。

## 2 逻辑回归

逻辑回归是从统计领域的机器学习中借用的另一种技术。它是二进制分类问题的首选方法（两个类值的问题）。

逻辑回归就像线性回归一样，目标是找到加权每个输入变量的系数的值。与线性回归不同，使用称为逻辑函数的非线性函数来转换输出的预测。

逻辑函数看起来像一个大S并将任何值转换为0到1的范围。这很有用，因为我们可以将一个规则应用于逻辑函数的输出，以将值捕捉到0和1（例如IF小于0.5然后输出1）并预测一个类值。

![ ](/assets/ml-algorithm-2.jpg)

逻辑回归

由于学习模型的方式，逻辑回归所做的预测也可以用作属于0级或1级的给定数据实例的概率。这对于需要给出更多基本原理的问题非常有用。一个预测。

与线性回归一样，当您删除与输出变量无关的属性以及彼此非常相似（相关）的属性时，逻辑回归确实更有效。这是一个学习二元分类问题的快速模型。

## 3 线性判别分析 (LDA)

逻辑回归是一种传统上仅限于两类分类问题的分类算法。如果您有两个以上的类，那么线性判别分析算法是首选的线性分类技术。

LDA的代表非常简单。它包含数据的统计属性，为每个类计算。对于单个输入变量，这包括：

每个班级的平均值。
在所有类别中计算的方差。

![ ](/assets/ml-algorithm-3.png)

通过计算每个类的判别值并对具有最大值的类进行预测来进行预测。该技术假设数据具有高斯分布（钟形曲线），因此最好事先从数据中删除异常值。它是分类预测建模问题的一种简单而强大的方法。

## 4 分类和回归树

决策树是预测建模机器学习的一种重要算法。

决策树模型的表示是二叉树。这是来自算法和数据结构的二叉树，没什么太花哨的。每个节点代表一个输入变量（x）和该变量上的分裂点（假设变量是数字）。

![ ](/assets/ml-algorithm-4.png)

树的叶节点包含用于进行预测的输出变量（y）。通过遍历树的分裂直到到达叶节点并在该叶节点处输出类值来进行预测。

树木学习速度快，预测速度非常快。它们通常对于广泛的问题也是准确的，并且不需要对您的数据进行任何特殊准备。

## 5 朴素贝叶斯

朴素贝叶斯是一种简单但令人惊讶的强大的预测建模算法。

该模型由两种类型的概率组成，可以直接根据您的训练数据计算：1）每个类的概率; 2）给出每个x值的每个类的条件概率。一旦计算，概率模型可用于使用贝叶斯定理对新数据进行预测。当您的数据是实值时，通常假设高斯分布（钟形曲线），以便您可以轻松估计这些概率。

![ ](/assets/ml-algorithm-5.png)

朴素贝叶斯被称为朴素，是因为它假定每个输入变量是独立的。这是一个强有力的假设，对于实际数据是不现实的，然而，该技术对于大范围的复杂问题非常有效。

## 6 K-Nearest Neighbors

KNN算法非常简单且非常有效。KNN的模型表示是整个训练数据集。简单吧？

通过搜索K个最相似的实例（邻居）的整个训练集并总结那些K个实例的输出变量，对新数据点进行预测。对于回归问题，这可能是平均输出变量，对于分类问题，这可能是模式（或最常见）类值。

诀窍在于如何确定数据实例之间的相似性。如果您的属性都具有相同的比例（例如以英寸为单位），则最简单的技术是使用欧几里德距离，您可以根据每个输入变量之间的差异直接计算该数字。

![ ](/assets/ml-algorithm-6.png)

KNN可能需要大量内存或空间来存储所有数据，但只在需要预测时才进行计算（或学习），及时。您还可以随着时间的推移更新和策划您的训练实例，以保持预测准确。

距离或接近度的概念可以在非常高的维度（许多输入变量）中分解，这会对算法在您的问题上的性能产生负面影响。这被称为维度的诅咒。它建议您仅使用与预测输出变量最相关的输入变量。

## 7 学习矢量量化

K-Nearest Neighbors的缺点是你需要坚持整个训练数据集。学习矢量量化算法（或简称LVQ）是一种人工神经网络算法，允许您选择要挂起的训练实例数量，并准确了解这些实例应该是什么样子。

![ ](/assets/ml-algorithm-7.png)

LVQ的表示是码本向量的集合。这些是在开始时随机选择的，并且适于在学习算法的多次迭代中最佳地总结训练数据集。在学习之后，可以使用码本向量来进行与K-Nearest Neighbors类似的预测。通过计算每个码本矢量和新数据实例之间的距离来找到最相似的邻居（最佳匹配码本矢量）。然后返回最佳匹配单元的类值或（回归情况下的实际值）作为预测。如果将数据重新缩放至相同范围（例如0到1之间），则可获得最佳结果。

如果您发现KNN在您的数据集上提供了良好的结果，请尝试使用LVQ来降低存储整个训练数据集的内存要求。

## 8 支持向量机

支持向量机可能是最流行和最受关注的机器学习算法之一。

超平面是分割输入变量空间的线。在SVM中，选择超平面以最好地将输入变量空间中的点与它们的类（0级或1级）分开。在二维中，您可以将其视为一条线，并假设我们的所有输入点都可以被这条线完全分开。SVM学习算法找到导致超平面最好地分离类的系数。

![ ](/assets/ml-algorithm-8.jpg)

超平面和最近数据点之间的距离称为边距。可以分离两个类的最佳或最佳超平面是具有最大边距的线。只有这些点与定义超平面和分类器的构造有关。这些点称为支持向量。它们支持或定义超平面。实际上，优化算法用于找到使裕度最大化的系数的值。

SVM可能是最强大的开箱即用分类器之一，值得尝试使用您的数据集。

## 9 套袋(Bagging)和随机森林

随机森林是最流行和最强大的机器学习算法之一。它是一种称为Bootstrap Aggregation或bagging的集成机器学习算法。

引导程序是用于从数据样本估计数量的强大统计方法。比如一个意思。您可以获取大量数据样本，计算平均值，然后平均所有平均值，以便更好地估计真实平均值。

在装袋中，使用相同的方法，但是用于估计整个统计模型，最常见的是决策树。获取训练数据的多个样本，然后为每个数据样本构建模型。当您需要对新数据进行预测时，每个模型都会进行预测，并对预测进行平均以更好地估计真实输出值。

![ ](/assets/ml-algorithm-9.png)

随机森林

随机森林是对这种方法的一种调整，其中创建决策树，使得不是选择最佳分裂点，而是通过引入随机性来进行次优分割。

因此，为每个数据样本创建的模型与其他情况相比更加不同，但仍然以其独特和不同的方式准确。结合他们的预测可以更好地估计真实的基础产值。

如果使用具有高方差的算法（如决策树）获得良好结果，则通常可以通过对该算法进行包装来获得更好的结果。

## 10 Boosting和AdaBoost

Boosting是一种集合技术，试图从许多弱分类器中创建一个强分类器。这是通过从训练数据构建模型，然后创建第二个模型来尝试从第一个模型中纠正错误来完成的。添加模型直到完美预测训练集或添加最大数量的模型。

AdaBoost是第一个为二进制分类开发的真正成功的增强算法。这是理解助力的最佳起点。现代助推方法建立在AdaBoost上，最着名的是随机梯度增强机。

![ ](/assets/ml-algorithm-10.jpg)

AdaBoost

AdaBoost用于短决策树。在创建第一个树之后，每个训练实例上的树的性能用于加权创建的下一个树应该关注每个训练实例的注意力。难以预测的训练数据被赋予更多权重，而易于预测的实例被赋予更少的权重。模型是一个接一个地顺序创建的，每个模型更新训练实例上的权重，这些权重影响序列中下一个树所执行的学习。构建完所有树之后，将对新数据进行预测，并根据训练数据的准确性对每棵树的性能进行加权。

因为通过算法如此关注纠正错误，所以必须删除带有异常值的干净数据。