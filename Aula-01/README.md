# Normas SQuaRE
(__S__oftware product __Qua__lity, __R__equirements and __E__valuation)  

Normas que tem como foco ajudar a melhorar a __qualidade do produto__ e a __qualidade do desenvolvimento do produto__.  
Essas normas não estão completas, elas tem evoluído com o tempo.  

Sendo __n__ um número qualquer, cada uma dessas divisões cuidam de uma parte da qualidade.  
- __2500n__: Gerenciamento de Qualidade
  - Nesta divisão se define todos os modelos, termos e definições que vão ser referenciadas por todas as divisões.
- __2501n__: Modelo de Qualidade
  - Nesta divisão se descobre as características de qualidade desejadas pelo produto.
- __2502n__: Medições de Qualidade
  - Nesta divisão se decide como vai ser a medição para cada característica desejada.
- __2503n__: Requisitos de Qualidade
  - Nesta divisão se especifica os requisitos de qualidade.
- __2504n__: Avaliação de Qualidade  
  - Nesta divisão se diz como vai avaliar o produto.

![ISO 25000](http://iso25000.com/images/figures/en/iso25000-divisions.png)  
Fonte: http://iso25000.com/index.php/en/iso-25000-standards  
Fonte 2: https://pt.wikipedia.org/wiki/ISO/IEC_25000

# Qualidade de Produto (ISO/IEC 25010)
* **Adequação funcional** - Software fazer sua *função* corretamente.  
* **Performance** - O *desempenho* do software (tempo/recurso).  
* **Compatibilidade** - O quanto o software é *compatível* com outros sistemas que tem que interagir.  
* **Usabilidade** - Facilidade de *usar* o software.  
* **Confiabilidade** - O quanto a informação do sistema é *confiável*.  
* **Segurança** - O quanto está *protegido* contra ataques.  
* **Manutenibilidade** - Facilidade de fazer *manutenção* no software.  
* **Portabilidade** - Software *porta* em diferentes plataformas.  

![Software Product Quality](http://iso25000.com/images/figures/en/iso25010.png)
Fonte: http://iso25000.com/index.php/en/iso-25000-standards/iso-25010?limit=3&limitstart=0

## V&V
* Verificação  

*Estamos construindo certo o programa?*  
Aqui queremos saber se estamos construindo de maneira certa, ou seja, se está funcionando.  

* Validação

*Estamos construindo o programa certo?*  
Aqui queremos saber se estamos construindo a coisa certa, ou seja, se é o que o cliente quer.  

## Testes

* **Análise estática** - Conjunto de ferramentas que *analisam* seu código para ver se tem problemas mas sem rodar seu código.
  * Verificação
* **Teste de unidade** - Testar uma unidade do software, geralmente uma função/classe.
  * Verificação
* **Teste integração** - Testar se as funções/classes estão se comunicando corretamente, ou seja, testar um módulo.
  * Verificação
* **Teste de sistema** - Testar o sistema como se fosse um usuário utilizando, verificar se compriu os requisitos.
  * Verificação
* **Teste de aceitação** - Testar o sistema mas sendo um usuário utilizando.
  * Validação
* **Revisões de software** -
  * Verificação e Validação

Fonte: https://en.wikipedia.org/wiki/Software_testing#Testing_levels
