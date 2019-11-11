# Retrofitting Contextualized Word Embeddings with Paraphrases
ELMo等をはじめとする文脈を考慮した単語埋め込みモデルでは、表層が同じ単語であっても異なった単語のベクトルを出力する。このようなモデルでは、文脈が言い換えられた場合に、同等な意味であっても、ベクトル表現としては大きく異なってしまう場合がある。ここでは、言い換え認識や含意関係認識のデータを用いて、同等な意味を持つ文脈の場合にベクトル表現が近づくように、単語埋め込みモデルを調整する。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/68568207-57a50d80-049e-11ea-8fe4-6b4e815a26fb.png width=400pt>
</p>


## 文献情報
- 著者: Weijia Shi, Muhao Chen, Pei Zhou, and Kai-Wei Chang
- リンク: [https://www.aclweb.org/anthology/D19-1113.pdf](https://www.aclweb.org/anthology/D19-1113.pdf)
- 学会: EMNLP-IJCNLP2019