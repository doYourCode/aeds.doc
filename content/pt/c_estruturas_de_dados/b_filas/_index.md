---
weight: 2
title: "Filas"
date: 2023-04-12T01:00:36-03:00
draft: true
---
<!--    Documentação - Fila
Grupo:      Hugo Leonardo Viana
            Jairo Pedro Santana
            Mateus Borges e Guimarães
            Willy Brener Alves Oliveira-->
<h2> Conteúdo </h2>
{{< toc "format=html" >}}



## O que é uma fila?

Em Ciências da Computação, uma fila é uma estrutura de dados que organiza elementos em uma ordem específica, conhecida como "primeiro a entrar, primeiro a sair" (FIFO - First-In-First-Out). Ela representa uma coleção de elementos em que novos elementos são adicionados ao final da fila e a remoção ocorre no início da fila. Em termos visuais, imagine uma fila de pessoas esperando em um guichê de atendimento, onde a pessoa que chegou primeiro é a primeira a ser atendida.

A fila pode ser implementada usando diferentes estruturas de dados, como arrays, listas ligadas ou filas duplamente ligadas. Cada elemento na fila é chamado de item ou nó, e eles são mantidos em uma sequência linear. O primeiro elemento adicionado à fila é conhecido como "cabeça" ou "início", e o último elemento é chamado de "cauda" ou "fim".



## Vantagens da Fila
- **Ordem garantida:** Uma das principais vantagens das filas é que elas garantem a ordem dos elementos. Quando os elementos são adicionados à fila, eles são processados na sequência em que foram inseridos, o que é importante em muitos casos, como processamento de pedidos ou eventos em ordem cronológica.

- **Controle de prioridade:** As filas também podem ser usadas para controlar a prioridade de processamento. Por exemplo, em um sistema de gerenciamento de tarefas, tarefas com maior prioridade podem ser colocadas na frente da fila e, assim, serem processadas primeiro.

- **Coordenação e sincronização:** Filas são frequentemente utilizadas para coordenar a comunicação e sincronização entre diferentes partes de um sistema. Por exemplo, em sistemas produtor-consumidor, onde um produtor gera dados e um consumidor os processa, uma fila pode ser usada para passar os dados de forma segura e sincronizada entre os dois.

- **Implementação de algoritmos:** Filas são essenciais na implementação de algoritmos como Busca em Largura (BFS - Breadth-First Search), onde a ordem de processamento é fundamental. Além disso, filas são usadas em algoritmos de cache, agendamento de tarefas, impressão em spool, entre outros.

- **Simplicidade conceitual:** A fila é uma estrutura de dados conceitualmente simples, o que a torna fácil de entender e implementar. Isso facilita o desenvolvimento de programas e algoritmos que envolvem a manipulação de elementos em uma sequência específica.

- **Eficiência:** Tanto a inserção quanto a remoção de elementos em uma fila possuem uma complexidade de tempo constante, O(1). Isso significa que o tempo necessário para adicionar ou remover um elemento não depende do tamanho da fila.

## Desvantagens da Fila

- **Tamanho fixo:** Dependendo da implementação, filas podem ter um tamanho máximo fixo. Isso pode levar a problemas de estouro caso a fila atinja sua capacidade máxima. Se a fila atingir seu tamanho máximo e novos elementos forem adicionados, isso pode resultar em perda de dados ou no impedimento de inserção de novos elementos na fila.
- **Acesso limitado:** O acesso direto a elementos específicos em uma fila é limitado. Normalmente, só é possível acessar o primeiro elemento da fila e removê-lo. Se for necessário acessar elementos no meio da fila, pode ser necessário remover vários elementos na frente até chegar ao elemento desejado.
- **Ineficiência na remoção de elementos intermediários:** Se for necessário remover um elemento que não esteja no início da fila, todos os elementos anteriores precisam ser removidos antes dele. Isso pode ser ineficiente se houver a necessidade frequente de remover elementos em posições intermediárias.
- **Uso de memória contínua:** Alguns tipos de implementações de fila requerem o uso de memória contínua, o que significa que o espaço de memória para a fila precisa ser alocado de forma contínua. Isso pode ser um desafio em situações onde a memória é limitada ou fragmentada.
- **Limitações de desempenho em grandes filas:** Conforme a fila cresce em tamanho, as operações de enfileirar e desenfileirar podem se tornar mais lentas, especialmente se a implementação não for otimizada. O tempo de execução dessas operações pode aumentar linearmente com o tamanho da fila, o que pode ser um problema em casos de filas extremamente grandes.

## Usos Comuns da Fila 

- **Gerenciamento de tarefas:** Filas são frequentemente utilizadas para o gerenciamento de tarefas, como em sistemas operacionais para escalonamento de processos. Por exemplo, em um sistema operacional, os processos são colocados em uma fila de prontos e o escalonador seleciona o próximo processo a ser executado com base no princípio FIFO.

- **Processamento assíncrono:** Filas são úteis para processar tarefas assíncronas, onde as requisições são enfileiradas e processadas uma após a outra. Por exemplo, em um servidor web, as solicitações dos clientes podem ser colocadas em uma fila e processadas em ordem, garantindo um tratamento justo para cada solicitação.

- **Simulação de eventos:** Em simulações computacionais, filas podem ser usadas para representar eventos futuros e processá-los na ordem correta. Por exemplo, em uma simulação de tráfego, os carros podem ser enfileirados em uma fila para atravessar um cruzamento, respeitando a ordem de chegada.

- **Processamento de mensagens ou eventos em sistemas distribuídos:** Filas são comumente utilizadas em sistemas distribuídos para processar mensagens ou eventos assíncronos. Por exemplo, em um sistema de mensagens instantâneas, as mensagens podem ser enfileiradas em uma fila centralizada antes de serem entregues aos destinatários.


## Operações típicas com a Fila

- **Enqueue:** Insere um elemento no final da fila.
- **Dequeue:** Remove o elemento no início da fila.
- **Front:** Retorna o elemento no início da fila sem removê-lo.
- **IsEmpty:** Verifica se a fila está vazia.
- **Size:** Retorna o número de elementos presentes na fila.
- **Clear:** Remove todos os elementos da fila, deixando-a vazia.
- **Contains:** Verifica se um determinado elemento está presente na fila.
- **Print:** Imprime todos os elementos da fila.
- **Rear:** Retorna o elemento no final da fila sem removê-lo.
- **Count:** Retorna o número de ocorrências de um determinado elemento na fila.
- **Remove:** Remove a primeira ocorrência de um elemento específico da fila.


## Utilização da Fila em Python

Abaixo segue a implementação e o uso de algumas funções da Fila Simples em Python:
{{< tabs "ex_1" >}}
{{< tab "Python" >}}
```Python
class FilaSimples:
    def __init__(self):
        self.fila = []

    def enqueue(self, item):
        self.fila.append(item)

    def dequeue(self):
        if self.is_empty():
            return "A fila está vazia."
        return self.fila.pop(0)

    def front(self):
        if self.is_empty():
            return "A fila está vazia."
        return self.fila[0]

    def is_empty(self):
        return len(self.fila) == 0

    def size(self):
        return len(self.fila)




fila = FilaSimples()
fila.enqueue("A")
fila.enqueue("B")
fila.enqueue("C")

print(fila.dequeue())  # Saída: "A"
print(fila.front())    # Saída: "B"
print(fila.size())     # Saída: 2
print(fila.is_empty()) # Saída: False

{{< /tab >}}
{{< /tabs >}}


## Referências

- [Wikipédia](https://pt.wikipedia.org/wiki/FIFO)
- [Treinaweb](https://www.treinaweb.com.br/blog/o-que-e-e-como-funciona-a-estrutura-de-dados-fila)
- [Otaviomiranda](https://www.otaviomiranda.com.br/2020/filas-em-python-com-deque-queue/)

