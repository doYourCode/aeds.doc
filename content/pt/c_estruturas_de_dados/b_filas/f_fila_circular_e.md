---
weight: 6
title: "Fila circular encadeada"
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

 
Uma fila circular com nós encadeados é uma estrutura de dados que combina as características de uma fila circular e uma lista encadeada. Ela permite a inserção e remoção eficiente de elementos no início e no final da fila, independentemente do tamanho da fila.
Em uma fila circular com nós encadeados, cada elemento é armazenado em um nó, que contém um valor e um ponteiro/referência para o próximo nó da fila. O último nó da fila aponta para o primeiro nó, formando um ciclo.

## Vantagens da Fila Circular com nós encadeados

- **Eficiência:** Uma fila circular com nós encadeados possui um desempenho eficiente em termos de inserção e remoção de elementos, independentemente do tamanho da fila. Isso ocorre porque a estrutura permite que os elementos sejam adicionados ou removidos no início ou no final da fila em tempo constante.
- **Utilização eficiente de memória:** A fila circular utiliza a memória de forma eficiente, pois não há desperdício de espaços vazios entre os elementos.
- **Implementação simples:** A implementação de uma fila circular com nós encadeados é relativamente simples, o que facilita sua compreensão e manutenção.

## Desvantagens da Fila Circular com nós encadeados

- **Tamanho fixo:** A fila circular com nós encadeados requer um tamanho fixo pré-definido. Isso significa que a capacidade da fila precisa ser especificada no momento da sua criação, e não pode ser alterada dinamicamente. Se a fila atingir sua capacidade máxima, novos elementos não poderão ser adicionados até que outros sejam removidos.
- **Acesso sequencial:** A fila circular permite o acesso sequencial aos elementos. Portanto, se for necessário acessar um elemento em uma posição específica, é necessário percorrer todos os elementos anteriores.

## Usos comuns da Fila Circular com nós encadeados

- **Gerenciamento de tarefas:** Uma fila circular com nós encadeados é frequentemente utilizada em sistemas de gerenciamento de tarefas, onde as tarefas são adicionadas à fila e processadas de acordo com sua ordem de chegada.
- **Armazenamento temporário:** Pode ser utilizada como uma estrutura de dados para armazenar temporariamente elementos que aguardam processamento posterior.
- **Simulação de eventos:** Em simulações, a fila circular pode ser usada para modelar a fila de eventos que devem ser processados em uma ordem específica.

## Operações típicas com a Fila Circular com nós encadeados

- **Enfileirar (enqueue):** Adiciona um elemento no final da fila.
- **Desenfileirar (dequeue):** Remove o elemento do início da fila.
- **Verificar se a fila está vazia:** Retorna verdadeiro se a fila estiver vazia, e falso caso contrário.
- **Verificar se a fila está cheia:** Retorna verdadeiro se a fila estiver cheia, e falso caso contrário.
- **Obter o tamanho da fila:** Retorna o número de elementos presentes na fila.

## Utilização Fila Circular com nós encadeados em python

{{< tabs "ex_1" >}}
{{< tab "Python" >}}
```Python
class Node:
    def __init__(self, value):
        self.value = value
        self.next = None

class CircularQueue:
    def __init__(self, capacity):
        self.capacity = capacity
        self.head = None
        self.tail = None
        self.size = 0

    def is_empty(self):
        return self.size == 0

    def is_full(self):
        return self.size == self.capacity

    def enqueue(self, value):
        if self.is_full():
            print("A fila está cheia. Não é possível enfileirar o elemento.")
            return

        new_node = Node(value)

        if self.is_empty():
            self.head = new_node
            self.tail = new_node
            new_node.next = new_node
        else:
            new_node.next = self.tail.next
            self.tail.next = new_node
            self.tail = new_node

        self.size += 1

    def dequeue(self):
        if self.is_empty():
            print("A fila está vazia. Não é possível desenfileirar.")
            return None

        value = self.head.value

        if self.size == 1:
            self.head = None
            self.tail = None
        else:
            self.head = self.head.next
            self.tail.next = self.head

        self.size -= 1

        return value
{{< /tab >}}
{{< /tabs >}}

## Referências
- <a href="https://docs.python.org/" target="_blank">Documentação Python</a>
- <a href="https://pt.stackoverflow.com/questions/89878/fila-com-lista-encadeada-circular-com-cabe%C3%A7a" target="_blank">Stackoverflow</a>