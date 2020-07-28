# Model-Agnostic Meta-Learning for Fast Adaptation of Deep Networks

Meta-learningとは、学習方法を学習するアルゴリズムの一種。「**少しのデータ・学習ステップの後、すぐに新しいタスクに適応できるモデル**」を学習するこを目標としている。本論文で提案しているModel-Agnostic Meta-Learning (MAML)では、様々なタスクTからデータをサンプリングし、モデルを学習する。そののちに、学習したパラメータと評価データを利用してモデルの初期パラメータを更新する。これを繰り返すことにより、「**少しの勾配法の学習ステップで、損失関数に関して大きく性能を改善できるようなモデルのパラメータ**」を探索する。MAMLの特徴としては、モデルの構造やタスク(分類, 回帰, 強化学習, ...)に依らず適用でき、汎用性の高い方法である点が挙げられる。


<p align="center">
  <img width=700 src=https://user-images.githubusercontent.com/53220859/88549552-6565e780-d05b-11ea-9ff7-2a61822e9c0c.png>
</p>


本論文では、様々なタスクで有効性を検証しており、下図からも事前学習よりも速く学習が収束し、なおかつ高い性能を実現していることが分かる。

<p align="center">
<img width="300" src="https://user-images.githubusercontent.com/53220859/88668971-4419ff80-d11e-11ea-83db-e4996f67e936.png">
<br>
<img width="700" src="https://user-images.githubusercontent.com/53220859/88668982-48deb380-d11e-11ea-8e25-6c89f63e3ca7.png">
</p>






## 文献情報

- 著者: Chelsea Finn, Pieter Abbeel, Sergey Levine
- リンク: [https://arxiv.org/abs/1703.03400](https://arxiv.org/abs/1703.03400)
- 学会: ICML2017



## 参考文献

- [[論文解説] MAML: Model-Agnostic Meta-Learning for Fast Adaptation of Deep Networks](https://qiita.com/ku2482/items/ee2fd87bbb5353664f59)
- [メタ学習：学習の仕方を学習する、MAMLやNeural Process](https://xtech.nikkei.com/atcl/nxt/mag/rob/18/00007/00009/)
- [From zero to research — An introduction to Meta-learning](https://medium.com/huggingface/from-zero-to-research-an-introduction-to-meta-learning-8e16e677f78a)
- [メタ学習（meta-learning）の紹介：Regression版で今年の東京の気温を当ててみました～](https://recruit.gmo.jp/engineer/jisedai/blog/meta-learning/)