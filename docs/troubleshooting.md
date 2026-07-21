# 🔍 Guia de Troubleshooting & Diagnóstico de Problemas

Este guia auxilia na identificação e solução de problemas comuns ao executar scripts de receitas ou manipular o repositório.

---

## 1. Problemas Frequentes e Soluções

> [!IMPORTANT]
> **Alimentação Incremental:** Novas ocorrências e soluções devem ser adicionadas incrementalmente no topo desta tabela.

| Sintoma / Erro | Causa Provável | Solução Recomendada |
| :--- | :--- | :--- |
| `GEMINI_API_KEY não encontrada no ambiente` | Variável de ambiente não foi exportada antes da execução do script | Execute `export GEMINI_API_KEY="sua_chave"` no terminal antes de rodar o Python. |
| `ModuleNotFoundError: No module named 'google'` | Dependências do SDK do Gemini não estão instaladas no Python local | Execute `pip install google-genai pydantic`. |
| `Permission denied (publickey)` ao dar `git push` | Chave SSH do GitHub não está ativa na sessão de terminal atual | Execute `eval "$(ssh-agent -s)"` e adicione sua chave com `ssh-add ~/.ssh/id_ed25519`. |
| Links de markdown não abrem no GitHub | Uso de sintaxe de arquivo local (`file:///...`) em vez de caminho relativo | Substitua a URL no Markdown para o formato relativo, como `./prompts/arquivo.md`. |

---

## 2. Checklist de Diagnóstico Rápido

Antes de abrir um chamado ou solicitar suporte:

1. [ ] Teste a variável de ambiente: `echo $GEMINI_API_KEY` (não deve estar vazia).
2. [ ] Teste a conexão Git: `ssh -T git@github.com`.
3. [ ] Verifique o status dos arquivos: `git status`.
