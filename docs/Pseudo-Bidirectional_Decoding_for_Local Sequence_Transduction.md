# Pseudo-Bidirectional Decoding for Local Sequence Transduction

Local sequence transduction task (i.e. 文法誤り訂正, スペル訂正, OCR訂正などをはじめとする、入力文をほとんど書き換えないようなタスク)において、タスクの特性を利用したBiredirectional decodingを提案。

具体的には、decodeの際に入力文の情報をコピーすることにより、擬似的に未来の情報へのアクセスを可能とする。提案手法により、計算コストを抑えつつbidirectional-decodingを可能にし、文法誤り訂正・スペルミス訂正・OCR訂正の3つのタスクにおいて性能を改善できることを示した。

<p align="center">
<img src="https://user-images.githubusercontent.com/53220859/73628902-e471f880-4694-11ea-8aef-a16bda9e223d.png" width=700pt>
</p>


## 文献情報

- 著者: Wangchunshu Zhou, Tao Ge, Ke Xu
- リンク: [https://arxiv.org/abs/2001.11694](https://arxiv.org/abs/2001.11694)
- 学会: arXiv