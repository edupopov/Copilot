# Exemplo: Configuração de Agente no Copilot Studio

## Cenário
Utilizar o Copilot para auxiliar no design, configuração e documentação de agentes (copilotos) personalizados no Microsoft Copilot Studio.

---

## Templates

### Design de Agente

```
Nome do agente: [NOME]
Objetivo: [O QUE O AGENTE DEVE FAZER]
Público-alvo: [QUEM VAI USAR]
Canais: [TEAMS / WEB / SHAREPOINT / OUTRO]
Integrações necessárias: [SISTEMAS, APIS, BASES DE CONHECIMENTO]
Restrições: [TEMAS FORA DO ESCOPO, LIMITAÇÕES DE DADOS]

Com base nas informações acima, sugira:
1. Os principais tópicos (topics) que o agente deve ter
2. A estrutura de boas-vindas e fallback
3. As variáveis de sessão necessárias
4. As integrações recomendadas com Power Automate ou conectores
```

### Criação de Tópico

```
Nome do tópico: [NOME]
Intenção do usuário: [O QUE O USUÁRIO QUER FAZER]
Variações da pergunta: [EXEMPLOS DE COMO O USUÁRIO PODE PERGUNTAR]
Informações necessárias: [DADOS QUE O AGENTE PRECISA COLETAR]
Ação esperada: [RESPOSTA / CHAMADA DE API / REDIRECIONAMENTO]

Crie o fluxo de conversação para este tópico no formato de diálogo (trigger phrases, perguntas, validações e resposta final).
```

---

## Exemplos Práticos

### Exemplo 1 – Design de Agente de Suporte de TI

```
Nome do agente: HelpDesk Copilot
Objetivo: Atender chamados de suporte técnico de nível 1, resolver problemas comuns e escalar casos complexos para técnicos humanos
Público-alvo: Colaboradores da empresa (todos os níveis técnicos)
Canais: Microsoft Teams
Integrações necessárias: ServiceNow (criação e consulta de tickets), base de conhecimento interna no SharePoint, Active Directory (para verificar dados do usuário)
Restrições: Não deve responder sobre assuntos não relacionados ao suporte de TI; não deve acessar dados de outros usuários

Com base nas informações acima, sugira:
1. Os 10 principais tópicos que o agente deve cobrir
2. A mensagem de boas-vindas e o menu inicial
3. O fluxo de escalação para técnico humano
4. As variáveis de sessão necessárias (ex: nome do usuário, número do ticket)
```

---

### Exemplo 2 – Criação de Tópico para Consulta de Status de Pedido

```
Nome do tópico: Consultar Status de Pedido
Intenção do usuário: Verificar o status atual de um pedido de compra
Variações da pergunta:
- "Qual o status do meu pedido?"
- "Quero saber sobre meu pedido número 12345"
- "Meu pedido foi aprovado?"
- "Quando meu pedido chega?"
Informações necessárias: Número do pedido (validar formato: 5 dígitos numéricos)
Ação esperada: Consultar a API de pedidos e retornar status, data estimada de entrega e última atualização

Crie o fluxo de conversação para este tópico, incluindo:
- Trigger phrases
- Coleta e validação do número do pedido
- Mensagem de erro para pedido não encontrado
- Resposta formatada com os dados do pedido
```

---

### Exemplo 3 – Configuração de Knowledge Base

```
Contexto: Preciso configurar uma base de conhecimento no Copilot Studio para um agente de RH.
Fontes de dados disponíveis:
- Site do SharePoint com políticas de RH (100 documentos PDF e Word)
- FAQ de RH no formato de planilha Excel com 200 perguntas e respostas
- Página de benefícios no portal do colaborador (URL pública interna)

Sugira:
1. Como organizar e priorizar as fontes de dados no Copilot Studio
2. Estratégias para garantir que as respostas sejam precisas e atualizadas
3. Como configurar o fallback quando a resposta não for encontrada na knowledge base
4. Métricas para monitorar a qualidade das respostas do agente
```

---

## Quando usar

- Para planejar e documentar agentes antes de iniciar a configuração no Copilot Studio
- Para criar fluxos de conversação estruturados para tópicos específicos
- Para revisar e melhorar agentes existentes
- Para preparar a documentação técnica de copilotos para aprovação e governança
