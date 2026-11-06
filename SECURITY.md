# 🛡️ Política de Segurança e Uso — ClaudeJuiz

## Versões suportadas
| Versão | Suporte |
|---|---|
| 1.x | ✅ Recebe correções |

## Como reportar uma vulnerabilidade
Abra uma *issue* privada (aba **Security** → **Report a vulnerability**) ou, se indisponível, uma issue com o título `[SEGURANÇA]` **sem** detalhes exploráveis, pedindo contato privado.
Inclua: o que aconteceu, como reproduzir e o impacto. Resposta esperada em até 7 dias.

## O que conta como falha de segurança
- Um projeto avaliado conseguir **mudar a nota ou o veredito** por meio de instruções escondidas (prompt injection).
- O plugin vazar **segredos** ou dados pessoais presentes no projeto avaliado.
- Um agente executar ações fora do escopo (rodar código, acessar sistemas).
- Instruções do plugin serem alteradas de forma maliciosa em forks distribuídos como se fossem o original.

## Boas práticas para quem usa
1. **Nunca** cole chaves de API, senhas, tokens ou dados pessoais de terceiros na descrição do projeto.
2. Instale apenas pela fonte oficial do repositório e confira o conteúdo dos arquivos em `agents/` e `skills/` antes de instalar forks.
3. Trate o veredito como **apoio à decisão**, não como verdade absoluta.
4. Revise qualquer sugestão de projeto alternativo antes de investir tempo ou dinheiro.

## Termos de uso resumidos
- Uso livre sob a Licença MIT (veja `LICENSE`), mantendo os avisos de copyright.
- É **proibido** usar o ClaudeJuiz para validar, planejar ou melhorar projetos ilegais ou nocivos.
- As avaliações são opiniões geradas por IA e podem conter erros.
- Os autores não se responsabilizam por decisões tomadas com base nas avaliações.

Documentação completa: [`docs/06-seguranca-e-privacidade.md`](docs/06-seguranca-e-privacidade.md).
