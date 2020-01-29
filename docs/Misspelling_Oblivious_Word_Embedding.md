# Misspelling Oblivious Word Embedding
スペルミスに耐性のある単語分散表現。スペルミス単語とそれに対応する正しい単語のベクトルが近づけるような項をFastTextの損失関数に導入する。内的評価(word similarity, word analogy, neighborhood similarity)・外的評価(POS tagging)の両方で、提案手法(MOE)の有効性を示した。 スペルミス単語と正しい単語のペアは、facebookの検索クエリログから収集する。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/72784758-d8397480-3c6c-11ea-9004-eb94f52ed9fe.png width=500pt>
</p>




## 文献情報
- 著者: Bora Edizel, Aleksandra Piktus, Piotr Bojanowski, Rui Ferreira, Edouard Grave, Fabrizio Silvestri
- リンク: [https://www.aclweb.org/anthology/N19-1326/](https://www.aclweb.org/anthology/N19-1326/)
- 学会: NAACL2019