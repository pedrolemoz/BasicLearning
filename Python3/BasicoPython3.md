# O básico de Python3

## O Hello World

O primeiro programa em Python deve se parecer com isso:

```python
print("Hello World")
```

Sim, é tão simples quanto escrever em inglês.

## Variáveis e tipos primitivos

Em Python, temos alguns tipos primitivos de dados. São eles:

- ```int```: **Números inteiros.** Ex.: 4.
- ```float```: **Números reais (ponto flutuante).** Ex.: 4.5.
- ```str```: **Conjunto de caracteres.** Ex.: "*O Pedro é um cara legal!*"
- ```bool```: **Valores lógicos** ```True``` **ou** ```False```**.**

> Nota: se um número real não tiver seu tipo especificado, em Python3, o valor padrão atribuído será ```float```.

Entendidos os tipos primitivos, podemos passar para as variáveis.
Variáveis são **espaços de memória** alocados para armazenar temporariamente um dado.

Em Python, a variável deve obedecer a seguinte sintaxe:

```python3
nomeDaVariavel = valorDaVariavel
```

Diferentemente de outras linguagens, em Python, uma variável pode mudar o tipo do dado que armazena. Para isso, basta realizar o ```casting```. Entretanto, algumas conversões são um pouco perigosas. Veja o exemplo:

- Converter de ```int``` para ```float```:

```python3
minhaVariavel = 20 # Atribuindo um inteiro
minhaVariavel = float(minhaVariavel)

print(minhaVariavel)

>>> 20.0
```

Ele converteu! Mas agora vejamos o inverso:

```python3
minhaVariavel = 3.14 # Atribuindo um real
minhaVariavel = int(minhaVariavel)

print(minhaVariavel)

>>> 3
```

Percebeu o que houve? A conversão funcionou, mas os números decimais foram perdidos. Fazer isso é útil em alguns casos, mas você deve ter cuidado.

Uma variável em Python é capaz de **inferir qual o tipo de dado** que foi armazenado. Portanto, quando há uma variável que armazena uma uma operação entre dois elementos, o valor armazenado sempre será o que tem maior abrangência. Por exemplo:

```python3
minhaDivisao = 10.0 / 2
type(minhaDivisao)

>>> <class 'float'>
```

Nesse caso, ```float``` é mais abrangente que ```int```. Logo, o tipo da variável é ```float```. Mas e se quiséssemos que o tipo da variável fosse um inteiro? Veremos a seguir os operadores do Python, onde responderemos essa dúvida.

## Operadores matemáticos e relacionais

Em Python, temos alguns operadores básicos, comuns a praticamente todas as linguagens de programação. São eles:

- Operadores matemáticos

```+, -, *, **, /, //, %```

- Operadores relacionais

```>, <, >=, <=, ==, !=, and, or, not, in```

O operador ```==``` serve para verificar igualdade:

```python3
x = 10

if x == 10:
    print(True)
else:
    print(Falar)

>>> True
```

Para forçar uma divisão inteira, temos o operador ```//```. Dessa forma, em nosso exemplo anterior, a variável teria o tipo inteiro. Temos também o operador ```**```, que eleva um número a potência de outro:

```python3
print(5 ** 5)

>>> 25
```

Mas e se quiséssemos tirar a raiz de algum número? Bom, você deverá lembrar que a potenciação é inversamente proporcional à radiciação. Então, basta elevar por 0.5 (ou ½):

```python3
print(25 ** 0.5)

>>> 5
```

Os operadores ```and```, ```or```, ```not``` e ```in``` são operadores lógicos e retornam ```True``` ou ```False```.

Não vou me alongar em explicar eles aqui, pois este não é um curso para iniciantes: você **deve** saber alguma coisa, mesmo que pouco.

## Interpolação e concatenação de strings

Como visto no Hello World, temos uma função chamada print, que imprime no console o que pedimos. Mas, e se quisermos utilizar **variáveis** dentro do print?

No Python3, temos algumas maneiras. Vou mostrar aqui as duas mais utilizadas.

- **.format()** (método antigo)

```python3
umCaraLegal = "Pedro Lemos"
print("Oi, eu sou {}".format(umCaraLegal))

>>> Oi, eu sou Pedro Lemos!
```

- **f-Strings** (do Python3.6 em diante)

```python3
umCaraLegal = "Pedro Lemos"
print(f"Oi, eu sou {umCaraLegal}")

>>> Oi, eu sou Pedro Lemos!
```

Eu pessoalmente prefiro as **f-Strings**, mas existe gosto pra tudo. E obviamente, podemos concatenar strings utilizando um método bem convencional, utilizado pela maioria das linguagens (e que em Java, é o mais utilizado).

```python3
nome = "Pedro"
sobrenome = "Lemos"
nomeCompleto = nome + " " + sobrenome

print(nomeCompleto)

>>> Pedro Lemos
```

A desvantagem de utilizar esse método é que **não podemos concatenar tipos de dados diferentes**. O código abaixo nos retorna um erro:

```python3
nome = "Pedro"
idade = 20
mensagemExibir = "Eu sou " + nome + " e tenho " + idade + " anos"

print(mensagemExibir)

>>>
Traceback (most recent call last):
File "<stdin>", line 3, in <module>
TypeError: can only concatenate str (not "int") to str
```

Bom, já temos o básico para começar a nos aprofundar em Python. Vamos prosseguir.
