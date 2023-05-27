---
weight: 2
title: "Fila circular (alocação contígua)"
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

Uma fila circular é uma estrutura de dados em que os elementos são organizados em uma sequência circular. Em uma fila circular, quando um elemento é removido do início da fila, o próximo elemento se torna o novo início, permitindo assim um aproveitamento eficiente do espaço de armazenamento. Neste contexto, vamos explorar a fila circular com foco nas vantagens, desvantagens, usos comuns, operações típicas e sua utilização em Python.

## Vantagens da Fila Circular
- **Eficiência espacial:** Ao contrário de uma fila convencional, em que os elementos são armazenados sequencialmente, uma fila circular otimiza o uso de memória, pois os elementos podem ser armazenados em uma estrutura circular sem desperdiçar espaço.
- **Acesso rápido aos elementos:** Como a fila circular permite que o início da fila seja atualizado, o acesso aos elementos subsequentes é rápido e direto, sem a necessidade de percorrer toda a estrutura.

## Desvantagens da Fila Circular
- **Tamanho fixo:** Uma fila circular possui um tamanho máximo predefinido. Se todos os slots estiverem ocupados e um novo elemento for adicionado, será necessário substituir um elemento existente para acomodar o novo. Isso pode causar a perda de dados se não for tratado adequadamente.
- **Complexidade de implementação:** A lógica de uma fila circular é mais complexa do que uma fila convencional, exigindo manipulação adicional dos índices para manter o rastreamento correto do início e do fim da fila.

## Usos comuns da Fila Circular
- **Buffers circulares:** Uma fila circular é frequentemente utilizada em sistemas que precisam armazenar dados temporariamente, como buffers de áudio ou vídeo. Os dados mais antigos são substituídos pelos novos à medida que a fila é preenchida.
- **Gerenciamento de tarefas:** Em sistemas operacionais, uma fila circular pode ser usada para agendar e executar tarefas, garantindo que todas as tarefas sejam atendidas em uma ordem justa.

## Operações típicas com a Fila Circular
- **Enfileirar (enqueue):** Adiciona um elemento ao final da fila circular.
- **Desenfileirar (dequeue):** Remove e retorna o elemento do início da fila circular.
- **Verificar se a fila está vazia:** Verifica se a fila circular está vazia, ou seja, se não contém elementos.
- **Verificar se a fila está cheia:** Verifica se a fila circular está cheia, ou seja, se todos os slots estão ocupados.

## Utilização da Fila Circular em Python

Em Python, a fila circular pode ser implementada utilizando listas e operações de índice. O módulo `collections` da biblioteca padrão também fornece a classe `deque`:

{{< tabs "ex_1" >}}
{{< tab "Python" >}}
```Python
from collections import deque

fila_circular = deque(maxlen=5)  # Define um tamanho máximo para a fila circular

fila_circular.append(1)  # Enfileirar elemento 1
fila_circular.append(2)  # Enfileirar elemento 2
fila_circular.append(3)  # Enfileirar elemento 3

print(fila_circular)  # Saída: deque([1, 2, 3], maxlen=5)

elemento_removido = fila_circular.popleft()  # Desenfileirar o primeiro elemento
print(elemento_removido)  # Saída: 1

print(fila_circular)  # Saída: deque([2, 3], maxlen=5)
{{< /tab >}}
{{< /tabs >}}

## Referências

- [Devmedia](https://www.devmedia.com.br/fila-circular-dinamica/24572)
- [Dantagens](https://acervolima.com/vantagens-da-fila-circular-em-relacao-a-fila-linear/)
- [Documentação Python](https://docs.python.org/3/library/collections.html#collections.deque)

