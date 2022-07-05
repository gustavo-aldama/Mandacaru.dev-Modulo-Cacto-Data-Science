# Mandacaru.dev-Modulo-Cacto-Data-Science-

Atividade 1 - Individual:

Os dados são relativos a transações fraudulentas em um banco. O dataset contém mais de 20 mil amostras, com 112 atributos (features) numéricas. (https://www.kaggle.com/datasets/volodymyrgavrysh/fraud-detection-bank-dataset-20k-records-binary)

OBS: entregar em formato jupyter notebook

* Utilize a base de dados fraud_detection_bank_dataset.csv - link alternativo (.zip).
* Utilize dois classificadores do scikit-learn entre SVM, Regressão Logística, Random Forests e KNN para identificar fraudes nas transações.
* Separe 80% das amostras para o conjunto de treinamento+teste e guarde os outros 20% para a validação. Não esqueça de selecionar as amostras aleatoriamente.
* Faça a validação cruzada em 10 folds durante o processo de treinamento. Use o processo para testar alguns hiperparâmetros dos modelos propostos.
* Após encontrar dois bons modelos para cada técnica, analise os resultados obtidos no conjunto de validação.
* Exiba as métricas dos modelos (acurácia, escore F1, precision/recall) para seus conjuntos de treino+validação e teste

Atividade 2 - Individual:

Escolha dois estados de acordo com a incial de seu primeiro nome.
 
Primeira letra do nome: 
A-F: Mato Grosso e Goiás
G-J: Minas Gerais e Espírito Santo
K-N: Bahia e Pernambuco
O-S: Pará e Tocantins
T-Z: Paraná e Santa Catarina
 
Utilize as APIs do IBGE, como visto na aula da semana 5, e apresente as visualizações solicitadas a seguir:
 
1) Exiba dois box plots lado a lado, um para cada estado, dos índices solicitados:
a - Rendimento nominal médio mensal per capita (3974, censo Demográfico 2010)
b - Número de cabeças de bovinos Total (1224 - Censo Agropecuário 2006)
obs: as amostras do box plot devem corresponder às cidades de cada estado.
 
2) Exiba um gráfico de linha, onde cada linha corresponda a um estado, com a informação de:
a - Índices da Construção Civil: Custo médio (2296) por número índice (49) a partir de 1º de Janeiro de 2000
b - Produto Interno Bruto: Índice Gini do PIB, referência 2010 (5939, 529) para cada estado, a partir de 2002
 
3) Crie uma visualização em mapa coroplético do número de fundações privadas e associações sem fins lucrativos:
a - Número total de unidades (6917 - 2122) por município, no ano de 2016
b - Exiba, também, o número de unidades per capita, utilizando os dados de estimativa populacional em 2021 

Atividade 3 - Equipe:

Clusterizando Dados de Estatísticas Bancárias por Região Geográfica do Brasil
 
Objetivo: Implementar uma solução de clusterização para comparar cidades na mesma região geográfica 
 
Arquivo base: https://colab.research.google.com/drive/1f2bPggfhJ3bVkXLR12uUqqHGJQuyzhlS
 
A tarefa deverá ser realizada pelos integrantes do mesmo time do desafio.
 
Escolha uma região geográfica com base no número do seu time, de acordo com a planilha de atividades. 
Times 1-5: Região Sudeste
Times 6-10: Região Nordeste
Times 11-15: Região Centro-Oeste
Times 16-19: Região Sul
 
Atividade: 
Utilize os dados dos Relatório por município e agência do ESTBAN de todas as cidades da região selecionada no ano de 2021 para encontrar similaridades no perfil de obtenção de crédito agropecuário e financiamento imobiliário entre cidades. 
 
Agrupe as colunas `VERBETE_163_FIN_RURAIS_AGRICUL_CUST/INVEST`, `VERBETE_164_FIN_RURAIS_PECUAR_CUST/INVEST`, `VERBETE_165_FIN_RURAIS_AGRICUL_COMERCIALIZ` e `VERBETE_166_FIN_RURAIS_PECUARIA_COMERCIALIZ` somando seus valores e dividindo pela população para calcular o volume total de financiamentos agropecuários em uma nova coluna `fin_agro_per_capita`. Modifique, também, a coluna `VERBETE_169_FINANCIAMENTOS_IMOBILIARIOS` para `fin_imob_per_capita` . Nos dois casos, divida os valores brutos médios anuais após agrupar por cidade pela população estimada total de cada município, para o ano de 2021.
 
Utilize o K-Means para encontrar 5 clusters nessas duas variáveis. Explique se você consegue enxergar alguma relação entre as cidades de cada cluster e exiba um mapa cloroplético.
Pesquise alguma das variáveis do censo do IBGE (por exemplo: o PIB de cada município) e apresente um histograma ou o box-plot dessa variável para cada cluster. Explique se essa variável tem comportamento diferente em cada cluster.
Usando o critério de inércia, varie a quantidade de clusters entre 2 e 10. Plote o gráfico de cotovelo e identifique qual quantidade de clusters você recomendaria nesse problema.
O projeto de lei suplementar 316/09 propôs uma classificação de municípios em cinco categorias:
Rural, se tiver população inferior a 50 mil habitantes, valor adicionado da agropecuária superior a uma terça parte do PIB municipal e densidade demográfica inferior a 80 habitantes por quilômetro quadrado;
Relativamente rural, se tiver população inferior a 50 mil habitantes, valor adicionado da agropecuária entre uma terça parte e quinze centésimos do PIB municipal e densidade demográfica inferior a 80 habitantes por quilômetro quadrado;
De pequeno porte, se tiver população inferior a 50 mil habitantes, valor adicionado da agropecuária inferior a quinze centésimos do PIB municipal e densidade demográfica inferior a 80 habitantes por quilômetro quadrado, ou se tiver população inferior a 20 mil habitantes e densidade populacional superior a 80 habitantes por quilômetro quadrado;
De médio porte, se tiver população entre 50 mil e cem mil habitantes, ou se tiver densidade demográfica superior a 80 habitantes por quilômetro quadrado e população entre 20 mil e 50 mil habitantes;
De grande porte, se tiver população superior a cem mil habitantes.
Recupere os dados necessários para montar esta classificação a partir da API do IBGE. Existe alguma similaridade entre os clusters obtidos e a classificação do municípío? Calcule o percentual de clusters pertencentes a cada classe. Existe alguma relação entre eles? Exiba um mapa cloroplético dos municípios de acordo com essa classe.
