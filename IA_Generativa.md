# IA Generativa

IA Generativa refere-se a modelos capazes de criar conteúdo novo — texto, imagem, áudio, vídeo ou código — a partir de padrões aprendidos em grandes volumes de dados, em vez de apenas classificar ou prever valores. É a categoria de IA que impulsionou a popularização recente da área, com modelos de linguagem de grande escala (LLMs) e modelos de difusão para geração de imagens como principais expoentes.

## Conceitos principais
- Large Language Models (LLMs): modelos Transformer treinados em vastos corpora de texto, capazes de gerar texto coerente e realizar diversas tarefas via prompt (GPT, Claude, Gemini, Llama).
- Modelos de difusão: arquitetura que gera imagens partindo de ruído aleatório e refinando-o progressivamente até formar uma imagem coerente (Stable Diffusion, DALL-E, Midjourney).
- Pré-treino e fine-tuning: LLMs são pré-treinados em texto genérico e depois ajustados (fine-tuning, RLHF) para seguir instruções e alinhar comportamento.
- Tokens e janela de contexto: unidades de texto processadas pelo modelo e o limite de quantos tokens ele pode considerar simultaneamente em uma interação.
- Temperatura e amostragem: parâmetros que controlam a aleatoriedade/criatividade das saídas geradas (temperatura alta = mais variado, baixa = mais determinístico).
- Alucinação: geração de informação incorreta ou inventada apresentada como fato, um dos principais desafios de confiabilidade em IA generativa.
- Modelos multimodais: capazes de processar e gerar mais de um tipo de dado simultaneamente (texto, imagem, áudio), como GPT-4V e Gemini.
- Fine-tuning vs. in-context learning: ajustar os pesos do modelo (fine-tuning) versus ensinar comportamento apenas via exemplos no próprio prompt.

## Na prática
- APIs de provedores (Anthropic, OpenAI, Google, Mistral) permitem integrar capacidades generativas em produtos sem treinar modelos do zero.
- Casos de uso: geração e resumo de texto, assistentes de código, criação de imagens e vídeos, geração de áudio/voz sintética, automação de atendimento.
- Modelos open-weight (Llama, Mistral, Qwen) permitem rodar localmente ou em infraestrutura própria, com mais controle sobre dados e custo.
- Técnicas como RAG e fine-tuning são usadas para adaptar modelos genéricos a domínios ou bases de conhecimento específicas.

## Pontos de atenção
- Alucinações exigem validação humana ou mecanismos de verificação em aplicações críticas (jurídico, médico, financeiro).
- Custos de inferência podem escalar rapidamente com volume de uso; escolher o modelo certo para cada tarefa (não usar o maior modelo para tudo) é importante.
- Direitos autorais e proveniência de dados de treino são temas legais ainda em disputa, especialmente para geração de imagem e código.
- Prompt injection e uso indevido (geração de desinformação, deepfakes) são riscos de segurança que devem ser mitigados por design.
- Avaliação de qualidade de saída generativa é subjetiva e requer critérios claros (benchmarks, avaliação humana, LLM-as-judge) para comparação confiável.
