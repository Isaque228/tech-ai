# Segurança em IA

Segurança em IA (AI Security) trata dos riscos técnicos específicos que surgem ao construir e operar sistemas de IA, incluindo ataques direcionados ao modelo, vazamento de dados sensíveis e uso indevido por atores maliciosos. É um campo distinto de segurança da informação tradicional porque os vetores de ataque exploram particularidades de como modelos de ML e LLMs processam entradas.

## Conceitos principais
- Prompt injection: inserir instruções maliciosas em conteúdo processado pelo modelo (documentos, páginas web, e-mails) para fazê-lo desviar do comportamento pretendido.
- Jailbreaking: técnicas usadas para contornar as restrições de segurança de um modelo e fazê-lo gerar conteúdo que normalmente seria bloqueado.
- Data poisoning: contaminação intencional dos dados de treino para induzir comportamentos indesejados ou backdoors no modelo resultante.
- Ataques adversariais: pequenas perturbações nos dados de entrada, muitas vezes imperceptíveis, que causam erros de classificação em modelos (comum em visão computacional).
- Extração de modelo (model extraction): reconstruir ou copiar um modelo proprietário através de consultas repetidas à sua API.
- Vazamento de dados de treino (memorization): modelos podem memorizar e reproduzir trechos específicos dos dados de treino, incluindo informação sensível.
- Exfiltração de dados via agentes: agentes com acesso a ferramentas e dados sensíveis podem ser manipulados para expor ou enviar essas informações para fora do ambiente controlado.
- Sandboxing e least privilege: princípio de restringir o acesso de modelos e agentes apenas ao mínimo necessário de dados e permissões para executar sua função.

## Na prática
- Aplicações que processam conteúdo de terceiros (RAG, agentes de navegação web) precisam tratar esse conteúdo como não confiável, similar a entrada de usuário em segurança web tradicional.
- Guardrails (filtros de entrada e saída) e classificadores de conteúdo são usados para detectar e bloquear tentativas de jailbreak ou saídas prejudiciais.
- Red teaming — testar ativamente o sistema com ataques simulados — é prática recomendada antes de lançar aplicações de IA em produção.
- Isolamento de execução (containers, sandboxes) é essencial quando agentes têm permissão para executar código ou comandos no sistema.

## Pontos de atenção
- Nunca conceder a agentes de IA permissões amplas (acesso irrestrito a arquivos, rede, credenciais) sem necessidade explícita e revisão.
- Confiar ciegamente em instruções vindas de conteúdo externo (documentos, resultados de busca) é uma das causas mais comuns de comprometimento via prompt injection.
- Logs e auditoria das ações de agentes são essenciais para investigar incidentes, já que o comportamento pode não ser totalmente determinístico.
- Segurança em IA é uma corrida constante: novas técnicas de ataque (jailbreak) e defesa evoluem continuamente, exigindo atualização contínua de guardrails.
- Testes de segurança tradicionais (pentest de infraestrutura) não cobrem os riscos específicos de modelos; é necessário avaliação especializada em IA.
