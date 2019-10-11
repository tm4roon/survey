# Contextual String Embeddings for Sequence Labeling
文字レベルを入力とした言語モデルから単語ベクトルを獲得する手法を提案。双方向のLSTMに文字レベルで入力。forward, backwardそれぞれLSTMから単語の末尾, 先頭の隠れ状態を獲得し、結合する。これを単語のベクトルとみなす。CoNLL2003 shared taskでstate-of-the-artを達成。また、文字レベルで入力することから、rare wordやmisspell wordなどにも対応可能。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/63939039-3ccb1b80-caa1-11e9-906b-4dffbd8ca478.png width=500pt>
</p>

## 文献情報
- 著者: Alan Akbik, Duncan Blythe and Roland Vollgraf
- リンク: [https://www.aclweb.org/anthology/C18-1139](https://www.aclweb.org/anthology/C18-1139)
- 学会: COLING2018

