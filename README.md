# Squad Dev Team

Squad de agentes customizados para transformar uma ideia em software testado e pronto para producao. O manifesto e [squad.yaml](squad.yaml), o fluxo e [pipeline/pipeline.yaml](pipeline/pipeline.yaml) e as regras compartilhadas estao em [.agents/rules/GEMINI.md](.agents/rules/GEMINI.md).

## Como usar

1. Abra este workspace no Antigravity.
2. Inicie uma tarefa com `/orchestrate` ou descreva diretamente o resultado desejado.
3. Informe apenas restricoes essenciais; o squad explora o repositorio e usa defaults quando nao houver bloqueio critico.
4. Acompanhe os artefatos em `.squad/` e o relatorio final com arquivos alterados, testes, riscos e URL de deploy.

Exemplo:

> Crie um dashboard de vendas responsivo com login, filtros por periodo, API segura, testes E2E e deploy em staging.

Para uma demanda sem UI, declare isso no pedido ou deixe o orquestrador detectar. As etapas de design e backend sao condicionais; exploracao, planejamento, frontend, revisao, testes e deploy fazem parte do fluxo padrao.

## Papéis

`explorer` mapeia o projeto, `planner` transforma requisitos em plano, `designer` define a experiencia, `backend-dev` implementa APIs e dados, `frontend-dev` implementa a interface, `reviewer` audita qualidade e seguranca, `qa` testa, `devops` valida e publica, e `orchestrator` coordena o conjunto.

## Economia de tokens e autonomia

- Carregar primeiro regras, frontmatter do agente e apenas as secoes de skills necessarias.
- Preferir buscas direcionadas, contexto local e resumos entre etapas.
- Fazer uma pergunta consolidada somente quando houver bloqueio critico.
- Reutilizar convencoes e scripts existentes antes de inventar abstracoes.
- Nunca declarar sucesso sem teste, auditoria de seguranca e health check registrados.

## Comandos uteis

```text
/orchestrate Crie um sistema de login com cadastro, recuperacao de senha e dashboard.
/plan Planeje uma API de pedidos com PostgreSQL.
/test Execute os testes da funcionalidade de autenticacao.
/deploy check Valide a release antes do deploy.
```

Requisitos: Node.js 18+ e Python 3.9+ para os scripts de auditoria.