---
title: "Estruturas de dados"
date: 2023-04-12T01:00:36-03:00
draft: false
---

## Algoritmos e Estruturas de Dados
Algoritmos e estruturas de dados (doravante AEDs) são componentes fundamentais do ensino de ciência da computação, a compreensão desses dois conceitos servirá como uma base sobre a qual muitos outros assuntos serão desenvolvidos. Muitos iniciantes evitam estudar AEDs, por vezes, por acharem o assunto muito complexo ou por acreditarem que terá pouca ou nenhuma aplicação para a sua vida cotidiana/profissional. Essa possível percepção inicial não se sustenta ao avaliar a importância do assunto na prática profissional de um programador, uma vez que o domínio de AEDs afeta a efetividade e eficiência com a qual ele resolve problemas recorrentes de programação. A principal função de AEDs é estruturação para uma melhor realização das tarefas computacionais.
***
## Pra que estruturar nossas tarefas?
Para compreender melhor a necessidade de AEDs, vamos sair brevemente do contexto computacional e pensarmos em uma analogia, analise a seguinte situação: você vai a um restaurante com a sua família, vocês se sentam em uma mesa e pedem churrasco, arroz e feijão. Por acaso, esse restaurante funciona de maneira desestruturada, os funcionários não ordenam cronologicamente a realização dos pedidos, e não organizam os pedidos em blocos únicos de informação, a cozinha apenas recebe notas do que devem preparar e os garçons umas outras notas, que dizem para onde devem levar a comida já preparada. Dessa forma, sob protesto de outros clientes que pediram antes de vocês, após 10 minutos vocês são servidos com o feijão, passados 10 minutos adicionais chega o arroz, vocês estranham, mas como a fome aperta, começam a comer assim mesmo. Após outros 20 minutos chega o churrasco, mas todos já perderam a fome, por descontentamento e por terem se saciado apenas com arroz e feijão (que por sinal estavam uma delícia).
![](https://github.com/doYourCode/algoritmos_e_estruturas_de_dados/blob/main/wiki/img/pedidos_exemplo_rest_intro_001.png?raw=true)
Essa experiência gastronômica te dá uma má impressão sobre esse restaurante (independentemente da qualidade e sabor da comida servida), pois a falta de organização transformou sua refeição em um momento aquém das expectativas. Pensando como desenvolvedores de soluções, como poderíamos resolver o principal problema desse restaurante? A desorganização do estabelecimento em questão pode ser resolvida de forma simples: num primeiro momento, o pedido deve ser realizado anotando todos os itens desse pedido em uma lista, em seguida, o pedido deve ser colocado em uma fila junto com os demais pedidos, para que a cozinha o prepare na ordem em que foi pedido (evitando assim injustiças entre os clientes). Tomando essas duas medidas, utilizando uma lista de itens pedidos e uma fila de clientes, o restaurante se tornará mais eficaz e eficiente, melhor utilizando os escassos recursos de tempo, produtos, pessoal, etc. e obtendo renome não somente pela boa comida, mas pelo bom atendimento.
![](https://github.com/doYourCode/algoritmos_e_estruturas_de_dados/blob/main/wiki/img/pedidos_exemplo_rest_intro_002.png?raw=true)
Se você entendeu bem, agora deve estar se perguntando "mas o que isso tem a ver com algoritmos e estruturas de dados"? Perceba que sequenciamos as atividades envolvidas na tarefa, e utilizamos listas e uma fila para auxiliar nesse sequenciamento. É justamente isso o que algoritmos fazem (sequenciam  operações para executar uma tarefa), assim como as estruturas de dados (organizam os dados para auxiliar as tarefas). Se esse exemplo parece muito óbvio, é essa a intenção, tornar óbvia a necessidade de utilizarmos algoritmos e estruturas de dados para realizar nossas tarefas, desde as mais básicas até as mais complexas.
***
## Algoritmos
Um algoritmo é um procedimento que consiste em um conjunto de passos ou operações que, executados em uma ordem determinada, realizam uma determinada tarefa. No contexto computacional vemos algumas definições que apesar de diversas, se complementam. Uma definição comumente encontrada é a de que podemos dizer que o algoritmo é um conjunto finito de passos elementares que são aplicados sistematicamente até que uma solução seja atingida, ou seja, de forma simples, podemos dizer que um algoritmo define o caminho que deve ser seguido para chegar até a solução de um determinado problema. Em outra definição vemos um enfoque na noção de que todo algoritmo recebe uma entrada, realiza sua tarefa e entrega uma saída ao final, conforme explica Cormen (2002, apud ASCENCIO, 2010) "um algoritmo é qualquer procedimento computacional bem definido que toma algum valor ou conjunto de valores como entrada e produz algum valor ou conjunto de valores como saída".
![](https://github.com/doYourCode/algoritmos_e_estruturas_de_dados/blob/main/wiki/img/algoritmo_def_intro.png?raw=true)
* pra que servem
* casos de uso
***
## Estruturas de Dados
O estudo de estruturas de dados, um componente fundamental da educação em ciência da computação, serve como base sobre a qual muitos outros campos da ciência da computação são construídos. O conhecimento desse campo, das estruturas de dados, é de importância para os estudantes que desejam trabalhar no desenvolvimento de projetos, implementação, teste ou manutenção de praticamente qualquer sistema de software.
* pra que servem
* casos de uso
***
## Referências
ASCENCIO, Ana Fernanda. **Estruturas de dados: algoritmos, análise da complexidade e implementações em Java e C/C++**. São Paulo. Pearson Prentice Hall, 2010.
DROZDEK, Adam. **Data Structures and algorithms in C++**. Cengage Learning, 2012.
