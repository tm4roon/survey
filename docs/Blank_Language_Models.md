# Blank Language Models
従来のleft-to-rightの言語モデルとは異なり、マスク単語予測とその単語の左右にマスクを挿入するかどうかの予測を繰り返すことで文生成を行うモデルを提案。

<p align="center">
<img src="https://user-images.githubusercontent.com/53220859/74651893-31db8300-51c8-11ea-9b04-ab01d0341b13.png" width=400>
</p>
<br>

具体的なモデルは下図に示す通り。(1)マスク位置の選択; (2)マスク単語の予測; (3) 次のマスク位置の生成; 全てのマスクが無くなるまで繰り返す。language modeling taskやsentiment transfer等、様々なタスクにおいて、従来の言語モデルを上回る性能を達成。

<p align="center">
<img src="https://user-images.githubusercontent.com/53220859/74651897-356f0a00-51c8-11ea-8f32-4726fafc6067.png" width=500>
</p>


## 文献情報
- 著者: Tianxiao Shen, Victor Quach, Regina Barzilay, Tommi Jaakkola
- リンク: [https://arxiv.org/abs/2002.03079](https://arxiv.org/abs/2002.03079)
- 学会: arXiv