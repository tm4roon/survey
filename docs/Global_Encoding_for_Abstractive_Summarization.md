# Global Encoding for Abstractive Summarization

Attention-based seq2seq modelのencoder側を拡張。RNNの上にConvolution Gated UnitとSelf-attention layerを被せることで、n-gramレベルの局所的な特徴と文を跨ぐような長期的な特徴を捉えることによって、性能を改善。また、重複したn-gramを生成してしまう問題を軽減。

<br>



## 文献情報

- 著者: Junyang Lin, Xu Sun, Shuming Ma, and Qi Su
- リンク: [https://www.aclweb.org/anthology/P18-2027](https://www.aclweb.org/anthology/P18-2027)