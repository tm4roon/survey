# Reducing Transformer Depth on Demand with Structured Dropout
Transformerのレイヤ自体をDropoutさせる方法LayerDropを提案。学習時には確率*p*でDropoutさせる。推論時には、レイヤ<a href="https://www.codecogs.com/eqnedit.php?latex=d&space;\equiv&space;0&space;(\lfloor{mod(1/p)\rfloor})" target="_blank"><img src="https://latex.codecogs.com/gif.latex?d&space;\equiv&space;0&space;(\lfloor{mod(1/p)\rfloor})" title="d \equiv 0 (\lfloor{mod(1/p)\rfloor})" /></a>でdropoutさせる。機械翻訳や要約, 言語モデル等のタスクにおいて、モデルを軽量化しつつ、性能を改善できることを示した。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/68070432-8261d880-fdb1-11e9-893f-d35a6da6f422.png width=500pt>
</p>

## 文献情報
- 著者: Angela Fan, Edouard Grave, Armand Joulin
- リンク: [https://arxiv.org/abs/1909.11556](https://arxiv.org/abs/1909.11556)
- 学会: arXiv