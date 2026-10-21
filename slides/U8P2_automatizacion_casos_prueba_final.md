---
title: Automatización de Casos de Pruebas - Material de examen final
theme: solarized
slideNumber: true
---

#### Ingenieria de Software
# Automatización de Casos de Pruebas
### Material de examen final

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

---

### Que es este mazo
<!-- .slide: style="font-size: 0.80em" -->

<div class="grid-item">

Estas filminas **no se dictan en clase** por razones de tiempo, pero
**entran en el examen final**.

Son la profundizacion de los temas que si se vieron en
**[Automatización de Casos de Pruebas](U8P2_automatizacion_casos_prueba.html)**. Conviene estudiarlas despues de ese mazo,
no antes.

</div>

Son **25 filminas**.

---

#### Ejercicio 1: Instalar NodeJs

1. Ingresar a https://nodejs.org/es
2. Descargar la versión recomendada
3. Realizar la instalación

---

#### Ejercicio 2: Instalar Git

1. Ingresar a https://git-scm.com/
2. Descargar git para el SO correspondiente
3. Realizar la instalación

---

#### Ejercicio 3: Instalar VSC

1. Ingresar a https://code.visualstudio.com/
2. Descargar VSC
3. Realizar la instalación

---

### Plugin o Extensiones
<!-- .slide: style="font-size: 0.90em" -->
Algunos plugin de utilidad son:
* **ESLint**: Es una herramienta de análisis estático que ayuda al proceso de **linting**. Es decir, realiza una revisión
del código para encontrar: errores de sintaxis, código poco intuitivo o difícil de mantener, uso de "malas prácticas", 
uso de estilos inconsistentes, entre otros.
* **Path Intellisense**: Realiza el autocompletado de rutas de archivos en el código. Reduce el riesgo de errores tipográficos.
* **Prettier**: Permite formatear automáticamente el código. Mejora la legibilidad del código.

---

### Plugin o Extensiones

* **Cypress Snippets**: Permite seleccionar tests rápidamente como .only para ejecutar solo uno. También agiliza escribir funciones.
* **Cypress Helper**: Agiliza procesos de autocompletado, go to definition, entre otros.
* **Better Comments**: Coloriza los comentarios para facilitar su lectura.

---

### Plugin o Extensiones

* **Bracket Pair Colorization Toggler**: Permite asignar colores diferentes a las llaves y paréntesis para facilitar la
lectura del código.
* **GitLens**: Permite ver con facilidad quien modificó las líneas de código y cuando (especialmente útil cuando se
trabaja en equipo).

---

#### Ejercicio 4: Instalar plugins en VSC

Instalar todos los plugins necesarios en el VSC:
* ESLint
* Path Intellisense
* Prettier
* Cypress Snippets
* Cypress Helper
* Better Comments
* Bracket Pair Colorization Toggler
* GitLens

---

#### Ejercicio 5: Instalar npm

1. Abrir el VSC
2. Ejecutar el comando **npm init** en la terminal
3. Verificar que el **package.json** se generó

---

#### Ejercicio 6: Instalar Cypress

1. Ejecutar el comando **npm install cypress** en la terminal
2. Verificar que el **package.json** se agregó cypress con la versión

---

#### Ejercicio 7: Inicializar Cypress
<!-- .slide: style="font-size: 0.90em" -->
1. Ejecutar el comando **npx cypress open** en la terminal
2. Seleccionar la opción **E2E testing**
3. Verificar los archivos nuevos que se generarán, y clickear en **Continue**
4. Seleccionar un navegador, y presionar **Start E2E testing in Chrome**
5. Click en **Scaffoolf example specs**
6. Click en **Okay, I got it!**
7. verificar que en el VSC se genero una carpeta llamada **Cypress** con 2 subcarperas> 1-getting-started y 2-advanced-examples
8. Seleccionar alguno de los tests-autogenerados de ejemplo para ejecutarlos.

---

### Page Object


Consiste en crear un objeto por cada conjunto de elementos significativos de la interfaz con la que interactuamos.

![Page Object Model](images/unidad8_automatizacion/POM.png)

---

### Page Object

* Representa componentes web
* Evita duplicación de código
* Automatizaciones mantenibles y fáciles de entender

![Page Object Model](images/unidad8_automatizacion/POM2.png)

---

### Page Object

Aunque el nombre sugiere representar una página de nuestra aplicación, si dentro de la página existen componentes, se
puede construir un page object de ese elemento para reutilizarlo.

---

### Page Object

Ejemplo: El header se repite a través de todas las páginas de esta web, entonces, en lugar de integrar los elementos
en el PageObject de la Home, es conveniente crear un PageObject a parte.
![Componentes](images/unidad8_automatizacion/componentes.png)

---

### Page Object: Modelo 1


En la parte superior se definen los locadores de los elementos, 
en la parte inferior las funciones que devuelven esos objetos.
![POM](images/unidad8_automatizacion/pom_modelo1.jpg)

---

### Page Object: Modelo 1


Para emplearlo en los tests, primero se importa, y luego se instancia el pageObject.
![POM](images/unidad8_automatizacion/pom_modelo1_uso.jpg)

---

### Page Object: Modelo 1

**Ventajas:**
Separación de la lógica del localizador (selector) y los métodos de interacción. Esto puede hacer que el código sea más
organizado y más fácil de mantener, especialmente si la página posee muchos elementos o acciones repetitivos.

**Desventajas**
Requiere crear una instancia del pageObject antes de utilizar los métodos. 

---

### Page Object: Modelo 2


Los locadores van dentro de los métodos.

![POM](images/unidad8_automatizacion/pom_modelo2.jpg)

---

### Page Object: Modelo 2


Para emplearlo en los tests, solo se debe importar.

![POM](images/unidad8_automatizacion/pom_modelo2_uso.jpg)

---

### Page Object: Modelo 2

**Ventajas:**
Se pueden emplear los métodos directamente sin necesidad de crear una instancia de la clase. Los métodos están 
disponibles globalmente para su uso directo, lo que puede resultar en un código más conciso. 

**Desventajas**
Se puede volver más complicado si hay muchos elementos o acciones repetitivas en la página. Se podría terminar repitiendo
el mismo selector en múltiples métodos.

---

### Locadores: Data-test


![Locadores: Data-test](images/unidad8_automatizacion/locator-datatest.jpg)

---

### Locadores: ID


![Locadores: ID](images/unidad8_automatizacion/locator-id.jpg)

---

### Locadores: Name


![Locadores: Name](images/unidad8_automatizacion/locator-name.jpg)

---

### Locadores: Class


![Locadores: Class](images/unidad8_automatizacion/locator-class.jpg)

---

### Locadores: Xpath


![Locadores: xpath](images/unidad8_automatizacion/locator-xpath.jpg)


---
## Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
