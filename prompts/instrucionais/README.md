# Prompts Instrucionais

Prompts instrucionais definem **role (papel)**, **persona** e **contexto** para guiar o Copilot a responder de forma mais precisa, alinhada ao cenário e ao público-alvo desejado.

## Por que usar prompts instrucionais?

Ao definir claramente quem o Copilot deve "ser" e qual o contexto da tarefa, você obtém respostas mais consistentes, com o tom, nível técnico e formato adequados.

## Estrutura recomendada

```
Você é [ROLE/PERSONA].
Seu contexto é [CONTEXTO].
Sua tarefa é [TAREFA].
Responda [FORMATO/TOM].
```

## Exemplos disponíveis

| Arquivo | Cenário |
|---|---|
| [`exemplo-role-persona.md`](exemplo-role-persona.md) | Definir papel e persona para o Copilot |
| [`exemplo-contexto.md`](exemplo-contexto.md) | Definir contexto de projeto ou organização |

## Dicas

- Seja específico ao definir o papel (ex: "arquiteto de soluções Azure" em vez de "especialista em TI")
- Inclua o nível de experiência do público-alvo (ex: "para uma audiência executiva não-técnica")
- Defina o formato de saída esperado (lista, tabela, texto corrido, markdown)
