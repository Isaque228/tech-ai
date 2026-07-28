# Machine Learning

Machine Learning (Aprendizado de Máquina) é o ramo da IA que estuda algoritmos capazes de identificar padrões em dados e melhorar seu desempenho em uma tarefa sem serem explicitamente programados para ela. É a base sobre a qual se constroem quase todas as aplicações modernas de IA, desde sistemas de recomendação até modelos de linguagem.

## Conceitos principais
- Aprendizado supervisionado: o modelo aprende a partir de exemplos rotulados (entrada-saída conhecida), como em classificação e regressão.
- Aprendizado não supervisionado: o modelo encontra estrutura em dados sem rótulos, como em clustering (K-means) e redução de dimensionalidade (PCA).
- Aprendizado por reforço: um agente aprende por tentativa e erro, recebendo recompensas ou punições ao interagir com um ambiente.
- Overfitting e underfitting: overfitting ocorre quando o modelo memoriza os dados de treino e generaliza mal; underfitting ocorre quando o modelo é simples demais para capturar os padrões.
- Viés (bias) e variância (variance): trade-off entre erro sistemático do modelo e sensibilidade a variações nos dados de treino.
- Validação cruzada (cross-validation): técnica para estimar o desempenho do modelo em dados não vistos, dividindo os dados em múltiplos folds.
- Feature engineering: processo de criar, transformar e selecionar variáveis de entrada que melhorem o desempenho do modelo.
- Métricas de avaliação: acurácia, precisão, recall, F1-score e AUC-ROC para classificação; RMSE e MAE para regressão.
- Regularização: técnicas como L1 (Lasso) e L2 (Ridge) que penalizam a complexidade do modelo para reduzir overfitting.

## Na prática
- Bibliotecas como scikit-learn, XGBoost e LightGBM são amplamente usadas para modelos clássicos (árvores de decisão, random forests, gradient boosting).
- Casos de uso comuns: detecção de fraude, previsão de churn, scoring de crédito, sistemas de recomendação e manutenção preditiva.
- Pipelines de ML em produção geralmente envolvem pré-processamento, treino, validação, versionamento de modelos (MLflow, DVC) e monitoramento contínuo (MLOps).
- Modelos baseados em árvores (gradient boosting) costumam ser a escolha padrão para dados tabulares por seu equilíbrio entre desempenho e interpretabilidade.

## Pontos de atenção
- Vazamento de dados (data leakage): informações do conjunto de teste ou do futuro que "escapam" para o treino, inflando artificialmente as métricas.
- Dados desbalanceados exigem técnicas específicas (oversampling, undersampling, class weights) para evitar modelos tendenciosos.
- Métricas agregadas podem esconder desempenho ruim em subgrupos específicos; sempre analisar por segmento.
- Modelos treinados em um contexto podem sofrer "drift" quando a distribuição dos dados em produção muda ao longo do tempo.
- Nem todo problema precisa de deep learning; modelos simples e interpretáveis costumam ser mais adequados e fáceis de manter.
