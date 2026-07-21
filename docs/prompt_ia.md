# 🤖 Instructions & System Context para Agentes de IA

Este documento contém o contexto de sistema permanente para assistentes e agentes de Inteligência Artificial (como Antigravity, Gemini Pro, Claude, ChatGPT, etc.) interagindo com este repositório de receitas.

---

## 1. Contexto do Repositório

- **Nome do Repositório**: `Receitas` (CDC)
- **Objetivo**: Repositório central de boilerplates, prompts, scripts de infraestrutura e padrões reutilizáveis de software/IA da empresa CDC.
- **Linguagens Principais**: Python, Bash, Markdown, JSON, YAML.
- **Git Remote**: `git@github.com:dxcdc/Receitas.git` (Branch padrão: `main`).

---

## 2. Regras Inegociáveis para Agentes de IA

1. **Nenhum Segredo no Código**: NUNCA escreva senhas reais, tokens ou chaves de API nos arquivos. Use `os.getenv()` ou placeholders genéricos (ex: `<GEMINI_API_KEY>`, `<MATTERMOST_WEBHOOK_URL>`).
2. **Links Relativos Nativos**: Sempre use links Markdown relativos (`./docs/ajuda_infra.md`). NUNCA use links com `file:///home/...`.
3. **Alimentação Incremental**: Ao atualizar documentos históricos como `postmortem.md` ou `troubleshooting.md`, adicione novos itens **no topo da lista/tabela**, sem apagar o histórico anterior.
4. **Nenhum Código Cortado**: Ao gerar receitas ou scripts, entregue código completo e executável. Não use reticências (`...`) para omitir trechos de código.
5. **Formatação Limpa**: Mantenha o `README.md` sempre sincronizado com qualquer nova receita adicionada nas pastas `prompts/`, `api/`, `infra/`, etc.

---

## 3. Prompts Rápidos de Manutenção

- **Adicionar nova receita**: "Crie uma receita para [DESCRIÇÃO], salve na pasta apropriada com sanitização total de credenciais e atualize o README.md."
- **Validar links e segurança**: "Audit o repositório em busca de links quebrados ou credenciais expostas."
