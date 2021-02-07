### Programação Orientada a Objetos
#### Relacionamento entre Classes
---

### Revisão 

#### Classe
- Abstração para agrupar objetos comuns
- Descreve de maneira _abstrata_ o comportamento dos objetos 

#### Objetos 
- *Instâncias* de uma classe
- Encapsulam um _estado_
---

### Revisão
- _Construtor_: inicializa os atributos
- _Atributos_: características da entidade sendo modelada
- _Métodos_: definem o __comportamento__
- `self`: referência ao próprio objeto
---

### Interfaces e Encapsulamento
#### Membros privados de Classe

- *Atributos*: representando o _estado_ que _não deve ser visível_ para os usuários da classe.
- *Métodos*: usados internamente.

#### Membros Públicos

- Métodos que podem ser chamados _externamente_.
- Especificam um _contrato_: operações que o objeto pode e deve realizar

> Alterações no estado de um objeto geralmente ocorrem através da _chamada de seus métodos_
---

### Interfaces e Encapsulamento

> As mudanças na implementação não devem afetar os usuários da classe.
---

### Objetivos

> As classes _não existem sozinhas_: elas têm _relacionamentos
> entre si_ que descrevem como os objetos __interagem uns com os outros__

Objetivos desta aula:

- Introduzir o conceito de diagrama de classes
- Explicar como os objetos _se relacionam_ em um sistema orientado a objetos
- Identificar os diferentes _tipos de relacionamento_ entre classes
- Implementar relações entre classes em Python
---

### Implementação de Classes

- Até então, vocês implementaram uma (ou no máximo duas) classes
  para os programas implementados
- A partir desta aula, deverá ficar claro quando mais de uma classe
  é necessário e qual o papel de cada uma delas
    - Como elas se relacionam entre si 
- Antes disto, para facilitar:
    - Como mostrar/ler rapidamente o que possui uma classe?
---

### Diagrama de Classe UML

<img src="./img/classe_pessoa1.png" width=250 />

 - `-` denota um membro de classe _privado_.
 - `+` denota um membro _público_

- Diagrama de classe da linguagem unificada de modelagem (UML)
    - Facilita a visão geral de sistemas maiores
- Ferramenta: [Draw IO](https://www.draw.io/)
---

### Relacionamentos de Associação 
- Indicam algum _relacionamento_ significativo e de interesse entre objetos
- Especificam que objetos de uma classe estão _ligados_ a objetos de outras classes 

#### Exemplos
- Em um Estacionamento estão _estacionados_ os Carros
- Um Professor _ministra_ várias Disciplinas
- Uma Mensagem _possui_ um Remetente e um Destinatário
- Exercício anterior: uma Pessoa possui um Conjunto de atividades
---

### Relacionamentos de Associação 
<img src="./img/multiplicidade.png" width="450"/>

- Um objeto tipo A está ligado com zero ou vários objetos tipo B
- Um objeto tipo B está ligado com um objeto tipo A
- Notação em diagrama de classes: **linha** conectando as classes que se relacionam

#### Multiplicidade:
 - `0` : zero
 - `0..1`: zero ou um
 - `1` : um
 -  `1..*`: um ou mais
 - `0..*` ou `*`: zero ou mais
---

### Relacionamentos de Associação
#### Exemplo

Um banco, no qual cada conta bancaria está relacionada com uma pessoa (o
titular da conta):

<img src="./img/pessoa_X_conta.png" width=400/>
---

### Relacionamentos de Agregração

- Representa uma relação _todo-parte_
- __As partes podem existir sem o todo__

#### Exemplos
 - Considere a relação entre o Carro, as Rodas e o Motor
 - Considere a relação entre um Computador,  o Teclado, a Tela
---

### Relacionamentos de Agregração

<img src="./img/agregacao.png" />

- A é o __todo__
- B são as __partes__
- Notação em diagrama de classes: diamante vazado na classe que representa o todo
juntamente com linha conectando as classes
---

### Relacionamentos de Agregração
#### Exemplo

Um carro que possui 1 motor e 4 rodas

<img src="./img/carro_X_rodas_X_motor.png" width=500 />
---

### Relacionamentos de Agregração

- Objetos do tipo Motor e Roda são instanciados
- Estas instâncias são associadas a um objeto do tipo Carro no inicializador
  deste último
- Ou seja, Motor, Roda e Carro podem ser __instanciados independentemente__
- Quando a instância de Carro é removida da memória, as instâncias de Motor e
  Roda associadas continuam a existir
---

### Relacionamentos de Composição

- Representa  uma relação _todo-parte_ mais *forte*
- Se o objeto "todo" deixar de existir, os seus objetos "parte" deverão também deixar
de existir

#### Exemplos
 - Um Estacionamento e seus Andares
 - Um Prédio e suas Salas.
---

### Relacionamentos de Composição

<img src="./img/composicao.png" width=400/>

- A é o todo e B as partes
- A existência de B não faz sentido se A não existir
- Notação em diagrama de classes: diamante preenchido na classe que representa o todo
juntamente com linha conectando as classes
---

### Relacionamentos de Composição
#### Exemplo

Prédio com várias salas

<img src="./img/predio_X_sala.png" width=500 />
---

### Resumindo
#### Associação
- Modela uma relação genérica entre duas classes
- Nenhum objeto é considerado dono/proprietário do outro objeto

#### Agregração
- Modela uma relação do tipo *tem um* fraca, ou seja, uma classe A é formada por
objetos de outra classe B
- Objetos da classe B podem existir sem que objetos da classe proprietária A
existam
---

### Resumindo
#### Composição
- Modela uma relação do tipo *tem um* forte
- Objetos da classe B deixam de existir quando objetos da classe proprietária A
deixam de existir
---

### Relações entre Objetos e Abstração
- A escolha de uma forma de associação específica
  está atrelada à abstração empregada no domínio
  do problema
- As classes ```Motor```, ```Roda``` e ```Carro```,
  por exemplo:
    - Podem ser implementadas como agregação em um sistema:
      é interessante que ```Motor``` e ```Roda``` sejam instanciados
      sem depender de um ```Carro```
    - Podem ser implementadas como composição em um outro sistema:
      ```Motor``` e ```Roda``` só podem ser instanciados
      quando um ```Carro``` é instanciado
---

### Relações entre Classes
[06-relacoes](06-Relacoes.ipynb)
