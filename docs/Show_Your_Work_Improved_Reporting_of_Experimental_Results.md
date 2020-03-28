# Show Your Work: Improved Reporting of Experimental Results

自然言語処理タスクにおけるモデルの評価は、事前に分割されたテストデータを用いて行われているが、手法の良し悪しの判断を行うにあたって、テストデータに対するスコアだけでは不十分であると主張している (計算環境によって結論は変わりうる、と述べている)。

ここでは、新たな評価方法 Expected validation performanceを提案している。具体的には、ハイパーパラメータの探索回数n回の条件下で、ベストなvalidation スコアを与えるパラメータ設定のモデルにおけるvalidationスコア分布Vn*の期待値を求める。

<p align="center">
<img src="https://user-images.githubusercontent.com/53220859/77619999-c336d580-6f7c-11ea-86e1-e37a0937b620.png" width=400>
<img src="https://user-images.githubusercontent.com/53220859/77620025-d21d8800-6f7c-11ea-8533-2a7324acaaf1.png" width=250>
</p>


これによって、計算環境に応じて実験の結論が変わりうることを示した。

<p align="center">
<img width="400" src="https://user-images.githubusercontent.com/53220859/77619986-ba460400-6f7c-11ea-920d-1da419457ad5.png">
</p>




## 文献情報

- 著者: Jesse Dodge, Suchin Gururangan, Dallas Card, Roy Schwartz, Noah A. Smith
- リンク: [https://www.aclweb.org/anthology/D19-1224](https://www.aclweb.org/anthology/D19-1224)
- 学会: EMNLP2019