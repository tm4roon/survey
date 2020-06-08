# A Unified MRC Framework for Named Entity Recognition

1つの単語に対して複数のタグが紐づく可能性を考慮した固有表現抽出 (Nested NER)に取り組んでいる。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/82971197-183ea880-a00d-11ea-8b65-47c6a0509597.png width=500>
</p>


固有表現抽出は系列ラベリング問題として捉えられ様々なモデルが提案されてきたが、今回取り組むNested NERへの適用は難しい。過去には、パイプライン処理(一番外側のタグから順に内側へ向かって固有表現抽出する方法, その逆も然り)などが提案されていたが、前段の誤差が後段へと伝搬していってしまうため好ましくない。

ここでは、 事前学習したBERTを効率的に利用するため、固有表現抽出を文書読解タスクとして捉えるといったアイデアを提案している。文書読解とは、<query, answer, passage>のトリプレットで与えられるタスクである。具体的には、入力されたquery文の内容に該当する部分をpassageから切り抜き回答する、というタスクである。

今回は、固有表現抽出を<“Find facilities in the text, including buildings, airports, ...“, span, “input sentence ... “>のようなタスクに変換してモデルを学習させる。
具体的なBERTへの入力は、“[CLS] クエリ文 [SEP] パッセージ“とし、始点の二値分類と終点の二値分類、始点と終点のマッチングの3つの問題を解かせる形式で学習させる。
結果として、Flat NER, Nested NER両方でかなり高いスコアを達成。


## 文献情報
著者: Xiaoya Li, Jingrong Feng, Yuxian Meng, Qinghong Han, Fei Wu and Jiwei Li
リンク: [https://arxiv.org/abs/1910.11476](https://arxiv.org/abs/1910.11476)
学会: ACL2020
ソースコード: [https://github.com/ShannonAI/mrc-for-flat-nested-ner](https://github.com/ShannonAI/mrc-for-flat-nested-ner)