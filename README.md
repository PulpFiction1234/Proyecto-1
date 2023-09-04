# Proyecto 1

![](https://media.discordapp.net/attachments/1117631627741384845/1136002963928785049/Diseno_sin_titulo_1.png)

## 1. Intro

##### Este repositorio es el proyecto solicidado por el staff de UDD Bootcamps DWFS
**PROYECTO 1: Landing de Negocio** 
##### a continuacion podran ver el proceso de desarrollo ocupado para esta pagina donde explicaremos algunos pasos y funcionalidad.


------------

## 2. Desarrollo html, css y js

##### Como primer paso de este proyecto se creo un archivo html:5, en el cual debiamos cumplir con ciertos estandares y secciones para tener un proyecto optimo.

![](https://raw.githubusercontent.com/UDDBootcamp/BOOT-M1-SEM4-PROY1/main/demo/layout.png?token=GHSAT0AAAAAACFMATL3RCQ4KG3BTENMQQAEZHVFYJQ)
###### -  Desarrollar prototipado simple.
###### -  Aplicar en todo el sitio HTML semántico de estándar no.5 (HTML5).
###### -  Aplicar tipos de selectores en CSS.
###### -  Sección Header, Jumbotron, footer
###### -  Sección de registro de usuario
###### - Sección artículos o catálogo
###### - Responsive Web Design (Vista en móviles con uso de media queries)



##### Sabiendo esto comence a trabajar en cada apartado por separado, creando cada uno de ellos en mi archivo html5 y asignandole clases a las etiquetas para asi poder trabajar en sus estilos, desarrollando una seccion a la vez en mis archivos html, css y js.
```html
<header>
        <button class="menu-icon" onclick="toggleMenu()">
            <i class="fa-solid fa-bars"></i>
        </button>
        <nav class="container-nav">
            <ul class="menu-left">
                <li class="li-menu-left"><a href="">Inicio</a></li>
                <li class="li-menu-left"><a href="productos.html">Productos</a></li>
                <li class="li-menu-left"><a href="">Nosotros</a></li>
                <li class="li-menu-left"><a href="">Contacto</a></li>
            </ul>
            <ul class="menu-right">
                <li class="li-menu-right"><a href="registro.html"><i class="fa-solid fa-user"></i></a></li>
            </ul>
        </nav>
    </header>
```
##### Una vez creado mi html y creada la primera seccion cree archivo css el cual tuve que linkear a mi archivo html .

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css/index.css">

```

##### En este archivo se le dieron selectores y estilos a cada una de nuestras secciones dentro del archivo html utilizando clases y etiquetas.
```css
body {
    background-color: #8C2020;
}

p {
    font-size: 19px;
}

/* Header */
.menu-icon {
    display: none;
    font-size: 24px;
    background-color: transparent;
    border: none;
    cursor: pointer;
    color: #FFF9C9;
}

.container-logo {
    display: flex;
    justify-content: center;
    margin-top: 10px;
}

.container-nav {
    width: 100%;
    height: 90px;
    display: flex;
}
```
##### Utilizando estos dos archivos cree mi pagina base (en formato para computadora) creando cada seccion y siguiendo los pasos ya explicados. 
##### Una vez terminada la pagina en formato de computadora se me solicitaba tambien tener un formato para dispositivos moviles, para esto cree un segundo archivo css el cual tuve que linkear tambien a mi html.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css/index.css">
    <link rel="stylesheet" href="css/media.css">
```
##### En este archivo lo que hice fue utilizar una propiedad llamada @media a la cual se le dieron ciertos requisitos de tamaño para que fuese ejecutada.

```css
@media screen and (max-width: 768px) 
```

##### Luego de darle nuestros requisito para que ser ejecutada comence a trabajar en los estilos para mi formato movil, haciendo que la pagina tomase otra forma cuando mi pantalla fuese mas pequeña a 768px

```css
@media screen and (max-width: 768px) {

    p {
        font-size: 19px;
    }

    .menu-left,
    .menu-right {
        display: none;
        flex-direction: column;
    }

    .li-menu-left,
    .li-menu-right {
        margin: 10px 0;
        border-bottom: solid 1px #E7E7E4;
    }

```
##### Gracias a este archivo pude hacer que mi barra de navegacion se convirtiera en un menu formato hamburguesa y me ayudo a ordernar mis secciones para que fuese mas comodo al momento de ingresar desde el movil.

##### Luego de esto cree mi archivo js, el cual fue linkeado mediante un script en mi archivo html.
```html
    </footer>
    <script src="js/index.js"></script>
</body>
</html>
```
##### En este archivo utilice una funcion para hacer que mi menu fuese desplegable al momento de clickearlo desde un movil.
```javascript
function toggleMenu() {
    console.log("Función toggleMenu() ejecutada.");
    var containerNav = document.querySelector('.container-nav');
    containerNav.classList.toggle('menu-active');
}
```
##### Ya con esto termine de trabajar en mi pagina principal y comence a crear la pagina para registro de usuario creando un nuevo archivo html el cual fue linkeado mediante un HREF a su respectivo icono dentro de mi html principal.
```html
 <ul class="menu-right">
    <li class="li-menu-right"><a href="registro.html"><i class="fa-solid fa-user"></i></a></li>
 </ul>
```
##### Para esta pagina copie todo el codigo de mi barra de navegacion y mi footer (html, css y js) para mantener un orden dentro mi sitio web.
##### Dentro de esta pagina adjunte un pequeño formulario sacado de boostrap, para poder utilizar boostrap en mi pagina tuve que linkear las librerias a mi archivo html.
```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-4bw+/aepP/YC94hEpVNVgiZdgIC5+VKNBQNGCHeKRQN+PtmoHDEXuppvnDJzQIu9" crossorigin="anonymous">

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js" integrity="sha384-HwwvtgBNo3bZJJLYd8oVXjrBZt8cqVSpeBNS5n7C8IVInixGAoxmnlMuBnhbgrkm" crossorigin="anonymous"></script>

```
![](https://scontent.xx.fbcdn.net/v/t1.15752-9/372419919_1031233591647883_6495145689122495544_n.png?stp=dst-png_p403x403&_nc_cat=105&ccb=1-7&_nc_sid=aee45a&_nc_ohc=MEnAaHXU_34AX_1ga0j&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.xx&oh=03_AdQyp8hr5bRu8T8lJFZaSJRXtxIL87hIOqc-ODjpjTw2qQ&oe=651CC26C)

##### Ya con esto completado di por terminado mi proyecto landing el cual fue enfocado unicamente en front end.

## 3. Librerias utilizadas

###### - https://fontawesome.com/search?q=menu&o=r
###### - https://fonts.google.com/
###### - https://getbootstrap.com/

