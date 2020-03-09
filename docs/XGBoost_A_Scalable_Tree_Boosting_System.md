# XGBoost: A Scalable Tree Boosting System

勾配ブースティング木(GBDT: Gradient Boosting Decision Tree)をベースとしたアルゴリズム(ツール)。

<p align="center">
<img width="400" src="https://user-images.githubusercontent.com/53220859/76211169-f2dda200-6248-11ea-9de5-94f429b98c29.png">
</p>

分類タスク時も回帰木を利用し、予測値を予測確率として算出する。過学習を抑制するために、目的関数における正則化項に加えて、shrinkageやsubsamplingを行っている。

- **Shrinkage**: GBDTでは(t-1)ステップまでの決定木の誤差を埋めるように、tステップの木を学習する。この時、その誤差を一気に埋めに行かないように学習率をかけて抑制すること。
- **Subsampling**: 決定木を構築する際に使用する特徴量やデータをサンプリングする (ランダムフォレストと同じ)。



また、計算時間を抑えるために分割点探索時には、Approximate algorithmを利用する (分割候補点をパーセンタイルで取る)。大規模なデータを利用する場合には、このパーセンタイルを求めるのに時間が掛かってしまうため、Weighted Quantile Sketchにより高速化を行っている。

<p align="center">
<img width="400" src="https://user-images.githubusercontent.com/53220859/76211101-cfb2f280-6248-11ea-8e77-9c3648d4263a.png">
</p>

さらに、欠損値やスパースなデータにも対応できるように、Sparsity-aware Split Findingを行っている。欠損データを右寄せと左寄せの両方を試し、最適な分割を探索する。

<p align="center">
<img width="400" src="https://user-images.githubusercontent.com/53220859/76211263-2d473f00-6249-11ea-8dbb-6532f55c0810.png">
</p>


## 文献情報

- 著者: Tianqi Chen, Carlos Guestrin
- リンク: [https://arxiv.org/abs/1603.02754](https://arxiv.org/abs/1603.02754)
- 学会: KDD2016

