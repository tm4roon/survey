# Improving Grammatical Error Correction via Pre-Training a Copy-Augmented Architecture with Unlabeled Data

文法誤り訂正に関する研究。文中の間違った部分と正しい文を分類タスク・生成タスクのMulti-task learningを行う。文法誤り訂正タスクでは多くの場合、誤り文と訂正文の間で単語が一致する。そのため、Copy mechanismを導入している。また、コピーを学習させるために、事前学習としてノイズ除去タスクを行い、性能を改善している。

![copy-arch](https://user-images.githubusercontent.com/53220859/65815104-b9c6ed80-e225-11e9-8c64-6cc87898be8f.png)



## 文献情報

- 著者: Wei Zhao, Liang Wang, Kewei Shen, Ruoyu Jia, Jingming Liu
- リンク: [https://arxiv.org/abs/1903.00138](https://arxiv.org/abs/1903.00138)

