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
