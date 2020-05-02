# Conversational Word Embedding for Retrieval-Based Dialog System 

対話応答タスクにおいて、<post, replay>のペアを相互関係を捉えた単語埋め込みを提案した論文。具体的には、はじめに統計的機械翻訳を用いて<post・replay>間の単語アライメントを取ったのちに、単語埋め込みの学習を行う。その後、CNNベースの分類モデルによりpost文とreplay文の関係性を捉える学習を行う。結果として、既存の単語埋め込みに比べて大きく性能を改善した。

<p align="center">
<img width="800" src="https://user-images.githubusercontent.com/53220859/80865617-9c7b6580-8cc5-11ea-8569-a3e0a7259812.png">
</p>



## 文献情報

- 著者: Wentao Ma, Yiming Cui, Ting Liu, Dong Wang, Shijin Wang, Guoping Hu
- リンク: [https://arxiv.org/abs/2004.13249](https://arxiv.org/abs/2004.13249)
- 学会: ACL2020