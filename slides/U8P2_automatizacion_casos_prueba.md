---
title: Automatización de Casos de Pruebas
theme: solarized
slideNumber: true
---

#### Ingeniería de Software
# Automatización de Casos de Pruebas
Created by <i class="fab fa-telegram"></i>
[edme88]("https://t.me/edme88")

---
<!-- .slide: style="font-size: 0.60em" -->
<style>
.grid-container2 {
    display: grid;
    grid-template-columns: auto auto;
    font-size: 0.8em;
    text-align: left !important;
}

.grid-item {
    border: 3px solid rgba(121, 177, 217, 0.8);
    padding: 20px;
    text-align: left !important;
}
</style>
## Temario
<div class="grid-container2">
<div class="grid-item">

### Automatización de Casos de Pruebas
* Tecnologías de Automatización
* Cypress
* Características de Cypress
* En estadísticas...
* Otras herramientas
* Extensiones
* npm
* Ejercicio básico

</div>
<div class="grid-item">

* PageObject
* Locadores

</div>
</div>

---

### Alcance de esta unidad
<!-- .slide: style="font-size: 0.80em" -->

Quedan **4 clases** y el programa no entra completo, asi que parte del material
de esta unidad no se desarrolla en el cursado.

<div class="grid-item">

Lo que **no se dicta en clase** esta completo en un mazo aparte:
**[Automatización de Casos de Pruebas: material de examen final](U8P2_automatizacion_casos_prueba_final.html)**

Es material de estudio y **se evalua en el examen final**.

</div>

Todo lo que sigue aca **si se dicta**, y es la base para el trabajo practico.

---

### Tecnologías de Automatización
Existe una gran variedad de tecnologías que permiten el desarrollo de pruebas automatizadas.

Entre las más usadas en el mercado encontramos:
* Selenium
* Cypress

![Tecnologias de Automatizacion](images/unidad8_automatizacion/selenium_cypress.png)

----

![Downloads](images/unidad8_automatizacion/downloads.jpg)

---
#### [Cypress](https://docs.cypress.io/)
Es un framework de testing moderno, fácil de aprender y de usar y que permite ejecutar pruebas sobre aplicaciones web.
Se emplea JavaScript.

Si bien lleve menos tiempo en el mercado que Selenium, ya cuenta con una gran comunidad, y una documentación muy extensa
y completa.

Además, tiene actualizaciones frecuentes, que agregan funcionalidades.

----

#### Cypress: Ventajas

![Cypress: ventajas](images/unidad8_automatizacion/ventajas-cypress.jpg)

----

#### Cypress: Características
<!-- .slide: style="font-size: 0.90em" -->
* Se toman **capturas de pantalla** o **videos** de forma muy sencilla mientras se ejecutan los tests, sin uso de otras 
dependencias.
* Durante la ejecución, al realizar cambios en el código, los tests se **auto-ejecutan** solos.
* Es muy sencillo **espiar** un servicio, para verificar los valores ó **entubarlo** y **modificarlo**.
* Las pruebas se ejecutan de manera **rápida** y sencilla.
* **Depuración** con herramientas como Chrome DevTools.
* Se realizarn **esperas automáticas**, sin necesidad de waits o sleeps.

----

#### Cypress: Cross-Browser

![Cypress: Cross Browser](images/unidad8_automatizacion/cross-browser.jpg)

---
### Otras Herramientas
En el proceso de automatización es fundamentar contar con las siguientes herramientas:
* **IDE**: Entorno de Desarrollo Integrado
* Versionado de Código
* Integración Continua

![Otras herramientas](images/unidad8_automatizacion/otras-herramientas.png)

---
### Herramientas para Cypress
* [Nodejs](https://nodejs.org/es)
* [Git](https://git-scm.com/)
* [VSC](https://code.visualstudio.com/)

----

### Plugin o Extensiones
Son componentes adicionales que se pueden instalar en el editor de código para agregar nuevas características,
funcionalidades y mejoras.

---

### Node Package Manager
**npm** es el manejador de paquetes de node, que permite descargar e instalar paquetes de JavaScript para usar en 
nuestro proyecto.

Todo proyecto **node** contiene un **package.json** donde se listan todas las librerías necesarias para el proyecto.

----

### npm init
Para crear el **package.json** por primera vez, se debe ejecutar el comando **npm init**.
Al ejecutar el comando, se permite ingresar:
* versión
* descripción
* entry point
* comandos de tests
* palabras clave
* repositorio de git
* autor
* licencia

---
### Page Object
Es un **patrón de diseño** que permite modelar el código y hacerlo más mantenible y utilizable (generalmente cuando hay cambios en la UI, suelen
ser de selectores, no tanto de funcionalidad, por lo que solo hay que actualizar el pageObject y no el test).

---
### Locadores

Un localizador es una query que busca y devuelve elementos específiicos del DOM (Document Object Model).

Orden de preferencia:
* Data-test o Data-cy
* ID
* Input Name
* Class Name
* Xpath

----

### Locadores: Modificadores
<!-- .slide: style="font-size: 0.80em" -->
* ```^```: Permite encontrar los elementos que en el nombre de la clase, id o atributo **empieza** con un determinado
texto. Ej: ```div[class^="ayuda_position"]```
* ```*```: Permite encontrar los elementos que en el nombre de la clase, id o atributo **contienen** un determinado
    texto. Ej: ```div[class*="user_name"]```
* ```$```: Permite encontrar los elementos que en el nombre de la clase, id o atributo **terminan** con un determinado
    texto. Ej: ```div[class$="summary_content"]```
* ```nth-child(X)```: Permite encontrar elementos en función de su posición entre un **grupo de hermanos**
Ej: ```th:nth-child(2)```
* ```nth-of-type(X)```: Permite encontrar elementos de un **tipo dado** en función de su posición entre un **grupo de hermanos**
  Ej: ```div:nth-of-type(1)```

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
