---
weight: 1
title: "Listas"
date: 2023-04-12T01:00:36-03:00
draft: false
---

Listas são estruturas de dados que permitem armazenar uma coleção de elementos em sequência. Cada elemento em uma lista é associado a uma posição ou índice específico, o que permite o acesso, inserção e remoção de elementos de forma controlada. Listas são amplamente usadas em de programação para auxiliar a solução de problemas que exigem lidar com conjuntos de elementos. As listas podem ter diferentes implementações e comportamentos a depender do propósito. Muitas linguagens de programação têm listas implementadas em suas bibliotecas básicas, nesse caso é sempre importante consultar a documentação e os recursos específicos da linguagem que você está usando para entender como as listas são implementadas e como usá-las corretamente. Entre os diferentes tipos de listas encontramos as encadeadas, duplamente encadeadas, circulares e por fim, sua implementação mais simples, listas de alocação contígua.
Nosso repositório conta com a implementação de algumas dessas listas, para mais informações:

- [Lista linear contígua](/c_estruturas_de_dados/a_listas/a_lista_linear_contigua/)
- Lista encadeada
- Lista duplamente encadeada
- Lista circular
- Lista circular duplamente encadeada

## Diferenças entre listas e arrays

Os arrays estão entre as estruturas de dados mais simples, implementados por quase todas as linguagens de programação, consistindo apenas em um espaço reservado de memória contígua e cujos endereços contém ou apontam para diferentes elementos. Tanto os arrays quanto as listas são estruturas de dados usadas para armazenar coleções de elementos em linguagens de programação. Embora possam ter funções semelhantes, há diferenças importantes entre listas e arrays em termos de funcionalidades, e como são implementados e como podem ser usados. São elas:

- **Tipos de dados:** Arrays são geralmente usados para armazenar elementos do mesmo tipo de dado (sendo necessário trabalhar com ponteiros para tipos vazios (void) e/ou ponteiros de ponteiros para contornar essa limitação). Por outro lado, listas podem, dependendo da implementação, armazenar elementos de diferentes tipos de dados.

- **Alocação e tamanho flexíveis:** Listas são mais flexíveis do que arrays em termos de tamanho e manipulação dos elementos. É mais fácil adicionar ou remover elementos em uma lista, seja no início, meio ou final desta. Já os arrays têm tamanho fixo, geralmente definido em tempo de compilação, e requerem redimensionamento manual se o número de elementos mudar.

- **Inserção e remoção de elementos:** Inserir ou remover um elemento no meio de um array pode ser ineficiente em termos de desempenho, pois pode exigir a realocação de elementos subsequentes para abrir espaço. Em contraste, listas são mais eficientes em termos de inserção e remoção de elementos em posições intermediárias.

- **Acesso a elementos:** Arrays geralmente oferecem acesso mais rápido aos elementos por meio de índices, uma vez que os elementos são armazenados em posições de memória contíguas. Já em listas, principalmente as encadeadas, o acesso a elementos pode ser mais lento, pois pode exigir a navegação pela lista a partir do início ou do fim.

- **Funcionalidades adicionais:** Listas geralmente têm funcionalidades adicionais, como operações de busca, ordenação e filtragem de elementos, que não estão disponíveis em arrays. Isso ocorre porque as listas são implementadas como estruturas de dados mais complexas, como listas encadeadas, que podem ter recursos adicionais além do armazenamento de elementos.

- **Uso em diferentes linguagens de programação:** Arrays são uma estrutura de dados comum em muitas linguagens de programação, como C, C++ e Java. Por outro lado, listas são mais comuns em linguagens de programação que oferecem suporte a tipos de dados dinâmicos, como Python, JavaScript e Ruby, embora possam ser implementadas como arrays em outras linguagens.

Em resumo, enquanto arrays são mais adequados para casos em que o tamanho dos elementos é fixo e a manipulação de elementos é simples, listas são mais flexíveis, oferecem funcionalidades adicionais e são mais adequadas quando o tamanho dos elementos é variável e é necessário realizar operações complexas de manipulação de dados. A escolha entre arrays e listas depende do contexto específico do problema que está sendo resolvido e dos requisitos do projeto em termos de flexibilidade, eficiência e funcionalidades necessárias.