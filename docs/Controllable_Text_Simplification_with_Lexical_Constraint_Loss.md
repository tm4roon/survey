# Controllable Text Simplification with Lexical Constraint Loss

テキスト平易化において、出力語彙の語彙的な制約を設けることにより、平易さの度合いを制御しようとした研究。平易さ度合いを表すラベルを入力文頭に付与するほか、損失関数***L'***の計算時に、各平易さ度合い***l***に対応する平易語***w***を効果的に学習するための重み付けを行なっている。TFIDF, PPMIの2つの方法によって重み付けを行なっている。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/67136355-2bf88400-f260-11e9-8d77-a325eafc7166.png width=300pt>
<br>
<img src=https://user-images.githubusercontent.com/53220859/67136356-2bf88400-f260-11e9-82d2-e7f55de2339d.png width=250pt>
</p>

### TFIDF

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/67136354-2bf88400-f260-11e9-91d0-15cc7bc3b19c.png width=350pt>
</p>

### PPMI

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/67136353-2b5fed80-f260-11e9-844a-6ff6b441a7d0.png width=250pt>
<br>
<img src=https://user-images.githubusercontent.com/53220859/67136352-2b5fed80-f260-11e9-8c6f-4ba839434277.png width=350pt>
</P>



##結果

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/67136485-bbeafd80-f261-11e9-9441-b7bd0479bf61.png width=500pt>
<br>
<br>
<img src=https://user-images.githubusercontent.com/53220859/67136484-bbeafd80-f261-11e9-8bfe-e176579cf293.png width=500pt>
</p>





## 文献情報

- 著者: Daiki Nishihara, Tomoyuki Kajiwara, Yuki Arase
- リンク: [https://www.aclweb.org/anthology/P19-2036/](https://www.aclweb.org/anthology/P19-2036/)
- 学会: ACL2019

