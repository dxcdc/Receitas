# 🚀 Estratégia de Execução, Versionamento e Contribuição

Este documento define o fluxo de trabalho Git, a organização das branches e o ciclo de inclusão de novas receitas no repositório **Receitas**.

---

## 1. Estratégia de Branches no Git

Adotamos uma versão simplificada e segura do GitFlow:

- **`main`**: Branch de produção e referência estável. Todo código e prompt na `main` deve estar testado, sanitizado e documentado.
- **`feature/<nome-da-receita>`**: Branch temporária para criação ou revisão de novas receitas antes de mesclar na `main`.

---

## 2. Padrão de Commits

Utilizamos o padrão de **Conventional Commits**:

- `feat:` Inclusão de novas receitas ou utilitários (ex: `feat: adiciona template de API da Anthropic`).
- `docs:` Atualização ou adição de arquivos de documentação (ex: `docs: atualiza guia de backup no README`).
- `fix:` Correção de erros em scripts de receita ou links quebrados.
- `style:` Formatação, alinhamento de tabela ou adição de badges visuais.

---

## 3. Checklist para Adição de Nova Receita

Antes de mesclar uma nova receita para a branch `main`:

1. [ ] **Sanitização de Código**: Garantir que nenhum segredo real (API Keys, senhas, tokens) esteja presente.
2. [ ] **Testabilidade**: Verificar se o código de exemplo roda sem erros de sintaxe.
3. [ ] **Atualização do Index**: Incluir a nova receita na tabela correspondente do `README.md` usando **links relativos**.
4. [ ] **Links Relativos**: Confirmar que não há links absolutos (`file:///home/...`).

---

## 4. Plano de Rollback

Caso um commit incorreto ou com dados sensíveis seja enviado acidentalmente:

```bash
# 1. Reverter o último commit localmente mantendo os arquivos:
git reset --soft HEAD~1

# 2. Remover o arquivo sensível do stage:
git rm --cached arquivo_sensivel.ext

# 3. Refazer o commit limpo:
git commit -m "fix: remove credencial exposta"

# 4. Forçar a atualização na branch (se necessário):
git push origin main --force
```
