# LabInventi Landing Page

Landing page estática da LabInventi para publicação no GitHub e integração com Cloudflare.

## Rodar localmente

Use um servidor simples na pasta `public/`:

```bash
python3 -m http.server 8080 --directory public
```

Acesse: [http://localhost:8080](http://localhost:8080)

## Estrutura

- `public/index.html`: conteúdo da landing page
- `public/styles.css`: estilos e responsividade
- `public/script.js`: script simples para ano dinâmico no rodapé
- `wrangler.jsonc`: configuração de deploy no Cloudflare Workers

## Publicar no GitHub

```bash
git add .
git commit -m "feat: initial LabInvent landing page"
git remote add origin <URL_DO_REPOSITORIO>
git push -u origin main
```

## Deploy no Cloudflare (Workers)

Este projeto usa assets estáticos com Wrangler:

```bash
npm run deploy
```

No Cloudflare (Git integration), use:

- Deploy command: `npx wrangler deploy`
- Build command: *(vazio)*

## Conectar ao Cloudflare Pages (alternativo)

1. No Cloudflare, abra **Pages** > **Create a project**.
2. Conecte com o GitHub e escolha o repositório.
3. Em build settings:
   - Framework preset: `None`
   - Build command: *(vazio)*
   - Build output directory: `public`
4. Faça deploy.
