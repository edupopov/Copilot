# Governança de Prompts Corporativos

Este documento define as diretrizes para governança, controle, aprovação e versionamento de prompts utilizados com Microsoft Copilot e Copilot Studio em ambientes corporativos.

---

## 🎯 Por que Governança de Prompts é Importante?

Prompts utilizados em escala corporativa devem ser:
- **Consistentes**: Mesmos cenários devem gerar respostas equivalentes
- **Rastreáveis**: Deve ser possível identificar quem criou, aprovou e modificou cada prompt
- **Seguros**: Não devem expor dados sensíveis ou contornar políticas de segurança
- **Auditáveis**: O uso de prompts deve ser registrado para fins de compliance
- **Reutilizáveis**: Bons prompts devem ser compartilhados e evoluídos pelo time

---

## 📋 Classificação de Prompts

| Categoria | Descrição | Aprovação Necessária |
|---|---|---|
| **Pessoal** | Uso individual, sem dados corporativos sensíveis | Nenhuma |
| **Operacional** | Uso em processos de trabalho do time, sem dados críticos | Líder técnico |
| **Estratégico** | Uso em decisões de negócio, análise de dados corporativos | Gestor + Compliance |
| **Regulatório** | Envolve dados sob LGPD, sigilo bancário ou jurídico | DPO + Jurídico + TI |

---

## 🔄 Ciclo de Vida de um Prompt Corporativo

```
[CRIAÇÃO] → [REVISÃO] → [APROVAÇÃO] → [PUBLICAÇÃO] → [MONITORAMENTO] → [ATUALIZAÇÃO/DESCONTINUAÇÃO]
```

### 1. Criação
- Qualquer colaborador pode propor um novo prompt
- Use os templates disponíveis neste repositório
- Documente: cenário de uso, público-alvo, resultado esperado e restrições

### 2. Revisão
- Revisão técnica: lógica, clareza e qualidade do prompt
- Revisão de segurança: verificar se há risco de exposição de dados sensíveis
- Revisão de compliance: verificar alinhamento com políticas internas

### 3. Aprovação
- Baseada na classificação do prompt (ver tabela acima)
- Registrada via Pull Request neste repositório

### 4. Publicação
- Merged no repositório com versionamento semântico
- Comunicado ao time via canal oficial

### 5. Monitoramento
- Coleta de feedback dos usuários
- Análise de efetividade e qualidade das respostas geradas
- Revisão periódica (mínimo semestral)

### 6. Atualização/Descontinuação
- Prompts desatualizados devem ser revisados ou marcados como obsoletos
- Nunca excluir — manter histórico com tag `[OBSOLETO]`

---

## 📁 Estrutura de Versionamento

Este repositório utiliza controle de versão Git. Ao criar ou modificar um prompt:

### Nomenclatura de Arquivos
```
[categoria]-[descricao-curta].md
Exemplo: tecnico-revisao-codigo-csharp.md
```

### Mensagens de Commit
```
[TIPO] [CATEGORIA]: descrição curta

Tipos: ADD | UPDATE | FIX | OBSOLETE
Categorias: instrucional | tecnico | automacao | analise | revisao | boas-praticas

Exemplos:
ADD tecnico: adiciona prompt de revisão de código C#
UPDATE instrucional: atualiza template de role/persona
OBSOLETE analise: marca prompt de análise de concorrentes como obsoleto
```

### Tags de Versão
```
v1.0.0 - Primeira versão estável do repositório
v1.1.0 - Adição de novos exemplos de automação
v1.1.1 - Correção de erros em exemplos existentes
```

---

## 👥 Papéis e Responsabilidades

| Papel | Responsabilidade |
|---|---|
| **Contribuidor** | Criar e propor novos prompts via Pull Request |
| **Revisor Técnico** | Validar qualidade e efetividade técnica do prompt |
| **Gestor de Compliance** | Aprovar prompts das categorias Estratégico e Regulatório |
| **DPO (Data Protection Officer)** | Aprovar prompts que envolvem dados pessoais ou sensíveis |
| **Mantenedor do Repositório** | Gerenciar o repositório, aprovar PRs e manter a estrutura |

---

## 📊 Métricas de Governança Recomendadas

- **Cobertura**: % de casos de uso recorrentes cobertos por prompts aprovados
- **Adoção**: Número de equipes/colaboradores utilizando prompts do repositório
- **Qualidade**: Taxa de satisfação com as respostas geradas (via feedback)
- **Atualização**: Idade média dos prompts publicados (meta: < 6 meses)
- **Compliance**: % de prompts revisados pelo DPO/Compliance quando necessário

---

## 🚨 Situações que Requerem Revisão Imediata

- Prompt que gerou resposta com dados de outros usuários
- Prompt que contornou políticas de segurança ou compliance
- Prompt que gerou conteúdo inadequado ou impreciso em escala
- Mudança significativa no modelo de IA ou na plataforma Copilot

---

## 📝 Template de Documentação de Prompt

Ao submeter um novo prompt, inclua as seguintes informações no arquivo:

```markdown
# [NOME DO PROMPT]

## Metadados
- **Categoria**: [instrucional / técnico / automação / análise / revisão]
- **Classificação**: [pessoal / operacional / estratégico / regulatório]
- **Criado por**: [NOME] em [DATA]
- **Aprovado por**: [NOME] em [DATA]
- **Versão**: [X.Y.Z]
- **Status**: [ATIVO / OBSOLETO]

## Cenário de Uso
[DESCRIÇÃO DO CENÁRIO EM 2-3 LINHAS]

## Público-Alvo
[QUEM DEVE USAR ESTE PROMPT]

## Template
[PROMPT TEMPLATE COM PLACEHOLDERS]

## Exemplos
[EXEMPLOS COMPLETOS DE USO]

## Resultado Esperado
[DESCRIÇÃO DO QUE UMA BOA RESPOSTA DEVE CONTER]

## Restrições e Alertas
[O QUE NÃO FAZER / RISCOS A EVITAR]
```
