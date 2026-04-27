# Boas Práticas de Prompt Engineering

Este guia apresenta os princípios e técnicas fundamentais para criar prompts eficazes com o Microsoft Copilot e Copilot Studio.

---

## 🎯 Princípios Fundamentais

### 1. Clareza e Especificidade
Prompts vagos geram respostas genéricas. Quanto mais específico o prompt, mais útil a resposta.

| ❌ Evite | ✅ Prefira |
|---|---|
| "Me fale sobre Azure" | "Explique as diferenças entre Azure App Service e Azure Container Apps para hospedar uma API REST em .NET 8, considerando escalabilidade e custo" |
| "Revise meu código" | "Revise o código Python abaixo com foco em segurança e tratamento de erros, apontando cada problema encontrado com sugestão de correção" |

---

### 2. Forneça Contexto Suficiente

O Copilot não tem acesso ao histórico da sua empresa, projeto ou decisões anteriores — você precisa fornecê-lo.

**Elementos de contexto essenciais:**
- **Quem**: Papel/persona desejado (arquiteto, analista, redator)
- **O quê**: Tarefa específica a ser executada
- **Para quem**: Público-alvo da resposta
- **Por quê**: Objetivo ou problema a resolver
- **Restrições**: Limitações técnicas, de prazo ou orçamento

---

### 3. Defina o Formato de Saída

Especificar o formato reduz o retrabalho e facilita o uso direto da resposta.

**Formatos comuns:**
- Lista com marcadores
- Tabela comparativa
- Passo a passo numerado
- Código comentado
- Resumo executivo (máximo N linhas)
- Markdown / JSON / XML

**Exemplo:**
```
Responda em formato de tabela com 3 colunas: Tecnologia | Vantagem Principal | Caso de Uso Ideal
```

---

### 4. Divida Tarefas Complexas

Para tarefas complexas, use uma sequência de prompts ao invés de um único prompt longo.

```
Passo 1: "Liste os 5 principais riscos de migração cloud para o cenário descrito"
Passo 2: "Para cada risco listado, sugira uma estratégia de mitigação"
Passo 3: "Converta os riscos e mitigações em uma tabela de gerenciamento de riscos no formato PMBOK"
```

---

### 5. Use Exemplos (Few-Shot Prompting)

Forneça exemplos do formato e qualidade de resposta esperados.

```
Preciso criar User Stories no seguinte formato:

Exemplo:
- Título: Consulta de saldo
- Como: colaborador
- Quero: consultar meu saldo de férias
- Para que: eu possa planejar minhas folgas
- Critérios de aceite:
  - Dado que o colaborador está autenticado
  - Quando acessa a área de férias
  - Então vê o saldo atualizado em dias

Agora crie User Stories no mesmo formato para as funcionalidades abaixo:
[LISTA DE FUNCIONALIDADES]
```

---

### 6. Itere e Refine

O primeiro prompt raramente é o ideal. Use prompts de refinamento:

- *"Torne a resposta mais concisa, máximo 3 parágrafos"*
- *"Reformule em linguagem mais técnica para engenheiros"*
- *"Adicione exemplos práticos para cada ponto listado"*
- *"Considere também o cenário em que [CONDIÇÃO ADICIONAL]"*

---

## 📐 Estrutura de Prompt Recomendada (RCTF)

| Elemento | Descrição | Exemplo |
|---|---|---|
| **R**ole | Qual papel o Copilot deve assumir | "Você é um arquiteto de soluções Azure Sênior" |
| **C**ontext | Contexto do problema ou projeto | "Trabalhando em uma migração de ERP legado para Azure" |
| **T**ask | Tarefa específica a executar | "Analise as alternativas de banco de dados e recomende a mais adequada" |
| **F**ormat | Formato esperado da resposta | "Responda em tabela comparativa com prós, contras e recomendação final" |

---

## ⚠️ Erros Comuns a Evitar

| Erro | Problema | Solução |
|---|---|---|
| Prompt muito longo e confuso | Copilot perde o foco principal | Divida em múltiplos prompts sequenciais |
| Ausência de contexto | Resposta genérica e inaplicável | Sempre forneça contexto do projeto/empresa |
| Múltiplas tarefas em um prompt | Resposta incompleta ou superficial | Um objetivo principal por prompt |
| Não especificar público-alvo | Tom e nível técnico inadequados | Sempre defina o público da resposta |
| Aceitar a primeira resposta sem iterar | Qualidade abaixo do potencial | Refine com prompts de ajuste |

---

## 🔄 Ciclo de Melhoria Contínua

```
1. Escreva o prompt inicial
2. Avalie a qualidade da resposta
3. Identifique o que faltou ou precisa melhorar
4. Refine o prompt (adicione contexto, exemplo ou restrição)
5. Documente o prompt que gerou o melhor resultado
6. Reutilize e compartilhe com o time
```

---

## 📚 Recursos Adicionais

- [Microsoft Copilot Adoption Hub](https://adoption.microsoft.com/copilot/)
- [Copilot Studio Documentation](https://learn.microsoft.com/copilot-studio/)
- [Prompt Engineering Guide (Microsoft)](https://learn.microsoft.com/azure/ai-services/openai/concepts/prompt-engineering)
