# 🎨 Roteiro de Personalização & Expansão de Categorias de Receitas

Este documento é um guia didático para a equipe expandir o repositório **Receitas** criando novas categorias, adicionando novos boilerplates ou personalizando a estrutura de documentação.

---

## 1. Como Adicionar uma Nova Categoria de Receita

Se você deseja adicionar um novo grupo de receitas (ex: `devops/`, `database/`, `frontend/`):

1. **Criar o diretório**:
   ```bash
   mkdir -p devops
   ```
2. **Criar o arquivo da receita**:
   Crie o arquivo Markdown ou de código com explicações claras, pré-requisitos e bloco de código auto-contido.
3. **Atualizar o `README.md`**:
   - Adicione o novo diretório na tabela **📂 Navegação de Diretórios** usando link relativo (ex: `[📂 devops/](./devops)`).
   - Adicione o item no **📑 Índice de Receitas Ativas**.
4. **Validar a ausência de segredos**:
   Verifique se o novo arquivo não contém API Keys ou senhas reais.

---

## 2. Padrão Recomendado para Arquivos de Receita

Toda nova receita deve seguir o seguinte esqueleto:

```markdown
# 🚀 [Título da Receita]

Breve descrição do que a receita resolve e qual problema ela evita.

---

## 📋 Pré-requisitos
- Dependências, bibliotecas ou ferramentas necessárias.

---

## 📝 O Código / Configuração

```python
# Bloco de código auto-contido e testado
```

---

## 🛠️ Como Usar
Passo a passo rápido de como copiar, colar e testar.
```
