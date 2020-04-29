# Injecting Numerical Reasoning Skills into Language Models

言語モデルに論理展開能力(e.g. 四則演算など)を導入する方法を提案している論文。本論文では、モデルの構造を変更することなく四則演算を行う事前学習方法を提案している。すなわち、事前学習済みのBERTを用いることが可能となる。

<p align="center">
<img width="500" src="https://user-images.githubusercontent.com/53220859/79069846-5f4a3600-7d0c-11ea-8731-a4b3fb6059c4.png">
</p>

提案手法はQueryやPassageから特定の範囲を抜き出すのか(Extractive)、具体的な計算が必要なのか(Generative)を判定しつつ、解答文を生成するモデルである。また、事前学習には自動生成したNumerical Data(ND)とテンプレートベースで生成したTextual Data(TD)を利用する。結果として、文書読解タスクの性能を損なうことなく、論理展開能力を導入できた。







## 文献情報

- 著者: Mor Geva, Ankit Gupta, Jonathan Berant
- リンク: [https://arxiv.org/abs/2004.04487](https://arxiv.org/abs/2004.04487)
- 学会: ACL2020