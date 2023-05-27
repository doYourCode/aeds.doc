---
weight: 8
title: "Fila dupla (Deque) encadeada"
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

Uma Fila Dupla com nós encadeados é uma estrutura de dados que estende o conceito de uma Fila Dupla, onde cada elemento (nó) contém um valor e uma referência ao próximo nó e ao nó anterior. Essa estrutura de dados permite a inserção e remoção de elementos em ambas as extremidades da fila, assim como uma Fila Dupla convencional, mas com a vantagem adicional de ter acesso aos nós adjacentes.

## Vantagens da Fila dupla com nós encadeados

**Flexibilidade:** A Fila Dupla com nós encadeados permite a inserção e remoção eficiente de elementos tanto na frente quanto na parte de trás da fila, oferecendo flexibilidade em termos de manipulação dos dados.

**Eficiência:** Comparada a outras estruturas de dados, a Fila Dupla com nós encadeados pode fornecer operações de inserção e remoção mais eficientes em ambas as extremidades.

**Acesso aos nós adjacentes:** A capacidade de acessar os nós adjacentes em uma Fila Dupla com nós encadeados pode ser útil em certos cenários, permitindo operações mais avançadas.

## Desvantagens da Fila dupla com nós encadeados

**Complexidade:** A implementação da Fila Dupla com nós encadeados pode ser mais complexa do que uma Fila Dupla convencional, devido à necessidade de gerenciar as referências entre os nós.

**Consumo de memória:** A estrutura de nós encadeados requer armazenamento adicional para as referências entre os nós, o que pode resultar em um consumo de memória maior em comparação com estruturas de dados mais simples.

## Usos Comuns da Fila dupla com nós encadeados

**Implementação de algoritmos de busca avançados:** A capacidade de acessar os nós adjacentes em uma Fila Dupla com nós encadeados pode ser útil na implementação de algoritmos de busca mais avançados, como busca bidirecional.

**Manipulação de histórico:** A Fila Dupla com nós encadeados pode ser usada para armazenar histórico de operações, permitindo desfazer e refazer ações em determinado contexto.

**Implementação de caches:** Em certos cenários, a Fila Dupla com nós encadeados pode ser usada para implementar caches de dados, permitindo acesso rápido a elementos recentemente usados.

## Operações típicas com a Fila dupla com nós encadeados

- **Inserção na frente:** Adicionar um novo nó na frente da fila.
- **Inserção na parte de trás:** Adicionar um novo nó na parte de trás da fila.
- **Remoção na frente:** Remover o nó na frente da fila.
- **Remoção na parte de trás:** Remover o nó na parte de trás da fila.
- **Acesso ao nó adjacente anterior:** Obter a referência para o nó anterior a um nó específico.
- **Acesso ao nó adjacente posterior:** Obter a referência para o nó posterior a um nó específico.

## Utilização da Fila dupla com nós encadeados  em Python

Abaixo segue uma possível implementação da Fila Dupla com nós encadeados em Python:

```Python
class Node:
        def __init__(self, value):
            self.value = value
            self.next = None
            self.prev = None

    class DoublyLinkedListDeque:
        def __init__(self):
            self.front = None
            self.rear = None

        def isEmpty(self):
            return self.front is None

        def addFront(self, value):
            new_node = Node(value)
            if self.isEmpty():
                self.front = self.rear = new_node
            else:
                new_node.next = self.front
                self.front.prev = new_node
                self.front = new_node

        def addRear(self, value):
            new_node = Node(value)
            if self.isEmpty():
                self.front = self.rear = new_node
            else:
                new_node.prev = self.rear
                self.rear.next = new_node
                self.rear = new_node

        def removeFront(self):
            if self.isEmpty():
                return None
            front_value = self.front.value
            if self.front is self.rear:
                self.front = self.rear = None
            else:
                self.front = self.front.next
                self.front.prev = None
            return front_value

        def removeRear(self):
            if self.isEmpty():
                return None
            rear_value = self.rear.value
            if self.front is self.rear:
                self.front = self.rear = None
            else:
                self.rear = self.rear.prev
                self.rear.next = None
            return rear_value

        def size(self):
            count = 0
            curr = self.front
            while curr:
                count += 1
                curr = curr.next
            return count
```

**Exemplo de uso da Fila Dupla com nós encadeados**
```python
d = DoublyLinkedListDeque()
print(d.isEmpty())  # True

d.addFront(8)
d.addRear(5)
d.addFront(7)
d.addFront(10)
print(d.size())  # 4
print(d.isEmpty())  # False

d.addRear(11)
print(d.removeRear())  # 11
print(d.removeFront())  # 10

d.addFront(55)
d.addRear(45)
print(d.size())  # 5
print(d.removeFront())  # 55
print(d.removeRear())  # 45
print(d.size())  # 3
```

    



## Referências

- <a href="https://en.wikipedia.org/wiki/Double-ended_queue" target="_blank">Wikipedia</a>
- <a href="https://www.geeksforgeeks.org/implementation-deque-using-doubly-linked-list/" target="_blank">Fila Dupla com nós encadeados </a>


