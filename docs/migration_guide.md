# 🚚 Guia de Migração, Clonagem e Onboarding

Este guia orienta o desenvolvedor ou profissional de DevOps a clonar, configurar e utilizar o repositório de **Receitas** em uma nova máquina física, máquina virtual ou ambiente de desenvolvimento.

---

## 1. Requisitos Prévios

- **Git** instalado e configurado com chave SSH autorizada no GitHub.
- **Python 3.10+** (para execução dos scripts de exemplo das APIs de IA).
- **Rclone** (opcional, para execução de receitas de backup offsite).

---

## 2. Passo a Passo de Clonagem

### Passo 1: Clonar o repositório via SSH
```bash
git clone git@github.com:dxcdc/Receitas.git
cd Receitas
```

### Passo 2: Validar o estado do repositório
```bash
git status
git log -n 3
```

### Passo 3: Configurar ambiente virtual Python (Para testar receitas de API)
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install google-genai pydantic requests
```

---

## 3. Validação pós-clonagem

1. Abra o arquivo `README.md` no seu editor ou visualizador de Markdown.
2. Certifique-se de que os links relativos apontam corretamente para os arquivos em `prompts/`, `api/`, `infra/` e `docs/`.
3. Teste a execução do script `api/gemini_quickstart.py` com sua variável de ambiente `GEMINI_API_KEY`.
