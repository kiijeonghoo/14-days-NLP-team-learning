# 14-days-NLP-team-learning 📑

2020年7月Datawhale组队学习挑战    

学习内容为：零基础入门NLP之[新闻文本分类挑战赛](https://tianchi.aliyun.com/competition/entrance/531810/introduction?spm=5176.12281973.1005.1.3dd52448ZYdHgU), 根据新闻文本字符对新闻的类别进行分类

**Star⭐ me if you find useful🤣**

## 学习内容与进度 📙

详细的个人笔记和注解见[notebook](/nbs/)中批注，以下是每个task的总结 👇

### Task00 - [Baseline](/nbs/Task00-Baseline.ipynb) 

### Task01 - [赛题理解](/nbs/Task01-赛题理解.ipynb) 🍻

- 赛题数据：新闻文本 ( 按照**字符**级别匿名处理 ) / 14个类别
- 数据构成：训练集 (20w) / 测试集A (5w) / 测试集B (5w)
- 评价指标：f1_score的均值
- 解题思路
  - 思路1：TF-IDF + 机器学习分类器
  - 思路2：FastText
  - 思路3：word2vec + 深度学习分类器
  - 思路4：Bert

### Task02 - [数据读取与数据分析](/nbs/Task02-数据读取与数据分析.ipynb) 🍻

- 数据读取：pandas / 类别+新闻字符
- 数据分析：
  - 句子长度分析：平均907字符 / 中位数676字符 / min-2字符 / max-57921字符 / 大部分在2000以内 / 在建模时可能**需要截断**
  - 新闻类别分布：类别分布不均匀 / 科技类股票类最多 / 星座最少
  - 字符分布统计：共6869个字 / 3750号字出现次数最多 / 3133字出现次数最少 / 3750, 900, 648很有可能是标点
  - 其他分析方向：根据标点统计每篇新闻平均由几个句子构成 / 每类新闻出现次数最多的字符

### Task03 - [基于机器学习的文本分类](/nbs/Task03-基于机器学习的文本分类.ipynb) 🍻

- 文本表示方法 part1：
  - One-hot：将每一个单词使用一个离散的向量表示，每个字/词编码一个索引，然后根据索引进行赋值
  - Bag of Words：词袋表示 / 每个文档的字/词用其出现次数 / 用sklearn中`CountVectorizer`实现
  - N-gram：与Count Vectors类似，加入了相邻单词组合成为新的单词，并进行计数
  - TF-IDF：词频-逆文档频率

- 基于机器学习的文本分类：

  - **Count Vectors + RidgeClassifier**：0.74
  
  - **TF-IDF + RidgeClassifier**：0.87 / 增加数据后 0.93

### Task04 - [基于深度学习的文本分类1](/nbs/Task04-基于深度学习的文本分类1.ipynb) 🍻

- 文本表示方法 part2：
  - FastText：网络结构 - Embedding→GlobalAveragePooling→Softmax / 可以表示句子相似性, 维度低

- 基于深度学习的文本分类1：
  - **FastText**：0.82 / 增加数据后 0.91

### Task05 - [基于深度学习的文本分类2](/nbs/Task05-基于深度学习的文本分类1.ipynb) 🍻

- 文本表示方法 part3：
  - 词向量 word2vec：Skip-grams / Continuous Bag of Words / 对出现在上下文环境里的词进行预测

- 基于深度学习的文本分类2：
  - TextRNN：
  - TextCNN：
  - HAN：

### Task06 - [基于深度学习的文本分类3](/nbs/Task05-基于深度学习的文本分类3.ipynb) 

## 直播和答疑

- 第一次直播：
- 第二次直播：
- 第三次直播：
- 答疑汇总：https://shimo.im/docs/ag3Bb0ZG86QF6cJ2

## 参考资料

Datawhale开源学习资料：https://github.com/datawhalechina/team-learning 

天池比赛论坛：https://tianchi.aliyun.com/competition/entrance/531795/forum

