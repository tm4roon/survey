# Lambda Dependency-Based Compositional Semantics

意味論的構文解析(Semantic Parsing)において、新たな形式表現(Lambda-DCS: Lambda Dependency-Based Compositional Semantics)を提案した論文。従来用いられていたラムダ式(Lambda calculus)に比べ、より簡潔に書くことができる。

以下に、Lambda calculusとLambda-DCSの比較を示す。

|                        |                 Utterance                 |                       Lambda calculus                        |                   Lambda-DCS                    |
| ---------------------- | :---------------------------------------: | :----------------------------------------------------------: | :---------------------------------------------: |
| Unary base case        |                     -                     |                       λx.[x = Seattle]                       |                     Seattle                     |
| Binary base case       |                     -                     |                   λx.λy.PlaceOfBirth(x, y)                   |                  PlaceOfBirth                   |
| Join                   |          people born in Seattle           |                 λx.PlaceOfBirth(x, Seattle)                  |              PlaceOfBirth.Seattle               |
| Join                   |  those who had children born in Seattle   |       λx.∃y.Children(x, y) ∧ PlaceOfBirth(y, Seattle)        |          Children.PlaceOfBirth.Seattle          |
| Intersection           |        scientists born in Seattle         |    λx.Profession(x, Scientist) ∧ PlaceOfBirth(x, Seattle)    |   Profession.Scientist ⊓ PlaceOfBirth.Seattle   |
| Union                  | Oregon, Washington and Canadian provinces | λx.[x = Oregon] ∨ [x = Washington] ∨ Type(x, CanadianProvince). |   Oregon ⊔ Washington ⊔ Type.CanadianProvince   |
| Negation               |      states not bordering California      |         λx.Type(x, USState) ∧ ¬Border(x, California)         |        Type.USState ⊓ ¬Border.California        |
| Higher-order functions |           the number of states            |                  count(λx.Type(x, USState))                  |               count(Type.USState)               |
| Higher-order functions |     the number largest state by area      |        argmax(λx.Type(x, USState), λx.λy.Area(x, y))         |           argmax(Type.USState, Area)            |
| Lambda abstraction     | those who had a child who influenced them |            λx.∃y.Children(x, y).Influenced(y, x)             |            µx.Children.Influenced.x             |
| Lambda abstraction     |     person who has the most children      |   argmax(λx.Type(x, Person), λx.count(λz.Children(x, z)))    | argmax(Type.Person, R[λx.count(R[Children].x])) |

 





## 文献情報

- 著者: Percy Liang 
- リンク: [https://arxiv.org/abs/1309.4408](https://arxiv.org/abs/1309.4408)
- 学会: arXiv2013