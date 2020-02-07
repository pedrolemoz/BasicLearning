# O básico de JavaScript

> Consideração rápida: antes de aprender JavaScript, é recomendado que você aprenda HTML e CSS antes. Por quê? Iremos mexer com tags e seletores, por isso é necessário que você tenha uma breve noção.

## O Hello World

O primeiro programa em JavaScript deve se parecer com isso:

```javascript
<script>
    console.log("Hello World")
</script>
```

O código JavaScript deverá ficar dentro de uma tag ```<script>``` no seu HTML. Você deverá colocar a tag no final do ```<body>```, por questões de otimização (o código JavaScript pode impedir a página de ser carregada, em certos casos).

Apesar de podermos incorporar o código dentro do HTML, pode ser que ele fique poluído, por ter várias sintaxes diferentes num mesmo arquivo. Por isso, é sempre recomendado trabalhar com um **arquivo separado**, e dentro do HTML, indicar que ele existe:

```javascript
<script scr="index.js">
</script>
```

## Variáveis e tipos primitivos

Em JavaScript, temos alguns tipos primitivos de dados. São eles:

- ```Number```: **Números inteiros e reais (ponto flutuante).** Ex.: 4, 4.5
- ```String```: **Conjunto de caracteres.** Ex.: "*O Pedro é um cara legal!*"
- ```Boolean```: **Valores lógicos.** ```true``` **ou** ```false```**.**
- ```Object```: **Tipo especial do JavaScript. Quase tudo é objeto.** Ex.: var pessoa = {nome: "Pedro", idade: 20}
- ```undefined```: **Não definido. Similar ao NULL e void em outras linguagens.**
- ```NaN```: **Não é um número. Literalmente isso.**

O JavaScript interpreta os números de uma maneira peculiar. Não temos declarações de inteiros ou reais, eles são simplesmente ```Number```.

Entendidos os tipos primitivos, podemos passar para as variáveis.
Variáveis são **espaços de memória** alocados para armazenar temporariamente um dado.

Em JavaScript, a variável deve obedecer a seguinte sintaxe:

```javascript
var nomeDaVariavel = valorDaVariavel
```

Diferentemente de outras linguagens, em JavaScript, uma variável pode mudar o tipo do dado que armazena. Para isso, basta realizar o ```casting```. Entretanto, algumas conversões são um pouco perigosas. Veja o exemplo:

- Converter de inteiro para real:

```javascript
var minhaVariavel = 20 // Atribuindo um inteiro
minhaVariavel = parseFloat(minhaVariavel)

console.log(minhaVariavel)

>>> 20.0
```

Ele converteu! Mas agora vejamos o inverso:

```javascript
var minhaVariavel = 3.14 // Atribuindo um real
minhaVariavel = parseInt(minhaVariavel)

console.log(minhaVariavel)

>>> 3
```

Percebeu o que houve? A conversão funcionou, mas os números decimais foram perdidos. Fazer isso é útil em alguns casos, mas você deve ter cuidado.

Uma variável em JavaScript é capaz de **inferir qual o tipo de dado** que foi armazenado. Portanto, quando há uma variável que armazena uma uma operação entre dois elementos, o valor armazenado sempre será o que tem maior abrangência. Por exemplo:

```javascript
var minhaDivisao = 10.0 / 2
typeof(minhaDivisao)

>>> 'number'
```

Nesse caso, ele retornou ```number```, mas sabemos que o resultado de 10.0 por 2 é 5.0. Portanto, nossa variável é um número real.

## Operadores matemáticos e relacionais

Em Python, temos alguns operadores básicos, comuns a praticamente todas as linguagens de programação. São eles:

- Operadores matemáticos

```+, -, *, **, /, %```

- Operadores relacionais

```>, <, >=, <=, !=, &&, ||, !, in```

Nesta parte do tópico, em outras linguagens, como [Python3](https://github.com/pedrolemoz/basiclearning/blob/master/Python3/BasicoPython3.md), você notará que lidamos com divisões inteiras, potenciação e radiciação. O JavaScript não possui um operador dedicado a realizar divisões exatas, e nem um para elevar a potência. Para realizar essas ações, você deverá utilizar a biblioteca Math, com as funções ```ceil()```, ```floor()```, ```trunc()``` e ```pow()```. Veremos sobre ela no futuro.

Os operadores ```&&```, ```||```, ```!``` e ```in``` são operadores lógicos, e retornam ```true``` ou ```false```.

Não vou me alongar em explicar eles aqui, pois este não é um curso para iniciantes: você **deve** saber alguma coisa, mesmo que pouco.

## Interpolação e concatenação de strings

Como visto no Hello World, temos uma função chamada ```console.log()```, que imprime no console o que pedimos. Mas, e se quisermos utilizar **variáveis** dentro do print?

No JavaScript, temos algumas maneiras. Vou mostrar aqui as duas mais utilizadas.

- **Interpolação**

```javascript
var umCaraLegal = "Pedro Lemos"
console.log("Oi, eu sou $umCaraLegal")

>>> Oi, eu sou Pedro Lemos!
```

Eu pessoalmente prefiro interpolar, mas existe gosto pra tudo. Mas ainda podemos concatenar strings utilizando um método bem convencional, utilizado pela maioria das linguagens (e que em Java, é o mais utilizado).

- **Concatenação**

```javascript
var nome = "Pedro"
var sobrenome = "Lemos"
var nomeCompleto = nome + " " + sobrenome

console.log(nomeCompleto)

>>> Pedro Lemos
```

## Comentários

Para comentar uma linha de código:

```javascript
// Esse é um comentário de uma linha
```

Para comentar várias linhas de código:

```javascript
/*
Várias linhas de comentário

*/
```

Bom, já temos o básico para começar a nos aprofundar em JavaScript. Vamos prosseguir.
