# Scale AR Media — Sitio estático

## Archivos
- `index.html` — la web completa (todo en un solo archivo, sin build)
- `sa-logo.png` — logo
- `sa-media.png` — logo grande del hero
- `.htaccess` — fuerza HTTPS y caché de assets (Hostinger)

## Cómo subirlo a Hostinger

1. Entrá al **hPanel** de Hostinger → **Administrador de archivos** (File Manager).
2. Abrí la carpeta **`public_html`** de tu dominio `.shop`.
3. Borrá el `index.html` por defecto si Hostinger creó uno.
4. Subí los 4 archivos de este zip directamente dentro de `public_html`:
   - `index.html`
   - `sa-logo.png`
   - `sa-media.png`
   - `.htaccess`  (asegurate que se llame `.htaccess` con el punto adelante)
5. Listo. Entrá a `https://tudominio.shop` y la web va a estar online.

## Conectar el dominio .shop

- Si compraste el dominio `.shop` en Hostinger, ya está apuntando al hosting automáticamente.
- Si lo compraste en otro lado, en el panel del registrador apuntá los **nameservers** a:
  - `ns1.dns-parking.com`
  - `ns2.dns-parking.com`
  (Hostinger te muestra los suyos en hPanel → Dominios.)
- El SSL (https) se activa solo desde hPanel → SSL → Instalar.

## Editar precios o textos
Abrí `index.html` con cualquier editor (Bloc de notas / VSCode) y buscá:
- Precios y paquetes: el array `PACKS` (línea ~+260)
- Alias / CBU: el objeto `PAYMENT`
- Número de WhatsApp: la constante `WA_NUMBER`
