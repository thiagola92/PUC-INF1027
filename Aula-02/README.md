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

## Garantia da Qualidade
Uma pessoa verifica se tudo que foi planejado foi implementado e se tudo implementado segue os padrões pré-estabelecidos.  
É importante que essas verificações sejam objetivas, por isso a pessoa que está verificando deve ser independente do projeto. Para ajudar a objetividade, também já se deve ter critérios de avaliação preparados para verificar.  

![Checklist](/Aula-02/checklist.png)  
Produto é quando você tem que abrir e olhar dentro de algum documento/arquivo.
O resto é considerado processo.  
**Não conformidade**: Sempre que a pessoa que está verificando encontrar algo não feito, essa coisa é uma não conformidade, não chamamos de erro ou defeito pois esses termos poderiam levar as pessoas a pensarem que tem algo feito errado.  

Note: Garantia da qualidade não está procurando verificar se as coisas estão funcionando como o cliente quer, apenas se existem e se os padrões estão sendo seguidos.  


## Verificação
_Estamos construindo certo o produto?_

Verificamos se o produto construido reflete os requisitos do cliente.  

Tipos de Revisão de Software
* Revisão aos Pares
  * Alguém escreve o documento e depois outra pessoa revisa
* Inspeções de Software
  * Entrega o documento para os responsáveis por revisar e eles entregam o feedback quando possivel
* Walkthroughs
  * Faz uma reunião com os responsáveis para que o escritor do documento vá explicando todo o processo feito e eles darem o feedback durante a reunião
