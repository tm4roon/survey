# Neural Machine Translation of Rare Words with Subword Units

ニューラル機械翻訳で低頻度語や未知語に対応するため、単語より細かい分割単位(Sub-word)によるtokenize手法を提案。具体的には[Byte-Pair-Encoding (BPE)]([https://ja.wikipedia.org/wiki/%E3%83%90%E3%82%A4%E3%83%88%E5%AF%BE%E7%AC%A6%E5%8F%B7%E5%8C%96](https://ja.wikipedia.org/wiki/バイト対符号化))を用いてtokenizeする。BPEの概略は次の通りである: (1) 文字レベルの分割で頻度をカウントし、それを初期辞書とする。(2) bigramを取り、頻度が高いものを連結し、一つのトークンとみなす。(3) (2)の処理を目的の語彙サイズになるまで繰り返す。BPEを用いたtokenizeにより、WMT 15において、BLEUが1.1 pt (En → Ge)、1.3 pt (En → Ru)向上。 



![wordpiece](https://user-images.githubusercontent.com/53220859/63146805-2a7bc700-c037-11e9-9b26-61228d81d1bc.png)



※ 図は元論文から引用。



## 文献情報

- 著者: Rico Sennrich and Barry Haddow and Alexandra Birch
- リンク: [https://arxiv.org/abs/1508.07909](https://arxiv.org/abs/1508.07909)