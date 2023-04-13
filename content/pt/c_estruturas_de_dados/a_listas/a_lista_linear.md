---
weight: 1
title: "Lista linear (alocação contígua)"
date: 2023-04-12T01:00:36-03:00
draft: false
---

A lista linear (também chamada de lista com alocação contígua) é uma estrutura de dados que consiste em uma sequência de elementos armazenados em locais adjacentes na memória (como em um array). Essa estrutura permite não apenas o acesso sequencial aos elementos, como também o acesso direto por meio de seus endereços de memória, o que torna a busca e a recuperação de elementos eficientes.

## Usos comuns

- **Armazenamento de dados sequenciais:** A lista linear é útil quando se deseja armazenar e acessar elementos em uma sequência específica, como uma lista de itens em uma compra online, registros em um banco de dados ou pixels em uma imagem. É importante frisar que esse tipo de lista desepenha melhor quando o número de elementos já é conhecido no momento da alocação.

- **Implementação de outras estruturas de dados:** É possível implementar, por exemplo, pilhas (LIFO) e filas (FIFO) usando listas lineares com alocação contígua. Nesse caso, o que diferenciará essas estruturas da lista linear serão as operações específicas que cada uma desempenha.

## Vantagens

- **Acesso direto aos elementos:** Como cada elemento é armazenado em uma posição de memória contígua e possui um endereço único, o acesso aos elementos é direto e eficiente, com tempo de acesso constante, O(1).

- **Operações de busca e recuperação rápidas:** A busca e recuperação de elementos em uma lista linear são geralmente rápidas, especialmente quando se conhece a posição do elemento na lista, em outros casos, pode-se também  implementador algoritmos como a busca binária.

- **Implementação eficiente de pilhas e filas:** Em certos casos, a implementação de pilhas e filas usando listas lineares é eficiente, pois permite a inserção e remoção de elementos em tempo constante, O(1), sem a necessidade de realocação de memória sempre que o número máximo de elementos for conhecido.

## Desvantagens

- **Tamanho fixo:** A alocação contígua de elementos em uma lista linear pode levar a um tamanho fixo da lista, o que pode ser inconveniente quando há a necessidade de variar dinamicamente o número de elementos. Nesses casos seria necessária a realocação de memória e ajustes na estrutura da lista, o que pode ser custoso em termos de tempo e recursos.

- **Inserção e remoção ineficientes:** A inserção e remoção de elementos em uma lista linear podem ser ineficientes em termos de tempo, especialmente quando é necessário inserir ou remover elementos no meio da lista. Isso pode exigir o deslocamento de elementos subsequentes, resultando em tempo de execução proporcional ao tamanho da lista, O(n).

- **Desperdício de memória:** Se a lista linear não for totalmente preenchida, pode-se dizer que há desperdício de memória, pois os locais de memória não utilizados permanecem reservados, o que pode resultar em uso ineficiente da memória.

## Operações

- **Inserção:** Adicionar um novo elemento à lista em uma posição específica, como no início ou em uma posição intermediária pode exigir o deslocamento de elementos subsequentes para acomodar o novo elemento, o que pode afetar o desempenho da operação. Inserções no final da lista geralmente não impactam o desempenho, a não ser que o número máximo de elementos tenha sido atingido, nesse caso a inserção exigirá uma realocação da lista que impactará o desempenho da operação.

- **Remoção:** A exclusão de um elemento específico da lista pode exigir o deslocamento de elementos subsequentes para preencher o espaço vago e manter a continuidade da lista, o que também pode afetar o desempenho da operação.

- **Busca:** Localizar a posição de um elemento específico na lista com base em seu valor pode ser realizada de forma sequencial, percorrendo a lista elemento por elemento, ou de forma otimizada, como por meio de uma busca binária, dependendo da ordenação dos elementos na lista.

- **Acesso:** Recuperar o valor de um elemento em uma posição específica da lista com base em seu índice é uma operação direta e eficiente, entretanto recuperar um valor com base em algum outro dado pode exigir também uma operação de busca.

Além dessas operações básicas, outras operações mais avançadas podem ser implementadas em uma lista linear, como ordenação, concatenação, particionamento e inversão, dependendo dos requisitos específicos de cada aplicação.

## Implementação e uso em python

A lista é uma das estruturas de dados mais versáteis e amplamente utilizadas em Python, não sendo necessário implementá-la, pois já é uma parte fundamental da biblioteca padrão da linguagem. Para criar uma lista em Python, você pode usar colchetes ` [ ] ` e separar os elementos por vírgulas. Por exemplo:

```Python {linenos=table}
# Criando uma lista de números inteiros
numeros = [1, 2, 3, 4, 5]

# Criando uma lista de strings
frutas = ['maçã', 'banana', 'laranja']
```

Uma característica importante das listas é a capacidade de conter diferentes tipos de elementos, como números, strings, booleanos e até mesmo outras listas. Além disso, as listas em Python são indexadas, o que significa que você pode acessar elementos individuais pelo seu índice, começando por 0 para o primeiro elemento. Por exemplo:

```Python {linenos=table}
# Acessando elementos em uma lista pelo índice
print(numeros[0])  # Saída: 1
print(frutas[1])    # Saída: 'banana'
```

As listas da biblioteca padrão de Python também suportam índices negativos, o que permite acessar elementos a partir do final da lista. O índice -1 representa o último elemento, -2 representa o penúltimo e assim por diante. Por exemplo:

```Python {linenos=table}
# Acessando elementos em uma lista com índices negativos
print(numeros[-1])  # Saída: 5
print(frutas[-2])    # Saída: 'banana'
```

Outra operação comum em listas é a fatiamento (slicing), que permite extrair uma parte específica da lista com base em um intervalo de índices. O fatiamento em Python é feito usando colchetes e dois pontos ` : ` para separar os índices inicial, final e o passo. Por exemplo:

```Python {linenos=table}
# Fatiamento de listas
print(numeros[1:4])    # Saída: [2, 3, 4]
print(frutas[:2])      # Saída: ['maçã', 'banana']
print(numeros[::2])    # Saída: [1, 3, 5]
```

As listas em Python também possuem uma ampla variedade de métodos embutidos que podem ser usados para realizar várias operações, como adicionar elementos com a função `append()`, remover elementos com `remove()`, contar o número de ocorrências de um elemento com `count()`, ordenar os elementos com `sort()` e inverter a ordem dos elementos com `reverse()`, entre outros.

Além disso, as listas em Python são mutáveis, o que significa que você pode modificar seu conteúdo diretamente atribuindo um novo valor a um determinado índice. Por exemplo:

```Python {linenos=table}
# Modificando elementos em uma lista
numeros[2] = 30  # Altera o valor do terceiro elemento para 30
frutas.append('uva')  # Adiciona 'uva' ao final da lista de frutas
```

Porém, é importante notar que, ao fazer alterações em uma lista, o seu tamanho pode mudar, o que pode afetar outros índices e elementos subsequentes. Portanto, é necessário ter cuidado ao modificar uma lista para evitar erros de índice ou perda de dados.

Outra característica importante das listas é que elas são mutáveis por referência. Isso significa que, se uma lista for atribuída a uma variável e, em seguida, essa variável for atribuída a outra variável, ambas as variáveis estarão referenciando a mesma lista na memória. Portanto, qualquer modificação feita em uma variável afetará todas as outras variáveis que referenciam a mesma lista. Por exemplo:

```Python {linenos=table}
# Mutabilidade por referência em listas
lista1 = [1, 2, 3]
lista2 = lista1  # lista2 faz referência à mesma lista que lista1

lista1[0] = 10  # Modifica o primeiro elemento de lista1

print(lista1)  # Saída: [10, 2, 3]
print(lista2)  # Saída: [10, 2, 3], pois lista2 faz referência à mesma lista que lista1
```

Para criar uma cópia independente de uma lista, é necessário usar o método `copy()` ou a função `list()` para criar uma nova lista com os mesmos elementos. Por exemplo:

```Python {linenos=table}
# Criando uma cópia independente de uma lista
lista1 = [1, 2, 3]
lista2 = lista1.copy()  # Cria uma nova lista (cópia) com os mesmos elementos de lista1

lista1[0] = 10  # Modifica o primeiro elemento de lista1

print(lista1)  # Saída: [10, 2, 3]
print(lista2)  # Saída: [1, 2, 3], pois lista2 é uma cópia independente de lista1
```

Em resumo, as listas são uma estrutura de dados versátil e poderosa em Python, que permite armazenar e manipular coleções de elementos de forma flexível. Elas suportam operações de indexação, fatiamento, e têm uma ampla variedade de métodos embutidos para realizar várias operações. É importante estar ciente da mutabilidade por referência e das possíveis mudanças no tamanho da lista ao fazer modificações. Com um bom entendimento das listas em Python, é possível realizar muitas tarefas de processamento de dados de forma eficiente e conveniente.