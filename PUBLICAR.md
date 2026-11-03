# Como publicar uma versão nova

> Sempre pelo script do app (repositório privado `corrigeai-mail`), nunca subindo arquivo à mão:
> ele monta o `latest.yml`, o `.blockmap` (atualização diferencial) e a cópia com nome estável
> `CorrigeAi-Mail-Setup.exe` usada no botão do site.

## Uma vez só (antes da 1ª release)

No repositório do app, em `release.config.cjs`:

```js
repositorioReleases: { owner: 'faustort', repo: 'coai-mail-instaladores' },
```

Com isso o build grava o `app-update.yml` e o atualizador passa a olhar este repositório.
**Nunca renomeie, transfira ou apague este repositório**: o nome fica gravado em cada instalação.

## A cada versão

1. Suba a versão no `package.json` do app (ex.: `1.2.0-rc.7` → próxima) e faça commit.
2. `npm run build:win` → o instalador sai em `C:\CorrigeAi-Instaladores\CorrigeAi-Mail\` como `CorrigeAi-Mail-Setup-X.Y.Z.exe`.
3. `npm run release:publish -- --executar` → cria a release como **rascunho** (pre-release se a versão tem `-rc`).
   Sem certificado de assinatura, acrescente `--permitir-sem-assinatura`.
4. Confira o rascunho no GitHub e registre a versão no `CHANGELOG.md` deste repositório.
5. `npm run release:promote -- --executar` → publica. A partir daí o link "latest" e o atualizador enxergam a versão.
6. Opcional, liberação gradual: `npm run release:rollout -- 10 --executar` (depois 50, 100).

**Desfazer uma versão ruim = publicar uma versão MAIOR.** O atualizador nunca volta versão.

## Atualização "estilo VS Code" (baixa sozinho, instala ao reiniciar)

Já está programada no app, mas só liga com o instalador **assinado** (certificado de assinatura de código)
e o `publisherName` gravado. Sem certificado, o app só **avisa** que há versão nova e abre a página de download.
Detalhes: `docs/release/DISTRIBUICAO-E-ATUALIZACAO.md` e `docs/release/CERTIFICADO.md` no repositório do app.
