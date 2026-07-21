# 🛠️ Infraestrutura, Estrutura de Pastas e Cheat Sheet

Este documento reúne os comandos rápidos de terminal e o mapa técnico de infraestrutura do repositório de **Receitas**.

---

## 1. Mapeamento de Diretórios

```text
/home/vier/Documentos/Code/CDC/Receitas/
├── README.md               # Painel visual com mapa Mermaid e links
├── .gitignore              # Proteção contra envio de venvs e credenciais
├── docs/                   # 8 arquivos oficiais de governança técnica
├── prompts/                # Prompts de sistema e meta-prompts para IAs
├── api/                    # Snippets de código de APIs em Python/Node
└── infra/                  # Receitas de backups, cofres OpenBao e DNS
```

---

## 2. Comandos Rápido de Terminal (Cheat Sheet)

### Git Operations
```bash
# Verificar modificações
git status

# Criar e alternar para uma nova branch de receita
git checkout -b feature/nova-receita

# Adicionar e commitar alterações
git add .
git commit -m "feat: adiciona receita de integração com Claude API"

# Enviar alterações para o GitHub
git push origin main
```

### Validação de Receitas em Python
```bash
# Definir chave temporária e rodar quickstart
export GEMINI_API_KEY="sua_chave_aqui"
python3 api/gemini_quickstart.py
```

### Teste de Alerta Webhook (Mattermost / Discord)
```bash
# Teste de webhook sanitizado
WEBHOOK_URL="https://seu-mattermost.com/hooks/<MATTERMOST_WEBHOOK_URL>"
curl -i -X POST -H 'Content-Type: application/json' \
  --data '{"text": "🧪 Teste de notificação de receita de infraestrutura"}' \
  "$WEBHOOK_URL"
```
