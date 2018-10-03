# Conceitos e Definições

**Teste**: Executar o software com o objetivo de revelar falhas  
**Depuração**: Analisar o software de parte em parte em busca do defeito, ou seja, uma vez que você sabe que tem falha no sistema, você procura a origem dela.  
**Caso de Teste**: Uma situação a ser testada. Valores são usados como *entrada* e gera um *resultado*.  
**Procedimento/Roteiro de Teste**: Descreve passo a passo o que se deve fazer para poder começar a testar.  
**Critérios de Cobertura dos Testes**: Quantas partes do software que precisam ser testadas.  
**Rodada/Bateria de Teste**: Cada vez que você testa tudo que deveria antes de apresentar ao cliente, você testou uma rodada. Se o cliente recusar, você precisa fazer outra rodada de testes.    
**Incidentes de Teste**: Algo inesperado aconteceu durante os testes, então pode ser uma falha e precisa ser analisada.  

## Fases de Teste
* **Unidade** - Desenvolvedor  
* **Integração** - Desenvolvedor  
  * Top-down  
  * Bottom-up
* **Sistema** - Testador  (ou Desenvolvedor faz pensando como Usuário)  
  * Funcional
  * Não-Funcional
    * Recuperação
      * Tenta fazer o sistema falhar pra ver o quão bem ele se recupera
    * Segurança
      * Tenta quebrar/invadir o sistema
    * Stress
      * Tenta sobrecarregar os sistema
    * Desempenho
      * Analisa a qualidade
* **Reteste** - Desenvolvedor/Testador  
  * Regressão
    * A cada nova versão executar todos os testes novamente
  * Smoke Test  
    * Não retesta tudo novamente, testa o minímo possível (apenas a parte alterada)
* **Aceitação** - Usuário  
  * Teste Alfa e Beta  
    * Alfa: Simula o ambiente do desenvolvedor e pede para testar
    * Beta: Ambiente real do desenvolvedor e pede para testar
* **Instalação** -  

Smoke Test: https://en.wikipedia.org/wiki/Smoke_testing_(software)
