# Soft Contextual Data Augmentation for Neural Machine Translation

ニューラル機械翻訳(NMT)におけるdata augmentationの手法を提案。言語モデルの出力分布をNMTの入力として利用する。NMTへの入力は基本的にone-hot表現の入力であるが、ここでは、確率的に言語モデルの出力分布を入力する。データが少ない場合、多い場合どちらにおいても、提案手法により性能を改善することが可能。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/63646654-1e87b780-c751-11e9-9978-e28d8fdd3fc1.png width=400pt>
</p>

## 文献情報
- 著者: Fei Gao, Jinhua Zhu, Lijun Wu, Yingce Xia, Tao Qin, Xueqi Cheng, Wengang Zhou, and Tie-Yan Liu
- リンク: [https://arxiv.org/abs/1905.10523](https://arxiv.org/abs/1905.10523)
- 学会: ACL2019
