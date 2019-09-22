# Hint-Based Training for Non-Autoregressive Machine Translation

翻訳には、翻訳文の単語を順次出力するAutoregressive translation(ART)と並列に出力するNon-Autoregressive translation(NART)がある。NARTは、推論時の計算時間がARTに比べて短いが、過去の出力情報をうまく参照することができず、翻訳品質が低い傾向にあった。そこで、ART modelのhidden states及びattention distributionとの差を損失関数に加えることによって、NARTのhidden satesやattention distributionをARTに近づけるような学習を行う。結果として、LSTM-based ARTを上回る性能を達成した。

![Hint-Based_Training](https://user-images.githubusercontent.com/53220859/65387781-97485680-dd85-11e9-8729-483697e27de6.png)







## 文献情報

- 著者: Zhuohan Li, Zi Lin, Di He, Fei Tian, Tao Qin, Liwei Wang, Tie-Yan Liu
- リンク: [https://arxiv.org/abs/1909.06708](https://arxiv.org/abs/1909.06708)

