# Classes

Para compreender bem o conceito de classe, é necessário introduzir a orientação a objetos.

### Introdução a orientação a objetos

Orientação a objetos nada mais é do que tentar modelar os problemas do mundo real de forma que eles sejam bem detalhados, bem definidos, e tenham as características que encontramos quando olhamos para eles de verdade.

Em orientação a objetos, nós temos o que chamamos de classes. Essas classes caracterizam o que mais utilizamos – os objetos. Os objetos possuem atributos, ou melhor dizendo, características que são inerentes a eles. Os objetos também são capazes de fazer algumas coisas, e por isso, têm métodos.

Podemos pensar em uma classe como a estrutura que vai definir algo. Por exemplo, suponha que queremos definir o que é uma pessoa. Que características as pessoas possuem? No mínimo, possuem um nome e sobrenome, uma idade, uma cor de pele, uma cor e tipo de cabelo. Tudo isso são características de uma pessoa. Então, definimos tudo isso dentro da nossa classe. Para que tenhamos um objeto do tipo Pessoa, devemos dizer quais são essas características básicas.

Um objeto é uma instância da classe. Como já mencionado antes, um objeto pode possuir atributos e métodos. Os métodos são coisas que aquele objeto pode fazer. Por exemplo, uma pessoa pode comer, falar, dormir. Todos esses podem ser caracterizados como métodos, ou ações dessa pessoa.

Existem algumas coisas que são privadas nossas, como por exemplo, nossos segredos. Existem outras informações que apenas um grupo específico de pessoas podem ter acesso. Um exemplo disso seria a nossa senha do banco. Somente pessoas de confiança podem ter essa informação, como um cônjuge. Já outras coisas triviais, qualquer pessoa pode saber, como o nosso nome. No Swift, temos os modificadores de acesso para fazer esse tipo de restrição. Veremos mais sobre eles em breve. Existem algumas outras relações entre classes, que veremos a seguir.

### Definição de herança

Quando um casal decide ter um filho, a criança herda características tanto do pai como da mãe. Se o pai tem cabelo liso e preto, e a mãe tem olhos puxados, é muito provável que o filho tenha essas características dos dois. Isso é herança. Na orientação a objetos, isso acontece quando uma classe possui características de outras. Melhor dizendo, uma classe é filha de outra. Porém, uma classe filha pode ter características novas além das que os pais possuem. Por exemplo, o filho pode nascer com olhos azuis e ser alto, mesmo que os pais não tenham essa característica. Ele sobrescreve o que foi herdado com uma caraterística nova. Veremos mais a fundo sobre isso em breve.

### Definição de polimorfismo

Uma coisa pode ser chamada de diferentes nomes dependendo da região. No Nordeste, o nome que se dá para a fécula de mandioca preparada na frigideira é tapioca. Na região Norte, se chama beiju. Mas continua sendo exatamente a mesma coisa e tendo o mesmo sabor.

### Sintaxe básica de uma classe

Agora que definimos o que é uma classe, de acordo com os conceitos de orientação a objetos, vamos ver a sintaxe em Swift:

```
class minhaClasse {
    var meuNome: String
    
    init(nome: String) {
        self.meuNome = nome
    }
    
    func dizerOi() {
        print("Olá, meu nome é \(self.meuNome)!")
    }
}

let pedro = minhaClasse(nome: "Pedro")
pedro.dizerOi()
>>>
Olá, meu nome é Pedro!
```

Achou complicado? Acredite, não é. Temos a nossa classe, que possui um atributo, o ```meuNome```, e temos um **método construtor** que fica responsável de pedir uma String do usuário e colocar dentro desse atributo. Para fazer isso, usamos o ```self```. Logo abaixo, a função ```dizerOi``` acessa o atributo e exibe uma mensagem na tela. Criamos uma instância dessa classe em uma constante chamada ```pedro```, e passamos o valor "Pedro" para a variável ```nome```. Assim, ao chamarmos o método ```dizerOi()```, ele exibe a mensagem.
