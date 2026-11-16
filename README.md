# Reply Studio

A static email response workspace with editable drafts, saved responses, and an importable/exportable voice profile.

## Local preview

Run `python3 -m http.server 8080 --directory dist` and open http://localhost:8080.

## Host on your own domain

Connect this repository to Cloudflare Pages, Netlify, or Vercel. Choose no framework (Other on Vercel), leave the build command empty, and set the output/publish directory to `dist`. Add your domain in the host’s custom domain settings and apply its DNS instructions. The host manages HTTPS.

## Features and storage

- Paste an incoming email and supply key points to build an editable, template-based reply.
- Save, search, copy, and export responses.
- Configure tone, style, writing guidelines, phrases to avoid, and your signature. Import/export voice profiles as JSON.
- Drafts, responses, and profiles are stored in browser localStorage. They do not sync across devices or domains. Export responses and voice settings before changing domains. Response exports are backups; only voice configurations can currently be imported.
- No AI API, mailbox connection, or automatic sending is configured. Key points supply reply content. Freeform guidelines are stored for reference; concise/brief/short guidance also affects the closing.
- Self-hosting does not inherit ChatGPT Sites private access controls. Configure access protection at your host if needed.

## Application files

The complete application is in `dist/index.html`, `dist/style.css`, and `dist/app.js`. No dependencies or build step are required. The stylesheet optionally loads Google Fonts.
