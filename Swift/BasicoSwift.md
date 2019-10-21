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

> Nota: se um número real não tiver seu tipo especificado, em Swift, o valor padrão atribuído será ```Double```

Entendidos os tipos primitivos, podemos passar para as variáveis.
Variáveis são **espaços de memória** alocados para armazenar temporariamente um dado.
As variáveis podem ser de dois tipos:

- ```var```: **Variável que é passível a mudanças de valores.**
- ```let```: **Variável que possui valor constante.**

Em Swift, a variável deve obedecer a seguinte sintaxe:

```var nomeDaVariavel:tipoDeDado = valorDaVariavel```

```let nomeDaVariavel:tipoDeDado = valorDaVariavel```

> Após iniciada uma variável var de um determinado tipo, ela permanecerá desse mesmo tipo **até o fim da execução** do programa.

Uma variável em Swift é capaz de **inferir qual o tipo de dado** que foi armazenado.
Graças a isso, podemos **simplificar** o nosso código:

```var nomeDaVariavel = valorDaVariavel```

```let nomeDaVariavel = valorDaVariavel```

Podemos ainda, inicializar uma variável, mas **sem atribuir** um valor a ela:

```var nomeDaVariavel```

```let nomeDaVariavel```

Certo, entendemos que variáveis têm seu tipo imutável. Mas e se precisarmos converter tipos?
Em Swift, os valores nunca são convertidos implicitamente. Isso significa dizer que nós deveremos especificar o valor para o qual queremos converter.

```
var numeroDouble:Double = 5000.00 // Variável do tipo Double
var numeroInt:Int = Int(numeroDouble) // Variável do tipo Int
var numeroString = String(numeroInt) // Variável do tipo String
```

## Operadores matemáticos e relacionais

Em Swift, temos alguns operadores básicos, comuns a praticamente todas as linguagens de programação. São eles:

- Operadores matemáticos

```+, -, *, /, %```

- Operadores relacionais

```>, <, >=, <=, !=, &&, ||, !(expressão)```

Não vou me alongar em explicar eles aqui, pois este não é um curso para iniciantes: você **deve** saber alguma coisa, mesmo que pouco.

## Interpolação e concatenação de strings

Como visto no Hello World, temos uma função chamada print, que imprime no console o que pedimos. Mas, e se quisermos utilizar **variáveis** dentro do print?

A forma que o Swift nos oferece é por usar uma barra invertida juntamente de dois parênteses, e dentro deles, o que desejamos adicionar.

```
var umCaraLegal = "Pedro Lemos"
print("Oi, eu sou \(umCaraLegal)!")

>>> Oi, eu sou Pedro Lemos!
```

Isso também serve para variáveis:

```
var nome = "Pedro Lemos"
var idade = 20
var mensagemExibir = "Oi, eu sou \(nome) e tenho \(idade) anos.
print(mensagemExibir)

>>> Oi, eu sou Pedro Lemos e tenho 20 anos.
```

E obviamente, podemos concatenar strings utilizando um método bem convencional, utilizado pela maioria das linguagens (e que em Java, é o mais utilizado).

```
var nome = "Pedro"
var sobrenome = "Lemos"
var nomeCompleto = nome + " " + sobrenome

print(nomeCompleto)

>>> Pedro Lemos
```

A desvantagem de utilizar esse método é que **não podemos concatenar tipos de dados diferentes**. O código abaixo nos retorna um erro, e não compila:

```
var nome = "Pedro"
var idade = 20
var mensagemExibir = "Eu sou " + nome + " e tenho " + idade + " anos"

print(mensagemExibir)

>>>

compiler.swift:3:53: error: binary operator '+' cannot be applied to operands of type 'String' and 'Int'
var mensagemExibir = "Eu sou " + nome + " e tenho " + idade + " anos"
```

Bom, já temos o básico para começar a nos aprofundar em Swift. Vamos prosseguir.
