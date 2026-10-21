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
**[Automatización de Casos de Pruebas](U8P3_gherkin.html)**. Conviene estudiarlas despues de ese mazo,
no antes.

</div>

Son **9 filminas**.

---

### Gherkin


![Gherkin](images/unidad8_automatizacion/gherkin.jpg)

---

### Cucumber

Los **objetivos** principales que se deben seguir:
* Los escenarios deben ser pensados como documentación.
* Los escenarios deben permitir la colaboración con gente de negocio (PO, BA)
* Los escenarios deben permitir la evolución del producto.

---

### Cucumber

Los proyectos con cucumber tienen principalmente 3 archivos:
* **nombreTests.feature**: Describen en Gherkin el comportamiento, empleando las palabras Givem, When, Then, etc.
* **nombreStep.js** Emplando Js se programa que acciones de código se deben realizar en cada paso.
* **nombrePage.js** Se colocan los locadores dentro de métodos que permitan obtenerlos y manipularlos con mayor facilidad.

---

#### BRIEF: Lenguaje Comercial

* Las palabras usadas deben venir del dominio comercial. No debe haber ambiguedades.
* Un error común es emplear palabras que tienen diferente significado en diferentes contextos.

---

#### BRIEF: Datos Reales

* Los ejemplos deben usar datos reales y contretos, para ayudar a entender el contexto.

---

#### BRIEF: Revelación de intención

* En el escenario debe quedar claro cuál es la intención, que se está tratando de lograr.

---

#### BRIEF: Esencial

* Cualquier paso que no contribuya a alcanzar el propósito principal debe elimianrse. Si son importantes, deben cubrirse 
por otros esenarios que ilustren otras reglas.
* Un error común es incluir demasiados detalles.

---

#### BRIEF: Enfocado

* Un escenario debería centrarse en una sola regla.

---

#### BRIEF: Breve

* Los escenarios no deberían tener más de 5 líneas, haciendo que sen fáciles de leer y entender.


---
## Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
