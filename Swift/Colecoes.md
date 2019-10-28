# Coleções
## Arrays (ou vetor)

A principal coleção que temos em Swift são os **arrays**. Um array é um conjunto de dados de um tipo único que possui um índice atrelado.

A sintaxe básica de um array é:

### Inicializar e modificar um array

- Para inicializar um array sem especificar os elementos:

```var meuArray = [tipoDado]()```

- Para inicializar um array com os elementos já inseridos:

```var meuArray = {1, 2, 3, 4, 5}```

- Para inicializar um array com uma quantidade de elementos pré-definida:

```var meuArray = Array(repeating = 0, count: quantidade)```

Usamos o índice para acessar e modificar os elementos do array:

```
var meuArray = ["Pedro", "Objective-C"]
meuArray[1] = "Swift"
print("Elemento 0: \(meuArray[0])\nElemento 1: \(meuArray[1])")

>>>
Elemento 0: Pedro
Elemento 1: Swift
```

Note que nós conseguimos modificar o valor da segunda posição do array. Isso não seria possível caso tentássemos substituir por um valor de tipo diferente do array – um inteiro, por exemplo.

### Métodos dos arrays

Se você tiver estudado estruturas de dados, saberá que um array é uma lista encadeada. Para tanto, temos todos os métodos básicos para trabalhar com ela.

- Adicionar elementos ao fim do array:

```meuArray.append(novoElemento)```

- Adicionar elementos em uma determinada posição:

```meuArray.append(novoElemento, at: posicao```

- Remove elementos do início do array:

```meuArray.removeFirst()```

- Remover elementos do fim do array:

```meuArray.removeLast()```

- Remover elementos de uma determinada posição:

```meuArray.remove(at: posicao)```

- Acessar o primeiro elemento do array:

```meuArray.first```

- Acessar o último elemento do array:

```meuArray.last```

- Verificar se um array está vazio:

```meuArray.isEmpty()```

- Obter o número de elementos de um array:

```meuArray.count```

- Obter a capacidade máxima de armazenamento do array:

```meuArray.capacity```

- Verificar se um elemento está dentro do array:

```meuArray.contains()```

- Retorna o menor elemento do array:

```meuArray.min()```

- Retorna o maior elemento do array:

```meuArray.max()```

- Ordena o array:

```meuArray.sort()```

- Inverte a ordem das posições de um array:

```meuArray.reverse()```

### Iterar sobre um array

Para iterar em um array como já visto no tópico sobre [Estruturas básicas do Swift](https://github.com/pedrolemoz/basiclearning/blob/master/Swift/EstruturasSwift.md), podemos usar o laço ```forEach```:

```
for i in meuArray{
    algumaCoisa
}
```

Alternativamente, podemos usar o laço ```for``` convencional e trabalhar com o índice, como em algumas linguagens:

```
for i in 0...meuArray.count{
    print(meuArray[i])
}
```

## Sets

Um set é basicamente uma coleção de elementos. Para usar um set, você deverá especificar o seu tipo. Um set é bem comparável a um conjunto matemático. Pegue o conjunto dos números inteiros não-negativos. Ele é um conjunto com um tipo bem definido, em que não se admite o número -π, por exemplo, pois trata-se de um irracional.

### Inicializar e modificar um Set

Para inicializar um set vazio, use a sintaxe abaixo:

```var meuSet = Set<tipoDado>()```

Para inicializar um set com valores:

```var meuSet: Set = ["Elemento 1", "Elemento 2"]```

É importante observar um detalhe: um set vazio não pode ter seu tipo de dado inferido, mas um que está sendo alimentado com elementos, sim. O Swift se encarrega de fazer isso por nós.

Observe que adicionamos os elementos em nosso set usando a sintaxe de colchetes. De forma análoga, podemos esvaziar o set simplesmente por usar:

```meuSet = []```

O tipo do set é imutável, e continuará sendo ```String```, independente do que façamos.

Podemos acessar algumas coisas dos sets usando alguns métodos que ele nos fornece. Alguns são os mesmos que usamos para os Arrays.

Adicionar um elemento:

```meuSet.insert()```

Remover um elemento:

```meuSet.remove()```

Contar a quantidade de elementos:

```meuSet.count()```

Verificar se o conjunto está vazio:

```meuSet.isEmpty()```

Verificar se determinado elemento está contido no conjunto:

```meuSet.contains()```

### Iterar sobre um set

Assim como em um Array, usamos o ```forEach``` para iterar sobre um set:

```
for i in meuSet{
    algumaCoisa
}
```

Com já mencionado, sets não possuem índices. Então, não podemos fazer igual como nos Arrays.

A princípio, nosso set é um conjunto desordenado. Porém, suponha que estamos iterando em um laço de repetição. Como iremos saber a ordem de cada elemento? Existe uma maneira de ter controle sobre isso? Observe o código abaixo:

```
for i in meuArray.sorted(){
    algumaCoisa
}
```

Não estamos trabalhando com um conjunto desordenado de dados, e sim, em um que está organizado em ordem crescente, para números, e em ordem alfabética para Strings. Note que para Strings, é usada a tabela ASCII para realizar essa operação. Isso significa dizer que essa ordenação é ```case sensitive```. Existem muitas coisas para serem mencionadas sobre o ```sorted```. Você pode passar funções anônimas (conhecidos como lambda, em algumas linguagens, como o Python) e fazer algumas outras coisas. Veja mais sobre isso [clicando aqui](https://docs.swift.org/swift-book/LanguageGuide/Closures.html).
