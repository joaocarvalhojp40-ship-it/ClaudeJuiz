# ⚖️ ClaudeJuiz

Um tribunal de **4 Claudes** que avalia o seu projeto e entrega um veredito honesto.

| Claude | Papel |
|---|---|
| ⚖️ **O Juiz** | Pondera tudo e decide se o projeto deve prosseguir |
| 😄 **O Bem-humorado** | Vê coisa boa em tudo |
| 😠 **O Mal-humorado** | Vê apenas coisas negativas |
| 🙂 **O Neutro** | Cliente leigo que só quer usar o projeto |

## O que é avaliado
Complexidade de execução, escassez no mercado, demanda real, diferencial, viabilidade técnica e de custo, monetização, clareza para o usuário e riscos. Se o projeto não for bom, o Juiz **sugere projetos parecidos** com mais chance de dar certo.

## Instalação
No Claude Code:

```
/plugin marketplace add joaocarvalhojp40-ship-it/ClaudeJuiz
/plugin install claude-juiz@claudejuiz
```

No Claude (chat / Cowork): adicione o plugin pelo menu de plugins, apontando para este repositório no GitHub, ou envie o `.zip` desta pasta.

## Uso
```
/julgar Um app de delivery de marmitas fitness para academias de São Paulo
```
Ou apenas converse: *"Claude, avalie meu projeto"*. A skill `julgamento` dispara sozinha.

## Como funciona
1. O Claude monta um resumo do projeto.
2. O Bem-humorado, o Mal-humorado e o Neutro avaliam **em paralelo**, sem ver o parecer um do outro.
3. O Juiz recebe os 3 pareceres, pesquisa o mercado, dá notas (0 a 10), a média e o veredito: **PROSSEGUIR**, **PROSSEGUIR COM AJUSTES** ou **NÃO PROSSEGUIR**.

## Estrutura
```
ClaudeJuiz/
├── .claude-plugin/
│   ├── plugin.json
│   └── marketplace.json
├── agents/
│   ├── juiz.md
│   ├── bem-humorado.md
│   ├── mal-humorado.md
│   └── neutro.md
├── commands/julgar.md
├── skills/julgamento/SKILL.md
├── LICENSE
└── README.md
```

## Licença
MIT
