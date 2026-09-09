# Squad Dev Team

<p align="left">
	<a href="https://www.npmjs.com/package/@uuartofc/squad-dev-team"><img src="https://img.shields.io/npm/v/@uuartofc/squad-dev-team?logo=npm&color=CB3837" alt="versao npm"></a>
	<a href="https://github.com/uuartofc/Web-Kit-Agents"><img src="https://img.shields.io/github/stars/uuartofc/Web-Kit-Agents?style=flat&logo=github" alt="estrelas no GitHub"></a>
	<a href=".agents/LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue" alt="licenca MIT"></a>
</p>

Um squad de agentes de IA para levar uma ideia de software da descoberta ao deploy verificado. Ele instala especialistas, skills, workflows, regras e scripts de qualidade no seu projeto.

## Comece em segundos

Na raiz do projeto que recebera o squad:

```bash
npx @uuartofc/squad-dev-team
```

O comando cria `.agents/` no diretorio atual e preserva uma instalacao existente. Para instalar globalmente:

```bash
npm install -g @uuartofc/squad-dev-team
squad-dev-team
```

Tambem e possivel indicar outro projeto:

```bash
npx @uuartofc/squad-dev-team ./meu-projeto
```

Depois, abra o projeto no Antigravity e inicie uma tarefa com `/orchestrate` ou descreva diretamente o resultado desejado.

> Requer Node.js 18+. Os scripts de auditoria tambem requerem Python 3.9+.

## Instalar a partir do GitHub

Para testar a versao mais recente sem esperar uma publicacao no npm:

```bash
npx --yes github:uuartofc/Web-Kit-Agents
```

Ou clone o repositorio e use o workspace local:

```bash
git clone https://github.com/uuartofc/Web-Kit-Agents.git
cd Web-Kit-Agents
npm install
npm link
cd ../meu-projeto
squad-dev-team
```

## O que e `.agents/`?

E a camada de contexto versionada do projeto: especialistas, conhecimento tecnico, processos, regras e verificacoes ficam disponiveis para os agentes.

```text
.agents/
├── agents/       Papeis especializados
├── skills/       Conhecimento reutilizavel
├── workflows/    Processos de desenvolvimento
├── rules/        Regras do workspace
├── scripts/      Testes e auditorias
└── mcp/          Integracoes externas
```

## O que o squad cobre

- **Descoberta e plano:** explora o repositorio e transforma requisitos em etapas executaveis.
- **Frontend:** UX, acessibilidade, tipografia, responsividade e performance.
- **Backend:** APIs, bancos de dados, autenticacao e arquitetura.
- **Qualidade:** testes unitarios, integracao, E2E e checklists de release.
- **Seguranca:** OWASP, autorizacao, SSRF, injecao, supply chain e resiliencia.
- **Deploy:** validacao de release, health check e relatorio final.

## Fluxo recomendado

```text
[ideia] Ideia -> [plano] Planejamento -> [codigo] Implementacao -> [teste] QA -> [escudo] Revisao -> [navio] Deploy
```

Comandos disponiveis no ambiente de agentes:

```text
/orchestrate Crie um sistema de login com cadastro e dashboard.
/plan Planeje uma API de pedidos com PostgreSQL.
/test Execute os testes da funcionalidade de autenticacao.
/deploy check Valide a release antes do deploy.
```

O pipeline padrao executa exploracao, planejamento, frontend, revisao, testes e deploy. Design e backend entram quando a demanda exigir.

## Validar a instalacao

```bash
python .agents/scripts/verify_all.py .
python .agents/scripts/checklist.py .
```

O resultado final deve registrar arquivos alterados, testes, riscos e URL de deploy quando houver.

## Documentacao

- [Arquitetura do workspace](.agents/ARCHITECTURE.md)
- [Manifesto do squad](squad.yaml)
- [Pipeline completo](pipeline/pipeline.yaml)
- [Regras compartilhadas](.agents/rules/GEMINI.md)
- [README do kit de agentes](.agents/README.md)

## Uso responsavel

Use o squad apenas em projetos proprios ou autorizados. Revise as configuracoes MCP antes de habilitar servidores externos e execute auditorias somente contra ambientes sob seu controle.

## Licenca

MIT. Consulte [.agents/LICENSE](.agents/LICENSE).
