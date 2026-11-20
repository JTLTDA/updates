# JTLTDA — Updates

Central de releases e feed de atualização dos programas JTLTDA.

## Como funciona

Cada produto tem um arquivo JSON em `dist/`. O app checa esse JSON ao iniciar,
compara a versão e mostra o banner de atualização se houver versão nova.

## Feed JSON (formato padrão)

```json
{
  "product": "nome-do-produto",
  "version": "X.Y.Z",
  "pub_date": "YYYY-MM-DD",
  "title": "descrição curta",
  "changelog": ["item 1", "item 2"],
  "installer": "https://github.com/JTLTDA/updates/releases/download/nome-vX.Y.Z/Setup.exe",
  "sha256": "hash_sha256_do_instalador",
  "size_bytes": 0,
  "mandatory": false
}
