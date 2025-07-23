# Algoritmos e Estruturas de Dados

O Livro adotado para o estudo dessa disciplina será o Introduction to Algorithms, de Thomas H. Cormen, Charles E. Leiserson, Ronald L. Rivest, Clifford Stein.

O livro é divido em 8 partes:

## Parte I | Fundamentos

A Parte I do livro serve como uma ao estudo de algoritmos. Ela estabelece as bases para o entendimento de como algoritmos são projetados e analisados ao longo de todo o livro.

Os pontos-chave abordados são:

- O que são algoritmos e sua importância
- Primeiros Algoritmos e Análise:
  - Ordenação por inserção (abordagem incremental)
  - Ordenação por intercalação
- Notação Assintótica
- Técnica de Divisão e Conquista e Recorrências
- Análise Probabilística e Algoritmos Aleatorizados

Em resumo, a Parte I equipa o leitor com as **ferramentas conceituais e matemáticas** necessárias para compreender a complexidade e a eficiência dos algoritmos discutidos nas partes seguintes.

## Parte II: Ordenação e Estatísticas de Ordem

A **Parte II** do livro foca principalmente em **algoritmos de ordenação por comparação**, estendendo os conceitos introduzidos na Parte I. As fontes sugerem que aborda esses algoritmos, citando o **Capítulo 8** que trata de ordenação e de ideias como o lema de ordenação 0-1 para algoritmos de comparação e permutação.

## Parte III: Estruturas de Dados

A Parte III do livro dedica-se ao estudo das estruturas de dados elementares que suportam operações de conjuntos dinâmicos.
Os tópicos principais abordados nesta parte são:

- **Árvores de Busca Binária (Capítulo 12)**: Introduz as árvores de busca binária como uma estrutura de dados fundamental para operações de conjunto dinâmicas, incluindo buscar, encontrar o mínimo, o máximo, o predecessor e o sucessor, além de inserir e eliminar elementos.
- **Árvores Vermelho-Preto (Capítulo 13)**: Detalha as árvores vermelho-preto, que são uma variação balanceada das árvores de busca binária. Elas garantem um desempenho eficiente para as operações de conjunto dinâmicas, assegurando que o comprimento dos caminhos da raiz às folhas seja aproximadamente balanceado através de regras de coloração e rotações.
Esta parte serve como a base para a compreensão de estruturas de dados mais complexas, que serão apresentadas em um nível mais avançado posteriormente no livro.

## Parte IV | Técnicas Avançadas de Projeto e Análise

A Parte IV introduz métodos mais sofisticados para projetar e analisar algoritmos eficientes.
Os principais tópicos e técnicas abordados são:

- **Programação Dinâmica (Capítulo 15)**: Foca em resolver problemas de otimização dividindo-os em subproblemas sobrepostos e ideais,armazenando os resultados para evitar recálculos (memoização). Exemplos incluem corte de hastes de aço e multiplicação de cadeias de matrizes.
- **Algoritmos Gulosos (Capítulo 16)**: Apresenta uma estratégia onde se faz a melhor escolha local na esperança de levar a uma solução ótima global, como no problema de seleção de atividades e códigos de Huffman.
- **Análise Amortizada (Capítulo 17)**: Uma técnica de análise de desempenho que avalia o custo médio de uma sequência de operações, em vez de focar no pior caso de uma única operação. Isso permite mostrar que uma sequência de operações, mesmo com picos de custo, tem um custo médio baixo.

Em resumo, a Parte IV equipa o leitor com ferramentas poderosas para lidar com problemas computacionais complexos.

## Parte V | Estruturas de Dados Avançadas

A Parte V do livro aprofunda a discussão sobre operações de conjuntos dinâmicos, baseando-se nas técnicas de análise mais sofisticadas [Parte V título da resposta anterior, indiretamente referenciando Parte IV].

Esta seção introduz estruturas de dados especializadas, que se destacam em cenários computacionais específicos:

- **B-árvores (Capítulo 18)**: São **árvores de busca balanceadas otimizadas para armazenamento em disco**. O desempenho é medido tanto pelo tempo de computação quanto, crucialmente, pelos acessos ao disco. Elas mantêm sua altura baixa para minimizar as operações de E/S de disco, tornando-as ideais para bancos de dados. A altura máxima de uma B-árvore com *n* nós internos e grau mínimo *t* é de **no máximo 2 lg(*n* + 1)** (a citação aqui é incorreta, deve ser do capítulo 18, mas o princípio é que a altura é logarítmica, afirma `h <= log_t((n+1)/2)`).
- **Heaps de Fibonacci (Capítulo 19)**: São projetados para suportar **operações de heap mescláveis**. O Capítulo 19 descreve procedimentos como `FIB-HEAP-DECREASE-KEY` e a operação de `CASCADING-CUT`.
- **Árvores de Van Emde Boas (Capítulo 20)**: Estruturas inovadoras que suportam operações de conjuntos dinâmicos como `SEARCH`, `INSERT`, `DELETE`, `MINIMUM`, `MAXIMUM`, `SUCCESSOR` e `PREDECESSOR` em **tempo O(lg lg u) no pior caso**. Isso é alcançado quando as chaves são inteiros dentro de um intervalo restrito (de 0 a *u*-1). A análise dessas operações é guiada por uma recorrência `T(u) = T(√u) + O(1)`, que se resolve em `O(lg lg u)`.
- **Estruturas de Conjuntos Disjuntos (Capítulo 21)**: Gerenciam uma coleção de conjuntos dinâmicos disjuntos. As operações primárias são `UNION` (unir dois conjuntos) e `FIND-SET` (identificar o representante de um elemento). Utilizam heurísticas como "união pelo posto" e "compressão de caminho". Uma sequência de *m* operações em *n* elementos é executada em **tempo O(m α(n)) no pior caso**, onde α(*n*) é uma função de crescimento muito lento (na prática, α(*n*) ≤ 4).

Em síntese, a Parte V explora **estruturas de dados avançadas e altamente otimizadas** que se sobressaem em cenários computacionais específicos, muitas vezes explorando propriedades particulares dos dados ou do ambiente de armazenamento.

## Parte VI | Algoritmos de Grafos

A **Parte VI** do livro concentra-se amplamente em **algoritmos de grafo**, fornecendo métodos para modelar e solucionar uma vasta gama de problemas computacionais através de grafos.

Os temas centrais abrangem:

- **Fundamentos de Grafos e Percursos**: Aborda como representar grafos e técnicas essenciais de travessia, como Busca em Largura (BFS) e Busca em Profundidade (DFS), que servem de base para algoritmos mais complexos. Inclui também ordenação topológica e identificação de componentes fortemente conexas.
- **Árvores Geradoras Mínimas (AGMs)** (Capítulo 23): Apresenta estratégias gulosas para encontrar subconjuntos de arestas que conectam todos os vértices com o custo total mínimo.
- **Caminhos Mínimos** (Capítulos 24 e 25): Dedica-se à descoberta das rotas mais curtas em grafos, tanto de uma única fonte (como em mapas rodoviários) quanto entre todos os pares de vértices. Enfatiza o tratamento de arestas com pesos negativos e ciclos de peso negativo.
- **Fluxo Máximo** (Capítulo 26): Explora a capacidade máxima de transporte em redes, introduzindo conceitos como redes residuais, caminhos aumentadores e o teorema do corte-mínimo/fluxo-máximo.

Em síntese, a Parte VI dota o leitor das **ferramentas necessárias para analisar e otimizar problemas de conectividade, roteamento e alocação de recursos** em estruturas de grafo.

## Parte VII | Tópicos Selecionados

A **Parte VII | Tópicos Selecionados** expande e complementa os conceitos anteriores do livro, introduzindo **novos modelos de computação e domínios especializados**, além de abordar as **limitações no projeto de algoritmos eficientes e técnicas para superá-las**.

Os temas abordados incluem:

- Algoritmos para Paralelismo** (Capítulo 27): Explora o projeto e a análise de algoritmos multithread, como multiplicação de matrizes e ordenação por intercalação paralelos, usando conceitos de trabalho e duração.
- **Operações com Matrizes** (Capítulo 28): Detalha algoritmos para operações fundamentais com matrizes, incluindo decomposição LUP e inversão de matrizes.
- **Programação Linear** (Capítulo 29): Apresenta as bases da programação linear e métodos para otimização, como o algoritmo Simplex.
- **Transformada de Fourier e Multiplicação Rápida de Polinômios** (Capítulo 30): Discute a representação e multiplicação eficiente de polinômios usando a Transformada Discreta de Fourier (DFT) e a Transformada Rápida de Fourier (FFT).
- **Teoria dos Números** (Capítulo 31): Cobre fundamentos de teoria dos números relevantes para algoritmos, como aritmética modular, algoritmo de Euclides, teoremas de Euler e Fermat, Teorema Chinês do Resto, e algoritmos para teste de primalidade (Miller-Rabin) e fatoração (Pollard-Rho).
- **Correspondência de Cadeias** (Capítulo 32): Apresenta algoritmos para encontrar padrões em textos, incluindo o algoritmo de Rabin-Karp, autômatos finitos e o algoritmo de Knuth-Morris-Pratt (KMP).
- **Geometria Computacional** (Capítulo 33): Aborda problemas geométricos como determinação de interseção de segmentos e cálculo de envoltórias convexas (Graham Scan, Marcha de Jarvis), utilizando conceitos como produtos cruzados.
- **NP-completude** (Capítulo 34): Examina as classes de complexidade e a teoria da NP-completude, ilustrando as limitações inerentes de certos problemas através de reduções polinomiais.
- **Algoritmos de Aproximação** (Capítulo 35): Introduz métodos para encontrar soluções próximas às ótimas para problemas NP-difíceis, como o problema da soma de subconjuntos.

Em resumo, a Parte VII é uma coletânea de **tópicos avançados que expandem o repertório de algoritmos e estruturas de dados**, focando tanto em **soluções eficientes para problemas complexos** quanto em **ferramentas para lidar com a intratabilidade computacional**.

## Parte VIII | APÊNDICE: FUNDAMENTOS DE MATEMÁTICA

A **Parte VIII | APÊNDICE: FUNDAMENTOS DE MATEMÁTICA** serve como um **compêndio essencial de ferramentas matemáticas** utilizadas na análise de algoritmos. Embora muitos conceitos possam ser familiares, esta seção consolida as notações e definições específicas usadas ao longo do livro.

Os tópicos centrais abrangem:

- **Somatórios (Apêndice A)**: Explica como o tempo de execução de algoritmos iterativos pode ser expresso como somas. Apresenta **fórmulas e propriedades de somatórios**, incluindo séries aritméticas, geométricas, harmônicas, e técnicas para **limitar ou quebrar somatórios** para análise assintótica.
- **Conjuntos, Relações, Funções e Grafos (Apêndice B)**: Define **elementos fundamentais da teoria dos conjuntos**, como conjuntos, relações (parciais, totais), e funções (injetoras, sobrejetoras, bijetoras). Aborda a **representação de grafos** (dirigidos e não dirigidos), seus vértices e arestas, e conceitos como adjacência, grau, caminhos (simples, ciclos), conectividade e tipos especiais de grafos (completos, bipartidos, acíclicos). Detalha também as **árvores** (livres, enraizadas, ordenadas, binárias, completas) e suas propriedades.
- **Contagem e Probabilidade (Apêndice C)**: Introduz princípios de contagem como a **regra do produto**, coeficientes binomiais e o triângulo de Pascal. Cobre **fundamentos de probabilidade**, incluindo espaços amostrais, eventos, probabilidade condicional e o **Teorema de Bayes**. Apresenta **variáveis aleatórias discretas** e suas distribuições, como a geométrica e a binomial.
- **Matrizes (Apêndice D)**: Define **matrizes, operações com matrizes** (soma, multiplicação) e suas propriedades básicas. Apresenta tipos específicos de matrizes como a identidade, tridiagonal, triangular (superior, inferior, unitária) e de permutação. Discute conceitos de álgebra linear como **posto de uma matriz** e **determinantes**.

Em suma, a Parte VIII é um **recurso fundamental** que equipa o leitor com o conhecimento matemático necessário para compreender e analisar a **eficiência e correção de algoritmos**, servindo de referência para as notações e conceitos utilizados em outras partes do livro.
