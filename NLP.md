# Processamento de Linguagem Natural (NLP)

NLP é a área da IA dedicada a fazer computadores compreenderem, interpretarem e gerarem linguagem humana. Abrange desde tarefas clássicas como classificação de texto e análise de sentimento até tradução automática e os modelos de linguagem de grande escala (LLMs) que hoje sustentam chatbots e assistentes de IA.

## Conceitos principais
- Tokenização: processo de dividir texto em unidades menores (palavras, subpalavras ou caracteres) que servem de entrada para os modelos.
- Embeddings: representações vetoriais densas de palavras ou frases que capturam significado semântico, permitindo operações matemáticas sobre linguagem.
- Modelos de linguagem (Language Models): sistemas que estimam a probabilidade de sequências de palavras, desde n-gramas até Transformers modernos.
- Attention e self-attention: mecanismo que permite ao modelo ponderar a relevância de diferentes partes do texto ao processar cada token.
- Named Entity Recognition (NER): identificação de entidades nomeadas (pessoas, organizações, locais) em um texto.
- Análise de sentimento: classificação da polaridade emocional (positiva, negativa, neutra) de um texto.
- Modelos pré-treinados (BERT, GPT): arquiteturas Transformer treinadas em grandes corpora de texto e depois ajustadas para tarefas específicas.
- Similaridade semântica: medir o quão próximos dois textos são em significado, geralmente via distância entre embeddings (cosseno).
- Stemming e lematização: técnicas de normalização de palavras às suas formas raiz ou canônica, comuns em pipelines mais tradicionais.

## Na prática
- Bibliotecas comuns: spaCy e NLTK para pipelines tradicionais; Hugging Face Transformers para modelos baseados em Transformer.
- Casos de uso: chatbots, análise de sentimento em redes sociais, extração de informação em documentos, tradução automática, sumarização de texto.
- Modelos como BERT são bons para tarefas de compreensão (classificação, NER); modelos como GPT são melhores para geração de texto.
- APIs de LLMs (OpenAI, Anthropic, Google) simplificaram tarefas de NLP que antes exigiam treino de modelos específicos.

## Pontos de atenção
- Ambiguidade linguística (polissemia, ironia, contexto cultural) continua sendo um desafio, mesmo para modelos avançados.
- Modelos treinados majoritariamente em inglês podem ter desempenho inferior em português e outras línguas com menos dados disponíveis.
- Viés presente nos dados de treino pode se refletir nas saídas do modelo, reforçando estereótipos ou associações problemáticas.
- Avaliação de qualidade de texto gerado é difícil; métricas automáticas (BLEU, ROUGE) nem sempre correlacionam bem com qualidade percebida por humanos.
- Pré-processamento inadequado (remoção excessiva de stopwords, normalização agressiva) pode destruir informação relevante para o modelo.
