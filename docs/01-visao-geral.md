# 01 · Visão geral

## O que é o ClaudeJuiz?
O ClaudeJuiz é um **plugin** que transforma o Claude em um pequeno tribunal. Em vez de uma única opinião, você recebe **quatro perspectivas** sobre o seu projeto e, no final, **um veredito**.

## O problema que ele resolve
Quando temos uma ideia, é comum cair em dois extremos:
- **Empolgação demais**: só vemos o lado bom e ignoramos riscos.
- **Medo demais**: só vemos obstáculos e desistimos cedo.
Além disso, quem constrói quase nunca consegue se colocar no lugar de um cliente leigo. O ClaudeJuiz força essas três visões e depois as pesa com imparcialidade.

## Os 4 personagens
| Personagem | Função | Pergunta que responde |
|---|---|---|
| ⚖️ **Juiz** | Decide | "Este projeto deve prosseguir?" |
| 😄 **Bem-humorado** | Otimista | "O que há de bom e quais as oportunidades?" |
| 😠 **Mal-humorado** | Pessimista | "O que pode dar errado?" |
| 🙂 **Neutro** | Cliente leigo | "Eu entenderia, usaria e pagaria por isso?" |

## O que é avaliado
Complexidade de execução, **escassez no mercado**, demanda real, diferencial, viabilidade técnica e de custo, potencial de monetização ou impacto, clareza para o usuário e riscos.

## Resultado final
- Um **veredito**: `PROSSEGUIR`, `PROSSEGUIR COM AJUSTES` ou `NÃO PROSSEGUIR`.
- Uma **tabela de notas** (0 a 10) com a média.
- Uma **análise de mercado** (concorrentes e escassez).
- **Projetos alternativos** parecidos, quando o projeto não é bom.
- **Próximos passos** práticos.

## O que o ClaudeJuiz NÃO é
- Não é uma garantia de sucesso nem de fracasso.
- Não substitui pesquisa de mercado real, advogado, contador ou conversa com clientes de verdade.
- Não executa o seu código nem acessa os seus sistemas.

## Para que tipos de projeto serve?
Aplicativos, sites, jogos, bots, comunidades, produtos físicos, negócios, canais de conteúdo, startups, projetos acadêmicos, ferramentas internas e qualquer ideia que possa ser descrita em texto.

## Arquitetura em uma imagem
```
            Você descreve o projeto
                     │
              Skill "julgamento"
              (monta o resumo)
                     │
      ┌──────────────┼──────────────┐
      ▼              ▼              ▼
 Bem-humorado   Mal-humorado     Neutro     ← em paralelo
      └──────────────┼──────────────┘
                     ▼
                   Juiz  ← pesquisa mercado, dá notas
                     │
         Veredito + alternativas + próximos passos
```
