# Utilizing BERT for Aspect-Based Sentiment Analysis via Constructing Auxiliary Sentence
 Aspect-Based Sentiment Analysis(ABSA)を含意関係認識や質問応答と同様のタスクとして捉えることにより、性能を大きく改善した、という内容の研究。ABSAとは、その名の通り、ある観点に基づいた感情分析タスクで、文単位の感情分析よりも細かい単位での感情分析である。具体的な例を以下に示す。

<p align="center">
<img width=300 src=https://user-images.githubusercontent.com/53220859/85190096-d6451180-b2ef-11ea-8add-87c662359ebc.png>
</p>

ここでは、ABSAを(sentence, aspect)のペアからそのsentimentを予測するタスクとして定義している。ABSAを質問応答や含意関係認識のタスクと同様な方法で解くために、以下の4つの方法により擬似入力文生成を行い、それぞれの結果を比較している。

- **QA-M**: (LOCATION1, safety) → "what do you think of the safety of LOCATION?"
- **NLI-M**: (LOCATION1, safety) → "LOCATION1 - safety"
- **QA-B**: (LOCATION1, safety) → "the polarity of the aspect safety of LOCATION1 is {positive, negative, none}" (yes/no questionに)
- **NLI-B**: (LOCATION1, safety) → "LOCATION1 - safety - {positive, negative, none}" (yes/no questionに)

これらの文を分析対象の文と結合して、BERTの入力とする。

<p align="center">
<img width=700 src="https://user-images.githubusercontent.com/53220859/85190094-d2b18a80-b2ef-11ea-9df6-ed915ad031d7.png">
</p>




## 文献情報
- 著者: Chi Sun, Luyao Huang, Xipeng Qiu
- リンク: [https://www.aclweb.org/anthology/N19-1035/](https://www.aclweb.org/anthology/N19-1035/)
- 学会: NAACL2019
- コード: [https://github.com/HSLCY/ABSA-BERT-pair](https://github.com/HSLCY/ABSA-BERT-pair)