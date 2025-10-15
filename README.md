# learning-kaggle-word2vec-nlp
这是一个记录我学习和实践 Kaggle["Bag of Words Meets Bags of Popcorn"](https://www.kaggle.com/competitions/word2vec-nlp-tutorial) NLP 教程的项目。

## 获取数据
前往[kaggle](https://www.kaggle.com/competitions/word2vec-nlp-tutorial/data) 下载 `labeledTrainData.tsv`, `unlabeledTrainData.tsv`, 和 `testData.tsv`。
## 代码part1: review_classification.ipynb
### 对文本数据的处理：
* 删除HTML标签
* 去除标点和数字
* 分词
* 去除停用词
### 调用sklearn中的随机森林分类器对训练数据进行拟合，对测试数据进行预测。
注：由于测试集数据是无标签数据，未进行模型评估。
## 代码part2-3:Word2Vec.ipynb
### 对文本数据的处理
与part1相似
### 划分句子
将原始的文本段落切分为以句子为单位，每个句子为一个词列表，便于后续word2vec模型的训练
### 调用gensim的word2vec模型将词转为向量
使用word2vec中的skip-gram
### 模型效果测试
* 语义匹配
* 语义相似
### 模型应用
1. 利用word2vec模型将词转为维度相同的向量，计算每个评论的平均向量，之后利用随机森林对向量进行情感分析。
2. 利用word2vec模型将词转为维度相同的向量，采用K-means聚类将词向量分到若干个簇中，将每条评论转化为维度大小与簇数量相同的向量。之后利用随机森林对向量进行情感分析。
注：与part1相同，未进行模型评估。

