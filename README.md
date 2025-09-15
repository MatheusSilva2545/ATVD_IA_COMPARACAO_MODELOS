# ATVD_IA_COMPARACAO_MODELOS
 
 **Critérios**

Escolha e justificativa do dataset: 2,0

Pré-processamento adequado dos dados: 1,0

Implementação dos três modelos: 1,0

Avaliação e comparação com métricas/gráficos: 1,0

Conclusão crítica (análise dos resultados): 2,0 

# Projeto: Classificação com o Dataset Wine

Descrição

Este irá implementar e comparar três algoritmos de classificação supervisionada aplicados ao Wine Dataset (UCI Machine Learning Repository, disponível via `scikit-learn`).
O objetivo é prever a classe do vinho a partir de suas características químicas.


# Questões:

# Q1. O que significa classificação supervisionada?
É O aprendizado de máquina em que o aprende a prever rótulos (classes) a partir de exemplos já classificados. 
Sendo necessário Forner ao algoritmo pares de entradas (features) e saídas (rótulos) para que ele aprenda a relação entre eles.

# Q.2 Importância de dividir o dataset em treino e teste
É importante dividir o dataset em treino e teste,pois a divisão evita o overfitting, garantindo que o modelo não apenas memorize os dados, mas seja avaliado quanto à sua capacidade de generalizar para novos exemplos.

# Q.3 Diferença entre Decision Tree e KNN

Decision Tree: constrói uma árvore de decisão baseada em perguntas sucessivas sobre as features, dividindo os dados até chegar à classe final.
KNN (K-Nearest Neighbors): não cria um modelo explícito, mas classifica novas amostras observando os K vizinhos mais próximos e decidindo pela maioria.

# Q.4
Dataset

Nome: Wine Dataset
Origem: UCI Machine Learning Repository (via `sklearn.datasets.load_wine()`)
Tamanho: 178 amostras e 13 atributos numéricos
Variável alvo: Tipo de vinho (target com 3 classes)
Exemplos de atributos: teor alcoólico, ácido málico, magnésio, fenóis, flavonóides, entre outros.

# Como foi Implementado

1. Carregamento do dataset com `load_wine()`.
2. Preparação dos dados: divisão em treino/teste e normalização com `StandardScaler`.
3. Treinamento de três algoritmos:

   DecisionTreeClassifier
   KNeighborsClassifier
   LogisticRegression
4. Avaliação com as métricas:

     Acurácia
     Precisão
     F1-score
     Matriz de confusão
5. Visualização: gráfico comparativo das acurácias dos três modelos.

# Resultados

 Modelo               Acurácia  F1-score  Precisão 

 Decision Tree          ~0.94    ~0.94    ~0.95   
 KNN                    ~0.98    ~0.98    ~0.98   
|Logistic Regression    ~0.96    ~0.96    ~0.97   

(Os valores são aproximados visto que podem variar ao executar o programa)

# Qual modelo apresentou melhor desempenho no dataset escolhido? 
O modelo KNN apresentou o melhor desempenho, com acurácia e F1-score em torno de 0.98.

# O resultado faz sentido? 
Sim. O dataset Wine possui atributos numéricos que representam características químicas bem distintas entre as classes. Isso favorece algoritmos baseados em proximidade, como o KNN, que consegue separar bem os grupos de vinhos.

# O que poderia ser feito para melhorar os modelos?

Ajustar hiperparâmetros dos modelos (ex.: profundidade da árvore, número de vizinhos no KNN).

Testar diferentes técnicas de normalização ou padronização dos dados.

Avaliar modelos adicionais, como Random Forest ou SVM.

Aumentar o dataset com mais amostras para maior robustez.



