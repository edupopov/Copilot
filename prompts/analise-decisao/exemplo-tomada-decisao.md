# Exemplo: Análise Comparativa e Tomada de Decisão

## Cenário
Utilizar o Copilot para apoiar decisões corporativas por meio de análise estruturada de alternativas, critérios de avaliação e recomendações fundamentadas.

---

## Templates

### Análise de Alternativas

```
Decisão a tomar: [DESCRIÇÃO DA DECISÃO]
Contexto: [SITUAÇÃO ATUAL E POR QUE A DECISÃO É NECESSÁRIA]
Critérios de avaliação (com peso de 1 a 5):
- [CRITÉRIO 1]: peso [N]
- [CRITÉRIO 2]: peso [N]
- [CRITÉRIO 3]: peso [N]

Alternativas:
1. [ALTERNATIVA A]
2. [ALTERNATIVA B]
3. [ALTERNATIVA C]

Restrições e premissas:
- [RESTRIÇÃO 1]
- [RESTRIÇÃO 2]

Analise cada alternativa com base nos critérios acima e recomende a melhor opção, apresentando:
1. Tabela de pontuação por critério
2. Análise de riscos de cada alternativa
3. Recomendação com justificativa
4. Próximos passos sugeridos
```

### Análise SWOT

```
Contexto: [PRODUTO / PROJETO / DECISÃO / EMPRESA A SER ANALISADA]

Realize uma análise SWOT completa considerando:
- Forças internas: [INFORMAÇÕES DISPONÍVEIS]
- Fraquezas internas: [INFORMAÇÕES DISPONÍVEIS]
- Ambiente externo (mercado, concorrência, regulação): [INFORMAÇÕES DISPONÍVEIS]

Apresente a análise em formato de quadrante SWOT e inclua 3 estratégias recomendadas (SO, WO ou ST) com base nos resultados.
```

---

## Exemplos Práticos

### Exemplo 1 – Escolha de Plataforma de CRM

```
Decisão a tomar: Escolha do sistema de CRM para o time comercial
Contexto: A empresa tem 50 vendedores, usa Microsoft 365 e Azure, e precisa substituir uma planilha Excel por um CRM em até 90 dias
Critérios de avaliação:
- Integração com Microsoft 365 (Teams, Outlook, SharePoint): peso 5
- Custo total (licenciamento + implantação): peso 4
- Facilidade de uso e curva de aprendizado: peso 4
- Suporte a automação de vendas e pipeline: peso 3
- Prazo de implantação: peso 3
- Suporte local em português: peso 2

Alternativas:
1. Microsoft Dynamics 365 Sales
2. Salesforce Sales Cloud
3. HubSpot CRM (versão enterprise)

Restrições:
- Budget máximo de R$ 150.000/ano incluindo licenças
- Time interno de TI com expertise em Microsoft; sem expertise em Salesforce
- Necessidade de estar operacional em 90 dias

Analise cada alternativa com base nos critérios acima e recomende a melhor opção.
```

---

### Exemplo 2 – Decisão de Build vs. Buy para uma Funcionalidade

```
Decisão a tomar: Desenvolver internamente ou contratar solução pronta para autenticação multifator (MFA) corporativa
Contexto: A empresa precisa implementar MFA para 800 usuários em 60 dias, atendendo requisitos de compliance
Critérios de avaliação:
- Tempo de implantação: peso 5
- Custo total de propriedade (3 anos): peso 4
- Segurança e compliance (LGPD, ISO 27001): peso 5
- Integração com Azure AD existente: peso 4
- Esforço de manutenção: peso 3

Alternativas:
1. Build: Desenvolver solução customizada de MFA internamente
2. Buy: Adotar Azure AD MFA (já incluso na licença Microsoft 365 E3)
3. Buy: Contratar Duo Security como solução de MFA de terceiros

Restrições:
- Time de desenvolvimento com capacidade limitada (2 devs disponíveis)
- Prazo máximo de 60 dias
- Infraestrutura já baseada em Azure AD

Analise as alternativas e recomende a melhor opção com base nos critérios e restrições.
```

---

### Exemplo 3 – Análise de Risco de Projeto

```
Contexto: Projeto de migração de ERP legado para SAP S/4HANA, com duração prevista de 18 meses e orçamento de R$ 5 milhões

Informações disponíveis:
- Time interno: 10 pessoas (5 de TI, 5 de negócio), sem experiência prévia em SAP
- Parceiro de implantação: empresa de consultoria com 3 projetos SAP concluídos
- Dependências críticas: integração com 12 sistemas legados
- Restrição regulatória: dados fiscais não podem ficar indisponíveis por mais de 4 horas

Realize uma análise de riscos do projeto incluindo:
1. Identificação dos 8 principais riscos (técnicos, operacionais e de negócio)
2. Avaliação de probabilidade e impacto (alto/médio/baixo) para cada risco
3. Estratégias de mitigação para os 3 riscos de maior criticidade
4. Recomendação sobre prosseguir, ajustar ou adiar o projeto
```

---

## Quando usar

- Para estruturar decisões complexas com múltiplas alternativas e critérios
- Para preparar análises para aprovação em comitês e conselhos
- Para identificar e priorizar riscos em projetos e iniciativas
- Para documentar o processo de tomada de decisão de forma auditável
