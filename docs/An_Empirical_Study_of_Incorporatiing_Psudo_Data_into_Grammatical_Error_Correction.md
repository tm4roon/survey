# An Empirical Study of Incorporatiing Psudo Data into Grammatical Error Correction

文法誤り訂正のタスクにおいて、擬似データ拡張手法について調査した研究。特に次の3つの点に注目して調査を行なっている。(i) データ拡張手法による違い: BACKTRANS(逆翻訳)かDIRECT NOISE(単語の追加・挿入・削除・マスク) (ii) 事前学習するデータによる違い: SimpleWiki, Wiki, Gigaword (iii) 学習方法による違い: JOINT (擬似データ+学習データを同時に学習), PRETRAIN(擬似データを学習後に、学習データでfine-tuning)。結果として、Gigwaword corpus + BACKTRANS pre-training が最も効果的であることがわかった。また、CONLL2014やJFLEG, BEAのタスクにおいて、モデル自体に改良を加えることなく性能を改善した。





## 文献情報

- 著者: Shun Kiyono, Jun Suzuki, Masato Mita, Tomoya Mizumoto, Kentaro Inui
- リンク: [https://arxiv.org/abs/1909.00502](https://arxiv.org/abs/1909.00502)









