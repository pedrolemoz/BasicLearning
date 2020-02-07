
# Coleções

## Listas

Como vimos anteriormente, podemos armazenar informações em nosso programa por meio de variáveis. Mas, uma variável consegue armazenar apenas um único dado por vez. Suponha que tenhamos que armazenar o nome de três pessoas. Seriam então, 3 variáveis, com nomes distintos. Porém, imagine que queremos adicionar 50 nomes. E agora? Iríamos criar 50 variáveis? E se a quantidade de pessoas que serão adicionadas fosse indeterminada? Bom, para essas e outras situações, existem as listas. As listas são estruturas que conseguem armazenar uma infinidade de elementos, como se fosse uma variável composta por pequenos espaços, para as variáveis que estão dentro da lista, e os tornando acessíveis por meio de um índice.

### Inicializar e modificar uma lista

Para inicializar uma lista de elementos vazia, a sintaxe é a seguinte:

```minhaLista = []```

Ou, se preferir:

```minhaLista = list()```

Para inicializar uma lista já com alguns elementos dentro:

```minhaLista = ["Elemento 1", 2, 3.0]```

Para acessar um elemento dentro da lista, usamos um par de colchetes, e dentro deles, o índice do elemento:

```python3
minhaLista = ["Elemento 1", 2, 3.0]
print(minhaLista[0])
>>> Elemento 1
```

Note que o primeiro elemento possui índice zero. Assim, cada elemento tem índice ```n - 1```.

E se quiséssemos modificar o conteúdo de uma lista?

```python3
minhaLista = ["Elemento 1", 2, 3.0]
minhaLista[0] = "Elemento alterado"
print(minhaLista[0])
>>> Elemento alterado
```
Com o auxílio dos índices, podemos fazer quase qualquer coisa em Python!

Se você já tem alguma experiência com Java ou C, deve ter notado uma particularidade: podemos adicionar tipos de dados distintos dentro da nossa lista! Isso é uma capacidade que o Python tem, e é extremamente útil e conveniente.
