# JTLTDA — Updates (feed multi-produto)

Central de releases e feed de atualização dos programas JTLTDA.

## Como funciona
Cada produto tem um arquivo JSON em `dist/`:

```json
{
  "product": "game-pro-fps",
  "version": "3.1.0",
  "pub_date": "2026-11-18",
  "title": "...",
  "changelog": ["..."],
  "installer": "https://github.com/JTLTDA/updates/releases/download/game-pro-fps-v3.1.0/GameProFPS_JTLTDA_Setup_v3.1.0.exe",
  "sha256": "...",
  "size_bytes": 0,
  "mandatory": false
}
```

O app (ex.: GAME PRO FPS JTLTDA) checa `https://jtltda.github.io/updates/dist/<produto>.json` ao iniciar,
compara com a versão instalada e mostra o banner de atualização.

## Produtos
- `game-pro-fps` — GAME PRO FPS JTLTDA (Focar no Jogo)

## Adicionando um produto novo
1. `dist/<produto>.json` seguindo o formato acima
2. Release com o instalador: `gh release create <produto>-v<versao> <Asset> --repo JTLTDA/updates`
3. O launcher do produto aponta seu `UPDATE_URL` para `dist/<produto>.json`
