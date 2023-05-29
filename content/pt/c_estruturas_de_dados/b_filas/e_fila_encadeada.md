---
weight: 5
title: "Fila encadeada"
date: 2023-04-12T01:00:36-03:00
draft: false
---
<!--    Documentação - Fila
Grupo:      Hugo Leonardo Viana
            Jairo Pedro Santana
            Mateus Borges e Guimarães
            Willy Brener Alves Oliveira-->
<h2> Conteúdo </h2>
{{< toc "format=html" >}}


Uma fila encadeada é uma estrutura de dados linear usada na computação para armazenar elementos onde a inserção e exclusão ocorrem em extremidades diferentes. É um tipo de fila onde cada elemento, chamado nó, contém um valor e um ponteiro para o próximo nó da fila. Essa estrutura de dados segue o princípio FIFO (First In First Out). Ou seja, o primeiro item a ser adicionado é o primeiro item a ser removido.

## Diferença entre Fila e Fila Encadeada

A diferença principal entre uma fila convencional e uma fila encadeada é a forma como os elementos são armazenados e acessados. Em uma fila convencional, os elementos são armazenados em uma estrutura contígua de memória, como um array, e as operações de inserção e remoção são realizadas deslocando-se os elementos na estrutura.

Por outro lado, em uma fila encadeada, cada elemento (nó) possui um ponteiro para o próximo nó, permitindo que os elementos sejam armazenados de forma não contígua na memória. Isso facilita a inserção e a remoção de elementos, pois não é necessário deslocar todos os elementos da fila.

## Vantagens da Fila Encadeada

- Inserção e remoção eficientes: A fila encadeada permite a inserção e a remoção de elementos em tempo constante, independentemente do tamanho da fila. Isso ocorre porque a estrutura encadeada não requer deslocamento de elementos como em uma fila convencional.
- Uso eficiente de memória: A fila encadeada utiliza apenas a quantidade de memória necessária para armazenar os elementos presentes na fila. Isso é especialmente útil quando o tamanho da fila varia ao longo do tempo.
- Flexibilidade: A estrutura de uma fila encadeada permite a implementação de operações adicionais, como inserção em qualquer posição da fila, remoção de elementos específicos, entre outros.

## Desvantagens da Fila Encadeada

- Acesso sequencial: Ao contrário de estruturas de dados como arrays ou listas, o acesso aleatório aos elementos de uma fila encadeada não é possível. É necessário percorrer sequencialmente os nós para acessar um elemento em uma posição específica.
- Uso adicional de memória: Cada nó em uma fila encadeada requer uma área de memória adicional para armazenar o ponteiro para o próximo nó. Em comparação com uma fila convencional, isso pode resultar em um consumo maior de memória.

## Usos Comuns da Fila Encadeada

A fila encadeada é comumente utilizada em situações em que a ordem de inserção dos elementos é importante e a remoção segue a ordem de chegada. Alguns exemplos de uso incluem:

- Simulações de eventos discretos, como a simulação de um sistema de atendimento ao cliente em uma empresa.
- Filas de tarefas em sistemas operacionais, onde os processos são colocados em uma fila para serem executados pelo processador.
- Implementação de caches de memória, em que os elementos menos utilizados são removidos da fila para abrir espaço para novos elementos.

## Operações típicas da Fila Encadeada

As operações básicas em uma fila encadeada incluem:

- Enqueue (Inserir): Adiciona um elemento ao final da fila.
- Dequeue (Remover): Remove o elemento do início da fila.
- Front (Primeiro): Retorna o valor do elemento no início da fila, sem removê-lo.
- IsEmpty (Vazia): Verifica se a fila está vazia.
- Size (Tamanho): Retorna o número de elementos presentes na fila.

## Utilização da Fila Encadeada em Python

A implementação de uma fila encadeada em Python pode ser feita utilizando classes e objetos. Cada nó da fila é representado por um objeto que contém o valor e uma referência para o próximo nó. Abaixo segue a implementação e o uso de algumas funções da Fila Encadeada em Python:

```python
class Node:
    def __init__(self, value):
        self.value = value
        self.next = None

class Queue:
    def __init__(self):
        self.head = None
        self.tail = None

    def enqueue(self, value):
        new_node = Node(value)
        if self.tail:
            self.tail.next = new_node
        else:
            self.head = new_node
        self.tail = new_node

    def dequeue(self):
        if not self.head:
            raise Exception("A fila está vazia")
        value = self.head.value
        self.head = self.head.next
        if not self.head:
            self.tail = None
        return value

    def is_empty(self):
        return self.head is None

    def size(self):
        count = 0
        current = self.head
        while current:
            count += 1
            current = current.next
        return count
```

## Referências:

- [SlideShare](https://pt.slideshare.net/FabianaLorenzi1/filas-encadeadas)
- [Readthedocs.io](https://aprendacompy.readthedocs.io/pt/latest/capitulo_19.html)
- [Growth](https://growthdev.com.br/programacao/estruturas-de-dados-listas-filas-pilhas-conjuntos-arvores-e-tabela-espelhadas/)
