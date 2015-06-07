# Testes de Aceitação #

Um teste formal realizado para determinar se o sistema satisfaz ou não os critérios de aceitação determinados e para permitir ao cliente decidir se aceita ou não o sistema.
São originalmente chamados de Testes Funcionais, pois cada teste de aceitação testa uma funcionalidade de uma [User Story](UserStories.md). Testes de Aceitação são diferentes dos [Testes Unitários](TestesUnitarios.md) que são escritos pelos desenvolvedores, enquanto que os Testes de Aceitação devem ser escritos pelo Cliente.
Os Testes de Aceitação foram propostos por [Kent Beck](http://www.threeriversinstitute.org/blog/) em uma votação na [XpMailingList](http://c2.com/xp/XpMailingList.html) no começo de abril de 2000. Aprovado pela comissão, agora é um padrão em [XP](eXtremeProgramming.md).


---


## Definição ##

Um teste formal realizado para determinar se o sistema satisfaz ou não os Critérios de Aceitação determinados e para permitir ao cliente decidir se aceita ou não o sistema. São originalmente chamados de **Testes Funcionais**, pois cada teste de aceitação testa uma funcionalidade de uma [User Story](UserStories.md). Durante os Testes de Aceitação o foco é simular o uso real da aplicação. Os Casos de Testes são escritos usando cenários do mundo real para a aplicação.

  * Cada caso de teste consiste de uma sequência de passos que irão simular a [User Story](UserStories.md) que deve ser testada e são desenvolvidos a partir dos Critérios de Aceitação.
  * Contem dados de entrada (se necessários) e a saída esperada.
  * Os casos de testes aprovados serão a medida da completude de uma [User Story](UserStories.md) que não pode ser considerada completa antes de todos os testes de aceitação associados a ela terem passado.
  * Quando existem longas iterações com várias semanas é fácil perder o foco inicial, testes de aceitação que foram feitos para cada [User Story](UserStories.md) no começo de cada iteração ajuda os desenvolvedores a manter o desenvolvimento de acordo com as expectativas do cliente.
  * Testes de aceitação servem como um excelente guia para os desenvolvedores para interpretarem melhor os requisitos de cada [User Story](UserStories.md).
  * A cada estória estão associados um conjunto de testes de aceitação, que devem ser definidos pelo cliente, antes da construção da estória.


---

**Um Teste de Aceitação deve ter os seguintes objetivos:**
  * Verificar e validar se a User Story foi implementada como deveria;
  * Os desenvolvedores devem ser capazes de verificar se o que desenvolveram está de acordo com os requisitos;
  * Determinar se o produto desenvolvimento atende as expectativas do usuário final.
**Indicar que estes são os testes que o cliente definiu como sendo necessários o sistema passar de modo a que a história possa ser dada como concluída.**


---

## Como Testar? ##

Os Testes de Aceitação são um tipo de teste caixa preta. O foco é a funcionalidade e a usabilidade da aplicação e não os aspectos técnicos.

Testes de Aceitação geralmente envolvem um ou mais das seguintes atividades:
  1. Planejamento dos Testes de Aceitação do Usuário
  1. Escrita dos Testes de Aceitação do Usuário
  1. Seleção dos envolvidos na execução dos Testes de Aceitação do Usuário
  1. Execução dos Testes de Aceitação do Usuário
  1. Documentação dos defeitos encontrados
  1. Correção dos bugs

---

## Exemplo ##

```
“Um cliente deve registrar-se indicando como código de utilizador o e-mail e escolhendo uma palavra-chave alfa-numérica." 
```

Que testes de aceitação podemos definir?


```
"Uma palavra-chave não deve aceitar caracteres que não os A-Z, a-z e 0-9." 
```


"Depois de registrado, o cliente deve receber uma confirmação provisória do registro."


---

## Card ##

**Frente**
|**US01** |
|:--------|
|Um cliente deve registrar-se indicando como código de utilizador o e-mail e escolhendo uma palavra-chave alfa-numérica.|

**Verso**
|Critérios para aceitação|
|:--------------------------|
| Uma palavra-chave não deve aceitar caracteres que não sejam os A-Z, a-z e 0-9. Depois de registrado, o cliente deve receber uma confirmação provisória do registro.|



---

## Testes de Aceitação ##

![http://extreme-programming-mds.googlecode.com/svn/wiki/001.jpg](http://extreme-programming-mds.googlecode.com/svn/wiki/001.jpg)

Algumas perguntas podem ser feitas quanto a usabilidade dessa funcionalidade, como por exemplo:

```
Como o usuário fará essa busca no sistema?
Como o usuário deseja que seja apresentada a informação solicitada?
O que deve ser feito se o livro não for encontrado?
```

![http://extreme-programming-mds.googlecode.com/svn/wiki/002.jpg](http://extreme-programming-mds.googlecode.com/svn/wiki/002.jpg)


---

## Exemplo - Sistema AVS ##

---


## US01 ##
![http://extreme-programming-mds.googlecode.com/svn/wiki/Sele%C3%A7%C3%A3o_021.png](http://extreme-programming-mds.googlecode.com/svn/wiki/Sele%C3%A7%C3%A3o_021.png)

---


## US02 ##
![http://extreme-programming-mds.googlecode.com/svn/wiki/Sele%C3%A7%C3%A3o_022.png](http://extreme-programming-mds.googlecode.com/svn/wiki/Sele%C3%A7%C3%A3o_022.png)


---

## US03 ##
![http://extreme-programming-mds.googlecode.com/svn/wiki/Sele%C3%A7%C3%A3o_023.png](http://extreme-programming-mds.googlecode.com/svn/wiki/Sele%C3%A7%C3%A3o_023.png)


---

## US04 ##
![http://extreme-programming-mds.googlecode.com/svn/wiki/Sele%C3%A7%C3%A3o_024.png](http://extreme-programming-mds.googlecode.com/svn/wiki/Sele%C3%A7%C3%A3o_024.png)


---

## US05 ##
![http://extreme-programming-mds.googlecode.com/svn/wiki/Sele%C3%A7%C3%A3o_025.png](http://extreme-programming-mds.googlecode.com/svn/wiki/Sele%C3%A7%C3%A3o_025.png)

![http://extreme-programming-mds.googlecode.com/svn/wiki/Sele%C3%A7%C3%A3o_026.png](http://extreme-programming-mds.googlecode.com/svn/wiki/Sele%C3%A7%C3%A3o_026.png)

![http://extreme-programming-mds.googlecode.com/svn/wiki/Sele%C3%A7%C3%A3o_027.png](http://extreme-programming-mds.googlecode.com/svn/wiki/Sele%C3%A7%C3%A3o_027.png)

---
