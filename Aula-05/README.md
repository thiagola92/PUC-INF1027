# Técnicas para Detecção de Defeitos

* **Ad-hoc**
  * Utilizar o conhecimento próprio para tentar achar defeito, ou seja, não usa nenhum procedimento ou ferramenta.  
* **Checklist**
  * Tem uma lista com tudo que tem que ser verificado no artefato, vai verificando um por um.  
* **Técnicas de Leitura**
  * Instruções que dizem como ler e o que procurar no artefato
  * Dependendo do artefato tem técnicas diferentes, exemplos:
    * **Requisitos**
      * Perspective Based Reading (PBR)
        * As instruções são baseadas no ponto de vista de pessoas diferentes (usuário, desenvolvedor ou testador)
    * **Projeto**
      * Object Oriented Reading Techniques (OORTs)
        * É aquela técnica antiga, envolvia marcar no texto com cores.
    * **Código**
      * Stepwise Abstraction
        * Basicamente ler o código e tentar reconstruir o que ele faz (entender o que el faz), verifica se ta correto com os requisitos
      * Abstract-driven Reading
* **Análise Estática**
  * Existe recurso para verificar certas carecteristicas do seu código, se foi escrito como deveria
  * Não consegue dizer se você está fazendo o que o cliente queria, então não é substituto para revisão
