# Improving Text-to-SQL Evaluation Methodology
Text-to-SQLの評価方法について調査した研究。従来の訓練・テストデータの分割方法は、自然言語文側に焦点を当てたものだった。この分割方法では、テストデータに訓練データと同様のSQL文が含まれてしまう。Text-to-SQLのタスクでは、一般的に自然言語文とSQL文は多対一の関係であるため、このような事例がたくさん発生してしまう。

そこで、本論文では、SQL文を基準に訓練・テストデータの分割を行う方法を提案している。具体的には、 SQL文の変数部分を以下のように適切なトークンに置き換え、テストデータに訓練データのSQL文が含まれないように分割を行う。

結果として、従来の分割方法では高性能を達成していたモデルにおいても、本手法で提案している方法で分割したデータでは難しいことが明らかとなった。


<p align="center">
<img width="400" src="https://user-images.githubusercontent.com/53220859/96333178-4fd4ec80-10a3-11eb-8781-0280578a73cb.png">
</p>


## 文献情報
- 著者: Catherine Finegan-Dollak, Jonathan K. Kummerfeld, Li Zhang, Karthik Ramanathan, Sesh Sadasivam, Rui Zhang, Dragomir Radev
- リンク: [https://www.aclweb.org/anthology/P18-1033/](https://www.aclweb.org/anthology/P18-1033/)
- 学会: ACL2018