# The AIP-Tohoku System at the BEA-2019 Shared Task

BEA-2019 におけるAIP-Tohoku systemを説明した論文。誤り訂正を行うTransformerと文レベルのエラー検出を行うモジュールを組み合わせたシステム。BEA2019において、Track1(Restricted Task)で9位、Track2(Unrestricted Task)で2位の結果を達成。

文レベルのエラー検出(SED: Sentence-level Error Detection)を行うモジュールでは、習熟度予測(PP: proficiency-level prediction)とのマルチタスク学習を行う。習熟度に応じたモデルでエラー検出を行うことで、より正しくエラーを検出できる。

<p align="center">
<img width="600" src="https://user-images.githubusercontent.com/53220859/76057839-075a3a00-5fbe-11ea-8588-bbfc5c6a1d4a.png">
</p>





## 文献情報

- 著者: Hiroki Asano, Masato Mita, Tomoya Mizumoto,  Jun Suzuki
- リンク: [https://www.aclweb.org/anthology/W19-4418/](https://www.aclweb.org/anthology/W19-4418/)
- 学会: The Fourteenth Workshop on Innovative Use of NLP for Building Educational Applications