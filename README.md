# Reevalúa Empresas · landing + calculadora

**Sitio público (GitHub Pages):** https://howquii.github.io/reevalua-empresas/  
Calculadora: https://howquii.github.io/reevalua-empresas/calculadora.html

Cada `git push` a `main` republica el sitio en 1 o 2 minutos.

Sitio estático, sin build. Dos páginas y una carpeta de assets:

- `index.html`  landing B2B (hero con video, secciones, comunidad HR, FAQ, footer)
- `calculadora.html`  flujo de 7 pasos con las fórmulas de la calculadora comercial
- `shared.css`  tokens de marca (Manual de identidad Reevalúa, mayo 2025) y componentes compartidos
- `assets/`  video del hero, póster, logos oficiales (`assets/real/`), logos de clientes (`assets/logos/`), fotos (`assets/photos/`)
- `dist/`  copias de un solo archivo para Artifacts (se regeneran con `python3 build_artifact.py`)
- `reevalua-empresas-standalone.html`  TODO en un solo archivo (video incluido) para reenviar por correo o Drive

## Ver en local
Doble clic en `index.html`. Necesita internet solo para la tipografía Inter (Google Fonts).

## Publicar en Vercel (un solo comando)
```bash
npm i -g vercel        # una sola vez
cd site
vercel login           # abre el navegador, una sola vez
vercel --prod          # responde: Set up and deploy? Y · Scope: tu cuenta · Link to existing? N · Project name: reevalua-empresas · Directory: ./
```
Vercel devuelve la URL pública (p. ej. `https://reevalua-empresas.vercel.app`). Cada cambio: volver a correr `vercel --prod`.

Alternativa sin terminal: en vercel.com → Add New → Project → arrastrar la carpeta `site/`.

## Pendientes funcionales
- Conectar el formulario del paso 6 y el de Comunidad HR a HubSpot (hoy son demo, no envían datos).
- Reemplazar fotos de stock por banco de fotos real de eventos y alianzas.
- Confirmar autorización de marca de los logos de clientes.
