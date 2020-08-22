# Active learning for deep semantic parsing

能動学習(active learning)を活用し、Semantic parsingで利用するデータの効率的な拡張方法を提案した論文。従来の能動学習では、小規模データにより学習したforward model(自然言語→形式表現)を用いて、新たにラベル付けすべきデータの順位付けを行っていた。しかし、形式表現から自然言語文を生成するデータ構築手法(overnight)では従来の順位付けはできない。そこで、overnightにも適用可能な手法を提案し、能動学習を行った。結果、ランダムなデータ選択と比べ、性能改善に寄与するデータを効率的に選択できることを示した。また、ATIS datasetにおいては元データの半量程度で最高性能を達成できることを示した。

<p align="center">
<img width="600" src="https://user-images.githubusercontent.com/53220859/90779477-d76add00-e338-11ea-9da5-c33de3c69655.png">
</p>

## 文献情報
著者: Long Duong, Hadi Afshar, Dominique Estival, Glen Pink, Philip Cohen, Mark Johnson
リンク: [https://www.aclweb.org/anthology/P18-2008/](https://www.aclweb.org/anthology/P18-2008/)
学会: ACL2018

