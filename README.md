<div align="center">

# 🧑‍🍳 Receitas de IA & Infraestrutura (CDC Recipes)

[![Status](https://img.shields.io/badge/status-ativo-brightgreen.svg)](#)
[![Organização](https://img.shields.io/badge/CDC-Receitas-blue.svg)](#)
[![Python](https://img.shields.io/badge/python-3.10+-3776AB?logo=python&logoColor=white)](#)
[![IA Powered](https://img.shields.io/badge/IA-Gemini%20%7C%20OpenAI%20%7C%20Claude-7B2CBF)](#)
[![Licença](https://img.shields.io/badge/licença-MIT-green.svg)](#)

*Repositório centralizado de boilerplates, configurações de infraestrutura, prompts de sistema e padrões de código de IA para cópia rápida em novos projetos.*

</div>

---

## 📂 Navegação de Diretórios

Clique abaixo para acessar o conteúdo de cada pasta diretamente no repositório:

| Diretório | Descrição | Conteúdo sugerido |
| :--- | :--- | :--- |
| [📂 **prompts/**](./prompts) | Prompts de sistema e engenharia de prompt | Prompts de sistema para codificação, meta-prompts de documentação, etc. |
| [📂 **api/**](./api) | Boilerplates de integração de APIs de LLM | Scripts prontos para Gemini, OpenAI, Anthropic, etc. |
| [📂 **infra/**](./infra) | Arquitetura, Backups, DNS e Segurança | Guia Rclone/GDrive, Cofres OpenBao/Vaultwarden, DNS e E-mail. |
| [📂 **mcp/**](./mcp) | Servidores MCP (Model Context Protocol) | Modelos básicos para criar e estender servidores MCP. |
| [📂 **agents/**](./agents) | Loops e frameworks de Agentes | Arquiteturas simples de agentes, tool use, etc. |
| [📂 **ui/**](./ui) | Interfaces rápidas para prototipagem | Templates Streamlit, HTML/CSS ou Gradio para testes rápidos. |

---

## 📑 Índice de Receitas Ativas

### 💬 Prompts & Governança
* 🔌 **[System Prompt de Codificação](./prompts/system_prompts.md)**: Prompt de sistema robusto para configurar LLMs para atuar como desenvolvedores seniores.
* ✍️ **[Meta-Prompt de Redação Técnica e Documentação](./prompts/meta_prompt_documentacao.md)**: Guia universal para alimentar a IA como Arquiteto de Informação, aplicando o modelo híbrido de escrita e alimentação incremental.

### 🐍 Integrações de API
* 🚀 **[Gemini Quickstart (Python)](./api/gemini_quickstart.py)**: Template em Python para iniciar rapidamente chamadas com a API do Gemini, suportando respostas em streaming e Structured Outputs (JSON).

### 🛠️ Infraestrutura & Segurança
* 📦 **[Backup Automatizado Rclone + Google Drive](./infra/estrategia_backup_rclone_gdrive.md)**: Guia de backup offsite incremental com Rclone no Google Drive e alertas em webhook para Mattermost/Discord/Slack.
* 🔐 **[Cofres Híbridos (Vaultwarden + OpenBao)](./infra/cofres_segredos_openbao_vaultwarden.md)**: Gestão de credenciais humanas vs máquinas, segredos dinâmicos com tempo de vida (TTL) e subdomínios ofuscados.
* 🌐 **[Checklist de Zonas DNS & E-mail Corporativo](./infra/dns_email_domain_checklist.md)**: Tabela de referência DNS para subdomínios de VPS, Vercel, Google Workspace, Postal SMTP, SPF, DKIM e DMARC.

---

## 🔒 Auditoria de Segurança

> [!IMPORTANT]
> Este repositório é auditado para garantir que **nenhuma credencial real, senha, chave privada ou webhook sensível** seja exposto. Todos os arquivos de exemplo usam variáveis de ambiente (`os.getenv`) ou placeholders genéricos (ex: `sua_chave_api_aqui`).

---

## 🛠️ Como Usar e Copiar

1. **Navegue** até o diretório da receita desejada clicando nas tabelas acima.
2. **Copie** o código ou prompt relevante.
3. **Cole** no seu novo projeto.

> [!TIP]
> Ao adicionar novas receitas, mantenha os scripts independentes e auto-contidos para que a cópia seja o mais simples possível.
