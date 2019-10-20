# Learning Simplifications for Specific Target Audiences

テキスト平易化において、対象となる読者に合わせて平易さ度合いを制御できるようにすることを試みた研究。平易さの度合いを制御するために、入力文頭に、「どのくらいのレベルに平易化したいか」と「その操作」をラベルとして加える。平易レベルとして、Flesch-Kincaid Grade Level scoreを利用している。また、操作のラベルとしては、次の4つを利用している。

- **<identical\> **:何も変換を行わない ( 入力文と平易文が一致)。
- **\<elaboration\>**: 入力文1文を平易文1文に変換する。
- **\<one-to-many>**: 文分割を行う。
- **\<many-to-one\>**: 文融合を行う。



<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/67136241-885aa400-f25e-11e9-9b26-33172c6510e0.png width=800pt>
</p>

また、Zero-shot text simplificationにも対応できることを示した。





## 文献情報

- 著者: Carolina Scarton, Lucia Specia
- リンク: [https://www.aclweb.org/anthology/P18-2113/](https://www.aclweb.org/anthology/P18-2113/)
- 学会: ACL2018



