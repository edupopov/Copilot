# Segurança, Privacidade e Compliance no Uso do Copilot

Este documento define as diretrizes de segurança e privacidade para uso responsável do Microsoft Copilot e Copilot Studio em ambientes corporativos.

---

## 🔒 Princípios Fundamentais de Segurança

### 1. Dados Sensíveis Nunca Devem Ser Inseridos em Prompts

**Nunca inclua em prompts:**
- Senhas, chaves de API, tokens de acesso ou certificados
- Dados pessoais identificáveis (CPF, RG, nome completo + cargo, dados de saúde)
- Informações financeiras de clientes ou da empresa (faturamento, margens, contratos)
- Dados sob sigilo legal ou regulatório (processos judiciais, acordos confidenciais)
- Propriedade intelectual de terceiros protegida por NDA
- Credenciais de sistemas internos (connection strings, senhas de banco)

**Em vez disso:**
- Use dados fictícios ou anonimizados para exemplos e testes
- Trabalhe com estruturas e padrões sem os dados reais
- Use variáveis e placeholders: `[NOME_DO_CLIENTE]`, `[VALOR_DO_CONTRATO]`

---

### 2. Entenda Onde Seus Dados Vão

| Produto | Dados enviados | Armazenamento | Treinamento |
|---|---|---|---|
| Microsoft 365 Copilot | Dados do tenant M365 | Dentro do tenant | Não usa dados para treinar |
| Copilot Studio (Publicado) | Conforme configuração | Dataverse + Azure | Não por padrão |
| Copilot Web (bing.com) | Prompt + histórico da sessão | Microsoft (limitado) | Consulte política atual |
| Azure OpenAI Service | Apenas o que você envia | Não retido por padrão | Não por padrão |

> **Importante**: Verifique sempre a política de dados vigente da Microsoft para o produto que está utilizando. As políticas podem ser atualizadas.

---

### 3. Proteção de Dados Pessoais (LGPD / GDPR)

**Antes de usar o Copilot com dados que possam envolver pessoas:**

- [ ] Verificar se há base legal para o tratamento dos dados
- [ ] Garantir que o usuário do Copilot tem permissão para acessar esses dados
- [ ] Confirmar que o processamento está dentro do escopo do DPA (Data Processing Agreement) com a Microsoft
- [ ] Documentar o tratamento conforme exigido pela LGPD (Art. 37)
- [ ] Avaliar se é necessário relatório de RIPD (Relatório de Impacto à Proteção de Dados)

---

## 🛡️ Controles de Segurança Recomendados

### Para Microsoft 365 Copilot

| Controle | Descrição | Ferramenta |
|---|---|---|
| **Sensibilidade de Dados** | Classificar e rotular documentos sensíveis | Microsoft Purview Information Protection |
| **Prevenção de Perda de Dados** | Bloquear compartilhamento indevido de dados | Microsoft Purview DLP |
| **Governança de Acesso** | Revisar permissões excessivas no M365 | Microsoft Entra Access Reviews |
| **Auditoria** | Monitorar atividades do Copilot | Microsoft Purview Audit |
| **Comunicações** | Monitorar conteúdo inadequado | Microsoft Purview Communication Compliance |

### Para Copilot Studio

| Controle | Descrição |
|---|---|
| **Autenticação** | Exigir autenticação via Azure AD para agentes corporativos |
| **Escopo de Dados** | Configurar conexões com permissões mínimas necessárias |
| **Moderação de Conteúdo** | Ativar filtros de conteúdo para respostas do agente |
| **Logging** | Habilitar telemetria e logs de conversação |
| **Revisão Periódica** | Auditar os tópicos e fontes de dados dos agentes regularmente |

---

## ⚠️ Cenários de Risco e Como Mitigá-los

### Risco 1: Vazamento de Dados via Prompt

**Situação**: Colaborador insere dados confidenciais de clientes em um prompt para análise.

**Mitigação**:
- Treinar usuários sobre o que pode e não pode ser inserido em prompts
- Implementar políticas de DLP que detectem padrões de dados sensíveis
- Usar dados sintéticos ou anonimizados para exemplos

---

### Risco 2: Acesso Indevido via Copilot

**Situação**: Copilot acessa documentos do SharePoint aos quais o usuário não deveria ter acesso.

**Mitigação**:
- Revisar e corrigir permissões excessivas no SharePoint e OneDrive
- Usar o Microsoft Entra Access Reviews regularmente
- O Copilot respeita as permissões do usuário — corrija as permissões na origem

---

### Risco 3: Prompt Injection em Agentes

**Situação**: Usuário mal-intencionado tenta manipular o agente com instruções maliciosas nos prompts.

**Mitigação**:
- Validar e sanitizar as entradas do usuário nos fluxos do Copilot Studio
- Definir escopo restrito no system prompt do agente
- Testar o agente com cenários de adversarial prompting antes do lançamento
- Monitorar conversas para detectar padrões de abuso

---

### Risco 4: Geração de Conteúdo Impreciso (Alucinação)

**Situação**: Copilot gera informações incorretas apresentadas como fatos.

**Mitigação**:
- Sempre revisar respostas críticas antes de usar em decisões de negócio
- Pedir ao Copilot para citar fontes quando possível
- Para informações regulatórias ou jurídicas, sempre validar com especialista humano
- Usar fontes de dados confiáveis e verificadas nas knowledge bases do Copilot Studio

---

## 📋 Checklist de Segurança para Uso do Copilot

### Antes de usar

- [ ] O prompt contém apenas dados que posso compartilhar conforme minha política corporativa?
- [ ] Os dados de pessoas físicas foram removidos ou anonimizados?
- [ ] Tenho permissão para trabalhar com as informações que vou inserir?

### Ao criar agentes no Copilot Studio

- [ ] O agente usa autenticação?
- [ ] As integrações usam princípio de menor privilégio?
- [ ] Os logs de conversação estão habilitados?
- [ ] O agente foi testado contra cenários de prompt injection?
- [ ] O escopo do agente está claramente definido no system prompt?
- [ ] O processo de aprovação e revisão foi seguido?

### Periodicamente

- [ ] Revisar permissões de acesso ao SharePoint e OneDrive (fontes do Copilot)
- [ ] Auditar logs de uso do Copilot no Microsoft Purview
- [ ] Verificar atualizações nas políticas de dados da Microsoft
- [ ] Revisar e atualizar os agentes no Copilot Studio
- [ ] Coletar e agir sobre feedback dos usuários sobre respostas inadequadas

---

## 📚 Referências

- [Microsoft 365 Copilot – Data Privacy](https://learn.microsoft.com/microsoft-365-copilot/microsoft-365-copilot-privacy)
- [Microsoft Purview – Compliance](https://learn.microsoft.com/purview/)
- [Copilot Studio – Security and Governance](https://learn.microsoft.com/microsoft-copilot-studio/security-and-governance)
- [LGPD – Lei Geral de Proteção de Dados](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm)
- [Microsoft AI Principles](https://www.microsoft.com/ai/responsible-ai)
