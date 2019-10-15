# Neural Text Generation with Unlikelihood Training

Neural text generationで頻繁に発生する、同じ単語を繰り返し出力してしまう問題や高頻度な単語を過剰に出力してしまう問題に対して、望まない出力に関する損失(**unlikelihood**)を追加すること提案。これにより、人手評価において有意に性能を改善。unlikelihoodとして、token-levelとsentence-levelの2つを定義している。


### token-level unlikelihood objective
過去に出力した単語に対してペナルティを与える。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/66375664-e5499500-e9e8-11e9-9603-707f5ce58b1f.png width=700pt>
</p>


### sentence-level unlikelihood objective
繰り返すn-gramに対してペナルティを与える。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/66375665-e5499500-e9e8-11e9-9575-582c7eca155d.png width=700pt>
</p>


## 文献情報
- 著者: Sean Welleck, Ilia Kulikov, Stephen Roller, Emily Dinan
- リンク: [https://arxiv.org/abs/1908.04319](https://arxiv.org/abs/1908.04319)
- 学会: arXiv
