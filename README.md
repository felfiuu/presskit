# Press Kit KELVIN_OS — Hospedagem e Atualização

## Onde está tudo

| Item | Local |
|---|---|
| Site (link da bio) | https://felfiuu.github.io/presskit/ |
| Repositório | https://github.com/felfiuu/presskit (branch `main`) |
| ZIP do kit completo | Release v1.0 → https://github.com/felfiuu/presskit/releases/download/v1.0/KELVIN_OS_Press_Kit.zip |
| Custo | R$ 0 (GitHub Pages + GitHub Releases) |

A pasta `deploy/` (em `D:/Projects/KELVIN_OS`) **é a fonte do site**. O que está nela é o que vai pro ar.

## Atualizar o site (textos, fotos, CSS)

```bash
cd D:/Projects/KELVIN_OS/deploy
# 1. edite os arquivos (index.html, pasta PRESS_KIT_KELVIN_OS/...)
git add -A        # obrigatório DEPOIS de editar, senão a mudança não entra
git commit -m "descreva a mudanca"
git push
```

O site atualiza sozinho em ~1 minuto. Limite: cada arquivo do repositório deve ter menos de 100 MB.

## Trocar o ZIP do press kit completo

Opção A — mesmo link (recomendado, botão não muda):

```bash
# gere o novo zip com o MESMO nome: KELVIN_OS_Press_Kit.zip
cd D:/Projects/KELVIN_OS
gh release upload v1.0 KELVIN_OS_Press_Kit.zip --repo felfiuu/presskit --clobber
```

Opção B — release novo (v1.1): criar o release e trocar o `href` do botão em
`deploy/index.html` (procure `releases/download`), depois `git add -A && git commit && git push`.

## Instagram

- **Bio**: Editar perfil → Links → Adicionar link externo → `https://felfiuu.github.io/presskit/` → título "Press Kit 🎧". São 5 slots nativos, grátis.
- **Stories**: sticker **Link** com a mesma URL.
- Legendas de posts **não são clicáveis** — sempre "link na bio".

## Credenciais (esta máquina)

- Git e GitHub CLI instalados (`winget install Git.Git GitHub.cli` se reinstalar).
- Login do `gh` salvo no cofre do Windows (conta **felfiuu**) — não expira em uso normal.
- Git configurado para autenticar via `gh` — `git push` não pede senha.
- Se precisar autenticar de novo: `gh auth login --web` e seguir o código na tela.

## Limites do plano grátis

- Página: ~100 GB/mês de banda (limite elástico; cada visita ≈ 2 MB — folga total).
- Repositório: 1 GB recomendado; arquivos individuais até 100 MB.
- Releases: até 2 GB por arquivo — o ZIP vive aqui justamente por isso.
