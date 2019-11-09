# Global Optimization under Length Constraint for Neural Text Summarization
要約文生成では、実用上、出力文長に制約がある場合が多い。従来の出力文長制御における研究では、ユーザが指定した文長を超えた出力となる事例が多かった。ここでは、ROUGEを直接最適化するMinimum risk trainingに、指定文長を上回ったことによるペナルティを設けることにより、要約の品質を落とさず、出力文長による制約を与えることを目指している。結果として、従来の手法に比べて、高い品質かつ指定した文長以内に要約文を収めることが可能となった。


## 文献情報
- 著者: Takuya Makino, Tomoya Iwakura, Hiroya Takamura, Manabu Okumura
- リンク: 
  - [https://www.aclweb.org/anthology/P19-1099/](https://www.aclweb.org/anthology/P19-1099/)
  - [https://www.anlp.jp/proceedings/annual_meeting/2018/pdf_dir/A3-6.pdf](https://www.anlp.jp/proceedings/annual_meeting/2018/pdf_dir/A3-6.pdf)
- 学会: ACL2019