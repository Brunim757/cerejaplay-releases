# CerejaPlay — Releases

Repositório público usado **apenas** para distribuir os binários dos apps do
CerejaPlay. O código-fonte fica nos repositórios privados.

## Canais

| App | Tag | Arquivo |
| --- | --- | --- |
| Android | `android-latest` | `cerejaplay-android.apk` |
| Windows | `desktop-latest` | `CerejaPlay-portable.exe` |

As tags são recriadas/atualizadas a cada build do CI. **Não use
`releases/latest`** neste repositório: ele aponta para a release mais recente do
repositório inteiro, não por app.

## Manifests

- `manifests/android.json`
- `manifests/desktop.json`

A API (`/api/app/update`) lê esses manifests para informar aos apps qual é a
versão mais recente, o link, o tamanho e o SHA-256.

## Atualização

- **Android:** o app baixa o APK e abre o instalador.
- **Windows:** o app baixa o `.exe`, confere o SHA-256 e troca o arquivo portátil
  após fechar (sem instalador).
