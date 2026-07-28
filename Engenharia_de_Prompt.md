# Engenharia de Prompt

Engenharia de Prompt é a prática de projetar e refinar as instruções (prompts) dadas a um modelo de linguagem para obter respostas mais precisas, úteis e consistentes. É uma habilidade central para extrair o máximo de LLMs sem precisar treinar ou ajustar o modelo, funcionando como a principal interface entre intenção humana e comportamento do modelo.

## Conceitos principais
- Zero-shot vs. few-shot: pedir uma tarefa sem exemplos (zero-shot) ou fornecer alguns exemplos de entrada-saída no próprio prompt (few-shot) para guiar o comportamento.
- Chain-of-thought (cadeia de pensamento): instruir o modelo a raciocinar passo a passo antes de dar a resposta final, melhorando desempenho em tarefas complexas.
- System prompt: instrução de alto nível que define papel, tom e restrições do modelo, geralmente aplicada antes da conversa do usuário.
- Estrutura e formatação: uso de delimitadores (XML, markdown, JSON) para separar claramente instruções, contexto e dados de entrada, reduzindo ambiguidade.
- Especificidade e clareza: prompts vagos geram respostas vagas; especificar formato, restrições e critérios de sucesso reduz variabilidade indesejada.
- Prompt injection: quando conteúdo externo inserido no prompt (ex.: um documento) contém instruções que tentam sobrescrever as instruções originais do sistema.
- Role prompting: atribuir uma persona ou papel ao modelo ("aja como um revisor de código sênior") para influenciar o estilo e o foco da resposta.
- Iteração e avaliação: prompt engineering é um processo empírico de testar variações e medir resultados, não uma ciência exata de primeira tentativa.

## Na prática
- Ferramentas como playgrounds de API (Anthropic Console, OpenAI Playground) permitem testar e comparar variações de prompt rapidamente.
- Frameworks de avaliação (promptfoo, LangSmith) ajudam a medir de forma sistemática o impacto de mudanças no prompt sobre a qualidade das respostas.
- Técnicas comuns em produção: templates de prompt parametrizados, few-shot com exemplos representativos do domínio, instruções de formato de saída (JSON estruturado).
- Prompts bem escritos reduzem a necessidade de fine-tuning em muitos casos, sendo a primeira alternativa a testar antes de treinar um modelo customizado.

## Pontos de atenção
- Prompts muito longos ou com instruções conflitantes podem confundir o modelo e degradar a qualidade da resposta.
- Resultados podem variar entre versões de modelo; um prompt otimizado para um modelo específico pode não performar igual em outro.
- Prompt injection é um risco real em aplicações que processam conteúdo de terceiros (documentos, e-mails, páginas web) como parte do contexto.
- Depender excessivamente de "prompt tricks" frágeis (frases mágicas) em vez de instruções claras e testáveis torna o sistema difícil de manter.
- Testar apenas alguns exemplos manualmente não garante robustez; é importante avaliar em um conjunto diverso de casos, incluindo casos extremos (edge cases).
