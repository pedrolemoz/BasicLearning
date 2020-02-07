# Estruturas básicas do Python3

## Condicionais ```if``` , ```elif``` e ```else```

Como em toda linguagem, o Python3 possui uma estrutura de decisão condicional: ```if``` e ```else```. A sintaxe básica é:

```python3
if condicao:
    algumaCoisa
else:
    algumaOutraCoisa
```
Porém, ele possui o ```elif```, que serve para quando você não atende a condição inicial do ```if```, entra no ```else```, e ainda quer verificar outra condição antes de terminar a verificação (ir para o caso de "senão").

```python3
if condicao:
    algumaCoisa
elif condicao:
    algumaOutra
else:
    algumaOutraCoisa
```

A sintaxe é um pouco diferente do habitual. A maior diferença entre outras linguagens é que **não existem chaves** para delimitar o bloco de código (como em Java e C), mas sim, dois pontos e indentação.

## Laço de repetição ```while```

Para criar um laço de repetição ```while```, a sintaxe é a seguinte:

```python3
while condicao:
    algumaCoisa
```

Assim como na anterior, é necessário usar dois pontos e a indentação correta.

## Laço de repetição ```for```

Para criar um laço de repetição ```for``` clássico, a sintaxe é a seguinte:

```python3
for i in range(0, 10):
    algumaCoisa
```

Diferente, não é? Python é uma linguagem cheia de recursos, e um deles é o ```range()```. Não é necessário declarar uma variável ```i = 0```, dizer que essa variável é maior ou menor que o tamanho desejado e dizer que quer incrementar o ```i``` a cada repetição. É tudo muito simples. Porém, ainda existe um segundo ```for```, que chamamos de ```forEach```.


### Iterar em uma lista

Já sabemos como criar, acessar e modificar valores de uma lista. Mas como poderemos utilizar laços de repetições para fazer determinadas ações dentro de uma coleção desse tipo?

```python3
linguagens = ["Java", "C", "Python", "Swift"]
linguagens.sort()

for i in linguagens:
    print(i)

>>>
C
Java
Python
Swift
```

Esse tipo de ```for``` é especial para ser usado com coleções. Pode ser usado até mesmo em strings, já que elas são um array de caracteres.

```python3
nome = "Pedro"
for i in nome:
    print(i)

>>>
P
e
d
r
o
```
