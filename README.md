# ⚖️ ClaudeJuiz

> Um tribunal de **4 Claudes** que avalia o seu projeto e entrega um veredito honesto.

![licença](https://img.shields.io/badge/licen%C3%A7a-MIT-green) ![versão](https://img.shields.io/badge/vers%C3%A3o-1.1.0-blue) ![tipo](https://img.shields.io/badge/tipo-plugin%20Claude-purple)

| Claude | Papel |
|---|---|
| ⚖️ **O Juiz** | Pondera tudo e decide se o projeto deve prosseguir |
| 😄 **O Bem-humorado** | Vê coisa boa em tudo |
| 😠 **O Mal-humorado** | Vê apenas coisas negativas |
| 🙂 **O Neutro** | Cliente leigo que só quer usar o projeto |

## O que é avaliado
Complexidade de execução, **escassez no mercado**, demanda real, diferencial, viabilidade técnica e de custo, monetização, clareza para o usuário e riscos. Se o projeto não for bom, o Juiz **sugere projetos parecidos** com mais chance de dar certo.

## Instalação rápida
Claude Code:
```
/plugin marketplace add joaocarvalhojp40-ship-it/ClaudeJuiz
/plugin install claude-juiz@claudejuiz
```
Chat/Cowork: adicione o plugin pelo menu de plugins apontando para este repositório. Detalhes em [docs/02-instalacao.md](docs/02-instalacao.md).

## Uso
```
/julgar Um app de delivery de marmitas fitness para academias de São Paulo
```
Ou converse: *"Claude, avalie meu projeto"*. A skill `julgamento` dispara sozinha.

## Como funciona
1. O Claude monta um resumo do projeto.
2. Bem-humorado, Mal-humorado e Neutro avaliam **em paralelo e isolados**.
3. O Juiz recebe os 3 pareceres, pesquisa o mercado, dá notas (0 a 10), a média e o veredito: **PROSSEGUIR**, **PROSSEGUIR COM AJUSTES** ou **NÃO PROSSEGUIR**.

## 🛡️ Segurança e uso
- Contém só texto (sem código executável).
- Todos os agentes ignoram instruções escondidas no projeto (*prompt injection*), não repetem segredos e não validam projetos nocivos.
- **Nunca cole chaves, senhas ou dados pessoais** na descrição do projeto.
- As avaliações são apoio à decisão, sem garantia de resultado.
- Leia [SECURITY.md](SECURITY.md) e [docs/06-seguranca-e-privacidade.md](docs/06-seguranca-e-privacidade.md).

## 📚 Documentação
[Índice completo](docs/README.md): [Visão geral](docs/01-visao-geral.md) · [Instalação](docs/02-instalacao.md) · [Como usar](docs/03-como-usar.md) · [Os agentes](docs/04-os-agentes.md) · [Critérios](docs/05-criterios-e-notas.md) · [Segurança](docs/06-seguranca-e-privacidade.md) · [Personalização](docs/07-personalizacao.md) · [FAQ](docs/08-faq.md) · [Problemas](docs/09-solucao-de-problemas.md) · [Exemplo](docs/exemplos/exemplo-avaliacao.md)

## Estrutura
```
ClaudeJuiz/
├── .claude-plugin/ (plugin.json, marketplace.json)
├── agents/ (juiz, bem-humorado, mal-humorado, neutro)
├── commands/ (julgar.md)
├── skills/julgamento/ (SKILL.md)
├── docs/ (guias + exemplos/)
├── LICENSE · NOTICE · SECURITY.md
├── CODE_OF_CONDUCT.md · CONTRIBUTING.md · CHANGELOG.md
└── README.md
```

## Contribuir
Veja [CONTRIBUTING.md](CONTRIBUTING.md) e o [Código de Conduta](CODE_OF_CONDUCT.md).

## Licença e avisos
MIT (veja [LICENSE](LICENSE) e [NOTICE](NOTICE)). Projeto independente, não afiliado à Anthropic. "Claude" é marca da Anthropic, PBC.
