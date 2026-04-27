# Exemplo: Revisão e Melhoria de Documentos

## Cenário
Utilizar o Copilot para revisar, melhorar e adaptar documentos corporativos — garantindo clareza, consistência, correção gramatical e adequação ao público-alvo.

---

## Templates

### Revisão Geral

```
Tipo de documento: [E-MAIL / RELATÓRIO / APRESENTAÇÃO / POLÍTICA / OUTRO]
Público-alvo: [QUEM VAI LER: executivos / técnicos / clientes / colaboradores]
Tom desejado: [FORMAL / PROFISSIONAL / AMIGÁVEL / TÉCNICO]
Idioma: [PORTUGUÊS FORMAL / PORTUGUÊS SIMPLES / INGLÊS]
Foco da revisão: [CLAREZA / GRAMÁTICA / CONCISÃO / ESTRUTURA / TODOS]

Revise o texto abaixo considerando as diretrizes acima. Para cada mudança sugerida, explique brevemente o motivo:

[COLAR TEXTO AQUI]
```

### Adaptação para Público Diferente

```
Texto original (escrito para [PÚBLICO ORIGINAL]):
[COLAR TEXTO AQUI]

Adapte o texto acima para [NOVO PÚBLICO], mantendo as informações essenciais mas ajustando:
- Nível técnico: [REDUZIR / AUMENTAR]
- Tom: [DE: X PARA: Y]
- Formato: [MANTER / CONVERTER PARA: bullets / narrativa / tabela]
- Tamanho: [REDUZIR PARA X% / MANTER / EXPANDIR]
```

---

## Exemplos Práticos

### Exemplo 1 – Revisão de E-mail Formal para Diretoria

```
Tipo de documento: E-mail corporativo
Público-alvo: Diretoria Executiva (não-técnica)
Tom desejado: Formal e objetivo
Idioma: Português formal
Foco da revisão: Clareza, concisão e impacto

Revise o e-mail abaixo para torná-lo mais claro e direto para o público executivo. Elimine jargões técnicos, reduza o texto mantendo as informações essenciais e destaque a ação necessária dos destinatários:

---
Assunto: Atualização sistema legacy - migração database

Pessoal,

Conforme alinhado em nossa última sync, estamos progredindo com o projeto de migração do nosso ambiente on-premises para a cloud Azure. O processo de assessment inicial foi concluído e identificamos algumas dependências críticas nos módulos de billing e inventory que vão requerer um esforço adicional de refactoring antes do go-live.

O timeline original pode ser impactado em 3-4 sprints dependendo dos findings do pentest que está scheduled para a próxima semana. Vamos precisar do sign-off do board para proceder com a fase 2 considerando o revised budget.

Att,
João
---
```

---

### Exemplo 2 – Adaptação de Documentação Técnica para Usuários Finais

```
Texto original (escrito para desenvolvedores):

Para configurar a autenticação OAuth 2.0 no cliente, é necessário registrar o aplicativo no Azure Active Directory, obtendo o Client ID e o Tenant ID. Em seguida, configure o fluxo de Authorization Code com PKCE, definindo os redirect URIs e os scopes necessários (ex: openid, profile, api://[APP_ID]/data.read). O token JWT resultante deve ser incluído no header Authorization: Bearer {token} em cada requisição à API.

Adapte o texto acima para usuários finais (colaboradores sem conhecimento técnico) que precisam entender apenas como fazer o primeiro login no sistema. Mantenha apenas as informações relevantes para eles, usando linguagem simples e passos numerados.
```

---

### Exemplo 3 – Melhoria de Política Corporativa

```
Tipo de documento: Política de uso de IA generativa
Público-alvo: Todos os colaboradores
Tom desejado: Formal mas acessível
Idioma: Português simples
Foco da revisão: Estrutura, clareza e completude

Revise a política abaixo e sugira melhorias para torná-la mais clara e fácil de seguir. Identifique lacunas ou ambiguidades e proponha um texto revisado:

---
POLÍTICA DE IA

Os funcionários devem usar IA de forma responsável. Não compartilhe dados confidenciais com ferramentas de IA externas. Peça autorização antes de usar IA em projetos de clientes. O uso inadequado pode resultar em medidas disciplinares.
---
```

---

## Quando usar

- Para revisar comunicados, e-mails e documentos antes do envio
- Para adaptar conteúdo técnico para audiências não-técnicas
- Para melhorar a clareza e objetividade de políticas e procedimentos
- Para padronizar o tom e o estilo de documentos corporativos
