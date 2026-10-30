# Portafolio · Desarrollo de Software V

Universidad Tecnológica de Panamá · Centro Regional de Veraguas
II Semestre 2026

Plantilla del portafolio del curso. Cada estudiante crea el suyo a partir de
aquí y lo mantiene durante todo el semestre: en la portada va tu página
personal y, en `modulos/`, las prácticas y los laboratorios de cada módulo.

## Crear tu portafolio

1. Pulsa **Use this template → Create a new repository**.
2. Ponle este nombre, con tus datos, en minúsculas y sin tildes ni eñes:

   ```
   2026ii-dsv-portafolio-4gs121-NN-apellido-nombre
   ```

   Usa `4gs122` si estás en ese grupo. `NN` es tu número de lista, con dos
   cifras (`03`, no `3`).
3. Visibilidad: **Public**. GitHub Pages no publica repositorios privados en
   una cuenta gratuita.
4. Clona **tu** repositorio, no este:

   ```bash
   git clone https://github.com/TU-USUARIO/2026ii-dsv-portafolio-4gs121-NN-apellido-nombre.git
   ```

5. En tu repositorio: **Settings → Pages**, rama `main`, carpeta `/docs`.
   Al cabo de un minuto aparece la dirección de tu sitio:

   ```
   https://TU-USUARIO.github.io/2026ii-dsv-portafolio-4gs121-NN-apellido-nombre/
   ```

## Estructura

```
2026ii-dsv-portafolio-4gs121-NN-apellido-nombre/
├── README.md
├── .gitattributes
├── .gitignore
└── docs/                         ← lo que publica GitHub Pages
    ├── .nojekyll
    ├── index.html                ← tu página personal
    ├── assets/
    │   ├── css/
    │   │   ├── about-apellidos-nombre.css
    │   │   └── entregas.css
    │   └── img/
    │       ├── foto-apellidos-nombre-{160,320,480,640}.webp
    │       ├── logo-utp.svg
    │       └── logo-fisc.svg
    └── modulos/
        ├── index.html            ← índice de tus entregas
        ├── m01-control-versiones/
        │   ├── p01-taller-git/   ← M01 · Práctica 1
        │   └── lab01-github/     ← M01 · Laboratorio 1
        └── m02-html/
            └── p01-estructura/   ← M02 · Práctica 1
```

Las carpetas que ya existen traen solo un archivo `.gitkeep`, porque Git no
guarda carpetas vacías. Cuando pongas tu trabajo en una de ellas, borra su
`.gitkeep`. Las carpetas de las actividades siguientes las creas tú cuando
llegue cada una; su guía indica la ruta exacta.

No borres `.gitattributes` ni `docs/.nojekyll`. El primero evita que los
finales de línea de Windows te reescriban archivos completos. El segundo hace
que Pages publique todos tus archivos, también los que empiezan con guion bajo.

## Tu página personal

Si ya tienes tu perfil del Laboratorio 1, pasa su contenido a `docs/index.html`.
Las rutas de esta plantilla ya están ajustadas al portafolio; las del
laboratorio empezaban con `../../` y aquí no funcionan.

| En el Laboratorio 1 | Aquí |
| --- | --- |
| `about-apellidos-nombre.html` | `docs/index.html` |
| `assets/css/about-apellidos-nombre.css` | `docs/assets/css/` |
| `assets/img/foto-apellidos-nombre-*.webp` | `docs/assets/img/` |
| `../../assets/img/logo-*.svg` | `./assets/img/logo-*.svg` |
| Pestaña *Inicio* → `../../index.html` | *Mis entregas* → `./modulos/index.html` |

Antes de tu primer *commit*, revisa:

- [ ] Ya no queda ningún marcador `{{...}}` en `docs/index.html` ni en
      `docs/modulos/index.html`.
- [ ] Las cuatro fotos son tuyas, en sus cuatro tamaños reales y en recorte
      cuadrado. Si todavía ves «TU FOTO», falta cambiarlas.
- [ ] Los archivos de estilo y de fotos llevan tu nombre, y el HTML apunta a
      ellos.
- [ ] Borraste el comentario-guía del principio de `docs/index.html`.
- [ ] Abriste la página en el navegador: se ven la foto, los logos y los
      estilos, y *Mis entregas* lleva a `modulos/`.

Para buscar marcadores pendientes:

```bash
grep -rn "{{" docs/
```

## Publicar una entrega

1. Trabaja la actividad en la carpeta que indica su guía, dentro de
   `docs/modulos/`.
2. En `docs/modulos/index.html`, cambia el artículo «Pendiente de entregar» de
   esa actividad por uno publicado. El modelo está en un comentario dentro del
   Módulo I, y la guía trae el código, el título, el enlace y la descripción
   que debes poner.
3. Confirma y sube:

   ```bash
   git add docs/
   git commit -m "feat: publicar M02 Practica 1"
   git push
   ```

4. Espera a que Pages se actualice y abre la entrega desde tu sitio publicado,
   no desde tu computadora.
