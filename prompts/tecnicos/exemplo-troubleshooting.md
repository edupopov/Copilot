# Exemplo: Prompt para Troubleshooting

## Cenário
Utilizar o Copilot para diagnosticar erros, analisar logs, identificar causas-raiz e propor soluções para problemas técnicos em sistemas e infraestrutura.

---

## Templates

### Diagnóstico de Erro

```
Linguagem/Tecnologia: [LINGUAGEM, FRAMEWORK, SISTEMA OPERACIONAL]
Ambiente: [DESENVOLVIMENTO / HOMOLOGAÇÃO / PRODUÇÃO]
Descrição do problema: [O QUE ESTÁ ACONTECENDO]
Comportamento esperado: [O QUE DEVERIA ACONTECER]
Quando ocorre: [SEMPRE / INTERMITENTE / CONDIÇÃO ESPECÍFICA]

Mensagem de erro completa:
[COLAR MENSAGEM DE ERRO AQUI]

Stack trace (se disponível):
[COLAR STACK TRACE AQUI]

O que já foi tentado:
- [TENTATIVA 1]
- [TENTATIVA 2]

Analise o problema, identifique as possíveis causas e sugira os próximos passos para diagnóstico e resolução.
```

### Análise de Log

```
Sistema: [NOME DO SISTEMA]
Período: [DATA/HORA DE INÍCIO E FIM]
Sintoma observado: [DESCRIÇÃO DO PROBLEMA]

Log para análise:
[COLAR TRECHO DO LOG AQUI]

Analise o log acima, identifique anomalias, correlacione eventos e aponte a provável causa do problema.
```

---

## Exemplos Práticos

### Exemplo 1 – Erro de Conexão com Banco de Dados

```
Linguagem/Tecnologia: C# / .NET 8 / Azure SQL Database
Ambiente: Produção
Descrição do problema: A aplicação apresenta erros intermitentes de timeout ao conectar ao banco de dados, afetando cerca de 5% das requisições durante horários de pico
Comportamento esperado: Todas as requisições devem ser processadas com latência < 2 segundos
Quando ocorre: Intermitente, mais frequente entre 9h e 11h e 14h e 16h

Mensagem de erro completa:
Microsoft.Data.SqlClient.SqlException: Timeout expired. The timeout period elapsed prior to completion of the operation or the server is not responding.

O que já foi tentado:
- Reiniciar o App Service
- Verificar o status do Azure SQL (sem incidentes reportados)
- Aumentar o Connection Timeout de 30 para 60 segundos

Analise o problema, identifique as possíveis causas e sugira os próximos passos para diagnóstico e resolução.
```

---

### Exemplo 2 – Análise de Log de Falha em Pipeline CI/CD

```
Sistema: Azure DevOps Pipeline
Período: 27/04/2026 às 14:35
Sintoma observado: Pipeline de deploy falhou na etapa de publicação no Azure App Service

Log para análise:
##[error]Error: No package found with specified pattern: $(System.DefaultWorkingDirectory)/**/*.zip
##[error]Packages found in current dir:
##[error]/home/runner/work/1/s/src/api
##[error]/home/runner/work/1/s/src/api/obj
##[warning]Artifact download path: /home/runner/work/1/a
##[error]Error: Failed to find a package to deploy.

Analise o log acima, identifique a causa do erro e sugira a correção necessária no pipeline YAML.
```

---

### Exemplo 3 – Problema de Performance em API REST

```
Linguagem/Tecnologia: Node.js 20 / Express / MongoDB
Ambiente: Produção
Descrição do problema: Endpoint GET /api/reports/summary está retornando em 8-15 segundos; antes da última release retornava em < 1 segundo
Comportamento esperado: Resposta em menos de 2 segundos
Quando ocorre: Sempre, para todos os usuários

O que já foi tentado:
- Nenhuma mudança de infraestrutura recente
- A última release adicionou 3 novos campos ao retorno da API

Trecho do código do endpoint:
async function getReportSummary(req, res) {
  const reports = await Report.find({ status: 'active' });
  const enriched = await Promise.all(
    reports.map(async (r) => {
      const details = await ReportDetail.find({ reportId: r._id });
      const owner = await User.findById(r.ownerId);
      return { ...r.toObject(), details, owner };
    })
  );
  res.json(enriched);
}

Analise o código acima, identifique o problema de performance e sugira as otimizações necessárias.
```

---

## Quando usar

- Para acelerar o diagnóstico de erros em produção ou desenvolvimento
- Para analisar logs e identificar padrões de falha
- Para revisar código em busca de problemas de performance ou segurança
- Para documentar post-mortems com análise de causa-raiz
