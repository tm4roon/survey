# Controlling Text Complexity in Neural Machine Translation
翻訳する過程において、出力文の難易度を制御することを試みた研究。Newselaのデータ(1文に対して想定読者の学年を付与している)を用いて、英語-スペイン語間の翻訳を行う。Table1にコーパスの例を示す。出力制御を行うために、出力文の難易度を入力文の先頭にラベルとして付与するといった手法を採用。また、翻訳タスクと平易化タスクのマルチタスク学習を行うことで、さらに性能が改善される。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/68448146-e2c79e80-0225-11ea-8fc5-83ced41e87b5.png width=500pt>
</p>



## 文献情報

- 著者: Sweta Agrawal, Marine Carpuat
- リンク: [https://arxiv.org/abs/1911.00835](https://arxiv.org/abs/1911.00835)
- 学会: EMNLP-ICJNLP2019