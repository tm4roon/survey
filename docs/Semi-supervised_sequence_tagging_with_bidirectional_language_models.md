# Semi-supervised sequence tagging with bidirectional language models

事前学習済みの双方向ニューラル言語モデルの出力をSequence tagging taskのモデルの学習に組み込むことによって性能改善を試みた研究。CoNLL2003のNER taskとCoNLL2000のCunking taskにおいて提案手法の有用性を示した。また、事前学習済みモデルの重みをどこに組み込むのか、どの事前学習モデル(CNN, RNN)が後段のsequence tagging taskに有効か、などの調査を行っている。結果として、ForwardにCNN, BackwardにLSTMを用いた事前学習済みモデルの出力を、2層目のLSTMの出力と結合するのがベストという結果。

<p align="center">
<img width="500" src="https://user-images.githubusercontent.com/53220859/77245203-2a444980-6c60-11ea-93e6-b2df1d2233d7.png">
<img width="500" src="https://user-images.githubusercontent.com/53220859/77245204-2b757680-6c60-11ea-9adf-b21c2b45048e.png">
</p>






## 文献情報

- 著者: Matthew Peters, Waleed Ammar, Chandra Bhagavatula, Russell Power
- リンク: [https://www.aclweb.org/anthology/P17-1161/](https://www.aclweb.org/anthology/P17-1161/)
- 学会: ACL2017