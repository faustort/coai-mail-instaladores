# Histórico de versões — Corrige Aí Mail

Formato: [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/) · versões em [SemVer](https://semver.org/lang/pt-BR/).
Versões `-rc.N` são de teste: saem como *pre-release* e só chegam a quem liga "Receber versões de teste" no app.
Cada versão tem o instalador, o `.sha256` e o `latest.yml` na página de [Releases](https://github.com/faustort/coai-mail-instaladores/releases).

## [Não lançado]

### Novidades
- **Atualização automática:** o app baixa a versão nova sozinho e avisa "Atualização pronta para instalar". Para instalar, abra Configurações › Atualizações e suporte e clique em Reiniciar para atualizar.
- **Histórico do aluno:** mostra primeiro o diálogo aluno↔professor e separa a régua do restante.

## [1.2.0-rc.7] — 2026-11-03 · versão de teste (pre-release)

Primeira versão publicada neste repositório, para testadores.

### Novidades
- Mensagens de licença em português, links de ajuda ("Por que não consigo acessar?") e aviso de renovação.
- Link "Esqueci minha senha" na tela de ativação.
- Instalador de um clique, por usuário, sem pedir senha de administrador, em português; seus dados nunca são apagados ao desinstalar.
- Aba **Atualizações e suporte**, com pacote de suporte (sem segredos nem conteúdo de e-mail) e reparo de rede.
- **Redefinir configurações / Remover tudo**, com confirmação.
- Tela de abertura imediata com a identidade do Corrige Aí e espera mais longa pelo servidor.
- Histórico por RA com total e "Mostrar mais".

### Corrigido
- Resposta ao aluno só conta como enviada se o portal realmente aceitou.
- Envio e leitura não esperam mais uma sincronização longa.
- Fila de envio mais segura: sem duplicidade, sem itens órfãos.
- Item do lote só conclui se o rascunho foi gravado.
- Segurança reforçada: o app aceita só conexões locais, links de e-mail não abrem a ponte do app e o texto do aluno é tratado como dado no prompt da IA.
- Falhas de migração do banco ficam visíveis e o encerramento do app é limpo.
