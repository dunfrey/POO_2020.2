### Programação Orientada a Objetos
#### Polimorfismo
---

### Objetivo da aula

Nesta aula veremos: 

- O que é polimorfismo
- *Duck typing*
- Como utilizá-lo na linguagem Python
---

### Os Pilares de POO

- Abstração
- Encapsulamento
- Herança
- __Polimorfismo__
---

### Polimorfismo

> Mecanismo presente em linguagens OO que permitem a um objeto se comportar de
> formas diferentes 

- *Poli*: muitos, *morfismo*: formas
- Mais um recurso utilizado para promover a reutilização de código
- Uma mesma mensagem pode executar _diferentes_ métodos/código
---

### Polimorfismo em Linguagens Tipadas (Java)

1. Instanciando objetos da classe base utilizando construtores da classe derivada:

```java
// Gato é uma subclasse de Mamifero
Mamifero M = new Gato(); 
// Funcionario é uma subclasse de Pessoa
Pessoa P = new Funcionario(...); 

// Utilizando casting explicito
Gato G = new Gato();
Animal A2 = (Animal) G ;

// Erro!! Nem toda pessoa é um funcionário
Funcionario F = new Pessoa(...); 
```

Podemos atribuir objetos da subclasse a variáveis da superclasse
---

### Polimorfismo em Linguagens Tipadas (Java)

2. Considere um método que recebe como parâmetro objetos da classe base:

```java
void imprimirDados(Pessoa P){
 ...
}

Funcionario F = new Funcionario(...);
// Como todo funcionário é uma pessoa,
// podemos utilizar o método imprimirDados com parâmetro F
imprimirDados(F); 
```

Podemos _"substituir"_ o parâmetro do tipo `Pessoa` por um `Funcionario`
(porque todo `Funcionario` __é uma__ `Pessoa`)
---

### Polimorfismo em Linguagens Tipadas (Java)

3. _Sobrecarga_ de funções: uma mesma função se comporta de diversas
   formas, de acordo com seus parâmetros:

```java
int funcao(int x);
float funcao(float x);
char funcao(char x);
```

A função `funcao` possui diferentes __assinaturas__
---

### Em Python a História é Diferente

1. Sem tipos explícitos, isso aqui não faz sentido:

```java
Pessoa P = new Funcionario(...); 
```

Note que em Python, uma variável pode ser atribuída a objetos de tipos
diferentes (que não necessariamente pertencem __à mesma hierarquia__) 

```python 
x = 4 
x = [1,2,3] 
x = "alo" 
x = Pessoa(...) 
x = Carro(...) 
```
---

### Em Python a História é Diferente

2. Chamar funções/métodos com instâncias de alguma subclasse:

Como não temos tipos, podemos chamar uma função/método com objetos
de tipos diferentes (não necessariamente objetos de uma subclasse):

```python
str(3)
str(3.2)
P = Pessoa(...)
str(P)
####
len("alo") #3
len([1,2,3]) #3
```
---

### Em Python a História é Diferente

3. Sobrecarga de funções - em Python, não podemos criar 2 funções com 
diferentes assinaturas: 

```python
def funcao(x):
 ...

def funcao(x,y):  # a definição anterior de f já não existe mais
 ...

f(4) # Erro! 2 parâmetros são esperados
```
---

### Em Python a História é Diferente

Parece que só temos como alternativa (2):

```python
class Pessoa:
    def __init__(self, nome, idade): ...

    def compara_idades(self, p2):
        return p1.idade <= p2.idade

class Aluno(Pessoa): ...
class Professor(Pessoa): ...

p = Pessoa('joão', 25)
a = Aluno('maria', 20, 111) 
print(p.compara_idades(a)) # método funciona pq um Aluno é uma Pessoa
```
---

### Polimorfismo

- Capacidade de um objeto de ser referenciado de várias formas
- A chamada dos métodos é polimórfica: a mesma chamada pode se comportar
  de diferentes formas, de acordo com o tipo dos objetos envolvidos
---

### O princípio da substituição de Liskov
  <img src="Barbara.jpg" ></img> 

Barbara Liskov, cientista da computação estadunidense conhecida por criar o
_Princípio de Substituição de Liskov_, por ser uma das primeiras mulheres a
obter um PhD em Ciência da Computação nos Estados Unidos e por inventar o Tipo
Abstrato de Dado (TAD)(tomada da
[Wikipedia](https://pt.wikipedia.org/wiki/Barbara_Liskov)) 
---

### O princípio da substituição de  Liskov
  <img src="Barbara.jpg" ></img> 

Barbara recebeu em 2008 o Prêmio Turing da ACM por seu trabalho na concepção
de linguagens de programação e de metodologia de software que levaram ao
desenvolvimento da _programação orientada para objetos_.
---

### O princípio da substituição de  Liskov
- *Uma classe base deve poder ser substituída pela sua classe derivada*
- Considere o método ```q(x)```. Se ```q``` pode ser utilizado com objetos da
  superclasse T, então ```q``` deve poder também ser invocado com um objeto de
  uma subclasse ```S``` derivada de ```T```
---

### Duck Typing

>Quando eu vejo um pássaro que anda como pato, nada como um pato
e grasna como pato, então pra mim este pássaro é um pato

- Fundamento base da linguagem Python
- Lembre-se que Python possui tipagem dinâmica: o tipo dos objetos
  só pode ser determinado na execução  do programa
---

### Duck Typing

Forma de tipagem que está mais interessada no que o objeto possui como
atributos/métodos do que se ele é de uma determinada classe

*Duck typing* já foi utilizado diversas vezes:

- Quando usamos ```a + b```: não interessa os tipos de ```a``` e ```b```,
  desde que as classes de ```a``` e ```b``` implementem o operador de soma
  (método ```def __add__(self, outro):```)
- Quando usamos ```print(a)```: não interessa o tipo de ```a```,
  o objeto vai ser impresso (e o método ```__str__``` é chamado)
- Quando usamos ```a.liga()```: não interessa o tipo de ```a```, desde que
  este objeto possua o método ```liga```
---

### Mais exemplos
[10-polimorfismo](10-Polimorfismo.ipynb)
---
