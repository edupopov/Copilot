# Exemplo: Padronização de Templates e Documentação

## Cenário
Utilizar o Copilot para criar templates padronizados, garantir consistência na documentação de projetos e alinhar o conteúdo a padrões corporativos estabelecidos.

---

## Templates

### Criação de Template

```
Tipo de documento: [TIPO]
Propósito: [PARA QUE SERVE]
Público-alvo: [QUEM USA]
Seções obrigatórias: [SEÇÃO 1, SEÇÃO 2, SEÇÃO 3]
Tom e estilo: [FORMAL / TÉCNICO / NEUTRO]
Formato: [MARKDOWN / WORD / GOOGLE DOCS]
Exemplo de conteúdo: [OPCIONAL: EXEMPLO DE PREENCHIMENTO]

Crie um template completo para o documento descrito acima, incluindo:
1. Estrutura de seções com títulos e subtítulos
2. Instruções de preenchimento para cada seção
3. Exemplos de conteúdo entre colchetes [COMO ESTE]
4. Notas sobre o que NÃO deve ser incluído
```

### Padronização de Documentação Existente

```
Padrão de referência: [DESCREVA O PADRÃO OU COLE UM EXEMPLO]
Documento a padronizar:
[COLAR DOCUMENTO AQUI]

Reescreva o documento acima seguindo o padrão de referência, mantendo o conteúdo original mas ajustando estrutura, nomenclatura e formatação.
```

---

## Exemplos Práticos

### Exemplo 1 – Template de Especificação de Requisitos

```
Tipo de documento: Especificação de Requisitos de Software (ERS)
Propósito: Documentar os requisitos funcionais e não-funcionais de um sistema ou funcionalidade
Público-alvo: Desenvolvedores, QA, Product Owners e Arquitetos
Seções obrigatórias: Visão geral, Requisitos Funcionais, Requisitos Não-Funcionais, Restrições, Critérios de Aceite, Glossário
Tom e estilo: Técnico e objetivo
Formato: Markdown

Crie um template completo de ERS, incluindo instruções de preenchimento para cada seção e exemplos de conteúdo.
```

---

### Exemplo 2 – Template de Runbook de Operações

```
Tipo de documento: Runbook de Operações (procedimento operacional)
Propósito: Documentar procedimentos passo a passo para tarefas operacionais de TI (deploy, manutenção, rollback, etc.)
Público-alvo: Time de operações (N1, N2, N3) com conhecimento técnico variado
Seções obrigatórias: Visão geral, Pré-requisitos, Procedimento passo a passo, Validação, Rollback, Contatos de suporte
Tom e estilo: Técnico, direto, sem ambiguidades
Formato: Markdown

Crie um template de Runbook que minimize erros humanos durante procedimentos críticos. Inclua campos de checklist e pontos de validação entre etapas.
```

---

### Exemplo 3 – Padronização de README de Repositório

```
Padrão de referência: Os READMEs do time devem seguir esta estrutura:
1. Título e descrição curta
2. Badges de status (build, coverage, versão)
3. Pré-requisitos e instalação
4. Configuração (variáveis de ambiente)
5. Como executar (desenvolvimento e produção)
6. Como testar
7. Estrutura do projeto
8. Como contribuir
9. Licença e contatos

Documento a padronizar:
---
# API de Pedidos

Essa é a API de pedidos. Foi feita em Node.js.

Para rodar: npm start

Para testar: npm test

Qualquer dúvida falar com o João.
---

Reescreva o README acima seguindo o padrão de referência. Mantenha as informações existentes e adicione seções com conteúdo de exemplo onde não houver informação disponível.
```

---

## Templates Corporativos Sugeridos

| Template | Propósito |
|---|---|
| Especificação de Requisitos (ERS) | Documentar requisitos de sistemas |
| Architecture Decision Record (ADR) | Registrar decisões arquiteturais |
| Runbook de Operações | Procedimentos operacionais de TI |
| Post-Mortem de Incidente | Análise e aprendizados de incidentes |
| Plano de Projeto | Escopo, cronograma e responsabilidades |
| README de Repositório | Documentação técnica de projetos |
| Proposta Técnica | Apresentação de soluções para clientes |

---

## Quando usar

- Para criar templates padronizados para uso recorrente no time
- Para garantir consistência na documentação de projetos
- Para converter documentos informais em documentação corporativa estruturada
- Para alinhar a documentação de times diferentes a um padrão comum
