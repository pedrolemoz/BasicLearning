# Funções

O uso de funções é essencial para que possamos ter uma boa legibilidade e organização de nosso código.

Uma função deverá ser escrita depois de todas as variáveis que ela utiliza terem sido declaradas.

## Funções que não retornam nada

A sintaxe para uma função que não retorna valor algum é a seguinte:

```
func nomeDaFuncao() {
    algumaCoisa
}
```

Perceba que nós temos sempre a palavra reservada ```func``` para indicar que se trata de uma função. Também, após o nome da função, temos um par de colchetes. Eles servirão para pegar argumentos do usuário, como veremos mais a frente. A seguir, temos um abrir e fechar de chaves, que é o nosso bloco de código. É essencial que exista um espaço entre o nome da função e as chaves.

## Funções que retornam algum dado

Caso deseje retornar algo para o usuário, você deverá especificar o tipo de dado que irá retornar, e usar a palavra reservada ```return```.

```
func nomeDaFuncao() -≥ Int {
    return meuInteiro
}
```

Como você pode perceber, a sintaxe mudou um pouco. Agora, temos o ```->```, que é usado para indicar o **tipo da variável** que iremos retornar. Diferentemente de outras linguagens, nós indicamos isso **no final**, e não no começo da definição.

## Funções que pedem argumentos e retornam dados

Este é tipo mais comum de função. Nela, você obtém dados de uma variável externa, e que pode usar para trabalhar com a sua função. Note que, ao passar um valor, uma cópia dele é feita na memória, para que a função possa utilizá-lo.

```
func nomeDaFuncao(minhaVariavel: Int) -≥ Int {
    return meuInteiro * meuInteiro
}
```

A estrutura desse tipo de função segue o padrão das outras, porém, você deve dizer que quer uma variável e especificar o tipo dela.

### Exemplificando

Para fixar bem todos os tópicos vistos até agora, vamos criar um algoritmo simples de boletim, mas com a ajuda de funções.

```
var alunos = [String]()
var notas = [Double]()

func adicionarAluno(nome: String, nota: Double) {
    alunos.append(nome)
    notas.append(nota)
}

func exibirBoletim() {
    print("Aluno\t Nota\tSituação\n")
    var situacao: String
    for i in 0...alunos.count - 1 {
        if notas[i] > 7 {
            situacao = "Aprovado"
        }
        else if notas[i] < 3 {
            situacao = "Reprovado"
        }
        else {
            situacao = "Avaliação Final"
        }
        print("\(alunos[i])\t \(notas[i]) \t\(situacao)")
    }
}

adicionarAluno(nome: "Pedro", nota: 10.0)
adicionarAluno(nome: "Carlos", nota: 6.0)
adicionarAluno(nome: "Lucas", nota: 2.0)

exibirBoletim()

>>>
Aluno	 Nota	Situação

Pedro	 10.0 	Aprovado
Carlos	 6.0 	Avaliação Final
Lucas	 2.0 	Reprovado
```
Este algoritmo é bem simples, mas pode ser simplificado ainda mais. Observe:

```
var alunos = [String]()
var notas = [Double]()

func adicionarAluno(_ nome: String, _ nota: Double) {
    alunos.append(nome)
    notas.append(nota)
}

func verificarSituacao(_ nota: Double) -> String {
    if nota > 7 {
            return "Aprovado"
        }
        else if nota < 3 {
            return "Reprovado"
        }
        else {
            return "Avaliação Final"
        }
}

func exibirBoletim() {
    print("Aluno\t Nota\tSituação\n")
    var situacao: String
    for i in 0...alunos.count - 1 {
        var situacao = verificarSituacao(notas[i])
        print("\(alunos[i])\t \(notas[i]) \t\(situacao)")
    }
}

adicionarAluno("Pedro", 10.0)
adicionarAluno("Carlos", 6.0)
adicionarAluno("Lucas", 2.0)

exibirBoletim()

>>>
Aluno	 Nota	Situação

Pedro	 10.0 	Aprovado
Carlos	 6.0 	Avaliação Final
Lucas	 2.0 	Reprovado
```
Veja uma diferença interessante. No primeiro exemplo, o argumento que pedíamos era:

```func adicionarAluno(nome: String, nota: Double)```

Para passar o argumento para a funcão, tínhamos que escrever o nome da variável e seu valor:

```adicionarAluno(nome: "Pedro", nota: 10.0)```

Isso é um pouco inconveniente. Mas, com nossa melhoria, o código passou a ter um *underline* (`_`) antes do no nome da variável:

```func adicionarAluno(_ nome: String, _ nota: Double)```

Assim, nosso código principal ficou:

```adicionarAluno("Pedro", 10.0)```

O uso do *underline* é opcional, mas faz uma grande diferença na implementação.

Este é o básico sobre funções. Em resumo:

- ```func``` é a palavra reservada que você usa para definir uma função.
- Os argumentos dentro de uma função devem seguir a sintaxe ```nome: tipo```.
    - Nesse caso, na chamada da função, você deve usar a sintaxe ```nomeDaFuncao(variavel: tipo)```.
    - Para não precisar especificar o nome da variável, use um *underline* antes no nome, como na sintaxe ```_ nome: tipo```.
- ```return``` é a palavra reservada para que você retorne valores.
    - Você deverá especificar o tipo de valor que será retornado, usando a sintaxe ```-> tipo```.
