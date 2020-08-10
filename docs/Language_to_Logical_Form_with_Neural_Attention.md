# Language to Logical Form with Neural Attention

自然言語文を入力とし、その文の意図を木構造に変換する意味解析タスクに取り組んでいる。先行研究では、変換ルールの構築などを必要としていたため、モデル構築のコストが高かった。本研究では、SEQ2SEQを拡張したSEQ2TREEという、木構造を出力することに適したデコード手法を提案している。Semantic parsingにおける4種類のデータセットでSEQ2SEQを上回る性能を達成。また、固有名詞や数値表現を対応するラベル(type_i)への置き換え(Argument Identification)も組み込んでおり、学習データが少ない場合に、性能向上に大きく貢献するという結果が得られている。


<p align="center">
<img width="700" src="https://user-images.githubusercontent.com/53220859/89789950-40de3500-db5c-11ea-8c9d-6e09ca8b8b33.png">
</p>


## 文献情報

- 著者: Li Dong, Mirella Lapata
- リンク: [https://www.aclweb.org/anthology/P16-1004/](https://www.aclweb.org/anthology/P16-1004/)
- 学会: ACL2016
- コード: [https://github.com/donglixp/lang2logic](https://github.com/donglixp/lang2logic)

