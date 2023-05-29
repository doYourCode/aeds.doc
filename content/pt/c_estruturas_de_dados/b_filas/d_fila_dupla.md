---
weight: 4
title: "Fila dupla (Deque - alocação contígua)"
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




Em ciência da computação , uma Fila dupla é um tipo de dado abstrato que generaliza uma fila , para a qual elementos podem ser adicionados ou removidos da frente (cabeçalho) ou de trás (cauda).  

Uma Fila dupla é uma estrutura de dados que permite a inserção e remoção de elementos de ambas as extremidades. Isso é diferente de uma fila, que só permite a inserção em uma extremidade e a remoção na outra extremidade, seguindo uma ordem FIFO (first in first, out / primeiro a entrar, primeiro a sair). Filas duplas podem ter vários subtipos, incluindo Filas duplas restritos à entrada, onde a exclusão pode ser feita em ambas as extremidades, mas a inserção só pode ser feita em uma extremidade, e Filas duplas restritos à saída, onde a inserção pode ser feita em ambas as extremidades, mas a exclusão só pode ser feito de uma ponta.

Filas duplas são uma estrutura de dados fundamental na computação, e muitas outras estruturas de dados podem ser implementadas usando-as. Por exemplo, filas e pilhas podem ser consideradas especializações de Filas duplas. As operações básicas em uma Fila dupla são adicionar elementos a qualquer uma das extremidades e remover elementos de ambas as extremidades.

## Vantagens da Fila Dupla

A principal vantagem da Fila dupla sobre a Fila convencional é a possibilidade de adicionar ou remover os itens de ambos os lados da Fila Dupla. Na Fila convencional você só pode adicionar os dados de trás e removê-los de frente, além disso a Fila dupla também tem a vantagem de ser dinâmica em tamanho, oferecer um bom tempo para a execução das operações entre outras.





## Desvantagens da Fila Dupla

As principais desvantagens da Fila dupla são:

- Maior consumo de memória: O processo da Fila Dupla tem maior taxa de consumo de memória.
- Sincronização: Tem problemas de sincronização com multi thread.
- Suporte: Não pode ser implementado em todas as plataformas.
- Classificação: Não é adequado para implementar operações de classificação.
- Limitada: A Fila Dupla tem poucas funcionalidades.

## Usos Comuns da Fila Dupla

- Realizar operações de desfazimento no software.
- Para armazenar histórico em navegadores.
- Para implementar pilhas e filas.

Um exemplo em que uma Fila Dupla pode ser usada é o algoritmo de roubo de trabalho. Este algoritmo implementa escalonamento de tarefas para vários processadores. Uma Fila Dupla separada com threads a serem executados é mantida para cada processador. Para executar a próxima thread, o processador obtém o primeiro elemento da Fila Dupla (usando a operação da Fila Dupla ("remover primeiro elemento")). Se a thread atual bifurcar, ela é colocada de volta na frente da Fila Dupla ("inserir elemento na frente") e uma nova thread é executada. Quando um dos processadores termina a execução de suas próprias threads (ou seja, sua Fila Dupla está vazia), ele pode "roubar" uma thread de outro processador: ele pega o último elemento da Fila Dupla de outro processador ("remove último elemento") e executa isto. O algoritmo de roubo de trabalho é usado pela biblioteca Threading Building Blocks (TBB) da Intel para programação paralela.

## Operações típicas com a Fila Dupla

***push_back():*** insira um elemento da parte de trás de uma Fila Dupla.

***push_front():*** insira um elemento da frente de uma Fila Dupla.

***pop_back*** remove o elemento da parte de trás de uma Fila Dupla.

***pop_front():*** remove o elemento da frente da Fila Dupla.

***front():*** retorna o elemento na frente de uma Fila Dupla.

***back():*** retorna o elemento no final da Fila Dupla.

***at()-set:*** retorna no índice especificado.

***size():*** o número de elementos retorna.

***empty():*** retorna verdadeiro se a Fila Dupla estiver vazia.


## Utilização da Fila Dupla em Python

Abaixo segue a implementação e o uso de algumas funções da Fila Dupla em Python:

**Fila Dupla implementação em Python**

{{< tabs "ex_1" >}}
{{< tab "Python" >}}
```Python
class Deque:
    def __init__(self):
        self.items = []

    def isEmpty(self):
        return self.items == []

    def addRear(self, item):
        self.items.append(item)

    def addFront(self, item):
        self.items.insert(0, item)

    def removeFront(self):
        return self.items.pop(0)

    def removeRear(self):
        return self.items.pop()

    def size(self):
        return len(self.items)


d = Deque()
print(d.isEmpty())
d.addRear(8)
d.addRear(5)
d.addFront(7)
d.addFront(10)
print(d.size())
print(d.isEmpty())
d.addRear(11)
print(d.removeRear())
print(d.removeFront())
d.addFront(55)
d.addRear(45)
print(d.items)

{{< /tab >}}
{{< /tabs >}}

## Referências

- <a href="https://en.wikipedia.org/wiki/Double-ended_queue" target="_blank">Wikipedia</a>
- <a href="https://www.tutorialspoint.com/applications-advantages-and-disadvantages-of-deque" target="_blank">Aplicações vantagens e desvantagens da Fila Dupla</a>
- <a href="https://www.programiz.com/dsa/deque" target="_blank">Fila Dupla estrutura de dados</a>





