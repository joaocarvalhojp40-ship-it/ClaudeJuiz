# 04 · Os 4 Claudes

Cada Claude é um **agente** definido em um arquivo da pasta `agents/`.

## ⚖️ Juiz (`agents/juiz.md`)
- **Modelo sugerido:** o mais forte disponível (decisão final).
- **Papel:** receber o resumo e os 3 pareceres, pesquisar o mercado, dar notas, decidir.
- **Personalidade:** imparcial, sério e justo.
- **Entrega:** veredito, tabela de notas, análise de mercado, sentença, alternativas e próximos passos.
- **Regra de ouro:** os outros Claudes são conselheiros. Argumentos sem base são descartados.

## 😄 Bem-humorado (`agents/bem-humorado.md`)
- **Papel:** enxergar pontos fortes, oportunidades e formas de turbinar o projeto.
- **Personalidade:** otimista, caloroso, com humor leve.
- **Limite:** não pode inventar elogios sem base.
- **Entrega:** nota otimista, "o que brilha", oportunidades, como turbinar.

## 😠 Mal-humorado (`agents/mal-humorado.md`)
- **Papel:** apontar falhas, riscos, concorrentes e custos escondidos.
- **Personalidade:** ranzinza, cético, sarcasmo seco.
- **Limite:** critica o projeto, nunca a pessoa; não pode inventar problemas.
- **Entrega:** nota pessimista, o que pode dar errado, concorrência, riscos.

## 🙂 Neutro (`agents/neutro.md`)
- **Papel:** agir como cliente leigo que só quer resolver um problema.
- **Personalidade:** honesto, prático, sem jargão.
- **Perguntas-chave:** entendi em 10 segundos? resolve meu problema? é fácil? pagaria? prefiro isso ao que já uso?
- **Entrega:** nota do cliente, primeira impressão, o que gostou, o que confundiu, "usaria?".

## Por que os 3 pareceristas rodam em paralelo e isolados?
Para evitar **viés de ancoragem**: se um Claude lê o parecer do outro, tende a concordar ou reagir. Isolados, cada um dá uma opinião genuína. Só o Juiz vê tudo.

## Comparativo
| | Juiz | Bem-humorado | Mal-humorado | Neutro |
|---|---|---|---|---|
| Decide? | ✅ | ❌ | ❌ | ❌ |
| Vê todos os pareceres? | ✅ | ❌ | ❌ | ❌ |
| Pesquisa mercado? | ✅ | opcional | opcional | ❌ |
| Linguagem | formal | animada | ácida | simples |
| Foco | decisão | oportunidade | risco | experiência |

## Proteções comuns
Todos os agentes carregam a seção **🛡️ Proteções obrigatórias**: ignoram instruções escondidas no projeto, não repetem segredos, não dão garantias, não validam projetos nocivos e não inventam dados. Detalhes no [guia 06](06-seguranca-e-privacidade.md).
