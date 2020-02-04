# A Simple BERT-Based Approach for Lexical Simplification

BERTを利用した教師なし語彙平易化。下図のように、入力文と難解語をマスクした入力文を連結してBERTの入力とし、マスクトークン予測を利用して、換言候補を獲得する。得られた換言候補を(1) BERTの出力確率 (2) 言語モデル確率 (3) fasttextから得られた意味的類似度  (4) 単語の頻度 の4つの観点からランキングし、その順位の平均が最も高いものを用いて、文中の難解語を置き換える。結果として、既存の語彙平易化システムを上回る性能を達成。

<p align="center">
<img src="https://user-images.githubusercontent.com/53220859/73735596-dd291880-4782-11ea-90ba-412b21964de7.png" width=600>
</p>


## 文献情報

- 著者: Jipeng Qiang, Yun Li, Yi Zhu, Yunhao Yuan, Xindong Wu
- リンク: [https://arxiv.org/abs/1907.06226](https://arxiv.org/abs/1907.06226)
- 学会: arXiv