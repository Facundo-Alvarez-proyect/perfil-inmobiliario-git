# Portfolio inmobiliario

Trabajo final del curso. Es un sitio de varias páginas para un asesor inmobiliario. La idea era armar un portfolio profesional donde pueda mostrar los servicios, la cartera de propiedades y los datos de contacto particulares de un asesor.

## Tecnologías que usé

1. HTML5 semántico

2. SCSS compilado a CSS

3. Bootstrap 5 (navbar responsive)

4. AOS para las animaciones al hacer scroll

5. Git / GitHub

6. Visual Studio Code

7. Live Sass Compiler

8. Deploy en Vercel

## Cómo está organizado

- `index.html` → página de inicio

- `pages/`
  - `sobremi.html` → habla sobre el asesor y su experiencia
  - `servicios.html` → los servicios que ofrece
  - `cartera.html` → propiedades que tiene el asesor en cartera
  - `contacto.html` → datos de contacto del asesor

- `assets/` → imágenes y logos necesarios para la página

- `scss/`
  - `main.scss` → archivo principal que contiene únicamente los `@use`
  - `utilities/` → variables y mixins
  - `base/` → estilos base y tipografía
  - `layout/` → header, navbar, footer y estilos responsive
  - `components/` → estilos reutilizables como cards y botones
  - `pages/` → estilos propios de cada página

- `styles/`
  - `style.css` → CSS generado automáticamente a partir de `scss/main.scss`
  - `style.css.map` → archivo de mapa generado por Sass

## Cómo correrlo en tu máquina

1. Cloná el repositorio o descargalo en formato ZIP.

2. Abrí el proyecto en Visual Studio Code.

3. Abrí `index.html` con Live Server (extensión de VSCode) o directamente desde el navegador.

4. Desde `index.html` podés navegar a todas las páginas de `pages/` mediante la navbar.

Los estilos ya están compilados en `styles/style.css`, por lo que el proyecto puede ejecutarse directamente.

### Para modificar los estilos

El código fuente de los estilos se encuentra en la carpeta `scss/`.

El archivo principal es:

`scss/main.scss`

Este archivo utiliza `@use` para importar los diferentes parciales de SCSS.

Para compilar los cambios utilizo la extensión **Live Sass Compiler** de VSCode. Desde `scss/main.scss` se puede seleccionar **Watch Sass** para que los cambios se compilen automáticamente.

El archivo generado se guarda dentro de la carpeta `styles/` como `style.css`.

## Sitio en producción

[Ver sitio web](https://perfil-inmobiliario-git.vercel.app/)

El proyecto está publicado en Vercel y fue probado en desktop, tablet y celular.

## Checklist de la consigna

| Requisito | Dónde está |
|---|---|
| 5 HTML con etiquetas semánticas | `index.html` y los 4 archivos de `pages/` utilizan `header`, `nav`, `main`, `section`, `article` y `footer` |
| Title / meta description / meta keywords únicos | En el `<head>` de cada uno de los 5 HTML |
| Alt en todas las imágenes | Todas las imágenes utilizadas tienen atributo `alt` |
| Navbar de Bootstrap con hamburguesa, estilada desde SCSS | Bootstrap en los 5 HTML, estilos propios en `scss/layout/_nav.scss` y `scss/components/_buttons.scss` |
| Responsive sin scroll horizontal | Media queries en `scss/layout/_responsive.scss`, probado en mobile, tablet y desktop |
| SCSS con variables, nesting, mixins con parámetros, extend y partials | Variables en `utilities/_variables.scss`, mixin con parámetros `texto($tamanio, $peso)` en `utilities/_mixins.scss`, `@extend %texto-centrado` en `pages/_sobremi.scss` y estilos separados en partials |
| `main.scss` solo con `@use` | El archivo contiene únicamente las importaciones mediante `@use` |
| Animación nativa + librería externa | `transition` en los estilos de las páginas y AOS implementado en `pages/sobremi.html` |
| Deploy funcionando | Proyecto publicado en Vercel |
| Repo público con commits descriptivos | Repositorio público en GitHub con historial de commits |