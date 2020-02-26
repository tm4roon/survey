# Fine-Tuning Pretrained Language Models: Weight Initializations, Data Orders, and Early Stopping

BERTのfine-tuning時のハイパーパラメータの影響について調査した研究。ランダム性を有する、「classification layerのweight initialization」と「学習データの順序」に着目して大規模な実験を行なっている。結果として、2つのランダム要素の組み合わせによって、モデルの性能が大きく変化することを示した。また、いくつかのタスクに共通して性能が高くなる組み合わせが一定数存在することを明らかにした。どのような傾向があるのかは今後の課題としている。
<p align="center">
<img width="600" src="https://user-images.githubusercontent.com/53220859/75315109-18f85f00-58a5-11ea-95f0-cae5541f4352.png">
</p>


## 文献情報

- 著者: Jesse Dodge, Gabriel Ilharco, Roy Schwartz, Ali Farhadi, Hannaneh Hajishirzi, Noah Smith
- リンク: [https://arxiv.org/abs/2002.06305](https://arxiv.org/abs/2002.06305)
- 学会: arXiv