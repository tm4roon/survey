# LightGBM: A Highly Efficient Gradient Boosting Decision Tree

XGBoostをベースに、Gradient-based One-Side Sampling (GOSS)とExclusive Feature Bundling (EFB)を加え、性能を落とさずに計算を高速化した研究。



一般的に、決定木学習の計算量はO(#data × #features)である。そこで、#dataを減らす工夫としてGOSS、#featuresを減らす工夫としてEFBを提案している。

- **GOSS**: 勾配の小さいサンプルの一定数を無視する。
- **EFB**: 非ゼロ要素が重ならない特徴量を1つの特徴量としてまとめ上げる。





## 文献情報

- 著者: Guolin Ke, Qi Meng, Thomas Finley, Taifeng Wang, Wei Chen, Weidong Ma, Qiwei Ye, Tie-Yan Liu
- リンク: [https://papers.nips.cc/paper/6907-lightgbm-a-highly-efficient-gradient-boosting-decision-tree.pdf](https://papers.nips.cc/paper/6907-lightgbm-a-highly-efficient-gradient-boosting-decision-tree.pdf)
- 学会: NIPS2017