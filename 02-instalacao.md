# 02 · Instalação

## Requisitos
- Uma conta no Claude com suporte a **plugins** (Claude Code, Cowork ou chat com plugins habilitados).
- Acesso ao repositório do ClaudeJuiz no GitHub (público).
- Opcional, mas recomendado: **busca na web** ativada, para o Juiz verificar o mercado.

## Opção A · Claude Code (marketplace)
No terminal do Claude Code:
```
/plugin marketplace add joaocarvalhojp40-ship-it/ClaudeJuiz
/plugin install claude-juiz@claudejuiz
```
Depois, reinicie a sessão se o Claude pedir.

## Opção B · Chat do Claude / Cowork
1. Abra o menu de **plugins** do Claude.
2. Escolha **adicionar plugin** e aponte para o repositório do GitHub, ou envie o arquivo `.zip` do projeto.
3. Ative o plugin **claude-juiz** na conversa.

## Opção C · Instalação manual (cópia de arquivos)
Copie as pastas `agents/`, `commands/` e `skills/` para o diretório de configuração do seu Claude Code (por exemplo, `~/.claude/`).

## Estrutura que o repositório PRECISA ter
O plugin só funciona se as pastas estiverem corretas:
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
├── docs/ ...
├── LICENSE
├── NOTICE
├── README.md
├── SECURITY.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
└── CHANGELOG.md
```
> ⚠️ Se os arquivos estiverem soltos na raiz do repositório, o Claude **não reconhece** o plugin.

## Verificando a instalação
1. Digite `/` e procure por `julgar`.
2. Ou diga: *"Claude, avalie meu projeto"*. A skill `julgamento` deve disparar.

## Atualizando
```
/plugin marketplace update claudejuiz
```
Confira o `CHANGELOG.md` para ver o que mudou.

## Desinstalando
```
/plugin uninstall claude-juiz@claudejuiz
```
