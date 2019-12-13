# Self-Supervised Neural Machine Translation
NMTを対訳ペア抽出器として利用することにより、自己教師あり学習を行う手法を提案。具体的には、(1) 単語ベクトルの合計ベクトルとencoderの隠れ層の合計ベクトルを用いて、comparable corpusから対訳ペアを抽出 (2) 抽出した対訳ペアでNMTを学習。これを相互に繰り返すことにより、より高性能な翻訳器を構築する。  単語ベクトルには、pre-trianed cross-lingual word embeddingを利用。学習が進んでいくに連れて、対訳ペアが単語の一致する文から、より意味の複雑な文を抽出することができるようになった。  

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/70785151-64828d00-1dcd-11ea-96e3-e6b4f0190bb2.png width=500pt>
</p>

また、今回はあくまでcomparable corpusを利用しており、何からの対応関係があることが前提となっているデータを利用した実験設定になっている。そのため、monolingual corpusを利用した実験よりも有利な実験設定となっている。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/70785152-651b2380-1dcd-11ea-9d13-b624a7b175d2.png width=350pt>
</p>


## 文献情報
- 著者:Dana Ruiter, Cristina España-Bonet, Josef van Genabith
- リンク: [https://www.aclweb.org/anthology/P19-1178/](https://www.aclweb.org/anthology/P19-1178/)
- 学会: ACL2019