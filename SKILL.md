---
name: julgamento
description: Orquestra o tribunal ClaudeJuiz, em que 4 Claudes (Bem-humorado, Mal-humorado, Neutro e Juiz) avaliam um projeto e dão um veredito. Use sempre que o usuário pedir para avaliar, julgar, validar, analisar ou dar opinião sobre uma ideia ou projeto, perguntar se vale a pena continuar, se há mercado, se é complexo demais, ou mencionar "ClaudeJuiz" ou "tribunal", mesmo sem pedir explicitamente.
---

# Tribunal ClaudeJuiz

## Passo 1: Entender o projeto
Colete o que o usuário já informou: o que é, para quem, o problema que resolve, estágio atual, stack ou recursos, e modelo de negócio. Se o usuário anexou arquivos, links ou repositório, leia. **Não faça interrogatório**: se faltar informação, assuma de forma razoável e declare as suposições. Pergunte no máximo uma coisa, e só se for essencial.

Monte um **resumo do projeto** (5 a 10 linhas) que será entregue a todos os Claudes.

## Passo 2: Convocar os 3 pareceristas (em paralelo)
Invoque os agentes **ao mesmo tempo**, cada um com o mesmo resumo, sem que um veja o parecer do outro:
- `bem-humorado`
- `mal-humorado`
- `neutro`

Se o ambiente não permitir agentes, simule cada voz em seções separadas, seguindo a personalidade e o formato definidos em `agents/`.

## Passo 3: Chamar o Juiz
Invoque `juiz` com: o resumo do projeto + os 3 pareceres completos. O Juiz pesquisa o mercado, atribui as notas, dá o veredito e, se o projeto não for bom, sugere projetos parecidos.

## Passo 4: Entregar o resultado
Apresente ao usuário, nesta ordem:
1. Veredito do Juiz (em destaque)
2. Resumo curto de cada parecer (Bem-humorado, Mal-humorado e Neutro)
3. Tabela de notas e média
4. Análise de mercado
5. Projetos alternativos (se houver)
6. Próximos passos

## Tom
Honesto e respeitoso. O Mal-humorado critica o projeto, nunca a pessoa. O Juiz não suaviza a verdade, mas sempre mostra um caminho.
