## 2.2.1
- a
  - S -> SS+S* -> Sa+S* -> aa+S* -> aa+a*
- c
  - 足し算と掛け算ができる後置記法の言語

## 2.2.2
- a
  - 0がx回、1がx回連続した数を表す
- b
  - 足し算と引き算ができる前置記法
- c
  - () と空の記号列を含む任意の組み合わせの式を作る
- d
  - 同じ数のa、bと空の記号列を含む
- e
  - 正規言語を表す正規表現   

## 2.2.4

- a
  - S -> S S + | S S - | S S * | S S /| num
- b
  - S -> S, id | id
- c
  - S -> id, S | id
- d
  - expr -> expr + term | expr - term | term
    term -> term * factor | term / factor | factor
    factor -> id | digit | (expr)


## 2.3.1
expr -> {print('+')} expr1 + term | {print('-')} expr1 - term | term
term -> {print('\*')} term1 \* factor | {print('/')} term1 / factor | factor
factor -> digit {print('digit')}| (expr)

## 2.3.2
expr ->
  expr {print('+')} expr +
  | expr {print('-')} expr -
  | {print('(')} expr {print(')\*(')} expr {print(')')} \*
  | {print('(')} expr {print(')/(')} expr {print(')')} /
  | digit {print('digit')}
