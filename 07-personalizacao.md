# 07 · Personalização

Tudo no ClaudeJuiz é texto editável. Você pode adaptar sem programar.

## Mudar a personalidade
Edite a seção **Personalidade** do agente em `agents/`. Exemplos:
- Deixar o Mal-humorado mais sarcástico ou mais técnico.
- Tornar o Bem-humorado mais formal.
- Fazer o Neutro representar um público específico (ex.: "uma senhora de 60 anos que usa pouco o celular").

## Mudar os critérios
Em `agents/juiz.md`, altere a lista de critérios. Você pode:
- Adicionar: "Impacto ambiental", "Conformidade legal (LGPD)", "Facilidade de escalar".
- Remover os que não fazem sentido para o seu caso.
- Dar **pesos** (ex.: demanda vale o dobro) e explicar o cálculo da média ponderada.

## Mudar as faixas do veredito
Ajuste os limites (7 e 5) na seção **Veredito**. Um projeto acadêmico, por exemplo, pode usar limites mais brandos.

## Adicionar um quinto Claude
1. Crie `agents/novo-claude.md` com `name`, `description` e `model`.
2. Copie o cabeçalho de copyright e a seção **🛡️ Proteções obrigatórias**.
3. Em `skills/julgamento/SKILL.md`, inclua o novo agente no **Passo 2**.
4. Faça o Juiz considerar o novo parecer no **Passo 3**.

Ideias: **O Investidor** (retorno financeiro), **O Advogado** (riscos legais), **O Técnico** (arquitetura), **O Designer** (experiência visual).

## Mudar o idioma
Traduza os textos dos agentes e da skill. Mantenha os nomes dos arquivos e o campo `name` iguais.

## Escolher modelos
O campo `model` de cada agente aceita aliases como `sonnet` e `opus`. Use um modelo mais forte no Juiz e um mais rápido nos pareceristas para economizar.

## O que NÃO alterar
- A seção **🛡️ Proteções obrigatórias**.
- O cabeçalho de copyright e os arquivos `LICENSE` e `NOTICE`.
- O isolamento dos 3 pareceristas (rodar em paralelo, sem ver os outros).

## Versionar suas mudanças
Registre no `CHANGELOG.md` e use *tags* (`v1.2.0`).
