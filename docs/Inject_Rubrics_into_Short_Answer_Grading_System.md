# Inject Rubrics into Short Answer Grading System

Short Answer Grading Task(解答の自動採点タスク)において、Rubric(採点基準?)の情報を導入する機構を提案。解答とRubricのword-level attentionを取る機構により、教師データが少ない場合でも高い性能を達成できる。教師データが増えれば増えるほど、本稿で提案しているRubric componentの貢献は小さくなる。

<p align="center">
<img width="300" src="https://user-images.githubusercontent.com/53220859/76291665-e90f7980-62f0-11ea-8e2b-0703fd023d34.png">
<img width="600" src="https://user-images.githubusercontent.com/53220859/76291644-ddbc4e00-62f0-11ea-99e2-9d00a3d05da8.png">
</p>









## 文献情報
- 著者: Tianqi Wang, Naoya Inoue, Hiroki Ouchi, Tomoya Mizumoto, Kentaro Inui
- リンク: [https://www.aclweb.org/anthology/D19-6119/](https://www.aclweb.org/anthology/D19-6119/)
- 学会: Proceedings of the 2nd Workshop on Deep Learning Approaches for Low-Resource NLP (DeepLo)