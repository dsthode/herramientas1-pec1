# PEC 1 de Herramientas HTML y CSS 1

# Autor: Damián Serrano Thode

## Plataforma de desarrollo

Para el desarrollo de la práctica he seguido las instrucciones indicadas en los materiales de aprendizaje de los módulos 1 y 2.

Según esas instrucciones, he creado el proyecto usando el comando `npm init` y he instalado los siguientes módulos:

- ParcelJS
- Autoprefixer
- Parcel Bundler
- NPM Run All
- Rimraf

Además de estos módulos indicados en los materiales de la práctica, he instalado los siguientes módulos adicionales:

- Parcel Imagemin, este módulo lo utilizo para procesar las imágenes y reducirles la calidad para mejorar los tiempos de descarga.
- Posthtml, este módulo lo utilizo como base para procesar el código HTML con el siguiente plugin.
- Posthtml Include, este módulo lo utilizo para crear plantillas de HTML que posteriormente puedo incluir en otros archivos HTML.
- Fontawesome Free 5, este módulo lo utilizo para utilizar los iconos de esta tipografía en determinados puntos de la página web.

Para el desarrollo de la práctica he usado Vsiual Studio Code como editor de código fuente, y he usado Docker como entorno de ejecución, aparte de usar Ubuntu como el sistema operativo que tengo en mi equipo.

El motivo de usar Docker es que de esta manera puedo crear un entorno de desarrollo específico para esta práctica sin necesidad de **contaminar** mi equipo con versiones de NodeJS u otros paquetes que puedan crear conflictos con otros componentes presentes en mi equipo.

A través de un archivo `Makefile` puedo ejecutar los comandos en el contenedor de Docker sin necesidad de escribir una línea de comandos my larga.

## Estructura

El sitio web lo he organizado con la siguiente estructura:

```
--- css/
|-- images/
|-- partials/
|-- script/
--- *.html
```

En el directorio `css` se encuentran las hojas de estilo para las páginas.

En el directorio `images` se encuentran las imágenes usadas en el sitio web.

En el directorio `partials` se encuentran las plantillas HTML que posteriormente se incluirán en las otras páginas.

En el directorio `script` se encuentra el archivo JavaScript.

Y finalmente en el directorio raíz se encuentran los archivos HTML de cada una de las páginas que conforman el sitio.

### Estructura del CSS

El diseño del sitio ha sido compuesto en modo **desktop-first**, por lo que para componer las páginas he usado la visualización de ordenador de escritorio. Los estilos del sitio se han definido en el archivo `desktop.css` sin ningún cualificador de **media query**.

Una vez diseñada la presentación del sitio web he abierto la página en la vista de diseño adaptado del navegador y he ajustado el ancho a un dispositivo tipo tablet, y a partir de ahí he creado el archivo `tablet.css` y he añadido los ajustes necesarios en los estilos para que la presentación del sitio sea la correcta en este tipo de pantallas. Para este tipo de dispositivo he usado la siguiente media query, que ajusta la aplicación de estilos a un áncho máximo:

```css
@media only screen and (max-width:768px)

```

Y por último he ajustado la vista de diseño adaptado al tamaño de los dispositivos móviles y he hecho los ajustes necesarios en el archivo `mobile.css para que en este tipo de dispositivo se presente correctamente el sitio web. Puesto que se trabajaba sobre los ajustes ya realizados para tabletas, no ha sido necesario ajustar tantos elementos, pero aún así los estilos que se han adaptado se han hecho bajo la siguiente **media query**:

```css
@media only screen and (max-width:480px)
```

Finalmente, en el archivo `main.css` se han incluido todas las hojas de estilo usando la característica de definición en cascada de CSS, de modo que ha quedado de la siguiente forma la definición de los estilos:

```css
@import './desktop.css';
@import './tablet.css';
@import './mobile.css';
```

Así, las definiciones para el sitio de escritorio se van adaptando para cada dispositivo de menor tamaño.

### Estructura del HTML

Para el HTML, como ya había comentado antes, he usado el plugin de PostHTML llamado PostHTML Include, el cual me permite definir unas plantillas que posteriormente son incluidas en otras páginas.

De este modo puedo definir unos archivos con contenido común que luego incluyo en las otras páginas, y así no necesito repetir código.

Los archivos de plantilla que he creado son los siguientes:

- footer.html, para el contenido del pie de la página.
- header.html, para el contenido de la cabecera, con el logo y el menú de navegación.
- html_head.html, para el contenido común de la sección `<head>` de la página HTML.

Posteriormente, la forma de incluir alguno de estos archivos es la siguiente:

```html
<include src="partials/header.html"></include>
```

En el ejemplo anterior se muestra cómo se incluye el archivo de la cabecera en una página.

## Enlaces

La página web puede consultarse en la siguiente dirección: XXX

Y el repositorio donde está alojado el código fuente de la página es el siguiente: XXX
