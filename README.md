# CollabInk en Netlify

1. Subí esta carpeta a un repositorio (GitHub) y conectalo en Netlify, o usá `netlify deploy`.
2. En Discord Developer Portal → tu aplicación → OAuth2:
   - Redirects: `https://TU-SITIO.netlify.app/auth/callback` (y tu dominio propio, si tenés).
   - Copiá Client ID y Client Secret.
3. En Netlify → Site configuration → Environment variables:
   - `DISCORD_CLIENT_ID`
   - `DISCORD_CLIENT_SECRET`
   - `SESSION_SECRET` (32+ caracteres al azar, ej: `openssl rand -hex 32`)
4. Volvé a desplegar. Los datos se guardan en Netlify Blobs.

El Client Secret solo vive en las funciones (servidor); nunca llega al navegador.
