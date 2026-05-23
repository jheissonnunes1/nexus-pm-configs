# nexus-pm-configs

Mirror público de `nexus-pm/configs/` para drift check cross-repo sem autenticação.

## Conteúdo

| Arquivo | Propósito |
|---|---|
| `ruff.toml` | Config canônico do ruff (Python) |
| `.golangci.yml` | Config canônico do golangci-lint (Go) |

## Uso

Os CIs dos repos técnicos baixam estes arquivos via `raw.githubusercontent.com` e comparam
com a cópia local usando `nexus-pm/scripts/check-config-drift.sh`.

## Canonical

Os arquivos canônicos vivem em `nexus-pm/configs/`. Este repo é populado automaticamente
pelo workflow `nexus-pm/.github/workflows/sync-configs-to-public.yml` a cada push em `main`
que toque `configs/`.

Não edite diretamente — abra PR no canonical em `jheissonnunes1/nexus-pm`.
