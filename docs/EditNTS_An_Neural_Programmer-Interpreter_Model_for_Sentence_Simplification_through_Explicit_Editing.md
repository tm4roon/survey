# EditNTS: An Neural Programmer-Interpreter Model for Sentence Simplification through Explicit Editing
翻訳モデルを用いたテキスト平易化に加え、単語毎の平易化操作(KEEP, ADD, DELETE)の予測タスクを加えることで、モデルに平易化時を学習させる。平易化操作の教師ラベルを生成する際には、原文と平易文のLevenshtein distanceにより、KEEP, ADD, DELETEのいずれかのラベルを付与する。結果として、SoTAのモデルに比べ平易さの評価尺度であるSARIが向上。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/68023281-17010380-fcea-11e9-9fc3-fc408b02396e.png width=500pt>
</p>



## 文献情報
- 著者: Yue Dong, Zichao Li, Mehdi Rezagholizadeh, Jackie Chi Kit Cheung
- リンク: [https://arxiv.org/abs/1906.08104](https://arxiv.org/abs/1906.08104)
- 学会: ACL2019