**Funcional**:  
Até agora foram visto técnicas **caixa preta**, ou seja, não ligavamos para o que acontecia dentro do software ou como foi implementado, apenas se o resultado estava correto.  

**Estrutural**:  
Agora nós vamos estudar técnicas **caixa branca**, nós veremos como o código foi escrito.  

Para seu teste ser de alta qualidade você precisa misturar as duas técnicas de modo a maximizar os benefícios.  

# Grafo de Programa

**Nó**: Uma sequência de códigos que não tem bifurcação, ou seja, não tem como tomar outro fluxo de comandos  
**Arco**: O caminho existente de um nó para outro nó  
**Caminho**: ???  
**Fluxo de Controle**: ???  

![Exemplo de grafo](exemplo.jpg)  

## Sintaxe

![Sintaxe de grafo](exemplos.jpg)  

## Teste de Instruções  
A idéia é você testar todos os **nós** pelo menos uma vez, para isso você pode precisar rodar o programa mais que uma vez  

![Exemplo de grafo](exemplo2.jpg)  

Pegando todos os nós:  
* 1,2,3,6  
* 1,2,3,5,3,4,8  

Tabela:  

| nós | predicados | dados |
| --- | ---------- | ----- |
| {1,2,3,6} | ∀y, y < 0 | y = -10 |
| {1,2,3,5,3,4,8} | ∀y, y ≥ 0 | y = 10 |


## Arndt
A sintaxe ensinada pelo Arndt envolve utiliza  
Circulo: bloco sequencial  
Hexagono: Mudança de classe/função  
Retângulo: Inicio ou fim do escopo analisado  

Exemplo de um trabalho que tive que fazer em outra matéria:  
![Arndt](exemploArndt.jpg)

Estou falando isso pois não sei que sintaxe o professor vai cobrar já que ele mostra a sintaxe do Arndt e aquela anterior que são apenas circulos.    

### Exemplos
![Exemplo simples](simple.jpg)  

![Exemplo if else](ifelse.jpg)  

![Exemplo while for](whilefor.jpg)  

![Exemplo do while](dowhile.jpg)  

## Teste de Decisões
A idéia é você testar todos os **arcos/arestas/ramos** pelo menos uma vez, para isso você pode precisar rodar o programa mais que uma vez  
Eu não consegui ver muita diferença de usar esse e o *teste de instruções*  

![Exemplo de grafo](exemplo2.jpg)  

Pegando todos os arcos:  
* <1,2>, <2,3>, <3,6>  
* <1,2>, <2,3>, <3,5>, <5,3>, <3,4>, <4,8>  

Tabela:  

| nós | predicados | dados |
| --- | ---------- | ----- |
| {<1,2>, <2,3>, <3,6>} | ∀y, y < 0 | y = -10 |
| {<1,2>, <2,3>, <3,5>, <5,3>, <3,4>, <4,8>} | ∀y, y ≥ 0 | y = 10 |

### Restruturando código
A idéia não é realmente restruturar o código, apenas tentar ver ela de forma que facilite a analise das arestas. Um código pode ter várias avaliações na mesma linha, o que pode acabar nos levando a não testar todas possíveis arestas.   

Quando uma condição é muito grande, podemos querer abreviar, por exemplo:   
Vamos chamar `a >= 0 && a <= 200` de **C**.  

```java
if (a >= 0 && a <= 200) {
  m = 1
} else {
  m = 3
}
```


![Exemplo de and](andexample.jpg)  

Como isso dificulta a nossa analise das condições no grafo, podemos **tentar** restruturar o código de forma a mostrar as condições separadas.  

```java
if (a >= 0) {
  if (a <= 200) {
    m = 1
  } else {
    m = 3
  }
} else {
  m = 3
}
```

![Exemplo de and 2](andexample2.jpg)  

Conseguimos ver todas condições no grafo, mas o código está se tornando ilegível.  
Outra maneira de restruturar o código seria trocando && por ||, ou seja, trocar and por or.  

```java
if (a < 0 || a > 200) {
  m = 3
} else {
  m = 1
}
```

![Exemplo de and que pode ser usado para or ](andexample.jpg)  

Voltamos para o caso anterior, mas agora restruturar pode acabar sendo melhor  

```java
if (a < 0) {
  m = 3
} else if (a > 200) {
  m = 3
} else {
  m = 1
}
```

![Exemplo de or](orexample.jpg)  

Infelizmente acabamos com repetição de código, como você pode ver pelo `m = 3`.  
Lado positivo é que conseguimos avaliar todas as arestas.  

## Teste de Caminhos
Eu não entendi a diferença desse teste para os outros 2.  
Você quer percorrer todos os caminhos possíveis pelo menos uma vez (acho que os outros também eram assim).  

### Teste de Caminhos Básicos
Em vez de procurar todos os caminhos, você procura todos os caminhos independentes.  
Caminho independente: contém pelo menos 1 nova aresta do grafo de controle  
(não é como se antes eu ficasse pegando caminhos inúteis e que eu já percorri...)  

Existe formulas para saber quantos caminhos independentes podemos ter no máximo (se passar desses valores, você repetiu algum percurso):  
* Nós predicados + 1
* Regiões + 1
* Arestas - nós + 2

Vamos pegar um exemplo anterior qualquer e utilizar as 3 maneiras    

Nós predicados + 1  
Em outras palavras, nós que tem bifurcações + 1  
![Nós predicados](nospredicados.jpg)  
2 + 1 = 3  

Regiões + 1  
Como pode ver, eu pintei todos as áreas fechadas  
![Regiões](regioes.jpg)  
2 + 1 = 3  

Arestas - nós + 2  
Conta as arestas  
![Arestas](arestas.jpg)  
Conta os nós  
![Nós](nos.jpg)  
7 - 6 + 2 = 3  

### Teste de Laços
39:29
