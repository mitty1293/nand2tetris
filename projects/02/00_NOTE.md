# Project 02
## HalfAdder
真理値表を眺めると以下の法則があることがわかる。
* sum = a Xor b
* carry = a And b

|   a   |   b   |  sum  | carry |
|---|---|---|---|
|   0   |   0   |   0   |   0   |
|   0   |   1   |   1   |   0   |
|   1   |   0   |   1   |   0   |
|   1   |   1   |   0   |   1   |

## FullAdder
なにか書く

## Add16
なにか書く

## Inc16
* 0と1をfalseとtrueで表す。
* 16bitの配列をbit単位でなくそのまま扱う。

## ALU
* コードの上から順に理解すればわかりやすい。
* フラグによって出力を選択したいとき（≒if）はMux（マルチプレクサ）を用いると良い。
* 多ビットバスの出力を複数に分けて、一部分のみ利用することができる。

例：
```
Mux16(a=outf, b=notoutf, sel=no, out=out, out[0..7]=outlow, out[8..15]=outhigh, out[15]=ng);
```