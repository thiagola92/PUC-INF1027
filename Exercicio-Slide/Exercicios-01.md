# 1

## Classe Equivalência

| Classes Eq.    | Válidas                                                                                 | Inválidas                 |
| ---            | ---                                                                                     | ---                       |
| Dia            | 1 ≤ dia ≤ 31                                                                            | dia < 1 ou dia > 31       |
| Mês            | 1 ≤ mês ≤ 12                                                                            | mês < 1 ou mês > 12       |
| Ano            | 1812 ≤ ano ≤ 2025                                                                       | ano < 1812 ou ano > 2025  |
| Mês c/ 31 dias | V1 = `{dia = 31 e mês = 1,3,5,7,8,10,12}`<br/>V2 = `{dia < 31 e mês = 1,3,5,7,8,10,12}` | X                         |
| Mês c/ 30 dias | V3 = `{dia = 30 e mês = 4,6,9,11}`<br/>V4 = `{dia < 30 e mês = 4,6,9,11}`               | I1 = `{dia = 31 e mês = 4,6,9,11}` |
| Fev Ñ Bissexto | V5 = `{dia = 28 e mês = 2}`<br/>V6 = `{dia < 28 e mês = 2}`                             | I2 = `{dia > 28 e mês = 2}`        |
| Fev Bissexto   | V7 = `{dia = 29 e mês = 2}`<br/>V8 = `{dia < 29 e mês = 2}`                             | I3 = `{dia > 29 e mês = 2}`        |

V1,V3,V5,V7 = Mês vira  
V2,V4,V6,V8 = Mês não vira   

## Casos de Teste

| Data       | Resultado     |     |
| ---        | ---           | --- |
| 0/06/2000  | Dia inválido  |     |
| 32/06/2000 | Dia inválido  |     |
| 15/0/2000  | Mês inválido  |     |
| 15/13/2000 | Mês inválido  |     |
| 15/06/1811 | Ano inválido  |     |
| 15/06/2026 | Ano inválido  |     |
| 31/01/2000 | 01/02/2000    | V1  |
| 31/03/2000 | 01/04/2000    | V1  |
| ...        | ...           | V1  |
| 30/01/2000 | 31/01/2000    | V2  |
| 30/03/2000 | 31/03/2000    | V2  |
| ...        | ...           | V2  |
| 30/04/2000 | 01/05/2000    | V3  |
| 30/06/2000 | 01/07/2000    | V3  |
| ...        | ...           | V3  |
| 29/04/2000 | 30/04/2000    | V4  |
| 29/06/2000 | 30/06/2000    | V4  |
| ...        | ...           | V4  |
| 31/04/2000 | Data Inválida | I1  |
| 31/06/2000 | Data Inválida | I1  |
| ...        | ...           | I1  |
| 28/02/1999 | 30/03/2000    | V5  |
| 27/02/1999 | 30/03/2000    | V6  |
| 29/02/1999 | Data Inválida | I2  |
| 29/02/1999 | 01/03/2000    | V7  |
| 28/02/1999 | 29/03/2000    | V8  |
| 29/02/1999 | Data Inválida | I3  |

# 2

## Classe Equivalência

| Classes Eq.   | Válidas                                                                                                               | Inválidas                         |
| -----------   | -------                                                                                                               | ---------                         |
| #Ap           | 1 ≤ ap ≤ 500                                                                                                          | ap < 1 ou ap > 500                |
| #Inq.         | 1 ≤ inq ≤ 9                                                                                                           | inq < 1 ou inq > 9                |
| Limite        | 1 ≤ lim ≤ 100000                                                                                                      | lim < 1 ou lim > 100000           |
| Ap 1 a 100    | V1 = `{1 ≤ ap ≤ 100 e 1 ≤ inq ≤ 2}`                                                                                   | I1 = `{1 ≤ ap ≤ 100 e inq > 2}`   |
| Ap 101 a 300  | V2 = `{101 ≤ ap ≤ 300 e inq ≤ 3}`<br/>V3 = `{101 ≤ ap ≤ 300 e 4 ≤ inq ≤ 6}`                                           | I2 = `{101 ≤ ap ≤ 300 e inq ≥ 7}` |
| Ap 301 a 500  | V4 = `{301 ≤ ap ≤ 500 e inq ≤ 3}`<br/>V5 = `{301 ≤ ap ≤ 500 e 4 ≤ inq ≤ 6}`<br/>V6 = `{301 ≤ ap ≤ 500 e 7 ≤ inq ≤ 9}` | X                                 |
| Limite        | V7 = `{1 ≤ lim < 5000}`<br/>V8 = `{5000 ≤ lim ≤ 10000}`<br/>V9 = `{lim > 10000}`                                      | X                                 |

## Casos de Teste

| # Ap | # Inq | Limite | Custo Mensal | Frequência | |
| --- | --- | --- | --- | --- | --- |
| 0 | 2 | 5000 | Ap Inválido | | |
| 501 | 2 | 5000 | Ap Inválido | | |
| 200 | 0 | 5000 | Inq Inválido | | |
| 200 | 10 | 5000 | Inq Inválido | | |
| 200 | 2 | 0.99 | Limite Inválido | | |
| 200 | 2 | 100000.01 | Limite Inválido | | |
| 100 | 2 | 4999.99 | 200 | Mensal | V1 & V7 |
| 100 | 3 | 5000 | Inq Inválido | | I1 |
| 300 | 3 | 5000 | 450 | Bimensal | v2 & v8 |
| 300 | 4 | 10000.01 | 450 | Semetral | v3 & v9 |
| 300 | 7 | 5000 | Inq Inválido | | I2 |
| 500 | 3 | 5000 | 600 | Bimensal | V4 |
| 500 | 4 | 5000 | 600 | Bimensal | V4 |
| 500 | 7 | 5000 | 700 | Bimensal | V6 |
