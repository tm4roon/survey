# Deep Active Learning for Named Entity Recognition
固有表現抽出タスクにおいて、様々なアクティブラーニング手法の効果を検証した論文。出力確率の最も高いトークンの確率を利用してスコアリングするLeast Confidence (LC)を発展させたMaximum Normalized Log Probability (MNLP)や、Dropoutしたままモデルに推論させ、正解を出力できた回数を利用するBayesian Active Learning by Disagreement (BALD)などを利用。 結果として、アクティブラーニングを利用することで、20~30%程度のアノテーション量でBest Modelと同等程度の性能が達成できることを示した。


<p align="center">
<img width="450" src="https://user-images.githubusercontent.com/53220859/100515924-428f3f80-31c3-11eb-803f-e309d2831d61.png">
 </p>


 <p align="center">
<img width="700" src="https://user-images.githubusercontent.com/53220859/100515929-46bb5d00-31c3-11eb-8db4-21ff423d38fc.png">
 </p>


## 文献情報
- 著者: Yanyao Shen, Hyokun Yun, Zachary Lipton, Yakov Kronrod, Animashree Anandkumar
- リンク: [https://www.aclweb.org/anthology/W17-2630/](https://www.aclweb.org/anthology/W17-2630/)
- 学会: Proceedings of the 2nd Workshop on Representation Learning for NLP
- 解説ブログ: [アクティブラーニングを使って固有表現のアノテーション数を25%にする](https://hironsan.hatenablog.com/entry/deep-active-learning-for-named-entity-recognition)

