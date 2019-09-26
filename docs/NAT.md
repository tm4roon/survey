# Non-Autoregressive Neural Machine Translation

単語を順次出力させるのではなく、並列して出力させることにより推論時の計算時間を削減した翻訳モデルを提案。WMT 2016のRomanian→EnglishではBLEU 29.8でstate-of-the-artを達成。



## Architecture

<p algin=center>

<img src=https://user-images.githubusercontent.com/53220859/65657993-de259d00-e060-11e9-8b73-582abd69f54e.png>

</p>



### Encoder stack

transfomerと同様のencoder。



### Decoder stack

**Decoder inputs**: 以下の2つを入力とする。

- **Copy source inputs uniformly**: Round(T't/T)でsource inputsをコピーする。
- **Copy source inputs using fertilities**: 上図にあるように、encoderの出力でどの単語を何回連続でコピーするかを予測させる。

**Positional attention**: Encoderのpositional embeddingをquery及びkey、decoderのpositional embeddingをvalueとしたattention。



## 文献情報

- 著者: Jiatao Gu, James Bradbury, Caiming Xiong, Victor O.K. Li,  Richard Socher
- リンク: [https://arxiv.org/abs/1711.02281](https://arxiv.org/abs/1711.02281)



