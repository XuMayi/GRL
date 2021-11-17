# Graph Representation Learning


### 一、图数据结构
很多数据都是图结构，例如社交网络、经济网络、生物医学网络、信息网络（互联网网站、学术引用）、互联网、神经网络。而网络是它们的通用语言，因此具备极大的研究价值。
<img src='https://upload-images.jianshu.io/upload_images/8194602-e53724dc08cd2bd5.png?imageMogr2/auto-orient/strip|imageView2/2/w/1068' width = '800'>

图表示学习目标：将节点映射为向量表示的时候尽可能多地保留图的拓扑信息。
即用n个vectors表示图上的n个nodes。 
<img src='https://upload-images.jianshu.io/upload_images/8194602-53e142a781ab4132.png?imageMogr2/auto-orient/strip|imageView2/2/w/1057' width ='600'>

区别于词向量表示（e.g.，**[Word2Vec （学习笔记）](./Word2Vec.ipynb)**）,词向量表示的任务是将单词转换为包含语义的vectors，而图表示学习的目的是将图网络的节点表示为向量，图表示学习所涵盖的范围更广泛,
e.g.，drug-drug network，drug-disease network，protein-protein network, electronic network.

图表示学习类型：  
1）基于图结构的表示学习：对结点的向量表示只来源于图的拓扑结构，缺乏对图结点特征消息的表示。

2）基于图特征的表示学习：对结点的向量表示既包含了图的拓扑信息也包含了已有的特征向量。

### 二、应用场景
* 节点分类 ——预测一个给定节点的类型
* 链接预测 ——预测两个节点是否连接
* 社群检测 ——识别密集连接的节点群
* 网络相似度 ——两个子网络有多相似

### 二、基于图结构的表示学习模型

|   Model   | Paper   | Note     |Source Code |Train Script |
| :-------: | :------------ | :------------: | :-----------------: |:-----------------: |
| DeepWalk  | [KDD 2014][DeepWalk: Online Learning of Social Representations](http://www.perozzi.net/publications/14_kdd_deepwalk.pdf)   | [DeepWalk：学习笔记](./Deepwalk.ipynb)  | [deepwalk.py](./code/deepwalk.py) | [run_deepwalk.py](./code/run_deepwalk.py) |
|   LINE    | [WWW 2015][LINE: Large-scale Information Network Embedding](https://arxiv.org/pdf/1503.03578.pdf)                          | [LINE：学习笔记](./LINE.ipynb)      | [line.py](./code/line.py) |[run_line.py](./code/run_line.py) |
| Node2Vec  | [KDD 2016][node2vec: Scalable Feature Learning for Networks](https://www.kdd.org/kdd2016/papers/files/rfp0218-groverA.pdf) | [Node2Vec：学习笔记](./Node2Vec.ipynb)  | [node2vec.py](./code/node2vec.py)| [run_node2vec.py](./code/run_node2vec.py) |
|   SDNE    | [KDD 2016][Structural Deep Network Embedding](https://www.kdd.org/kdd2016/papers/files/rfp0191-wangAemb.pdf)               |  | |
| Struc2Vec | [KDD 2017][struc2vec: Learning Node Representations from Structural Identity](https://arxiv.org/pdf/1704.03165.pdf)        |  | |

### 三、基于图特征的表示学习模型

|   Model   | Paper   | Note     |Source Code |Train Script |
| :-------: | :------------ | :------------: | :-----------------: |:-----------------: |
| GCN  | [ICLR 2017][semi-supervised classification with graph convolutional networks](https://arxiv.org/pdf/1609.02907.pdf)   |  |  |  |
|   GraphSAGE    | [NeurIPS 2017][Inductive representation learning on large graphs](https://proceedings.neurips.cc/paper/2017/file/5dd9db5e033da9c6fb5ba83c7a7ebea9-Paper.pdf)                          |    |  | |
| GAT  | [ICLR 2018][Graph Attention Networks](https://arxiv.org/pdf/1710.10903.pdf) | | | |


### 三、一些高效的工具包
1、[PyG](https://github.com/pyg-team/pytorch_geometric#installation) 

<img src="https://raw.githubusercontent.com/pyg-team/pytorch_geometric/master/docs/source/_static/img/pyg1.svg?sanitize=true" width="200">

2、[DGL](https://github.com/dmlc/dgl)

<img src="https://camo.githubusercontent.com/c8e685c644c3fb27c874af87a405d53c382d0de61d8edde0fd0d9aac2a4345d8/687474703a2f2f646174612e64676c2e61692f61737365742f6c6f676f2e6a7067" width="200">

### 四、学习资料

[1] [Standford CS224W  
Machine Learning with Graphs  
Insturctor: Prof. Jure Leskovec](http://web.stanford.edu/class/cs224w/)

[2] [Representation Learning for Natural Language Processing   
Chapter 8: Network Representation  
Authors: Zhiyuan Liu, Yankai Lin, Maosong Sun   
Springer, July 2020](https://link.springer.com/content/pdf/10.1007%2F978-981-15-5573-2_8.pdf)

[3] [Hamilton W L. Graph representation learning[J]. Synthesis Lectures on Artifical Intelligence and Machine Learning, 2020, 14(3): 1-159.](https://www.morganclaypool.com/doi/abs/10.2200/S01045ED1V01Y202009AIM046)

[4] [A Gentle Introduction to Graph Neural Networks, Google Research](https://distill.pub/2021/gnn-intro/)
