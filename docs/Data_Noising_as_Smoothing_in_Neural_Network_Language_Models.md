# Data Noising as Smoothing in Neural Network Language Models

言語モデルを学習させる際に、擬似的に学習データを増やすことで性能向上をはかる試み。データ拡張の方法として、次の2つの手法を提案: (1) 確率γで文中のtokenをplaceholder token "_"に置き換える。 (2) 確率γで文中のtokenを確率分布q(x) (e.g. unigram頻度分布)からサンプリングされたtokenに置き換える。

<img src=https://user-images.githubusercontent.com/53220859/65744850-abe56f80-e134-11e9-8bc8-fe0798fced66.png width=700pt>



結果として、bigram Kneser-Ney noisingにより、データ拡張なしの手法に比べ、perplexityを大幅に改善。また、翻訳タスクに利用した際にも、BLEUを1.4pt改善。

![bigramkn](https://user-images.githubusercontent.com/53220859/65744849-abe56f80-e134-11e9-88bb-a5f5d90ad2e3.png)



## 文献情報

- 著者: Ziang Xie, Sida I. Wang, Jiwei Li, Daniel Levy, Aiming Nie, Dan Jurafsky, Andrew Y. Ng
- リンク: [https://arxiv.org/abs/1703.02573](https://arxiv.org/abs/1703.02573)





