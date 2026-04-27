# Exemplo: Prompt para Arquitetura de Soluções

## Cenário
Utilizar o Copilot para apoiar decisões arquiteturais, criar documentação técnica, comparar alternativas de design e registrar Architecture Decision Records (ADRs).

---

## Templates

### Decisão Arquitetural

```
Contexto:
- Sistema: [NOME E DESCRIÇÃO]
- Requisitos funcionais relevantes: [RF1, RF2...]
- Requisitos não-funcionais: [PERFORMANCE, DISPONIBILIDADE, SEGURANÇA, ESCALABILIDADE]
- Restrições: [TECNOLÓGICAS, ORÇAMENTÁRIAS, DE TIME]

Alternativas em consideração:
1. [ALTERNATIVA A]
2. [ALTERNATIVA B]

Analise as alternativas acima considerando os requisitos e restrições listados. Apresente os trade-offs de cada uma e recomende a melhor opção com justificativa.
```

### Architecture Decision Record (ADR)

```
Contexto: [SITUAÇÃO QUE MOTIVOU A DECISÃO]
Decisão: [ALTERNATIVA ESCOLHIDA]
Justificativa: [MOTIVOS]

Formate esta decisão como um ADR no padrão MADR (Markdown Architectural Decision Records), incluindo seções de status, contexto, decisão, consequências positivas e negativas.
```

---

## Exemplos Práticos

### Exemplo 1 – Escolha de Padrão de Mensageria

```
Contexto:
- Sistema: Plataforma de e-commerce com microsserviços
- Requisitos funcionais: Processamento de pedidos, notificações de status, sincronização de estoque
- Requisitos não-funcionais: Latência < 500ms para pedidos, garantia de entrega de mensagens, rastreabilidade
- Restrições: Infraestrutura Azure, time com experiência em .NET

Alternativas em consideração:
1. Azure Service Bus (filas e tópicos)
2. Azure Event Grid (eventos reativos)
3. Azure Event Hubs (streaming de alta volumetria)

Analise as alternativas acima para o cenário descrito, apresente os trade-offs e recomende a melhor opção ou combinação de serviços.
```

---

### Exemplo 2 – Estratégia de Autenticação para API Pública

```
Contexto:
- Sistema: API REST pública para parceiros comerciais
- Requisitos funcionais: Autenticação de parceiros, controle de acesso por escopo, revogação de acesso
- Requisitos não-funcionais: Segurança (OAuth 2.0 ou superior), auditoria de acessos, suporte a múltiplos clientes
- Restrições: Azure API Management já em uso; parceiros usam linguagens diversas

Alternativas em consideração:
1. API Keys simples com rotação manual
2. OAuth 2.0 Client Credentials Flow via Azure AD B2C
3. OAuth 2.0 via Azure API Management com políticas de validação de JWT

Analise as alternativas considerando segurança, facilidade de implementação e manutenção. Recomende a mais adequada com justificativa.
```

---

### Exemplo 3 – Documentação de Diagrama de Componentes

```
Contexto: Preciso documentar a arquitetura de uma aplicação web de 3 camadas hospedada no Azure.

A aplicação consiste em:
- Frontend React hospedado no Azure Static Web Apps
- API REST em .NET 8 no Azure App Service
- Banco de dados Azure SQL Database
- Autenticação via Azure Active Directory
- Cache com Azure Cache for Redis
- Armazenamento de arquivos no Azure Blob Storage

Gere uma descrição textual detalhada da arquitetura no formato C4 (Context e Container), incluindo as responsabilidades de cada componente e os principais fluxos de dados.
```

---

## Quando usar

- Para apoiar decisões técnicas com análise estruturada de alternativas
- Para documentar decisões arquiteturais em formato padronizado (ADR)
- Para revisar e melhorar documentação de arquitetura existente
- Para preparar diagramas e descrições para apresentações técnicas
