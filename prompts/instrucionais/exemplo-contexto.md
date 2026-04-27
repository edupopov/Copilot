# Exemplo: Prompt com Definição de Contexto

## Cenário
Você precisa fornecer ao Copilot o contexto do seu projeto, organização ou situação para que as respostas sejam relevantes e aplicáveis ao seu caso específico.

---

## Template

```
Contexto do projeto:
- Nome do projeto: [NOME]
- Objetivo: [OBJETIVO]
- Stack tecnológica: [TECNOLOGIAS]
- Fase atual: [FASE: planejamento / desenvolvimento / homologação / produção]
- Restrições: [RESTRIÇÕES TÉCNICAS, ORÇAMENTÁRIAS OU DE PRAZO]

Com base nesse contexto, [TAREFA OU PERGUNTA].
```

---

## Exemplos Práticos

### Exemplo 1 – Contexto de Projeto de Migração Cloud

```
Contexto do projeto:
- Nome: Migração ERP para Azure
- Objetivo: Migrar o ERP legado on-premises para Azure, garantindo disponibilidade de 99,9% e redução de custo operacional de 30%
- Stack tecnológica: Windows Server 2019, SQL Server 2019, Azure Migrate, Azure SQL Managed Instance
- Fase atual: Planejamento e discovery
- Restrições: Janela de manutenção de apenas 4 horas por semana; dados sensíveis sob LGPD

Com base nesse contexto, sugira uma estratégia de migração (Lift & Shift vs. Re-platform) e os principais riscos a considerar.
```

---

### Exemplo 2 – Contexto de Desenvolvimento de Aplicação

```
Contexto do projeto:
- Nome: Portal de Autoatendimento de RH
- Objetivo: Permitir que colaboradores consultem e atualizem seus dados cadastrais, visualizem holerites e solicitem férias
- Stack tecnológica: React 18, Node.js 20, Azure App Service, Azure AD para autenticação (SSO)
- Fase atual: Desenvolvimento (Sprint 3 de 8)
- Restrições: Time de 4 desenvolvedores; entrega em 60 dias

Com base nesse contexto, proponha a arquitetura de componentes do frontend e a estratégia de gerenciamento de estado mais adequada.
```

---

### Exemplo 3 – Contexto Organizacional para Adoção do Copilot

```
Contexto organizacional:
- Empresa: Média empresa do setor financeiro, ~1.200 colaboradores
- Objetivo: Adotar o Microsoft 365 Copilot para aumentar a produtividade em 20%
- Ambiente atual: Microsoft 365 E3, sem licenças Copilot ainda
- Fase atual: Avaliação e planejamento do piloto
- Restrições: Budget limitado; necessidade de aprovação do DPO para uso de dados corporativos

Com base nesse contexto, sugira um plano de piloto para adoção do Copilot, incluindo critérios de seleção dos primeiros usuários, métricas de sucesso e riscos a mitigar.
```

---

## Quando usar

- No início de uma sessão longa de trabalho com o Copilot
- Quando as respostas precisam ser específicas para o seu projeto ou organização
- Quando há restrições técnicas, regulatórias ou de negócio que devem ser consideradas
- Para garantir consistência nas respostas ao longo de múltiplas interações
