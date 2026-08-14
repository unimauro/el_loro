# 🦜 El Loro — La Expo de Gael

Página web de la exposición de **Gael Cárdenas Urrutia** (YMCA · 3 años) sobre los loros.
Sitio estático (HTML/CSS/JS), mobile-first, sin dependencias, listo para GitHub Pages.

## Ver en vivo
👉 https://unimauro.github.io/el_loro/

## Secciones
Inicio · El loro · Plumas · Pico · Habla (Blipii) · Alas · ¿Dónde vive? · Especies · Comparte tu loro.

## Fotos
En `assets/` hay fotos reales de dominio público (Wikimedia Commons) de cada especie:
`ara_macao`, `ara_ararauna`, `amazona_ochrocephala`, `psittacus_erithacus`, `cacatua_galerita`.

### Usar los posters de diseño
Cada sección intenta cargar primero un **poster** y, si no existe, usa la foto real como respaldo.
Para poner tus diseños, sube estos archivos a `assets/` (un solo push actualiza el sitio):

| Archivo | Sección |
|---|---|
| `poster-hero.jpg`   | Portada |
| `poster-loro.jpg`   | El loro |
| `poster-plumas.jpg` | Plumas |
| `poster-pico.jpg`   | Pico |
| `poster-habla.jpg`  | Habla (Blipii) |
| `poster-alas.jpg`   | Alas |
| `poster-donde.jpg`  | ¿Dónde vive? |

## Comparte tu loro (muro)
La sección "Comparte tu loro" guarda comentarios y fotos en el propio dispositivo (localStorage).
Para hacerlos **compartidos entre todos los celulares**, conecta la Tunky API definiendo en el HTML:

```html
<script>window.TUNKY_API = 'https://tu-endpoint-tunky/loros';</script>
```

El formulario hace `POST` con `{nombre, mensaje, img, fecha}`.
