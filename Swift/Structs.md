# Structs em Swift

Em Swift, temos uma estrutura chamada de Struct, que lembra muito uma Classe (são extremamente parecidas, com poucas diferenças). Ela se define pela palavra reservada ```struct```, o nome do struct e um par de chaves. A maior diferença de um struct para uma classe é a forma que lida com dados: aqui, tudo é por valor, nada é por referência (como nas classes). Também, aqui não temos herança e nem polimorfismo.

```
struct nomeDoStruct {
    algumaCoisa
}
```

Podemos definir atributos dentro de um struct, da mesma forma que declaramos strings:

```
struct nomeDoStruct {
    let linguagemLegal = "Swift"
}
```

Para chamar um atributo, podemos usar a seguinte sintaxe:

```nomeDoStruct.atributo```

Atente-se ao ponto. É com ele que podemos fazer isso.

Podemos pedir informações ao usuário para inicializar o struct, mas não precisamos de um método construtor – ele já vem por padrão na definição do struct:

```
struct Pessoa {
    var nome: String
    var idade: Int
}

let pedro = Pessoa(nome: "Pedro", idade: 20)
```

Também podemos ter funções dentro de um struct:

```
struct Pessoa {
    var nome: String
    var idade: Int
    
    mutating func passaAno(){
        self.idade += 1
    }
}

let pedro = Pessoa(nome: "Pedro", idade: 20)
```

"Ué, self? Então isso é uma classe?"
Não, não é uma classe, mas parece muito. O self do struct é "imutável", ao contrário do que acontece nas classes, pela natureza de ser value type. Para que consigamos mudar o valor usando uma função, temos que usar a palavra reservada ```mutating``` antes de ```func```.

## Demonstrando o ```value type``` do struct

```
struct Pessoa {
    var nome: String
    var idade: Int
    
    func dizerOi(){
        print("Oi, eu sou \(nome)")
    }
}

var pedro = Pessoa(nome: "Pedro", idade: 20)
var lucas = pedro
lucas.nome = "Lucas"

pedro.dizerOi()
lucas.dizerOi()

>>>
Oi, eu sou Pedro
Oi, eu sou Lucas
```

Observe que a variável ```pedro``` não é referenciada, e sim, copiada para ```lucas```. Essa é a diferença entre ```value type``` e ```reference type```.
