# LabInvent Landing Page

Landing page estática da LabInvent para publicação no GitHub e integração com Cloudflare Pages.

## Rodar localmente

Abra `index.html` direto no navegador ou use um servidor simples:

```bash
python3 -m http.server 8080
```

Acesse: [http://localhost:8080](http://localhost:8080)

## Estrutura

- `index.html`: conteúdo da landing page
- `styles.css`: estilos e responsividade
- `script.js`: script simples para ano dinâmico no rodapé

## Publicar no GitHub

```bash
git add .
git commit -m "feat: initial LabInvent landing page"
git remote add origin <URL_DO_REPOSITORIO>
git push -u origin main
```

## Conectar ao Cloudflare Pages

1. No Cloudflare, abra **Pages** > **Create a project**.
2. Conecte com o GitHub e escolha o repositório.
3. Em build settings:
   - Framework preset: `None`
   - Build command: *(vazio)*
   - Build output directory: `/`
4. Faça deploy.
