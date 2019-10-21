# Estruturas básicas do Swift
## Condicionais

Como em toda linguagem, Swift possui uma estrutura de decisão condicional: ```if``` e ```else```. A sintaxe básica é:

```
if condicao {
    algumaCoisa
}
else {
    algumaOutraCoisa
}
```

Sim, é parecido com C e Java. A maior diferença aqui é que **não existe o parêntese** para delimitar o que é condição e o que é instrução. Ao invés, o Swift obriga você a **dar um espaço** entre a condição e os colchetes.

## Laço de repetição ```while```

Para criar um laço de repetição ```while```, a sintaxe é a seguinte:

```
while condicao {
    algumaCoisa
}
```

Assim como na anterior, o espaço entre os colchetes é requerido.

## Laço de repetição ```for```

Para criar um laço de repetição ```for``` clássico, a sintaxe é a seguinte:

```
for i in 0..10{
    algumaCoisa
}
```

Diferente, não é? Mas é bem simples. Mas ainda existe um segundo ```for```, que chamamos de ```forEach```.


### Iterar em um array

Já sabemos como criar, acessar e modificar valores de um array. Mas como poderemos utilizar laços de repetições para fazer determinadas ações dentro de uma coleção desse tipo?

```
var linguagens = ["Java", "C", "Python", "Swift"]
linguagens.sort()

for i in linguagens {
    print(i)
}

>>>
C
Java
Python
Swift
```

Esse tipo de ```for``` é especial para ser usado com coleções. Pode ser usado até mesmo em strings, já que elas são um array de caracteres.

```
var nome = "Pedro"
for i in nome {
    print(i)
}

>>>
P
e
d
r
o
```
