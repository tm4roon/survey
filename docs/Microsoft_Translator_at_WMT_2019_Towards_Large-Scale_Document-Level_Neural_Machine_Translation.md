# Microsoft Translator at WMT 2019: Towards Large-Scale Document-Level Neural Machine Translation

WMT19において、Microsoftが提出したシステムの説明。文書単位の翻訳により、高い性能を実現。encoderを強化するためのBERTによるmulti-task learningやback-translationによる擬似的なデータ拡張により性能を改善している。また、dual encoderを用いて、文単位の翻訳文と文書を入力することにより、post-editingと翻訳を同時に学習することにより、さらに性能を改善した。

文書を入力とする際には、文書の先頭に\<BEG\>, 文書の末尾に\<END\>、文間に\<SEP\>を挿入する。また、入力文書の上限は1,000 sub-wordsとし、その時点で文書が終了していない場合は、\<BRK\>を挿入し、次の入力で、\<CNT\>トークンを先頭に挿入する。これにより、長い文書であったとしても、ある程度の文脈の情報を考慮した翻訳が可能となる。

<p align="center">
  <img src=https://user-images.githubusercontent.com/53220859/69400653-cc493900-0d35-11ea-9052-d61fd581143b.png width=800pt>
</p>



## 文献情報

- 著者: Marcin Junczys-Dowmunt 
- リンク: [https://www.aclweb.org/anthology/W19-5321/](https://www.aclweb.org/anthology/W19-5321/)
- 学会: WMT2019