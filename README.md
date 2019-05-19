# Sort-Methods
Sistema que contem 9 métodos de ordenação implementados para fins acadêmicos, sendo eles: Bubble Sort, Selection Sort, Insertion Sort, Heap Sort, Merge Sort, Quick Sort, Count Sort, Bucket Sort e Radix Sort todos linguagem PHP

Esse sistema foi desenvolvido para a entrega de um trabalho da matéria Pesquisa, Ordenação e Técnicas de armazenamento contendo os gráficos e comparações feitas em tempo de execução do programa, para tal desenvolvimento foram gerados vetores aleatórios a partir de uma estrutura de dados criada chamada “ControleArray”, essa estrutura contém dois métodos “montarArray” e “popularArray”. O método “montarArray” cria uma coleção de dados inteiros com o tamanho especificado em seu parâmetro e com todas as posições zeradas, já o método “popularArray” por sua vez ficou responsável por receber o array anteriormente criado e populá-lo com inteiros aleatórios gerados a partir de um random entre 1 e 999 para cada posição do array recebido.

Para cada algoritmo implementado foi-se observado em quais momentos haviam comparações entre os elementos presentes no array, então cada algoritmo de ordenação se tornou uma classe herdando a estrutura de dados “ControleArray” que possui a propriedade “número de comparações”, quando identificado uma comparação na ordenação de um determinado array essa propriedade é incrementada em 1, gerando assim a coleta das comparações para cada instância de uma classe de ordenação e para cada array ordenado.

Foi realizado o polimorfismo no método “ordenarArray” herdado da estrutura “ControleArray” para cada classe de ordenação, pois assim foi possível que cada algoritmo pudesse ter sua regra de negócio implementada e manter um padrão de projeto no sistema. O método “montarArray”, explicado acima, retorna um array com o número de posições especificado em seu parâmetro e esse retorno foi inserido em uma matriz chamada “arraysParaOrdenar”. Com essa matriz devidamente montado e populada (método popularArray o responsável) cada instância de ordenação, ao chamar o método sobrescrito “ordenarArray”, recebe como parâmetro um array presente na matriz para ser ordenado (arraysParaOrdenar), quando esse processo é terminado o método retorna um novo objeto da classe instanciada contendo:
1.	Número de comparações feitas pelo algoritmo
2.	Tempo que levou para ser ordenado
3.	Quantos elementos estão presentes no array
4.	O próprio array ordenado
Esse novo objeto então é salvo em uma lista de objetos para cada método de ordenação e por sua vez a matriz de arrays (arraysParaOrdenar) mantem-se íntegra, podendo então ser passada para os próximos algoritmos de ordenação uma vez que eles seguem a mesma estrutura explicada acima.
