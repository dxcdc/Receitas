# 📝 Registro de Postmortem & Lições Aprendidas (Cultura Blameless)

Este documento registra análises de incidentes, falhas operacionais e lições aprendidas durante o desenvolvimento e manutenção das receitas da organização.

---

## 1. Princípio da Cultura Blameless (Não-Culpável)

Análises de incidentes não buscam culpados individuais, mas sim falhas em processos, documentações ou ferramentas. O objetivo é ajustar os processos para evitar recorrências.

---

## 2. Histórico Incremental de Incidentes

> [!IMPORTANT]
> **Alimentação Incremental:** Novos relatórios de postmortem devem ser adicionados **no topo da tabela abaixo**, preservando o histórico completo.

| ID | Data | Severidade | Resumo do Incidente | Causa Raiz | Ação Corretiva |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **INC-001** | 2026-07-21 | Baixa | Links absolutos locais (`file:///home/...`) no README não funcionavam no GitHub | Utilização de gerador de links local sem validação no GitHub Web | Substituição de todos os links do README por caminhos relativos (`./`) |

---

## 3. Modelo de Registro de Novo Incidente

Ao registrar um novo incidente crítico, copie a estrutura abaixo:

```markdown
### Incidente INC-XXX: [Título Resumido]
- **Data:** AAAA-MM-DD
- **Severidade:** [Crítica / Alta / Média / Baixa]
- **Impacto:** [Descrição do impacto observado]

#### 1. Linha do Tempo (Timeline)
- `14:00` - Ocorrência da falha detectada.
- `14:15` - Início da investigação.
- `14:30` - Correção aplicada e validada.

#### 2. Causa Raiz (5 Porquês)
1. Por que ocorreu? Explicar a falha inicial.
2. Por que isso não foi evitado? Falha no processo ou falta de teste.

#### 3. Ações Preventivas
- [ ] Criar receita de teste ou validação.
- [ ] Atualizar a documentação correspondente.
```
