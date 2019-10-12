# RoBERTa: A Robustly Optimized BERT Pretraining Approach

BERTの学習方法について詳細に調査した研究。

- 学習データサイズやバッチサイズは、大きくすればするほど良い。
- 学習は時間をかければかけるほど良い。
- Next Sentence Prediction (NSP)は行わない方が良い。
- マスク単語予測は動的に行った方が良い。
<br>


BERTに以下の変更を加えたものを、ここではRoBERTaと呼んでいる。

- Dynamic masking: マスク単語を学習のたびに変更する。
- FULL-SENTENCES without NSP loss: 文書中で隣接する文を結合して入力する(指定の文長となるまで複数の文を結合する)。
- Large mini-batches: 論文中では、バッチサイズを8Kに設定。
- Larger byte-level BPE: 論文中では、語彙サイズを30Kに設定。
<br>



GLUE, RACE, SQuADでstate-of-the-artを達成。
<br>


## 文献情報

- 著者: Yinhan Liu, Myle Ott, Naman Goyal, Jingfei Du, Mandar Joshi, Danqi Chen, Omer Levy, Mike Lewis, Luke Zettlemoyer, Veselin Stoyanov
- リンク: [https://arxiv.org/abs/1907.11692](https://arxiv.org/abs/1907.11692)
