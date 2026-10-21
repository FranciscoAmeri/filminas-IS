---
title: Automatización de Casos de Pruebas
theme: solarized
slideNumber: true
---

#### Ingeniería de Software
# Automatización de Casos de Pruebas 2
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
* BDD
* Gherkin

</div>
<div class="grid-item">

*

</div>
</div>

---

### Alcance de esta unidad
<!-- .slide: style="font-size: 0.80em" -->

Quedan **4 clases** y el programa no entra completo, asi que parte del material
de esta unidad no se desarrolla en el cursado.

<div class="grid-item">

Lo que **no se dicta en clase** esta completo en un mazo aparte:
**[Automatización de Casos de Pruebas: material de examen final](U8P3_gherkin_final.html)**

Es material de estudio y **se evalua en el examen final**.

</div>

Todo lo que sigue aca **si se dicta**, y es la base para el trabajo practico.

---

### BDD
Significa **Desarrollo Dirigido por Comportamiento**, y es una evolución del TDD (Desarrollo Dirigido por Pruebas).

Consiste en describir el comportamiento antes de escribir el código fuente.

Las pruebas verifican que el comportamiento del código es correcto desde el punto de vista del negocio.

----

![BDD](images/unidad8_automatizacion/bdd.jpg)

----

![BDD](images/unidad8_automatizacion/bdd2.jpg)

----

### BDD: Ventajas
Emplea lenguaje ubicuo, **Gherkin**, lenguaje semiformal entendido por desarrolladores y personal NO técnico.

Combina aspectos técnicos y de negocio: los requisitos de negocio forman parte del proceso de desarrollo.

---
### Gherkin
Es un lenguaje fácil de leer, entender y escribir; con él vamos a describir las funcionalidades definiendo el 
comportamiento del software, sin entrar en su implementación.

La **documentación** forma parte de los tests.

----

### Gherkin
<!-- .slide: style="font-size: 0.80em" -->
Necesitamos conocer **5** palabras:
* **Feature** Indica el nombre de la funcionalidad que vamos a probar. Debe ser un título claro y explícito.
* **Scenario** Describe cada escenario que vamos a probar.
* **Given** Provee contecto para el escenario en que se va a ejecutar el test, prerequisitos. Incluye los pasos necesarios
para poner al sistema en el estado que se desea probar.
* **When** La interacción del usuario que acciona la funcionalidad que deseamos testear.
* **Then** Especifica el resultado esperado en el test. Observamos los cambios en el sistema y vemos si son los deseados.

---
### Cucumber
Es una herramienta para implementar metodologías como el Behaviour Driven Development BDD, que permite ejecutar 
descripciones funcionales en texto plano.

Las descipciones funcionales se escriben en Gherkin.

----

### Cucumber
Es una gran herramienta para mantener en un solo lugar:
* **Living Documentation:** Es una forma de definir las características de forma tal que puedan ser entendidas por los 
equipos comerciales y técnicos.
* Los **tests automatizados**
* **Especificaciones Ejecutables:** Porque cada paso en el escenario está vinculado a un fragmento de código que realiza
esa acción.

---

### Ejercicio: Cypress+Cucumber
1. Ingresa a git https://github.com/edme88/cypressCucumberPIL/tree/main
2. Clona el repositorio
3. Ejecutar el comando **npx cypress open**
4. Ejecuta algún test

---

### Gherkin - BRIEF
Los siguientes principios permiten alcanzar estas metas:
* Lenguaje Comercial (Business language)
* Datos reales (Real data)
* Revelación de intención (Intention revealing)
* Esencial
* Enfocado (Focused)
* Breve (brief)

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
