# RAG (Retrieval-Augmented Generation)

RAG é uma técnica que combina busca de informação (retrieval) com geração de texto por LLMs, permitindo que o modelo responda com base em documentos externos e atualizados em vez de depender apenas do conhecimento memorizado durante o treino. É a abordagem mais comum para adaptar LLMs a bases de conhecimento específicas sem precisar treinar ou ajustar o modelo.

## Conceitos principais
- Retrieval: etapa de busca que recupera os trechos de documentos mais relevantes para a pergunta do usuário, geralmente via similaridade vetorial.
- Embeddings e busca vetorial: textos são convertidos em vetores numéricos e armazenados em um banco vetorial (vector database) para busca por similaridade semântica.
- Chunking: divisão de documentos longos em pedaços menores (chunks) para indexação, cujo tamanho e overlap afetam diretamente a qualidade da busca.
- Vector databases: sistemas especializados em armazenar e consultar embeddings, como Pinecone, Weaviate, Qdrant, Milvus e pgvector.
- Reranking: etapa opcional que reordena os resultados recuperados usando um modelo mais preciso (porém mais custoso) antes de enviá-los ao LLM.
- Prompt augmentation: os trechos recuperados são inseridos no prompt do LLM como contexto adicional antes da geração da resposta final.
- Busca híbrida (hybrid search): combinação de busca vetorial (semântica) com busca por palavras-chave (lexical, ex.: BM25) para melhorar cobertura.
- Grounding: ancorar as respostas do modelo em fontes verificáveis, reduzindo alucinações e permitindo citar a origem da informação.

## Na prática
- Frameworks como LangChain, LlamaIndex e Haystack facilitam a construção de pipelines RAG (ingestão, indexação, retrieval, geração).
- Casos de uso: chatbots de suporte com base em documentação interna, assistentes jurídicos que citam legislação, busca semântica em bases de conhecimento corporativas.
- Pipeline típico: ingestão de documentos → chunking → geração de embeddings → indexação no vector database → busca por similaridade → reranking (opcional) → geração com contexto.
- Modelos de embedding populares incluem os da OpenAI, Cohere e modelos open-source como os da família BGE e E5.

## Pontos de atenção
- A qualidade do RAG depende fortemente da estratégia de chunking; chunks muito grandes diluem a relevância, muito pequenos perdem contexto.
- Retrieval ruim ("recuperou o trecho errado") é a causa mais comum de respostas erradas em sistemas RAG, mais do que falha do LLM em si.
- Atualização e sincronização da base de conhecimento precisam de um processo de reindexação contínuo para não ficar defasada.
- RAG reduz mas não elimina alucinações; o modelo ainda pode ignorar o contexto fornecido ou misturá-lo com conhecimento prévio incorreto.
- Avaliar sistemas RAG requer métricas específicas de retrieval (recall@k, precisão) além das métricas de qualidade da geração final.
