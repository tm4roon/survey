# Understanding Back-Translation at Scale

逆翻訳により擬似的にデータを生成する際に、beam search + noise (単語の削除, マスク, 並び替え)を行うことにより、WMT2014 En-GeでBLEU 35ptを達成。(データセットが少ない場合はノイズは加えない方が良い。)

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/66712196-f2dd9100-edd3-11e9-892c-60a4ef9e7847.png width=600pt>
</p>





## 文献情報

- 著者: Sergey Edunov, Myle Ott, Michael Auli, David Grangier
- リンク: [https://arxiv.org/abs/1808.09381](https://arxiv.org/abs/1808.09381)
- 学会: EMNLP2018