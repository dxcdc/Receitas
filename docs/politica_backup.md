# 💾 Política de Backup 3-2-1 e Sincronização Offsite

Este documento estabelece as diretrizes de proteção de dados, versionamento offsite e prevenção contra perdas para o repositório **Receitas**.

---

## 1. Estratégia de Backup 3-2-1

Aplicamos os princípios da regra 3-2-1 para o repositório de receitas:

- **3 Cópias dos Dados**:
  1. Cópia de desenvolvimento na máquina física do desenvolvedor.
  2. Cópia principal no serviço de Git (GitHub remote em `git@github.com:dxcdc/Receitas.git`).
  3. Cópia offsite criptografada via Rclone no Google Drive Corporativo.
- **2 Meios de Armazenamento Diferentes**:
  1. Disco local SSD / Git local.
  2. Nuvem (GitHub + Google Workspace Drive).
- **1 Cópia Offsite Criptografada**:
  - Armazenada no Google Drive em pasta protegida via Rclone Crypt.

---

## 2. Frequência e Metas (RPO / RTO)

- **RPO (Recovery Point Objective)**: Máximo de 24 horas (em caso de falha completa de hardware, perde-se no máximo o trabalho do dia atual se não tiver sido commitado).
- **RTO (Recovery Time Objective)**: Máximo de 15 minutos (tempo necessário para dar um `git clone` em uma nova máquina).

---

## 3. Teste Periódico de Restauração (Audit Trail)

> [!IMPORTANT]
> **Alimentação Incremental:** Os testes de restauração e simulação de perda de dados devem ser registrados incrementalmente na tabela abaixo.

| Data do Teste | Tipo de Teste | Resultado | Tempo de Recuperação | Responsável |
| :--- | :--- | :--- | :--- | :--- |
| **2026-07-21** | Simulação de clonagem em nova máquina via SSH | Sucesso total (100% das receitas e docs clonados) | 2 minutos | Equipe CDC |
