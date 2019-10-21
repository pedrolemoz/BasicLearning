# Coleções
## Arrays (ou vetor)

A principal coleção que temos em Swift são os **arrays**. A sintaxe básica de um array é:

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

- Remover elementos do fim do array:

```meuArray.removeLast()```

- Remover elementos de uma determinada posição

```meuArray.remove(at: posicao)```
