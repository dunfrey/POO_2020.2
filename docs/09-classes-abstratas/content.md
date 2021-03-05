### Programação Orientada a Objetos
#### Classes Abstratas
---

### Objetivo da aula

- Apresentar o mecanismo de __classes abstratas__
 - O que são classes abstratas
 - Identificar quando utilizar classes abstratas em um projeto orientado a objetos
 - Como utilizá-las na linguagem Python
---

### Herança (revisão)

- Permite que classes derivadas _herdem o comportamento_ (atributos e métodos) de
  uma classe base
- Introduz a relação _"é um"_ (ex.: "trem" é um "meio de transporte")
- O código da superclasse é _reutilizado_ pelas classes derivadas
- As classes derivadas podem _reescrever_ métodos da superclasse com
  __funcionalidades específicas__
---

### Herança (revisão)

Observe um possível diagrama do exercício da aula anterior:

<img src="img/contas.png" width=400 />

- Faz sentido criar objetos tipo ``Conta``?
- Senão, qual é a utilidade dessa classe ?
---

### Classe Abstrata

- É uma classe que __não deve ser instanciada__
- Define um _comportamento comum_ para outras classes derivadas
- O código da classe abstrata pode  ser reutilizado/implementado por classes derivadas
- Toda classe que não é abstrata é chamada classe **concreta**
---

### Método Abstrato

- Estão presentes __somente em classes abstratas__
- É um método _que deve ser obrigatoriamente reescrito_ nas classes derivadas
- Se a classe possui pelo menos um método abstrato, então ela é uma classe
  abstrata (não é possível instanciar objetos desta classe)
- Em geral, um método abstrato não possui implementação
    - Em Python: podem possuir implementação
---

## Classes Abstratas em Python

Em Python, as classe abstratas herdam da classe ```ABC```
(**A**bstract **B**ase **C**lass), do módulo ```abc``` e tem, pelo menos, um
método abstrato (denotado com o decorador `@abstractmethod`):

```python
from abc import ABC, abstractmethod

class A(ABC):
    
    '''Exemplo de uma classe abstrata'''
    def __init__(self, v):
        self._v = v

    @abstractmethod
    def m(self):
        '''Método abstrato (sem implementação)'''
        pass 
```
---

## Classes Abstratas em Python

A classe `B` herda de `A` e provê um implementação para o método `m`:

```python
class B(A):
    def __init__(self, v, v2):
        super().__init__(v)
        self.v2 = v2

    def m(self):
        '''Implementando o método abstrato'''
        self.v2 += 1
        return self.v2
```
---

## Classe Abstrata - UML

Na notação UML, uma classe abstrata
possui seu nome *em itálico*:

Os métodos abstratos também são indicados com fonte itálica. 

<img src="img/contas_classe_abstrata.png" />
---

## Observações Importantes

- Classes concretas __não podem ter métodos abstratos__
- Se a subclasse não reescreve *todos* os métodos abstratos da superclasse, ela é também abstrata 
- Uma classe abstrata pode ter métodos abstratos e métodos implementados
---

### Mais exemplos
[09-classes-abstratas](09-Classes-Abstratas.ipynb)
---
