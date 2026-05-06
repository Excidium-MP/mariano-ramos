# Mariano Ramos — sitio web

Single-page static site for Mariano Ramos. Pure HTML + CSS + a tiny bit of vanilla JS. No build step.

## Probarlo localmente

Abrí `index.html` con doble click. No hace falta servidor.

(Opcional, para ver cambios en vivo: `npx serve .` en la carpeta del proyecto.)

## Cómo cambiar las cosas pendientes

### 1. Foto de Mariano
Reemplazá el archivo en `assets/mariano.jpg` (mismo nombre, formato JPG). Idealmente vertical (proporción 4:5) y de buena calidad. No hay que tocar el código.

### 2. Imagen de fondo del banner (hero)
Reemplazá `assets/hero-bg.jpg` (mismo nombre). Conviene que sea horizontal, de alta resolución (ej. 1920×1080) y con un sujeto centrado o despejado, porque arriba va texto blanco.

> Si todavía no tenés ninguna foto, el sitio igual se ve bien: el banner usa un degradado oscuro de fondo y la zona de la foto un degradado terroso.

### 3. Redes sociales
En `index.html`, buscá el bloque `<ul class="socials">`. Hay tres `<a>` con `class="social hidden"` para Instagram, Facebook y TikTok.

Para activar una red:
1. Reemplazá `href="#"` por la URL real (ej. `https://instagram.com/marianoramos`).
2. Sacá la clase `hidden` (queda `class="social"`).

Si Mariano no tiene una de las redes, dejala con `hidden` y no se va a mostrar.

### 4. WhatsApp
Ya está cargado: **+54 9 11 2454-9817**. Si cambia, buscá `5491124549817` en `index.html` (aparece 3 veces: dos botones y el botón flotante) y reemplazalo. Formato: código país + área + número, sin `+`, sin espacios, sin guiones.

## Cómo publicarlo (gratis)

Cualquiera de estas tres opciones funciona — todas gratuitas para sitios estáticos chicos:

### Opción A — Netlify (la más fácil)
1. Entrá a https://app.netlify.com/drop
2. Arrastrá la carpeta `mariano-ramos` entera al recuadro.
3. Listo: te da una URL del tipo `algo-feliz-1234.netlify.app`. La podés cambiar gratis a `mariano-ramos.netlify.app` (o similar) en Site settings → Domain.

### Opción B — Vercel
1. Subí el proyecto a un repo de GitHub.
2. Entrá a https://vercel.com, "Import Project", elegí el repo.
3. Deploy con configuración por defecto (Vercel detecta sitio estático).

### Opción C — GitHub Pages
1. Subí los archivos a un repo de GitHub.
2. Settings → Pages → Deploy from a branch → `main` / `(root)`.
3. URL: `https://<tu-usuario>.github.io/mariano-ramos/`.

## Dominio propio (opcional)

Si querés un dominio tipo `marianoramos.com.ar`:
- Comprarlo en NIC.ar (dominios `.com.ar`) o cualquier registrar (Namecheap, Cloudflare, etc.).
- Apuntarlo al hosting elegido (Netlify y Vercel tienen instrucciones simples para custom domains).

## Estructura del proyecto

```
mariano-ramos/
├── index.html         estructura y contenido
├── styles.css         estilos
├── script.js          scroll suave
├── assets/
│   ├── favicon.svg    icono de pestaña (monograma "MR")
│   ├── hero-bg.jpg    PENDIENTE — fondo del banner
│   └── mariano.jpg    PENDIENTE — foto de Mariano
└── README.md          este archivo
```

## Cambios de copy

Todo el texto vive en `index.html`. Los lugares más comunes para editar:

- Tagline del hero: línea con `class="hero__tagline"`.
- Texto "Sobre Mariano": dentro de `<div class="about__text">`.
- Servicios: lista `<ul class="services">`.
- Zona de cobertura: párrafo con `class="coverage__text"`.
