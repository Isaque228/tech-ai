# Deep Learning

Deep Learning (Aprendizado Profundo) é um subcampo do Machine Learning baseado em redes neurais artificiais com múltiplas camadas, capazes de aprender representações hierárquicas dos dados automaticamente. Foi o principal responsável pelos avanços recentes em visão computacional, processamento de linguagem natural e IA generativa, especialmente com o aumento da disponibilidade de dados e poder computacional (GPUs/TPUs).

## Conceitos principais
- Rede neural: conjunto de camadas de neurônios artificiais conectados por pesos, que transformam a entrada através de funções de ativação não lineares.
- Backpropagation: algoritmo que calcula o gradiente do erro em relação aos pesos da rede, permitindo o ajuste via gradiente descendente.
- Funções de ativação: ReLU, sigmoid, tanh e variantes (GELU, Swish) introduzem não linearidade e afetam a capacidade de aprendizado e a estabilidade do treino.
- Redes convolucionais (CNNs): arquitetura especializada em dados espaciais (imagens), usando filtros convolucionais para extrair características locais.
- Redes recorrentes (RNNs/LSTMs): projetadas para dados sequenciais, mantendo um estado interno que captura dependências temporais.
- Transformers: arquitetura baseada em mecanismos de atenção (self-attention) que substituiu RNNs como padrão em NLP e além, permitindo paralelização e captura de dependências de longo alcance.
- Transfer learning e fine-tuning: reaproveitar um modelo pré-treinado em uma tarefa e ajustá-lo para outra, reduzindo drasticamente a necessidade de dados e computação.
- Gradient descent e otimizadores: SGD, Adam e variantes ajustam os pesos da rede minimizando uma função de perda (loss function).
- Vanishing/exploding gradients: problemas de instabilidade no treino de redes profundas, mitigados por técnicas como normalização (batch norm, layer norm) e conexões residuais (ResNet).

## Na prática
- Frameworks dominantes: PyTorch e TensorFlow/Keras, com PyTorch sendo o mais usado em pesquisa e boa parte da indústria atualmente.
- GPUs e aceleradores especializados (TPUs) são essenciais para treinar modelos com milhões a bilhões de parâmetros em tempo viável.
- Casos de uso: reconhecimento de imagem e voz, tradução automática, geração de texto e imagem, sistemas de recomendação profundos.
- Modelos pré-treinados disponíveis via Hugging Face permitem começar de arquiteturas testadas (BERT, ResNet, ViT) em vez de treinar do zero.

## Pontos de atenção
- Treinar redes profundas exige grandes volumes de dados e recursos computacionais; nem sempre é a opção mais custo-efetiva.
- Redes profundas são propensas a overfitting; técnicas como dropout, data augmentation e early stopping ajudam a mitigar isso.
- A escolha de hiperparâmetros (taxa de aprendizado, tamanho de batch, arquitetura) tem impacto grande e muitas vezes exige busca sistemática (grid/random search, Bayesian optimization).
- Modelos profundos são frequentemente "caixas-pretas", dificultando explicabilidade em domínios regulados (saúde, crédito).
- Reprodutibilidade exige controle de seeds aleatórios, versionamento de dados e ambiente, já que pequenas variações podem gerar resultados diferentes.
