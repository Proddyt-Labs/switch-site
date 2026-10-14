# Proddyt Studio — site

Landing page do **Proddyt Studio** (antigo "Proddyt Switch"): suíte gratuita e offline de 12 apps de criação e escritório.

- URL: https://switch.proddyt.com
- Repo: `Proddyt-Labs/switch-site`

## Estrutura

- `index.html` — página única (HTML + um `<style>` pequeno de layout).
- `CNAME` — domínio customizado (`switch.proddyt.com`). Não remover.
- `.github/workflows/pages.yml` — deploy no GitHub Pages.

## Editar e visualizar localmente

Edite `index.html` e sirva a pasta:

```
python -m http.server 8771 --bind 127.0.0.1
```

Abra http://127.0.0.1:8771. Fontes, tokens, CSS base e ícones vêm do CDN (precisa de internet).

## Deploy

Push na `main` dispara o workflow `Deploy Pages` (também manual via `workflow_dispatch`), que publica a raiz do repo com `configure-pages`, `upload-pages-artifact` e `deploy-pages`. O domínio vem do `CNAME`.

## Marca

Identidade compartilhada de `Proddyt-Labs/brand`, tag `@1`, via jsDelivr: `tokens.css`, `base.css`, `theme.js`, `marks/studio-mark.svg` e `marks/apps/<bin>.png`. Documentação da marca: https://proddyt-labs.github.io/brand/
