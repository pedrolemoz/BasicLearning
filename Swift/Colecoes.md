# Coleções

Esse é um tópico bem extenso, tire um tempo para ler com calma.

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

Usamos o **índice** para acessar e modificar os elementos do array:

```
var meuArray = ["Pedro", "Objective-C"]
meuArray[1] = "Swift"
print("Elemento 0: \(meuArray[0])\nElemento 1: \(meuArray[1])")

>>>
Elemento 0: Pedro
Elemento 1: Swift
```

Note que nós **conseguimos** modificar o valor da segunda posição do array. Isso não seria possível caso tentássemos substituir por um valor de tipo diferente do array – um inteiro, por exemplo.

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

### Métodos dos arrays

Se você tiver estudado estruturas de dados, saberá que **um array é uma lista encadeada**. Para tanto, temos todos os métodos básicos para trabalhar com ela.

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

## Sets

Um set é basicamente uma **coleção de elementos**. Para usar um set, você deverá especificar o seu tipo. Um set é bem comparável a um **conjunto matemático**. Pegue o conjunto dos números inteiros não-negativos. Ele é um conjunto com um tipo bem definido, em que não se admite o número π, por exemplo, pois trata-se de um irracional.

### Inicializar e modificar um Set

Para inicializar um set vazio, use a sintaxe abaixo:

```var meuSet = Set<tipoDado>()```

Para inicializar um set com valores:

```var meuSet: Set = ["Elemento 1", "Elemento 2"]```

É importante observar um detalhe: um set vazio **não** pode ter seu tipo de dado inferido, mas um que está sendo alimentado com elementos, sim. O Swift se encarrega de fazer isso por nós.

Observe que adicionamos os elementos em nosso set usando a sintaxe de colchetes. De forma análoga, podemos esvaziar o set simplesmente por usar:

```meuSet = []```

O tipo do set é **imutável**, e continuará sendo ```String```, independente do que façamos.

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

### Iterar sobre um Set

Assim como em um Array, usamos o ```forEach``` para iterar sobre um set:

```
for i in meuSet{
    algumaCoisa
}
```

Com já mencionado, sets **não possuem índices**. Então, não podemos fazer igual como nos Arrays.

A princípio, nosso set é um **conjunto desordenado**. Porém, suponha que estamos iterando em um laço de repetição. Como iremos saber a ordem de cada elemento? Existe uma maneira de ter controle sobre isso? Observe o código abaixo:

```
for i in meuArray.sorted(){
    algumaCoisa
}
```

Não estamos trabalhando com um conjunto desordenado de dados, e sim, em um que está **organizado em ordem crescente**, para números, e em ordem alfabética para Strings. Note que para Strings, é usada a tabela ASCII para realizar essa operação. Isso significa dizer que essa ordenação é ```case sensitive```. Existem muitas coisas para serem mencionadas sobre o ```sorted```. Você pode passar funções anônimas (conhecidos como lambda, em algumas linguagens, como o Python) e fazer algumas outras coisas. Veja mais sobre isso [clicando aqui](https://docs.swift.org/swift-book/LanguageGuide/Closures.html).


### Operações fundamentais de um Set

> Nota: agora o autor vai começar a falar de matemática, então, caso tenha faltado as aulas de matemática discreta, seja cuidadoso!

Lembra que comparei um set a um conjunto matemático? Que disse que ele é bem semelhante? Pois bem, não foi por acaso. Em um set, temos algumas operações de conjuntos, algumas das quais são essenciais. Veja abaixo, com a ajuda de alguns diagramas de Venn.

<p align="center">
  <img src="https://docs.swift.org/swift-book/_images/setVennDiagram_2x.png" alt="Operações com conjuntos."/>

Perceba que é necessário que tenhamos 2 sets para realizar essas operações.

Antes de voltar para o código, vamos definir as operações.

*Sejam*

![formula](https://render.githubusercontent.com/render/math?math=%5CA%2C%20%5CB%20%5Cin%20%5CU%2C%20x%20%5Cin%20%5Cmathbb%20R)

#### Definição de união

Conjunto dos elementos que pertencem a um dos dois conjuntos (A ou B). Matematicamente:

![formula](https://render.githubusercontent.com/render/math?math=%5CA%20%5Ccup%20%5CB%20%3D%20%5C%7Bx%20%5Cin%20%5CU%20%5Cmid%20x%20%5Cin%20%5CA%20%5Clor%20x%20%5Cin%20%5CB%20%5C%7D)

#### Definição de intercessão

Conjunto dos elementos que pertencem simultaneamente a A e B. Matematicamente:

![formula](https://render.githubusercontent.com/render/math?math=%5CA%20%5Ccap%20%5CB%20%3D%20%5C%7Bx%20%5Cin%20%5CU%20%5Cmid%20x%20%5Cin%20%5CA%20%5Cland%20x%20%5Cin%20%5CB%20%5C%7D)

#### Definição de diferença

Conjunto dos elementos que pertencem a A, mas não pertencem a B. Matematicamente:

![formula](https://render.githubusercontent.com/render/math?math=%5CA%20-%20%5CB%20%3D%20%5C%7Bx%20%5Cin%20%5CU%20%5Cmid%20x%20%5Cin%20%5CA%20%5Cland%20x%20%5Cnotin%20%5CB%20%5C%7D)

#### Definição de diferença simétrica

Conjunto dos elementos que pertencem a A e B, mas que não pertencem a intercessão entre A e B. Matematicamente:

![formula](https://render.githubusercontent.com/render/math?math=%5CA%20%5Ctriangle%20%5CB%20%3D%20%5C%7B(%5CA%20%5Ccup%20%5CB)%20-%20(%5CA%20%5Ccap%20%5CB)%5C%7D)

Agora que já definimos o que é cada uma das operações, vejamos um pouco da sintaxe:

#### União:

```meuSet.union(meuOutroSet)```

#### Intercessão:

```meuSet.intersection(meuOutroSet)```

#### Diferença:

```meuSet.subtracting(meuOutroSet)```

#### Diferença simétrica:

```meuSet.symetricDifference(meuOutroSet)```


### Relações entre conjuntos

Existem algumas relações entre os conjuntos, dado um conjunto universo em que todos estão inclusos. Observe a imagem abaixo:

<p align="center">
  <img src="https://docs.swift.org/swift-book/_images/setEulerDiagram_2x.png" alt="Relações entre conjuntos."/>

Esta imagem mostra três conjuntos, os quais tem algumas relações interessantes.

O conjunto B é **subconjunto** (ou está contido em) de A, pois todos os elementos de B também pertencem a A, e o conjunto A é **superconjunto** (ou contém) de B, que por sua vez é **subconjunto** do conjunto universo. B e C são dois **conjuntos disjuntos**, pois não há relação alguma entre eles, e não compartilham elementos. B é igual a ![formula](https://render.githubusercontent.com/render/math?math=A%20\cap%20B).

A sintaxe das relações em Swift é a seguinte:

#### Verificar se um set é subconjunto de outro:

```meuSet.isSubset(of: meuOutroSet)```

#### Verificar se um set é superconjunto de outro:

```meuSet.isSuperset(of: meuOutroSet)```

#### Verificar se os sets são disjuntos:

```meuSet.isDisjoint(with: meuOutroSet)```

#### Verificar se um set é igual a outro:

```meuSet == meuOutroSet```

### Dicionários

Os dicionários armazenam dados, assim como os Arrays e os Sets. A grande diferença está em que cada dado possui um **identificador único**. É semelhante ao índice de um array, porém, este índice é definido por você, programador.

#### Inicializar e modificar um dicionário

A sintaxe para criar um dicionário vazio é:

```var meuDict = [tipoChave: tipoValor]()```

Para criar um dicionário com valores:

```var meuDict: [tipoChave: tipoValor] = [chave1: valor1, chave2: valor2]```

Para acessar um dicionário, você pode usar a chave como índice:

```
var meuDict = [String: String]()
meuDict["Pedro"] = "Programador"
print(meuDict["Pedro"])
>>>
Programador
```

Você pode usar alguns métodos dos Arrays e Sets, como o ```count```, ```contains``` e outros. Porém, para os dicionários existem outros. Relembre o código anterior. Suponha que você deseje mudar o conteúdo da chave "Pedro". Observe:

```
let valorAnterior = meuDict.updateValue("Programador inteligente", forKey: "Pedro")
print("O valor anterior era \(valorAnterior)")
>>>
O valor anterior era Programador
```

Note uma coisa interessante: além de mudar o valor da chave, esse método **retorna o valor anterior** que essa chave tinha. Útil pra quando desejarmos saber se houve ou não uma alteração.

Para remover um valor de um dicionário, temos duas possibilidades. A primeira é acessar a chave e definir o valor dela como ```nil``` (valor nulo):

```meuDict["Pedro"] = nil```

Também podemos usar um método pra isso:

```meuDict.removeValue(forKey: "Pedro")```

Para remover todos os valores de um dicionário:

```meuDict = [:]```

### Iterando sobre um dicionário

Se você já tem conhecimento de dicionários em Python 3, vai compreender facilmente como iterar em um dicionário. Temos algumas alternativas:

```
let meuDict = ["Pedro": "Programador", "Lucas": "Designer"]

for (chave, valor) in meuDict{
    print("\(chave): \(valor)")
}
>>>
Pedro: Programador
Lucas: Designer
```

Certo, mas e se eu quiser acessar só as chaves ou só os valores? Exatamente a mesma coisa, mas adicione ```.keys``` ou ```.values```.

```
let meuDict = ["Pedro": "Programador", "Lucas": "Designer"]

for chaves in meuDict.keys{
    print("\(chaves)")
}

for valores in meuDict.values{
    print("\(valores)")
}
>>>
Pedro
Lucas
Programador
Designer
```

Até que enfim chegamos ao final desse tópico! Bem extenso, mas também é essencial saber.

> Nota: as imagens dos diagramas utilizados são da própria documentação do Swift
