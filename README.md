# Corrige Aí Mail — instaladores para Windows

Lê as mensagens do Colaborar e sugere respostas no seu tom.

Este repositório existe só para **distribuir** o app: os instaladores ficam em
[Releases](https://github.com/faustort/coai-mail-instaladores/releases). O código-fonte é privado.

## Baixar

**[Baixar a versão mais recente](https://github.com/faustort/coai-mail-instaladores/releases/latest/download/CorrigeAi-Mail-Setup.exe)** · `CorrigeAi-Mail-Setup.exe`

O link acima sempre aponta para a última versão **estável**. Enquanto só houver versões de teste (`-rc`),
baixe pela página de [Releases](https://github.com/faustort/coai-mail-instaladores/releases) (a mais nova fica no topo) ou pelo site, em **Minha conta › Baixar os apps**.

> Para usar o app é preciso uma assinatura ativa em [corrigeai.nw2.com.br](https://corrigeai.nw2.com.br/).
> Entre no app com o mesmo e-mail e a mesma senha da sua conta no site.

## Instalar

1. Abra o arquivo baixado com dois cliques. Não precisa de senha de administrador.
2. Se aparecer **"O Windows protegeu o computador"**, clique em **Mais informações** e depois em
   **Executar assim mesmo**. O aviso aparece enquanto o instalador não tem assinatura digital.
3. O app abre sozinho no fim da instalação e cria atalhos na Área de Trabalho e no menu Iniciar.

**Requisitos:** Windows 10 ou 11 (64 bits), cerca de 500 MB livres e internet. 

## Atualizações

O app verifica se há versão nova (30 segundos depois de abrir e depois a cada 6 horas).
Quando encontra, avisa no painel. Seus dados e configurações são mantidos em qualquer atualização,
e desinstalar o app também não apaga seus dados.

## Conferir o arquivo (opcional)

Cada release traz o `latest.yml` com o SHA-512 do instalador; o próprio atualizador recusa um arquivo adulterado.
Para conferir manualmente no PowerShell:

```powershell
Get-FileHash .\CorrigeAi-Mail-Setup.exe -Algorithm SHA256
```

e compare com o `.sha256` publicado na mesma release.

## Suporte

Pelo site: [corrigeai.nw2.com.br](https://corrigeai.nw2.com.br/).
