# Aula 2

## Dívida Técnica
Quando gerente ou desenvolver toma uma decisão para poder fazer uma entrega mais rápida (tentar comprir com o prazo), essa decisão geralmente é abrir mão de partes de qualidade.  

**Exemplos**:  
Decide restruturar/limpar o código depois pois iria custar tempo agora.  
Deixa de fazer todos os testes possíveis pois custaria muito tempo monta-los.  
Deixar de fazer a validação de algo por causa do tempo.  

Geralmente quando você vê um **TODO** ou **FIXME** no código, é uma dívida técnica.  

Fonte: https://en.wikipedia.org/wiki/Technical_debt

## Code Smell
Parte dos códigos que estão estruturados de forma que da a entender que ali tem um problema de projeto.  

**Exemplos**:  
Feature Envy: Uma classe que toda hora chama métodos de outra classe.  
Large class: Uma classe que cresceu demais, que faz coisa demais.  

Fonte: https://en.wikipedia.org/wiki/Code_smell

## Safety vs Security
Em português ambas palavras são traduzidas como segurança mas em inglês elas tem significados diferentes.  

**Safety**: Prevenir riscos de acidentes.  
Esses acidentes podem ou não incluir um agente humano, mas não são intencionais.  
- Usar coberto para evitar pegar um resfriado durante uma noite fria  
- Carregar um guarda-chuva para prevenir que não se molhe se chover  
- Botar uma placa avisando que o equipamento tem alta voltagem  

Não existe um agente humano tentando o atingir, mas você está se prevenindo contra algo ruim que possa acontecer com você.  


**Security**: Prevenir riscos de atividades maliciosas.   
Essas atividades são de um agente humano com intenções maliciosas.  
- Assalto  
- Ataque terrorista  
- Extorsão  

Existe alguém com intenções de causar algum mal a você, então você está se prevenindo contra algo ruim que outra pessoa possa fazer com você.  

**Computação exemplo**  
Safety: Impedir que seu sistema cause dano a outros sem querer, carro inteligente atropelar alguém, ...    
Security: Impedir que invadam seu sistema, prevenir ataques ao sistema...

# Gerência da Qualidade de Software
![Gerência da Qualidade](/Aula-02/gerencia.png)  

*Só conseguimos gerência a qualidade de coisas que conseguimos medir*  
Por isso, junto de cada parte dessas precisamos ter uma maneira de medir.

## Garantia da Qualidade
Uma pessoa verifica se tudo que foi planejado foi implementado e se tudo implementado segue os **padrões** pré-estabelecidos.  
É importante que essas verificações sejam objetivas, por isso a pessoa que está verificando deve ser independente do projeto. Para ajudar a objetividade, também já se deve ter critérios de avaliação preparados para verificar.  

Exemplo de *checklist*
![Checklist](/Aula-02/checklist.png)  
Produto é quando você tem que abrir e olhar dentro de algum documento/arquivo.
O resto é considerado processo.  

**Não-conformidade**: Sempre que a pessoa que está verificando encontrar algo não feito, essa coisa é uma não-conformidade, não chamamos de erro ou defeito pois esses termos poderiam levar as pessoas a pensarem que tem algo feito errado.  

Note: Garantia da qualidade não está procurando verificar se as coisas estão funcionando como o cliente quer, apenas se existem e se os padrões estão sendo seguidos.  

## Verificação & Validação
**Verificação**  
_Estamos construindo certo o produto?_  

Na verificação você está procurando saber se o software está sendo construindo de maneira que funcione.  
Durante as etapas de revisão e testes, você deve estar focado apenas em conferir se tudo está funcionando.  

**Validação**  
_Estamos construindo o produto certo?_  

Na validação você procurando saber se o software está realizando aquilo que o cliente e usuário desejavam.  
Durante as etapas de revisão e testes, você deve estar constantemente pegando feedback do cliente/usuário.

---

**Artefato de software**: Qualquer parte tangível do software, desde requisitos até códigos.  
Artefato: https://en.wikipedia.org/wiki/Artifact_(software_development)  

### Revisões
Ler o artefato de software procurando ver se está fazendo o que deveria.  

Tipos de Revisão de Software:
* **Revisão aos Pares**
  * Alguém escreve o documento e depois outra pessoa revisa
* **Inspeções de Software**
  * Entrega o documento para os responsáveis por revisar e eles entregam o feedback quando possivel
* **Walkthroughs**
  * Faz uma reunião com os responsáveis para que o escritor do documento vá explicando todo o processo feito e eles darem o feedback durante a reunião

Software Review: https://en.wikipedia.org/wiki/Software_review

Quando fazer revisão? No caso ideal, seria fazer para qualquer artefato do software. Mas o recomendado é pelo menos fazer para os requisitos, para ter certeza que não está construindo a coisa errada.  

### Testes

* Perspectiva dos Projetistas e Desenvolvedores
  * **Teste de unidade**
    * Testar uma unidade do software, geralmente uma função/classe.
  * **Teste integração**
    * Testar se as funções/classes estão se comunicando corretamente, ou seja, testar um módulo.  


* Perspectiva dos Clientes e Usuários
  * **Teste de sistema**
    * Testar o sistema como se fosse um usuário utilizando, verificar se   compriu os requisitos.
  * **Teste de aceitação**
    * Testar o sistema mas sendo um usuário utilizando.

Professor já focou um pouco em teste de sistema, onde é importante testar o aspecto funcional e aspecto não-funcional.  
Por exemplo, testar a recuperação em caso de falha, testar segurança do software, testar o stress do software quando exigido muito recurso dele, testar desempenho...

Non-functional requirement: https://en.wikipedia.org/wiki/Non-functional_requirement  

### Medindo
Como podemos medir se estamos bem ou mal? Usando a informação coletada de cada categoria.  

Garantia da Qualidade   
* Ver quantas não-conformidades tiveram
* Tempo que demora pra corrigir não-conformidades
* Quantidade de não-conformidades não solucionadas
* ...

Verificação  
* Taxa de defeitos encontrados
  * Defeitos por página
  * Defeitos por revisão
  * Defeitos por caso de uso
  * ...
* Tempo médio para a correção
* Densidade de defeitos identificados em revisões
* Medir o retrabalho
* ...

Validação  
* Esforço de retrabalho para correção de defeitos nos requisitos
* Esforço de retrabalho para a correção de defeitos em teste de aceitaçãoo
* ...
