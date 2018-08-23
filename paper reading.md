7月25日的paper reading : Deep Clustering for Unsupervised Learning of Visual Features (ECCV 2018) 讲了一个非常朴素直观的
结合深度学习和传统机器学习的一个非监督学习方法。 将CNN 的特征进行 K-means 聚类，以聚类的结果作为监督信息，从而实现无监督的学习。

8月8日：
讲了一篇自动设计CNN 网络的一种算法，其中有一个关键算法是用于搜索模块， 当然基础模块是人为提前定义的一些（几十种吧）。———— 这个似乎可以用到
合成生物学上，自动的设计，而非人为设计。

8月15日：
讲了两篇weakly supervision （只有图像分类的标签-可以是multilabel， 没有分割的gt）的做语义分割的paper。思路一致，都是通过训练分类网络，利用CAM的机制
找到一个大致的跟label corresponding的区域作为 分割的label。然后训练分割网络。
两篇paper的不同之处是分类网络的设计，一个设计更复杂，使得分类所得CAM的区域更准确，但是分类和分割的训练分离；
另一个分类网络相对简单，但是分类和分割网络有交互，分类所得CAM区域可以得到分割网络的反馈和更新

8月22日
我讲了两篇paper，一个是做instance-level human partition segmentation的， 用 edge detection 来辅助instance的实现，从而实现一个网络端到端的训练
再加上后处理就可以得到instance级别的人体部位解析。
另一篇paper是做referring expression 的grounding的。利用语法解析，来提取句子中不同成分的层次结构，针对每个层次结构（node)都设计了相应的
neural module来实现对该node所对应的text 在image中的localization。
