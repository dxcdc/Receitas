# 🧑‍🍳 Receitas de IA & Infraestrutura (CDC Recipes)

Bem-vindo ao repositório de **Receitas de IA & Infraestrutura**! Este é o seu espaço centralizado para armazenar códigos, configurações, prompts e padrões de arquitetura e integração que podem ser facilmente copiados e colados em qualquer novo projeto.

O objetivo aqui é economizar tempo de configuração inicial e garantir que você e sua equipe sempre comecem com as melhores práticas.

---

## 📂 Estrutura do Repositório

Aqui está a organização das receitas:

| Diretório | Descrição | Conteúdo sugerido |
| :--- | :--- | :--- |
| [📂 prompts/](file:///home/vier/Documentos/Code/CDC/Receitas/prompts) | Prompts de sistema e engenharia de prompt | Prompts de sistema para codificação, meta-prompts de documentação, etc. |
| [📂 api/](file:///home/vier/Documentos/Code/CDC/Receitas/api) | Boilerplates de integração de APIs de LLM | Scripts prontos para Gemini, OpenAI, Anthropic, etc. |
| [📂 infra/](file:///home/vier/Documentos/Code/CDC/Receitas/infra) | Arquitetura, Backups, DNS e Segurança | Guia Rclone/GDrive, Cofres OpenBao/Vaultwarden, DNS e E-mail. |
| [📂 mcp/](file:///home/vier/Documentos/Code/CDC/Receitas/mcp) | Servidores MCP (Model Context Protocol) | Modelos básicos para criar e estender servidores MCP. |
| [📂 agents/](file:///home/vier/Documentos/Code/CDC/Receitas/agents) | Loops e frameworks de Agentes | Arquiteturas simples de agentes, tool use, etc. |
| [📂 ui/](file:///home/vier/Documentos/Code/CDC/Receitas/ui) | Interfaces rápidas para prototipagem | Templates Streamlit, HTML/CSS ou Gradio para testes rápidos. |

---

## 📑 Índice de Receitas Ativas

### 💬 Prompts & Governança
* 🔌 **[System Prompt de Codificação](file:///home/vier/Documentos/Code/CDC/Receitas/prompts/system_prompts.md)**: Prompt de sistema robusto para configurar LLMs para atuar como desenvolvedores seniores.
* ✍️ **[Meta-Prompt de Redação Técnica e Documentação](file:///home/vier/Documentos/Code/CDC/Receitas/prompts/meta_prompt_documentacao.md)**: Guia universal para alimentar a IA como Arquiteto de Informação, aplicando o modelo híbrido de escrita e alimentação incremental.

### 🐍 Integrações de API
* 🚀 **[Gemini Quickstart (Python)](file:///home/vier/Documentos/Code/CDC/Receitas/api/gemini_quickstart.py)**: Template em Python para iniciar rapidamente chamadas com a API do Gemini, suportando respostas em streaming e Structured Outputs (JSON).

### 🛠️ Infraestrutura & Segurança
* 📦 **[Backup Automatizado Rclone + Google Drive](file:///home/vier/Documentos/Code/CDC/Receitas/infra/estrategia_backup_rclone_gdrive.md)**: Guia de backup offsite incremental com Rclone no Google Drive e alertas em webhook para Mattermost/Discord/Slack.
* 🔐 **[Cofres Híbridos (Vaultwarden + OpenBao)](file:///home/vier/Documentos/Code/CDC/Receitas/infra/cofres_segredos_openbao_vaultwarden.md)**: Gestão de credenciais humanas vs máquinas, segredos dinâmicos com tempo de vida (TTL) e subdomínios ofuscados.
* 🌐 **[Checklist de Zonas DNS & E-mail Corporativo](file:///home/vier/Documentos/Code/CDC/Receitas/infra/dns_email_domain_checklist.md)**: Tabela de referência DNS para subdomínios de VPS, Vercel, Google Workspace, Postal SMTP, SPF, DKIM e DMARC.

---

## 🛠️ Como Usar e Copiar

1. **Navegue** até o diretório da receita desejada.
2. **Copie** o código ou prompt relevante.
3. **Cole** no seu novo projeto.

> [!TIP]
> Ao adicionar novas receitas, mantenha os scripts independentes e auto-contidos para que a cópia seja o mais simples possível.
