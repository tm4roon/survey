# Soft Contextual Data Augmentation for Neural Machine Translation

ニューラル機械翻訳(NMT)におけるdata augmentationの手法を提案。言語モデルの出力分布をNMTの入力として利用する。NMTへの入力は基本的にone-hot表現の入力であるが、ここでは、確率的に言語モデルの出力分布を入力する。データが少ない場合、多い場合どちらにおいても、提案手法により性能を改善することが可能。

![sca](https://user-images.githubusercontent.com/53220859/63646654-1e87b780-c751-11e9-9978-e28d8fdd3fc1.png)

<br>



## 文献情報

- 著者: Fei Gao, Jinhua Zhu, Lijun Wu, Yingce Xia, Tao Qin, Xueqi Cheng, Wengang Zhou, and Tie-Yan Liu
- リンク: [https://www.aclweb.org/anthology/P19-1555](https://www.aclweb.org/anthology/P19-1555)