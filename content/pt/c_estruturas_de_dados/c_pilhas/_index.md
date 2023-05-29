---
weight: 3
title: "Pilhas"
date: 2023-04-12T01:00:36-03:00
draft: true
__author__ = ["Wender Alves da Silva", "Jefferson Eduardo Santos Lima", "Marina Jessiara Araújo Fonseca"] __date__ = "27/05/2023" "was8@aluno.ifnmg.edu.br","jesl@aluno.ifnmg.edu.br","mjaf@aluno.ifnmg.edu.br".
__credits__ = ["https://algoritmosempython.com.br/cursos/algoritmos-python/estruturas-dados/pilhas/"]
---

Pilha em Python

A pilha é uma estrutura de dados sequencial que nos permite recuperar os dados na ordem inversa à que foram inseridos. Esta restrição sobre a entrada e saída de dados na estrutura é conhecida como política de acesso e, no caso da pilha, leva o nome LIFO (Last In, First Out) traduzindo, “Último a Entrar, Primeiro a Sair.”

Uma pilha de pratos ou de livros, tal como habitualmente as conhecemos, reflete a ideia dessa estrutura de dados, pois colocamos estes objetos um sobre o outro, empilhando-os. Assim, na hora de removê-los, é mais fácil retirar o de cima primeiro, o topo da pilha, que foi o último objeto inserido.

Em python, a pilha pode ser implementada usando uma lista, aproveitando as operações de adição e remoção de elementos no final da lista.

Veja o exemplo a seguir:

pilha = [1, 2, 3, 4, 5]
print("Pilha: ", pilha)

pilha.inserir(11)
print("Inserindo um elemento: ", pilha)

pilha.inserir(12)
print("Inserindo outro elemento: ", pilha)

pilha.desempilhar()
print("Desempilhando um elemento: ", pilha)

pilha.desempilhar()
print("Desempilhando outro elemento: ", pilha)


Pilha:  [1, 2, 3, 4, 5]
Inserindo um elemento:  [1, 2, 3, 4, 5, 11]
Inserindo outro elemento:  [1, 2, 3, 4, 5, 11, 12]
Desempilhando um elemento:  [1, 2, 3, 4, 5, 11]
Desempilhando outro elemento:  [1, 2, 3, 4, 5]
Como pilhas só precisam de métodos para adicionar e remover itens do seu topo, as listas do Python já fazem esse trabalho com excelência e complexidade de tempo O(1), ou tempo constante. Ou seja, é super rápido.
Porém, ou você só usa esses dois métodos (inserir e desempilhar), ou você cria sua própria estrutura de dados chamada de Pilha. Segue o exemplo:


Para Type annotation
from typing import List

Pilha de livros com type annotation
pilha_de_livros: List[str] = [ ]  # {1}

Adicionando livros no topo da pilha
pilha_de_livros.inserir('Livro 1')  # {2}
pilha_de_livros.inserir('Livro 2')  # {2}
pilha_de_livros.inserir('Livro 3')  # {2}

Obtendo o elemento mais novo
livro = pilha_de_livros.desempilhar()  # {3}
print(livro)  # Livro 3 {4}


Perceba que no código acima, criei uma pilha de livros (pilha_de_livros) como uma lista vazia {1}. Quando precisei adicionar livros na pilha, usei o método inserir, que é padrão de listas em Python para adicionar itens ao final da lista {2}. Além disso, quando precisei obter o livro mais novo (do topo da pilha), usei o método desempilhar, que também é padrão de listas em Python para obter o último item da lista (ou o elemento do topo da pilha) {3}.

Na verdade, o método desempilhar faz duas coisas. Além de remover o item do topo da pilha, ele também retorna este valor. Então, Isso me permitiu fazer duas coisas em {3}: remover o item do topo da pilha e coletar seu valor em uma variável.
Por fim {4}, imprimimos o valor de livro, que foi o “Livro 3”.
