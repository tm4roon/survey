# Neural Architectures for Nested NER through Linearization

エンティティが入れ子になった固有表現抽出 (Nested NER)に取り組んでいる。入力・出力は以下のようなフォーマットでsequence-to-sequence modelの学習を行う。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/82971748-686a3a80-a00e-11ea-9232-26b935096cde.png width=300>
</p>

embedding layerに事前学習済みのELMo, BERT, Flairなどを組み合わせて与えることでパワーアップさせている。 結果として、seq2seqだけでもLSTM-CRF + Flairに匹敵するくらいの性能を出せる。seq2seq + BERT + Flairがベスト。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/82971758-6b652b00-a00e-11ea-80bf-cbf6baf6d0a6.png width=500>
</p>

## 文献情報
- 著者: Jana Strakova ́ and Milan Straka and Jan Hajicˇ
- リンク: https://www.aclweb.org/anthology/P19-1527/
- 学会: ACL2019

