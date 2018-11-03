### Análise estática de aplicações
A partir de análise dos logs, você descobre os erros no programa.  
Por exemplo, em Java você costuma análisar as Exceptions lançadas para descobrir a origem da falha.  

O seu programa lançar Exceções afeta  
* Confiabilidade
  * Exceções fazem seu programa parar, o que é muito ruim dependendo da aplicação
* Usabilidade
  * Usuário não vai entender nada do que está acontecendo
* Segurança

Exceção não tratada: quando uma parte do código que poderia levantar uma exceção não tem nenhum tratamento para caso levante.  
`Float f = (Float)request.getParameter("f");`  
Porém pode não existir parâmetro "f" para `getParameter` pegar, isso causa uma exceção.  

### Tratamento
Uma maneira de tratar exceção é usar `try catch`.  
```
try {
  Float f = (Float)request.getParameter("f");
  ...
} catch (Exception e) {
  ...
}
```

Outra maneira de tratar isso é utilizar `if`  
```
if(request.getParameter("f") != null) {
  ...
}
```

### Log
A idéia é registrar todas as exceções ocorridas no código em um local, para depois conseguir trata-las.  

```
java.lang.NullPointerException: null
	at uk.thetasinner.LogWriter.dumpCrap(LogWriter.java:29)
	at uk.thetasinner.LogWriter.main(LogWriter.java:19)
  ...
java.lang.NullPointerException
	at org.eclipse.e4.core.internal.di.InjectorImpl.invoke(InjectorImpl.java:217)
	at org.eclipse.e4.core.contexts.ContextInjectionFactory.invoke(ContextInjectionFactory.java:90)
  ...
java.lang.NullPointerException
	at org.eclipse.e4.core.internal.di.InjectorImpl.invoke(InjectorImpl.java:217)
	at org.eclipse.e4.core.contexts.ContextInjectionFactory.invoke(ContextInjectionFactory.java:90)
```

O log consegue nos dizer a linha onde o erro ocorreu, o arquivo em qual ocorreu e qual foi a exceção gerada.  

16:20
