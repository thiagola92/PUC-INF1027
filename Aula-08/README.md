# Técnicas de Teste

**Caixa Branca**: Tem acesso ao código  
**Caixa Preta**: Não tem acesso ao código (libraries)  

---

* **Classes de Equivalência**
  * **Classes válida**
    * As entradas dos testes que deveriam dar certo
  * **Classes inválida**
    * As entradas dos testes que deveriam dar errado

Exemplo, um sistema requer senha  

| Entrada                          | Classes válidas   | Classes inváldas |
| :------------------------------: | :---------------: | :--------------: |
| Tamanho t da senha               | 1 ≤ t ≤ 6         | t > 6 ou t = 0   |
| Primeiro caractere c é uma letra | Sim               | Não              |

## Particionamento por Equivalência
Dado os lados, dizer o tipo de triângulo

| Classe de Equivalência        | a   | b   | c   | Resultado Esperado |
| :---------------------------: | :-: | :-: | :-: | :----------------: |
| Um lado maior que dois juntos | 7   | 3   | 3   | Não é triângulo    |
| Um lado maior que dois juntos | 3   | 7   | 3   | Não é triângulo    |
| Um lado maior que dois juntos | 3   | 3   | 7   | Não é triângulo    |
| Tamanho iguais                | 3   | 3   | 3   | Equilátero         |
| Dois lados são iguais         | 3   | 4   | 4   | Isóceles           |
| Dois lados são iguais         | 4   | 4   | 3   | Isóceles           |
| Dois lados são iguais         | 4   | 3   | 4   | Isóceles           |
| Tamanho iguais                | 3   | 4   | 5   | Escaleno           |

## Análise do Valor Limite
Os problemas costumam ocorre nos limites das faixas de valores.
A idade para entrar pagando inteira é de 18 até 64, abaixo ou acima disso paga meia.  

```
|-------------------------------|
18                             64
```
Valor limite é justamente o valor que altera a reação  
18 paga inteira, 17 paga meia.  
64 paga inteira, 65 paga meia.  

| Idade | Resultado Esperado |
| :---: | :----------------: |
| 18    | Inteira            |
| 17    | Meia               |
| 64    | Inteira            |
| 65    | Meia               |

## Grafo Causa-Efeito
270
## Error Guessing
