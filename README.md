# Offload.ar — Tienda de camisetas

Stack: HTML/JS estático + JSON en GitHub + Netlify. Mismo esquema que usaste en CATAS FC.

## 1. Crear el repo
1. Andá a GitHub → New repository → nombre: `offload-ar` (o el que quieras) → público o privado, da igual → Create.
2. Subí **todos los archivos de esta carpeta** (`index.html`, `admin/`, `data/`, `assets/`) manteniendo la misma estructura. Podés arrastrarlos desde la web de GitHub ("Add file → Upload files") o con git desde la terminal.

## 2. Conectar Netlify
1. Netlify → Add new site → Import an existing project → GitHub → elegí el repo `offload-ar`.
2. Build command: dejalo vacío. Publish directory: `/` (la raíz).
3. Deploy. Netlify te da una URL tipo `offload-ar.netlify.app` (después le podés poner dominio propio).

## 3. Generar el token de GitHub (lo hacés vos, una sola vez)
1. GitHub → foto de perfil → Settings → Developer settings → Personal access tokens → Tokens (classic) → Generate new token.
2. Marcá el scope **repo** (acceso completo al repositorio).
3. Generate → copiá el token (empieza con `ghp_...`). No lo vas a poder ver de nuevo, guardalo en un lugar seguro.

## 4. Configurar el panel en el celu de tu amigo
1. Abrí `https://TU-SITIO.netlify.app/admin/` desde el celular de tu amigo.
2. Va a pedir: usuario/repositorio (ej: `simfactor06/offload-ar`), rama (`main`) y el token del paso 3.
3. Guardar y entrar. Con eso queda configurado para siempre en ese celular — tu amigo no vuelve a tocar esta pantalla.

## 5. Uso diario (para tu amigo)
- Entra a `/admin/`, toca **Agregar camiseta**, elige la foto de la galería, completa nombre/precio/talles y toca **Guardar camiseta**.
- Para dar de baja una camiseta vendida: **Editar** → destildar "Disponible" → Guardar (queda marcada como Agotada en la web, no se borra).
- Los cambios tardan ~30-60 segundos en verse en la página pública (Netlify redeploya solo).

## Notas
- El precio del WhatsApp y el nombre de la tienda se editan en la sección "Datos de contacto" del panel.
- Las fotos se guardan en `images/` dentro del mismo repo — no dependen de ningún servicio externo.
- Si algún día cambian de repositorio o token, tocan "Cambiar repositorio / token" al final del panel.
