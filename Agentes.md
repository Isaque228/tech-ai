# Agentes de IA

Agentes de IA são sistemas construídos sobre LLMs que, além de gerar texto, podem planejar, tomar decisões e executar ações no mundo real ou digital por meio de ferramentas (tools/function calling), operando de forma mais autônoma para atingir um objetivo em múltiplas etapas. Representam a evolução de chatbots simples para sistemas capazes de resolver tarefas complexas com pouca supervisão humana direta.

## Conceitos principais
- Function calling / tool use: capacidade do LLM de invocar funções externas (APIs, bancos de dados, scripts) estruturando a chamada em um formato definido.
- Loop agente (agent loop): ciclo de raciocínio-ação-observação em que o agente decide uma ação, executa, observa o resultado e decide o próximo passo.
- Planejamento: quebrar um objetivo complexo em subtarefas menores e sequenciá-las, podendo ser feito pelo próprio LLM ou por um planejador externo.
- Memória: mecanismos para o agente manter contexto além da janela de uma única conversa, seja de curto prazo (dentro da sessão) ou longo prazo (persistida entre sessões).
- Multi-agente: arquiteturas em que vários agentes especializados colaboram, cada um responsável por uma parte do problema, coordenados por um agente orquestrador.
- ReAct (Reasoning + Acting): padrão de prompting em que o modelo alterna entre raciocínio explícito e execução de ações antes de chegar à resposta final.
- MCP (Model Context Protocol): padrão aberto para conectar agentes a ferramentas e fontes de dados externas de forma padronizada.
- Human-in-the-loop: pontos de checagem onde uma pessoa aprova ou corrige ações do agente antes de execução, especialmente em ações irreversíveis.
- Autonomia vs. controle: grau de liberdade dado ao agente para decidir e agir sem intervenção humana, um trade-off central no design de agentes.

## Na prática
- Frameworks e SDKs: LangGraph, CrewAI, AutoGen e o Claude Agent SDK oferecem abstrações para construir agentes com ferramentas e memória.
- Casos de uso: assistentes de codificação que leem, editam e testam código autonomamente; agentes de atendimento que consultam sistemas internos e executam ações (reembolsos, agendamentos); automação de pesquisa e análise de dados.
- Agentes de código (coding agents) como Claude Code combinam leitura de arquivos, execução de comandos e edição para completar tarefas de engenharia de ponta a ponta.
- Orquestração multi-agente é usada quando tarefas exigem especialização clara, como um agente pesquisador e outro revisor.

## Pontos de atenção
- Agentes autônomos podem executar ações indesejadas ou em loop se o objetivo ou as ferramentas não estiverem bem delimitados.
- Ações irreversíveis (deletar dados, enviar pagamentos, publicar conteúdo) devem sempre ter camadas de confirmação ou permissão explícita.
- Custos podem escalar rapidamente, já que cada etapa do loop agente consome chamadas adicionais ao modelo.
- Falta de observabilidade (logs, rastreamento de decisões) dificulta debugar por que um agente tomou determinada ação.
- Segurança das ferramentas expostas ao agente é crítica: uma ferramenta mal projetada pode ser explorada via prompt injection para causar dano.
