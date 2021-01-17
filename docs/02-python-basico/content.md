## Python Básico

--- 

### Objetivos

O objetivo da aula é introduzir comandos básicos em Python:
 - Terminal interativo de comandos
 - Variáveis e tipos
 - Operadores e expressões
 - Entrada e saída
 - Controle de fluxo (`if`, `while`, `for`)
 ---

## A Linguagem Python

- Criada no início dos anos 90 (Guido van Rossum) 

- Versão 3: lançada em 2008

- Diferentes tipos de aplicações:
    - Linguagem de script (auxiliar)
    - Aplicações das grandes indústrias  (Google, Dropbox, Intel, Netflix, etc.)
    - Aplicações científicas (NASA, Robot Operating System, etc.)
    - Bibliotecas de IA: Deep learning (PyTorch, TensorFlow)
- _Crescimento de uso considerável na década atual_
 ---

## A Linguagem Python

Por que Python?

- Simplicidade
- Facilidade de aprendizado e de correção de erros
- Código limpo
- Código multiplataforma (Linux/Mac/Windows)
- **Suporta o paradigma de programação orientada a objetos**
---

## A Linguagem Python

- É uma linguagem interpretada
- Suporta um terminal de comandos interativo
- Qualquer comando da linguagem pode ser executado
    - Agiliza a programação
    - Facilita a depuração de erros
    - Visualiza ajuda das funções/classes declaradas
---

## A Linguagem Python

- Instalação (Windows):
    1. Baixar a distribuição [Anaconda](https://repo.anaconda.com/archive/Anaconda3-2020.11-Windows-x86.exe) para Python
    2. Instalar a distribuição
    3. Executar terminal Python
- Instalação (Linux):
    1. Instalar pip:
    ```shell
    sudo apt-get install python3-pip
    ```
    2. Atualizar pip:
    ```shell
    pip3 install --upgrade pip
    ```
    3. Instalar Jupyter Notebook via pip:
    ```shell
    pip3 install jupyter
    ```
---

## Terminal de comandos interativo
<video data-autoplay src="./img/terminal.mp4"></video>
---

## Arquivos .py
<video data-autoplay src="./img/exec.mp4"></video>
---

## Jupyter Notebook
<video data-autoplay src="./img/jupyter.mp4"></video>
---

## Zen do python

```
import this
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Readability counts.
If the implementation is hard to explain, it's a bad idea.
```
---

## Diferenças entre C++ e Python

 - Os tipos são determinados automaticamente

 ```python
 x = 4 
 type(x) # int
 s = "alo"
 type(s) # str

 ```
---

## Diferenças entre C++ e Python

 - Indentação obrigatória: 

 ```python
 def f(n):
   return n+1 # Código indentado 
 ```
---

## Diferenças entre C++ e Python

 - `;` não é necessário

 ```python
 i = 5
 i +=1
 print(i)
 ```
---

## Diferenças entre C++ e Python

 - Laços for

```cpp
for(int i=0 ; i < n ; i++)
   cout << i << endl ;
```

```python
for i in range(0,n): # até n-1
   print(i)
```
---

## Jupyter Notebook

<div style="text-align:center">
Roteiro com comandos Python e exercícios:<br>
<a href="02-Python-Basico.ipynb">02-Python-Basico</a>
</div>
