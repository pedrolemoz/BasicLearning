# O básico de Swift

## O Hello World

O primeiro programa em Swift deve se parecer com isso:

```print("Hello World")```

Sim, é tão simples quanto escrever em inglês.

## Variáveis e tipos primitivos

Em Swift, temos alguns tipos primitivos de dados. São eles:

- ```Int```: **Números inteiros.** Ex.: 4.
- ```Float```: **Números reais (ponto flutuante).** Ex.: 4.5.
- ```Double```: **Números reais, porém em um intervalo maior que os** ```Float```**.**
- ```String```: **Conjunto de caracteres.** Ex.: "*O Pedro é um cara legal!*"
- ```Boolean```: **Valores lógicos** ```true``` **ou** ```false```**.**

Entendidos os tipos primitivos, podemos passar para as variáveis.
Variáveis são **espaços de memória** alocados para armazenar temporariamente um dado.
As variáveis podem ser de dois tipos:

- ```var```: **Variável que é passível a mudanças de valores.**
- ```let```: **Variável que possui valor constante.**

Em Swift, a variável deve obedecer a seguinte sintaxe:

```var nomeDaVariavel:tipoDeDado = valorDaVariavel```

```let nomeDaVariavel:tipoDeDado = valorDaVariavel```

> Após iniciada uma variável var de um determinado tipo, ela permanecerá desse mesmo tipo até o fim da execução do programa.

Uma variável em Swift é capaz de **inferir qual o tipo de dado** que foi armazenado.
Graças a isso, podemos **simplificar** o nosso código:

```var nomeDaVariavel = valorDaVariavel```

```let nomeDaVariavel = valorDaVariavel```

