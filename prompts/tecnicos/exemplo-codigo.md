# Exemplo: Prompt para Geração e Revisão de Código

## Cenário
Utilizar o Copilot para gerar, revisar, refatorar ou documentar código de forma eficiente, fornecendo contexto técnico suficiente para respostas precisas.

---

## Templates

### Geração de Código

```
Linguagem: [LINGUAGEM E VERSÃO]
Framework: [FRAMEWORK E VERSÃO]
Contexto: [DESCRIÇÃO DO QUE O CÓDIGO PRECISA FAZER]
Requisitos:
- [REQUISITO 1]
- [REQUISITO 2]
Restrições: [PADRÕES, LIBS PROIBIDAS, PERFORMANCE, ETC.]

Gere o código para [FUNCIONALIDADE], incluindo tratamento de erros e comentários explicativos.
```

### Revisão de Código

```
Linguagem: [LINGUAGEM]
Contexto: [O QUE ESTE CÓDIGO FAZ]
Preocupações: [PERFORMANCE / SEGURANÇA / LEGIBILIDADE / BOAS PRÁTICAS]

Revise o código abaixo e aponte problemas, sugerindo melhorias justificadas:

[COLAR CÓDIGO AQUI]
```

---

## Exemplos Práticos

### Exemplo 1 – Geração de Endpoint REST em C#

```
Linguagem: C# 12 / .NET 8
Framework: ASP.NET Core Minimal API
Contexto: API de gerenciamento de produtos para um e-commerce
Requisitos:
- Endpoint GET /products com paginação (page e pageSize)
- Endpoint POST /products para criação com validação de dados
- Respostas no padrão ProblemDetails para erros
- Logging com ILogger
Restrições: Não usar Entity Framework, usar Dapper; seguir padrão REST

Gere o código para os endpoints acima, incluindo a definição do modelo Product e tratamento de erros adequado.
```

---

### Exemplo 2 – Revisão de Query SQL com Foco em Performance

```
Linguagem: T-SQL (SQL Server 2019)
Contexto: Query que lista pedidos pendentes com dados do cliente, usada em relatório executivo
Preocupações: Performance (tabela Orders com 10 milhões de registros), uso correto de índices

Revise a query abaixo e aponte problemas de performance, sugerindo melhorias com justificativa:

SELECT c.Name, c.Email, o.OrderDate, o.TotalAmount
FROM Orders o
JOIN Customers c ON o.CustomerId = c.Id
WHERE o.Status = 'Pending'
ORDER BY o.OrderDate DESC
```

---

### Exemplo 3 – Refatoração de Função JavaScript

```
Linguagem: JavaScript (ES2022) / Node.js 20
Contexto: Função legada de validação de formulário que precisa ser refatorada para melhor legibilidade e testabilidade
Preocupações: Legibilidade, separação de responsabilidades, facilidade de teste unitário

Refatore a função abaixo, separando as validações em funções menores e adicionando JSDoc:

function validate(data) {
  if (!data.name || data.name.length < 3) return false;
  if (!data.email || !data.email.includes('@')) return false;
  if (!data.age || data.age < 18 || data.age > 120) return false;
  return true;
}
```

---

## Quando usar

- Para acelerar a criação de código boilerplate e estruturas repetitivas
- Para revisões de código antes de Pull Requests
- Para refatorar código legado com foco em qualidade
- Para gerar testes unitários para funções existentes
