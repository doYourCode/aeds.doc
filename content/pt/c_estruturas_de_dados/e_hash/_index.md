---
weight: 5
title: "Tabela Hash"
date: 2023-04-12T01:00:36-03:00
draft: false
---

Muitos métodos de busca funcionam segundo o mesmo princípio: procuram a informação desejada com base na comparação de suas chaves, isto é, com base em algum valor que a compõem. Nesse contexto, algoritmos eficientes exigem que os elementos sejam armazenados de forma ordenada, obtendo assim o custo da ordenação O (N log N)  no melhor caso e custo de busca O (log N).

Desta forma, a busca ideal seria o acesso direto ao elemento procurado, eliminando a etapa de comparação de chaves, com o custo O (1). Assim a solução é o uso da Tabela Hash, que é um tipo abstrato de dados que permite distribuir pares de chave e valor dentro da "Tabela". Assim, dada uma chave, a função Hash decide em qual endereço dessa tabela aquele valor deve ser armazenado.

## Para quê a tabela hash é usada

É uma estrutura de dados utilizada para tornar o processo de busca mais eficiente. Assim, esta estrutura de dados é muito utilizada não para inserções ou remoções, mas quando há a necessidade de realizar muitas buscas e com rápido tempo de resposta.

## Função Hash

É possível usar funções de hashing para codificar dados, transformar a entrada em um “código hash” ou em um “valor hash”. O algoritmo hash é projetado para minimizar a possibilidade de duas entradas terem o mesmo valor do hash, o que é chamado de colisão.

## Há tabelas hash em diferentes linguagens?
Sim, existem tabelas Hash em praticamente todas as linguagens de programação de alto nível. Em dicionários Python, map em C++ e Go, array em PHP, Hash em Ruby, Hashtable em Java e assim por diante.

## Vantagens do uso da tabela Hash
- Tabelas hash armazenam uma coleção de registros com chaves
- O local de um novo registro depende do valor hash de sua chave
- Quando ocorre uma colisão, é usado o próximo local disponível
- Procurar por uma chave é, geralmente, rápido.
- Quando um item é removido, o local deve ser marcado de maneira especial, para que na busca se saiba que a célula já foi utilizada

## Desvantagens do uso da tabela hash

- **Colisões:** Ocorrem quando diferentes chaves são mapeadas para o mesmo índice, resultando em potenciais problemas de desempenho e necessidade de tratamento de colisões.

- **Espaço de armazenamento:** As tabelas hash requerem espaço significativo de armazenamento, especialmente com um alto fator de carga, podendo resultar em desperdício de memória.

- **Operações de redimensionamento:** O redimensionamento da tabela hash pode ser uma operação custosa, exigindo a criação de uma nova tabela e realocação de elementos existentes.

- **Ordem dos elementos:** As tabelas hash não mantêm a ordem dos elementos de forma previsível, o que pode ser problemático quando a ordem é relevante.

- **Dificuldade na ordenação:** A ordenação dos elementos em uma tabela hash pode ser complexa, exigindo o uso de outras estruturas de dados ou algoritmos.


## Colisão e tratamento de colisão

Colisões em tabelas hash ocorrem quando duas ou mais chaves diferentes são mapeadas para o mesmo índice. Existem diferentes abordagens para tratar colisões. 

O encadeamento separado lida com colisões mantendo uma lista encadeada de pares chave-valor em cada slot da tabela.

O endereçamento aberto procura por slots vazios na tabela para armazenar os pares colididos, usando estratégias como linear probing, quadratic probing ou double hashing.

O rehashing envolve redimensionar a tabela quando o fator de carga excede um limite.

Cada técnica tem vantagens e desvantagens, e a escolha depende do contexto. A função hash também desempenha um papel importante na redução de colisões, distribuindo uniformemente as chaves na tabela.

## Exemplo de aplicação da tabela hash

Um exemplo de aplicação de uma tabela hash pode ser o armazenamento e busca eficiente de informações em um catálogo de produtos. Suponha que você esteja desenvolvendo um sistema de comércio eletrônico e precise armazenar os detalhes de diversos produtos, como nome, descrição, preço e quantidade em estoque.

Nesse caso, você pode usar uma tabela hash para mapear o código de cada produto para seus respectivos detalhes. A chave seria o código do produto e o valor seria um objeto contendo as informações do produto.

Ao adicionar um novo produto à tabela hash, você calcula o índice usando uma função hash que leva em consideração o código do produto. Em seguida, armazena o objeto de detalhes do produto no slot correspondente.

Ao buscar um produto pelo código, você utiliza a mesma função hash para calcular o índice e acessar diretamente o slot correspondente na tabela, obtendo assim os detalhes do produto de forma rápida e eficiente.

Esse exemplo ilustra como uma tabela hash pode ser usada para agilizar a busca e recuperação de informações em um contexto específico, como um catálogo de produtos. Vale ressaltar que na prática, a implementação real de uma tabela hash pode variar dependendo da linguagem de programação e dos requisitos específicos do sistema.