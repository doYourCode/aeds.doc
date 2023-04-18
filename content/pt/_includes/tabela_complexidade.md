|       Estrutura de dados      | Complexidade de tempo |           |           |           |           |           |           |           | Complexidade espacial |
|:-----------------------------:|:---------------------:|:---------:|:---------:|:---------:|:---------:|:---------:|:---------:|:---------:|:---------------------:|
|                               |       Caso médio      |           |           |           | Pior caso |           |           |           |       Pior caso       |
|       Estrutura de dados      |         Acesso        |   Busca   |  Inserção |  Remoção  |   Acesso  |   Busca   |  Inserção |  Remoção  |                       |
| Array                         |          Θ(1)         |    Θ(n)   |    Θ(n)   |    Θ(n)   |    O(1)   |    O(n)   |    O(n)   |    O(n)   |          O(n)         |
| Lista                         |          Θ(n)         |    Θ(n)   |    Θ(1)   |    Θ(1)   |    O(n)   |    O(n)   |    O(1)   |    O(1)   |          O(n)         |
| Fila                          |          Θ(n)         |    Θ(n)   |    Θ(1)   |    Θ(1)   |    O(n)   |    O(n)   |    O(1)   |    O(1)   |          O(n)         |
| Pilha                         |          Θ(n)         |    Θ(n)   |    Θ(1)   |    Θ(1)   |    O(n)   |    O(n)   |    O(1)   |    O(1)   |          O(n)         |
| Árvore binária de busca (BST) |       Θ(log(n))       | Θ(log(n)) | Θ(log(n)) | Θ(log(n)) |    O(n)   |    O(n)   |    O(n)   |    O(n)   |          O(n)         |
| Árvore AVL                    |       Θ(log(n))       | Θ(log(n)) | Θ(log(n)) | Θ(log(n)) | O(log(n)) | O(log(n)) | O(log(n)) | O(log(n)) |          O(n)         |
| Árvore B                      |       Θ(log(n))       | Θ(log(n)) | Θ(log(n)) | Θ(log(n)) | O(log(n)) | O(log(n)) | O(log(n)) | O(log(n)) |          O(n)         |
| Tabela hash                   |          N/A          |    Θ(1)   |    Θ(1)   |    Θ(1)   |    N/A    |    O(n)   |    O(n)   |    O(n)   |          O(n)         |