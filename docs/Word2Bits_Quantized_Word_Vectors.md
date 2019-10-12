# Word2Bits: Quantized Word Vectors
word2vecを8~16倍軽量化しつつ、高精度を実現する手法word2bitsを提案。word2vecの損失関数に量子化関数Qを追加することで、各要素が32bitsで表現されているベクトルを、1, 2bitsに落とし込む。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/64063612-72067380-cc31-11e9-917a-7cece2e916d9.png width=700pt>
</p>

1, 2bitsの量子化関数は以下のように定義する。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/64063621-89456100-cc31-11e9-8486-1cd5dde327d9.png width=300pt>
</p>

## 文献情報
- 著者: Maximilian Lam
- リンク: [https://arxiv.org/pdf/1803.05651.pdf](https://arxiv.org/pdf/1803.05651.pdf)
- 学会: arXiv2018
