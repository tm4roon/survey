# CatBoost: unbiased boosting with categorical features

GBDTに潜む2つの*Target leakage* (予測時に利用できない情報を学習に利用してしまうこと)の可能性についての対策を提案。

図は[Anna Veronika Dorogush - CatBoost - the new generation of Gradient Boosting](https://www.youtube.com/watch?v=oGRIGdsz7bM&list=PL5kFsL5kpnhrw3Gc9mfL7yY7uhpSATKxX)から引用。
<br>

### Target leakageの可能性

- **カテゴリカルデータの前処理 (Target encoding)**: Target encodingとは、目的変数の情報を用いてカテゴリカル変数を数値に変換する方法。例えば、カテゴリ変数の各水準における目的変数の平均値などを利用する。このとき、単純にデータ全体から平均をとってしまうと、自身のレコードの目的変数をカテゴリカル変数に含んでしまうため、Target leakageが起こってしまう。
- **Boosting Algorithm**: 前段の木の予測結果に基づいて、次の木を構築するこという流れで学習することから、木を構築する際に学習データにおける目的変数の情報を入力に与えてしまっている(?)。
<br>

### 対策方法

対策方法の基本的なアイデアはどちらも共通で、データに順番を与えて過去のデータのみを参照すること。

1. まず、乱数を発生させて各データに順番を与える。すなわち、データに時系列性を付与する。
2. **Ordered Target Statistics**: ある時点のデータをTarget Encodingする際にはそれよりも過去のデータのみを参照する。
   **Orderd Boosting**:ある時点までのデータを学習に利用する際にはそれよりも過去のデータのみを参照する。

<p align="center">
<img width="400" src="https://user-images.githubusercontent.com/53220859/76826855-d224d600-6860-11ea-89ab-eb7bc29696e7.png">
<img width="400" src="https://user-images.githubusercontent.com/53220859/76828913-58431b80-6865-11ea-88de-a9ffe9732abc.png">
</p>

<br>



### その他
その他、CatBoostには以下のような特徴がある。
- **Symmetric Decision Tree**: 各深さの分岐の条件式が全て同じ決定木。過学習抑制や推論の高速化などの効果がある。
- **Feature Combinations**: 適切なカテゴリカル変数の組み合わせを貪欲法により探索。

<p align="center">
<img width="400" src="https://user-images.githubusercontent.com/53220859/76826698-7f4b1e80-6860-11ea-8aa0-a79fb2db45e2.png">
</p>

<br>

## 文献情報
- 著者: Liudmila Prokhorenkova, Gleb Gusev, Aleksandr Vorobev, Anna Veronika Dorogush, Andrey Gulin
- リンク: [https://papers.nips.cc/paper/7898-catboost-unbiased-boosting-with-categorical-features.pdf](https://papers.nips.cc/paper/7898-catboost-unbiased-boosting-with-categorical-features.pdf)
- 学会: NeurIPS2018
<br>



## 解説記事
- [『CatBoost: unbiased boosting with categorical features』at NeurIPS2018読み会](https://speakerdeck.com/tomoto/catboost-unbiased-boosting-with-categorical-features-at-neurips2018du-mihui)
- [Anna Veronika Dorogush - CatBoost - the new generation of Gradient Boosting](https://www.youtube.com/watch?v=oGRIGdsz7bM&list=PL5kFsL5kpnhrw3Gc9mfL7yY7uhpSATKxX)

- https://www.youtube.com/watch?v=oGRIGdsz7bM&list=PL5kFsL5kpnhrw3Gc9mfL7yY7uhpSATKxX)