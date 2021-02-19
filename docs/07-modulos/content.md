### Programação Orientada a Objetos
#### Módulos em Python
---

### Objetivos
- Apresentar o conceito e a utilidade de _Módulos_ em Python
---

### Módulos em Python:

Conjunto de variáveis, funções e classes contidos em um ou mais arquivos `.py`

Módulos podem ser importados por um programa (similar ao `#include` de C++)

Em Python, um módulo pode ser considerado sinônimo de biblioteca
---

### Importação de Módulos

Considere o código a seguir:

```
import math # modulo da biblioteca padrão
print(math.e) # constante de Euler
print(math.sqrt(16)) # raiz quadrada de 16
```

- Note o uso de `math.sqrt`
- O nome do módulo deve ser utilizado como prefixo
---

### Importação de Módulos

Podemos importar também __todas__ as definições de um módulo:

```
from math import *
print(e) # contante de Euler
print(sqrt(16)) # raiz quadrada de 16
```

- Note o uso da função `sqrt` (sem o nome do módulo)
---

### Importação de Módulos

Também podemos importar algumas das definições do módulo:

```
from math import e, sqrt
print(e)
print(sqrt(16))
```

- Note que `math.sin` não pode ser usado porque apenas foram importadas as
  definições `e` e `sqrt`
---

### Biblioteca Padrão

```
import math
dir(math)
help(math)
```

As funções `help` e `dir` podem ser utilizadas para obtermos
mais informações sobre módulos
---

### Definindo Módulos

Todo arquivo `.py` é um módulo
```
#arquivo alo.py
```

```
def dois():
 '''Função que retorna 2'''
 return 2

class Alo:
 '''Classe ainda não implementada'''
 pass
```

Como pdeomos utilizar esse arquivo?
- Como script/programa (forma como estamos fazendo)
- Como módulo (para ser importado)
---

### Importando Módulos Implementados

No console Python:

```
import alo
dir(alo)
help(alo)
print(alo.dois())
x = alo.Alo()
```

(o console deve ser executado na mesma pasta onde está o arquivo `alo.py`)
---

### Importando Módulos Implementados

Mas também podemos importar o módulo `alo` em outro módulo:

```
#arquivo test.py
```

```
import alo

def printDois():
    '''Imprimir o resultados de alo.dois()'''
    print(alo.dois())

def main():
    '''Função principal'''
    printDois()

if __name__ == "__main__":
    main()
```
---

### Importando Módulos Implementados

O que significa `__name__ == "__main__"`?

- Execute `python test.py`
- Agora, entre no console e execute `import test`
    - Note que a função `main` não é executada
    - Isto acontece porque o atributo especial de um módulo
      `__name__` contém a string `"__main__"` apenas quando
      ele não está sendo importado
- Verifique isto executando `dir()` e depois `print(__name__)`
---
