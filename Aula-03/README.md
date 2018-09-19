# Verificação e Validação

## Defeitos de Software
Erro => Defeito => Falha  

* **Erro**
  * Algum engano feito durante o desenvolvimento do software por um ser humano, ou seja, escreveu o código errado ou fazendo algo que não deveria.
  * Errar é humano.
* **Defeito / Falta / Bug**
  * Consequência do erro, como alguém errou ao escrever o código o artefato ficou com defeito.
  * O defeito está no artefato.
* **Falha**
  * Consequência de ter defeito dentro do artefato, leva problemas ao executar o software. Quando alguém for testar o software, ele vai falhar.
  * Falha ocorre quando o software é executado.

Se você encontra uma falha durante o teste, então o software tem algum defeito.  
Se o software tem defeito, é porque alguém cometeu um erro no código.  

O oposto não é necessariamente verdade, você pode ter um erro e ele passar nos teste ou nunca se manifestar.

* **Vulnerabilidade**
  * É um defeito mas que só se manifesta em situações inesperadas ou particulares.

## Exemplo de Medidas para Confiabilidade e Manutenibilidade
* Mean Time Between Failures (MTBF) - **Confiabilidade**
  * Quanto tempo leva para o sistema falhar?
  * De quanto em quanto tempo ele falha?
* Mean Time To Recover (MTTRc) - **Confiabilidade**
  * Quanto tempo leva para o sistema se recuperar?
  * Já ocorreu alguma falha e foi solucionada, quanto tempo leva para botar o sistema funcionando de novo?
* Mean Time To Repair (MTTRp) - **Manutenibilidade**
  * Quanto tempo leva para corrigir o problema?
  * Você cadastra que tem um defeito e analisa o tempo que leva para corrigir
* Mean Time To Evolve (MTTEv) - **Manutenibilidade**
  * Quanto tempo para evoluir o sistema?
  * Solicitão uma alteração (ou querem adicionar algo novo), quanto tempo leva para evoluir o sistema?

## Taxonomia para defeitos
Podem ser usados para requisitos, projetos, códigos, ...

| Natureza do Defeito | Definição                                                              |
| ------------------- | ---------------------------------------------------------------------- |
| Omissão             | Informação necessária não incluída                                     |
| | Faltou inserir alguma informação no diagrama/requisito                                     |
| Ambiguidade         | Informação passível de ter múltiplas interpretações                    |
| | Alguma informação não está clara e poderia levar outra pessoa a fazer a coisa errada       |
| Iconsistência       | Informação conflitantes                                                |
| | Uma informação em um diagrama/requisito não está batendo com a de outro diagrama/requisito |
| Fato Incorreto      | Informação que não é verdade para as condições especificadas           |
| | A informação inserida no diagrama ou no requisito está incorreta                           |
| Informação Estranha | Informação desnecessária                                               |
| | Uma informação inútil foi acrescentada ao diagrama/requisito (mesmo que seja verdadeira)   |
