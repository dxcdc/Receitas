# 💾 Política de Backup 3-2-1, Rclone (Google Drive) e Alertas no Mattermost

Este documento estabelece as diretrizes de proteção de dados, versionamento offsite via Rclone no Google Drive e alertas em tempo real no Mattermost para o repositório **Receitas**.

---

## 1. Estratégia de Backup 3-2-1 com Rclone

Aplicamos os princípios da regra 3-2-1 para o repositório de receitas:

- **3 Cópias dos Dados**:
  1. Cópia de desenvolvimento na máquina física do desenvolvedor.
  2. Cópia principal no serviço de Git (GitHub remote em `git@github.com:dxcdc/Receitas.git`).
  3. Cópia offsite criptografada via **Rclone** no Google Drive Corporativo (`cdc-gdrive:CDC_Backups/`).
- **2 Meios de Armazenamento Diferentes**:
  1. Disco local SSD / Git local.
  2. Nuvem (GitHub + Google Workspace Drive via Rclone).
- **1 Cópia Offsite Criptografada**:
  - Armazenada no Google Drive em pasta protegida via Rclone Crypt / GPG.

---

## 2. Frequência e Metas (RPO / RTO)

- **RPO (Recovery Point Objective)**: Máximo de 24 horas.
- **RTO (Recovery Time Objective)**: Máximo de 15 minutos.

---

## 3. Notificação Automática por Webhook no Mattermost

Todo script de backup offsite via Rclone notifica o canal operacional do Mattermost ao finalizar a execução:

- 🟢 **Sucesso**: Envia o nome do repositório, timestamp, tamanho do backup e hash SHA-256.
- 🔴 **Falha**: Dispara alerta com tag de emergência no canal `#alertas-infra` do Mattermost descrevendo a falha na sincronização do Rclone ou permissões do Google Drive.

---

## 4. Teste Periódico de Restauração (Audit Trail)

> [!IMPORTANT]
> **Alimentação Incremental:** Os testes de restauração e simulação de perda de dados devem ser registrados incrementalmente na tabela abaixo.

| Data do Teste | Tipo de Teste | Resultado | Tempo de Recuperação | Responsável |
| :--- | :--- | :--- | :--- | :--- |
| **2026-07-21** | Simulação de clonagem e restore Rclone no Google Drive | Sucesso total (100% das receitas e docs clonados) | 2 minutos | Equipe CDC |
