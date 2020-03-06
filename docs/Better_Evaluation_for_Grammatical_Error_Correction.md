# Better Evaluation for Grammatical Error Correction
文法誤り訂正のシステム評価に広く利用されているMaxMatch(M2)を提案した論文。出力文と参照文の単純な単語の一致度ではなく、「適切な編集操作を行うことができているか」という点に関して評価する手法。


次のような手順で、「システムが行った編集(出力文)」が「人手で行った編集(参照文)」と最も一致するようにスコア計算を行う。

1.  2文間のlevenshtein matrix(Figure1)からedit lattice(Figure2)を構築。この時、gold-standardの編集に関しては、負の重みを付与する。これにより、最短経路探索時に、gold-standardと最も一致する編集操作を探索することが出来る。
2.  1.の最短経路をBellman-Ford algorithmにより求める 。

Note: edit latticeを構築する際には、過剰に長い系列を1つのedgeに割り当てないようにするため、1つのedgeに割り当てる変更しない単語数に制限を加える。下記の例では、2単語としている。

<p align="center">
<img width="400" src="https://user-images.githubusercontent.com/53220859/76045575-e0d9d600-5fa0-11ea-9449-7f5b9dafbaab.png">
<img width="700" src="https://user-images.githubusercontent.com/53220859/76045581-e505f380-5fa0-11ea-9d50-d3d92df38b06.png">
</p>



## 文献情報
- 著者: Daniel Dahlmeier, Hwee Tou Ng
- リンク: [https://www.aclweb.org/anthology/N12-1067/](https://www.aclweb.org/anthology/N12-1067/)
- 学会: NAACL2012
