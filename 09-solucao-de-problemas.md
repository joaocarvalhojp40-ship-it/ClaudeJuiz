# 09 · Solução de problemas

## O plugin não aparece / não é reconhecido
**Causa mais comum:** os arquivos estão soltos na raiz do repositório.
**Solução:** confira a estrutura de pastas do guia 02. Os arquivos precisam estar em `agents/`, `commands/`, `skills/julgamento/` e `.claude-plugin/`.

## Falta a pasta `.claude-plugin`
Pastas que começam com ponto não são enviadas em alguns uploads. No GitHub, use **Add file → Create new file** e digite `.claude-plugin/plugin.json` no campo do nome (as barras criam as pastas).

## Erro ao adicionar o marketplace
- Confira se o repositório é **público**.
- Confira se existe `.claude-plugin/marketplace.json` válido (sem vírgulas sobrando).
- Confira o nome: `usuario/ClaudeJuiz`.

## O comando `/julgar` não aparece
- Verifique se `commands/julgar.md` existe e começa com `---`.
- Reinicie a sessão do Claude.

## A skill não dispara sozinha
Diga explicitamente "use o ClaudeJuiz" ou use `/julgar`. Confira se `skills/julgamento/SKILL.md` está em uma pasta com esse nome.

## Os agentes não rodam em paralelo
Alguns ambientes não suportam agentes. A skill então simula as quatro vozes em seções separadas. O resultado é parecido, só menos isolado.

## O Juiz não pesquisou o mercado
Ative a **busca na web** nas configurações. Sem ela, o Juiz avisa que as estimativas são do conhecimento geral.

## A resposta veio muito longa ou muito curta
Peça: "versão resumida" ou "aprofunde o mercado". Ou ajuste o **Formato da resposta** do Juiz.

## O Claude avisou sobre "tentativa de manipulação"
É a proteção funcionando: algum texto no projeto parecia instrução. Revise o conteúdo; se foi engano, remova a frase e rode de novo.

## O Claude recusou avaliar o projeto
A proteção contra projetos nocivos foi acionada. Se acredita que foi engano, reformule a descrição deixando claro o objetivo legítimo.

## Erro de JSON
Valide `plugin.json` e `marketplace.json` em um validador de JSON. Erros comuns: vírgula no último item, aspas erradas.

## Ainda com problemas?
Abra uma issue com: onde instalou, o que digitou, o que esperava e o que aconteceu.
