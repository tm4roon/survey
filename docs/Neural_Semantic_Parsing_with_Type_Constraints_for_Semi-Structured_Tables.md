# Neural Semantic Parsing with Type Constraints for Semi-Structured Tables

近年のSemantic ParsingではSequence-to-Sequence modelをベースとしたモデルが利用されているが、これは自然言語文と形式表現のペアから変換規則を学習しているだけなので、明示的に文法規則を導入している訳ではない. そのため、対象としているテーブルの構造上実現し得ない形式表現も生成されてしまう恐れがある. 本研究では、「文法規則の予測(エンティティ部分は空欄)」「空欄のエンティティを埋める」の2つを繰り返しながらデコードすることで、より適切な形式表現を生成することを試みた. また、対象テーブルそのものをグラフ埋め込みを通して入力情報として利用したり、Question-Answeringのデータセットを学習データとして利用する枠組みを作ることにより性能改善を目指した. 結果として、WikiTableQuestions datasetでSOTAを達成.

[![img](https://user-images.githubusercontent.com/53220859/92985666-ca807a00-f4ef-11ea-9fb7-d492f8f2cc33.png)](https://user-images.githubusercontent.com/53220859/92985666-ca807a00-f4ef-11ea-9fb7-d492f8f2cc33.png)

[![img](https://user-images.githubusercontent.com/53220859/92985669-cce2d400-f4ef-11ea-9d46-3c4dd0e35396.png)](https://user-images.githubusercontent.com/53220859/92985669-cce2d400-f4ef-11ea-9d46-3c4dd0e35396.png)

## 文献情報

- 著者: Jayant Krishnamurthy, Pradeep Dasigi, and Matt Gardner
- リンク: https://www.aclweb.org/anthology/D17-1160/
- 学会: EMNLP2017
- 発表スライド: https://nlp.stanford.edu/seminar/details/jkrishnamurthy.pdf