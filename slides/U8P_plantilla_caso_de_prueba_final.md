---
title: Casos de Pruebas - Material de examen final
theme: solarized
slideNumber: true
---

#### Ingenieria de Software
# Casos de Pruebas
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
**[Casos de Pruebas](U8P_plantilla_caso_de_prueba.html)**. Conviene estudiarlas despues de ese mazo,
no antes.

</div>

Son **15 filminas**.

---

## Plantilla de Casos de Pruebas
<!-- .slide: style="font-size: 0.80em" -->
2. **Documentación:** Los CP actúan como documentación detallada de cómo se debe probar una funcionalidad. Esto es útil 
para los equipos de desarrollo y pruebas, ya que proporciona instrucciones claras sobre qué se debe probar y cómo hacerlo.
3. **Automatización:** Los CP son esenciales para la automatización de pruebas. Pueden ser traducidos a scripts de 
pruebas automatizadas que permiten ejecutar las pruebas de forma repetitiva y consistente, lo que ahorra tiempo y 
recursos a largo plazo.
4. **Validación de cambios:** Cuando se realizan cambios en una aplicación o sistema, los CP existentes pueden utilizarse 
para verificar que las modificaciones no hayan introducido nuevos errores y que las funcionalidades existentes sigan 
funcionando como se espera.

---

## Plantilla de Casos de Pruebas
<!-- .slide: style="font-size: 0.80em" -->
5. **Reproducción de errores:** Los CP permiten a los equipos de desarrollo y pruebas reproducir errores informados por 
los usuarios. Esto facilita la identificación y corrección de problemas específicos.
6. **Estándares de calidad:** Los CP son una parte fundamental de los estándares de calidad en el desarrollo de software. 
Ayudan a mantener la coherencia en las pruebas y a garantizar que todas las funcionalidades se evalúen de manera adecuada.
7. **Mejora de la confiabilidad:** Al realizar pruebas sistemáticas y controladas, se mejora la confiabilidad y 
estabilidad del software, lo que reduce la probabilidad de fallos inesperados y garantiza una mejor experiencia para los usuarios.

---

### Identificador de caso de uso e Identificador de la prueba
<!-- .slide: style="font-size: 0.90em" -->
Un identificador de caso de uso puede ser una etiqueta alfanumérica única o un número, y a menudo se organiza de manera 
estructurada para reflejar la jerarquía o el flujo de trabajo de un sistema. Por ejemplo, podría tener un formato como 
"CU-001" para el primer caso de uso de un sistema, "CU-002" para el segundo, y así sucesivamente. Y de manera similar
para los tests "TST-001", "TST-002".

La elección del formato y la convención de nomenclatura dependen de las prácticas específicas de documentación adoptadas 
por el equipo de desarrollo.

---

### Nombre del Caso de Uso
<!-- .slide: style="font-size: 0.80em" -->
Los principales propósitos del nombre son:
* **Identificación:** El nombre del caso de uso es una forma rápida de identificar un CU particular dentro de la 
documentación del sistema. Proporciona un nombre único y distintivo que facilita la referencia y la comunicación entre 
los miembros del equipo.
* **Clarificación del Propósito:** El nombre del CU proporciona una descripción concisa del propósito o la funcionalidad 
que el caso de uso representa. Esto ayuda a responder la pregunta "¿Qué hace este caso de uso?" sin necesidad de una 
descripción detallada.

---

### Nombre del Caso de Uso
<!-- .slide: style="font-size: 0.80em" -->
* **Comunicación Efectiva:** El nombre del CU actúa como un medio de comunicación eficiente al proporcionar un resumen 
rápido y legible de la funcionalidad que se está abordando.
* **Búsqueda y Referencia:** Permite a los miembros del equipo buscar y hacer referencia rápidamente a un CU específico 
cuando sea necesario.
* **Contextualización:** Ayuda a poner en contexto el CU en el flujo general de trabajo o el comportamiento del sistema. 
El nombre debe ser lo suficientemente descriptivo para que otros puedan entender su función sin tener que leer toda la 
documentación detallada.

---

### Informador

Se especifica quién es la persona o el equipo que documentó la prueba a realizar. 

---
### Responsable

Se especifica quién es la persona o el equipo encargado de ejecutar la prueba. Es importante para asignar la 
responsabilidad de ejecutar y documentar la prueba.

---
### Fecha de la Prueba

Se registra cuándo se realizó la prueba. Esto es crucial para llevar un registro de cuándo se ejecutó el caso de prueba 
y para rastrear el progreso del proceso de pruebas.
En algunos sistemas habitual tener múltiples campos tipo fecha: Fecha de Creación, Fecha de Última Modificación, FechaS
de ejecuciones, etc.

---
### Detalle de lo que se Prueba

Este campo se enfoca en los aspectos específicos o las características que se están probando en este caso de prueba en 
particular. Ayuda a definir claramente el alcance de la prueba.

---
### Funciona / No Funciona / Requiere mantenimiento perfectivo

Este campo indica si el caso de prueba funciona según lo esperado, no funciona (en caso de fallo) o si se requiere 
realizar ajustes o mejoras en el software (mantenimiento perfectivo).

---
### Comentarios

Los comentarios permiten agregar información adicional, aclaraciones o detalles relevantes relacionados con la ejecución 
de la prueba. Pueden ser útiles para proporcionar contexto adicional o explicar situaciones específicas.

---

![Jira 2](images/unidad8/jira2.jpg)


---

![Jira Ejemplo 1](images/unidad8/jira-ejemplo1.jpg)


---

![Jira Ejemplo 2](images/unidad8/jira-ejemplo2.jpg)


---

![Jira Ejemplo 3](images/unidad8/jira-ejemplo3.jpg)



---
## Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
