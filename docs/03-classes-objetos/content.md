### Programação Orientada a Objetos
#### Classes, Objetos e Abstração
---

### Objetivos

Nesta aula aprenderemos a:
 - Definir uma _classe_.
 - Adicionar _atributos_, _métodos_ e _construtores_ a uma classe. 
 - Aprender novos comandos básicos de Python.
---

### Classes e Abstrações

Considere um carro:
 1. Quais são as características de um carro?
 2. Que coisas pode "fazer" um carro ?
 3. Todos os carros alcançam a mesma velocidade ?

 <img src="img/carros.jpg" width=350/>

 Foto: [Revista carro](https://revistacarro.com.br/)
---

### Classes

Abstração para agrupar objetos comuns que têm _o mesmo comportamento_.

Descrevem de maneira _abstrata_ o _comportamento_ dos objetos.
---

### Classes

>> A palavra classe vem da taxonomia da biologia. Todos os seres vivos de uma
>> mesma classe biológica têm uma série de _atributos_ e _comportamentos em
>> comum_, mas eles  __não são iguais__, podem variar nos valores desses atributos
>> e como realizam esses comportamentos.
---

### Objetos

Objetos são _instâncias_ de uma classe:

 - _Encapsulam_ um _estado_ (conjunto de valores em um determinado instante)
 - Respondem às _mensagens_ com a execução de um _método_.

>> Os objetos de uma mesma classe _compartilham o comportamento_ definido pela sua classe.
---

### Atributo e Estado

O _estado_ de um objeto está definido pelos valores dos _atributos_ de classe.

Os tipos dos atributos podem ser:

 - Tipos primitivos: `int`, `float`, `double`, etc.
 - Tipos definidos pelo usuário (classes).
---

### Atributo e Estado
O _estado_ está definido pelos valores dos _atributos_.
<table>
<tr>
<td>
<img src="img/carros2.jpg" width=450/>
<td>

```cpp
Class Carro:
 // Atributos
  - marca
  - potencia
```
---

### Tipos Estruturados vs POO
Considere a classe _Círculo_:

 - Quais são as características de um círculo ?

Em C++ provavelmente definiríamos o tipo
```cpp
struct Circulo{
    double x,y; // Coordenadas do centro
    double raio; //Raio
 };
```
---

### Tipos Estruturados vs POO
Entretanto, o tipo Circulo definido como _struct_:

- É utilizado apenas para armazenar dados
- Não tem um _comportamento_ definido

Solução: Classes!
---

### Classes em Python

 - Em Python, tudo é um objeto:
 ```python
>>> type(5)
< class 'int' >
>>> type("alo")
< class 'str' >
```

>> Variáveis possuem _tipos_ $\equiv$ objetos possuem _classes_
---

### Programação Orientada a Objetos
Programar orientado a objetos envolve:

- Identificar _classes_ que agrupam objetos com um comportamento comum.
- Identificar os __atributos__ que deve armazenar cada objeto.
- Identificar como os objetos devem *se comportar*.
- Identificar como devem *interagir* os objetos do sistema.
--- 

### Primeiro pilar de POO: Abstração

_Abstração:_ escolher os aspetos _mais relevantes_ para representar uma entidade do mundo real.

 - __Simplicidade__: atributos irrelevantes devem ser ignorados.
 - Dividir e conquistar: o propósito de uma classe deve estar bem definido.
--- 

### Primeiro pilar de POO: Abstração

<img src="img/cat-abstraction.jpg" width=500 >

Imagem de [The Cat as a Metaphor in OO Software Development](https://effectivesoftwaredesign.com/2016/09/28/the-cat-as-a-metaphor-in-object-oriented-software-development/)
---

### Jupyter Notebook 
<a href="03-Classes-Objetos.ipynb">03-Classes-Objetos</a>
