---
title: Unidad 2 - Repaso integrador
theme: solarized
slideNumber: true
---

#### Ingeniería de Software
# Unidad 2
## Repaso integrador
Procesos de Software · Herramientas CASE

---
<!-- .slide: style="font-size: 0.75em" -->
<style>
.grid-item {
    border: 3px solid rgba(121, 177, 217, 0.8);
    padding: 20px;
    text-align: left !important;
}

.exercise-slide {
  border: 2px dashed #b58900;
  border-radius: 12px;
  padding: 20px;
}
</style>

## Cómo funciona

Catorce preguntas para pensar **en voz alta**. Ninguna se responde con una definición: todas
obligan a relacionar dos o más temas de la unidad.

* No hay una única respuesta correcta. Lo que se evalúa es **cómo se justifica**.
* Si la respuesta sale en diez segundos, probablemente no se entendió la pregunta.
* Vale cambiar de opinión a mitad de camino. Eso también es aprender.

<div class="grid-item">

**Bloque A** — Los modelos de proceso (1 a 4)
**Bloque B** — Actividades, cambio y prototipado (5 a 8)
**Bloque C** — Herramientas CASE (9 a 11)
**Bloque D** — Cruzando todo (12 a 14)

</div>

---
## Bloque A
### Los modelos de proceso

---

### 1
<!-- .slide: class="exercise-slide" -->

Las cuatro actividades fundamentales —especificación, diseño e implementación, validación y
evolución— **están presentes en todos los modelos de proceso**.

Entonces, si todos hacen lo mismo, **¿qué es exactamente lo que cambia de un modelo a otro?**

<!--
Adonde llevar la discusión: no cambia QUÉ se hace, cambia CUÁNDO y CUÁNTAS VECES.
En cascada las cuatro actividades van en secuencia y una sola vez; en incremental se
intercalan y se repiten en cada incremento; en espiral se repiten pero organizadas
alrededor del riesgo.
Si alguien dice "cambian las actividades", volver a la slide de las cuatro actividades:
son las mismas. Lo que cambia es el ORDENAMIENTO, que es justamente la definición de
"proceso" que dimos al principio de la unidad.
-->

---

### 2
<!-- .slide: class="exercise-slide" -->

El cambio es **inevitable** en todo proyecto grande de software. Lo dijimos varias veces.

Y sin embargo, el modelo de cascada —que es el peor para absorber cambios— **se sigue usando**.

**¿Por qué? ¿En qué situación alguien elige, a conciencia, el modelo que peor tolera el cambio?**

<!--
Respuesta esperada: cuando el costo de equivocarse supera al costo de rehacer.
Aviónica, dispositivos médicos, señalización ferroviaria: hay un auditor externo que exige
trazabilidad documento por documento, y los requisitos vienen fijados por normativa, no por
un cliente que puede cambiar de opinión.
Segundo argumento: coordinación. Con equipos grandes y distribuidos, la cascada da un
marco común que la comunicación informal no puede sostener.
Repregunta útil: "¿y si el cliente igual cambia de opinión?" -> ahí aparece por qué esos
proyectos invierten tanto en la etapa de requerimientos.
-->

---

### 3
<!-- .slide: class="exercise-slide" -->

Un equipo dice: *"Nosotros trabajamos con desarrollo incremental, así que entregamos software
funcionando cada dos semanas."*

**¿Está bien usado el término? ¿Qué le corregirías?**

<!--
El equipo está describiendo ENTREGA incremental, no desarrollo incremental.
- Desarrollo incremental: cómo se CONSTRUYE (puede ser todo interno, invisible para el cliente).
- Entrega incremental: cómo se LIBERA al usuario.
Se puede hacer desarrollo incremental sin entregar nada hasta el final.
Repregunta: "¿se puede hacer entrega incremental sin desarrollo incremental?" -> es muy
difícil, pero el punto es que no son sinónimos y que la confusión es constante en la industria.
-->

---

### 4
<!-- .slide: class="exercise-slide" -->

El modelo **evolutivo** y el modelo **en espiral** son los dos iterativos.

**¿Cuál es la diferencia real entre iterar para descubrir requisitos e iterar para reducir
riesgos? Dame un proyecto donde uno sirva y el otro no.**

<!--
Evolutivo: itera porque NO SE SABE QUÉ construir. El motor de cada ciclo es el feedback
del usuario sobre un prototipo.
Espiral: itera porque HAY RIESGOS que despejar. El motor de cada ciclo es el análisis de
riesgo, y puede haber ciclos que no producen nada visible para el usuario.
Ejemplo donde sirve evolutivo y no espiral: la app del municipio, donde nadie sabe qué
quiere. El riesgo técnico es bajo; el riesgo es construir lo que nadie usa.
Ejemplo inverso: migrar historias clínicas de papel. Se sabe perfectamente qué hay que
construir; lo que puede fallar es la migración de datos, la adopción, la conectividad.
-->

---
## Bloque B
### Actividades, cambio y prototipado

---

### 5
<!-- .slide: class="exercise-slide" -->

Vimos dos estrategias frente al cambio: **evitarlo** (anticiparlo para no rehacer) y
**tolerarlo** (diseñar para que rehacer sea barato).

Un equipo decide invertir tres semanas en un prototipo antes de programar.

**¿Está evitando o tolerando el cambio? ¿Y qué pasa si además trabaja en incrementos?**

<!--
El prototipo es EVITAR el cambio: se anticipa para no rehacer después.
Trabajar en incrementos es TOLERAR: si el cambio llega igual, solo hay que alterar un
incremento.
El punto de la pregunta: no son excluyentes, y los procesos reales combinan las dos.
Repregunta: "¿cuál cuesta más?" -> evitar cuesta tiempo por adelantado y falla si el
cliente no sabe lo que quiere; tolerar cuesta disciplina técnica sostenida (refactorización,
pruebas automatizadas) que los equipos abandonan cuando están apurados.
-->

---

### 6
<!-- .slide: class="exercise-slide" -->

Un prototipo desechable, por definición, **se tira**.

Si el código no sobrevive, **¿qué es exactamente lo que el equipo se lleva de esas semanas de
trabajo? ¿Y cómo se justifica esa inversión ante un cliente que ve que "tiraron todo"?**

<!--
Lo que se conserva: conocimiento. Requisitos que quedaron claros, decisiones de interfaz
validadas, flujos de pantalla, casos de prueba que surgieron al probarlo, y sobre todo la
lista de cosas que el cliente creía querer y resultó que no.
La justificación ante el cliente: el prototipo no es el producto, es el instrumento para
saber qué producto construir. Tirarlo es más barato que descubrir el error después de
haber construido el sistema de producción.
Conectar con la pregunta 5: el prototipo es la forma más pura de "evitar el cambio".
-->

---

### 7
<!-- .slide: class="exercise-slide" -->

La ingeniería orientada a **reutilización** promete menos tiempo, menos costo y menos riesgo
técnico.

**¿Cuál es el precio que se paga? ¿Y en qué etapa del proceso aparece ese precio, que en los
otros modelos no existe?**

<!--
El precio: se heredan las limitaciones de cada componente. Si la plataforma no permite algo,
el requisito se negocia o se paga muy caro.
La etapa que no existe en los otros modelos: "modificación de requerimientos", el paso 3
del modelo. Es el único proceso donde los REQUISITOS se ajustan a la SOLUCIÓN disponible,
y no al revés.
Repregunta fuerte: "¿eso no viola todo lo que dijimos sobre ingeniería de requerimientos?"
Discusión honesta: sí, es una tensión real. Se acepta porque el ahorro compensa, pero hay
que ser consciente de que se está negociando con el cliente sobre lo que puede tener.
-->

---

### 8
<!-- .slide: class="exercise-slide" -->

*"La validación es la etapa donde se comprueba que el sistema hace lo que el cliente quiere."*

**En el modelo de cascada, ¿cuándo ocurre eso? ¿Y en el incremental?**

**¿Qué consecuencia práctica tiene esa diferencia sobre el costo de un error de
especificación?**

<!--
Cascada: la validación con el cliente ocurre al final, después de integrar. Un error de
especificación cometido en el mes 1 se descubre en el mes 10.
Incremental: se valida en cada incremento. El mismo error se descubre en semanas.
La consecuencia: el costo del error crece con el tiempo que pasa sin detectarse. Conectar
con la curva de costo del cambio que se ve en la unidad de ágil.
Matiz importante para no simplificar: eso NO hace al incremental siempre mejor. En un
sistema donde un error mata gente, se prefiere gastar diez meses en verificar antes de
construir. La pregunta es siempre qué se está optimizando.
-->

---
## Bloque C
### Herramientas CASE

---

### 9
<!-- .slide: class="exercise-slide" -->

Las clasificaciones de herramientas CASE que vimos son de los años 80 y 90: Upper y Lower CASE,
IPSE, toolkits y workbenches.

**¿Siguen sirviendo? Ubicá GitHub en las tres clasificaciones y contame qué te costó.**

<!--
Por cobertura: se acerca a I-CASE, porque cubre desde la gestión del trabajo hasta el
despliegue. Pero no hace análisis ni diseño: no es I-CASE en el sentido clásico.
Por integración: entorno integrado, el heredero directo del IPSE.
Por función: soporte + gestión de proyectos + integración y prueba. Cruza tres.
Lo que debería costar: que ninguna casilla le queda bien. Y ese es el aprendizaje: las
taxonomías describen bien el panorama de su época. No están mal, están fechadas.
Si nadie se traba, insistir con un asistente de IA, que rompe la clasificación todavía más.
-->

---

### 10
<!-- .slide: class="exercise-slide" -->

Uno de los objetivos declarados de las herramientas CASE es **estandarizar la documentación**.

Uno de los valores del Manifiesto Ágil es **software funcionando por sobre documentación
extensiva**.

**¿Se contradicen? ¿Puede un equipo ágil usar herramientas CASE sin traicionar sus principios?**

<!--
No se contradicen, y el malentendido es muy común.
El Manifiesto no dice "no documentar": dice qué priorizar cuando hay que elegir. Un equipo
ágil documenta, pero documenta lo que se usa.
Además: la mayoría de las herramientas que usa un equipo ágil SON herramientas CASE
(el IDE, Git, la integración continua, las pruebas automatizadas, Jira). Lo que evitan no
son las herramientas, es la documentación que nadie lee.
Buen cierre: la integración continua y las pruebas automatizadas son herramientas CASE
que hacen la documentación innecesaria, porque el código verificado cuenta la verdad.
-->

---

### 11
<!-- .slide: class="exercise-slide" -->

Una desventaja de las herramientas CASE es la **dependencia de la metodología**: el equipo
termina adaptándose a la herramienta en lugar de al revés.

**Dame un ejemplo concreto que hayas visto o sufrido. ¿Cómo te darías cuenta de que le está
pasando a tu equipo?**

<!--
Ejemplos que suelen salir: un tablero de Jira con estados que no reflejan cómo trabaja el
equipo, pero nadie los cambia; diagramas que se dibujan "porque la herramienta los pide";
campos obligatorios que se completan con cualquier cosa para poder avanzar.
La señal de alarma: cuando alguien dice "hacemos esto porque la herramienta lo pide" en
lugar de "porque nos sirve". O cuando existe un paso del proceso que solo existe para
alimentar a la herramienta.
Conectar con el ejercicio de los diagramas UML que nadie abre hace ocho meses.
-->

---
## Bloque D
### Cruzando todo

---

### 12
<!-- .slide: class="exercise-slide" -->

**¿Cambia el conjunto de herramientas según el modelo de proceso que elijas?**

Armá mentalmente el *toolchain* de dos equipos: uno que trabaja en **cascada** sobre un sistema
regulado, y otro que hace **entrega incremental** de una app de consumo.

**¿En qué se parecen y en qué no?**

<!--
Se parecen más de lo que los alumnos esperan: los dos usan IDE, control de versiones y
pruebas. El núcleo es el mismo.
Diferencias reales:
- Cascada regulada: mucho peso en herramientas de documentación, trazabilidad de
  requisitos, gestión de la configuración y verificación formal. El auditor necesita ver
  el rastro de cada requisito hasta su prueba.
- Entrega incremental: mucho peso en integración continua, despliegue automatizado,
  observabilidad y feedback de usuarios en producción.
La conclusión que interesa: el proceso no determina las herramientas, determina DÓNDE se
pone el esfuerzo. Ambos equipos versionan; solo uno necesita demostrárselo a un auditor.
-->

---

### 13
<!-- .slide: class="exercise-slide" -->

Los asistentes de IA generan código, escriben pruebas, documentan y refactorizan.

**Si una herramienta hace todo eso, ¿cambia el modelo de proceso que conviene elegir? ¿O el
proceso es independiente de las herramientas?**

<!--
No hay respuesta cerrada; el objetivo es que argumenten en las dos direcciones.
A favor de que sí cambia: si prototipar cuesta horas en lugar de semanas, los enfoques
evolutivos y de descarte se vuelven mucho más baratos, y "evitar el cambio" mediante
prototipos se hace más atractivo frente a "tolerarlo".
A favor de que no cambia: el proceso responde a la naturaleza del problema —incertidumbre,
riesgo, regulación—, no a la velocidad de tipeo. Una auditoría de aviónica no acepta menos
trazabilidad porque el código se escribió más rápido.
Punto clave a rescatar: la IA acelera la CONSTRUCCIÓN, no la comprensión del problema. Y el
modelo de proceso se elige por lo segundo. Si alguien llega solo a esto, la pregunta cumplió.
-->

---

### 14
<!-- .slide: class="exercise-slide" -->

Cierre.

**Si tuvieras que explicarle a alguien que no cursó esta materia por qué "no existe el mejor
modelo de proceso", ¿qué le dirías en tres oraciones?**

**Y la repregunta incómoda: ¿eso significa que da igual cuál elegir?**

<!--
Lo que se busca: que puedan sintetizar sin caer en el relativismo.
La primera parte suele salir: cada modelo optimiza algo distinto —previsibilidad, velocidad,
absorción del cambio, control del riesgo— y qué conviene depende de qué se esté construyendo,
para quién, con qué restricciones.
La repregunta es la importante. NO da igual: elegir mal tiene consecuencias concretas y caras.
"No hay un modelo correcto" no significa "todos sirven igual", significa que la decisión
depende del contexto y hay que saber justificarla. Un equipo que elige cascada para una
startup, o ágil para un marcapasos, se equivocó, y se puede explicar por qué.
-->

---

## Para llevarse

<!-- .slide: style="font-size: 0.85em" -->

Tres ideas que atraviesan toda la unidad:

1. **Lo que cambia entre modelos no es qué se hace, sino cuándo y cuántas veces.**
2. **Todo modelo optimiza algo y paga con otra cosa.** No hay uno mejor; hay uno más adecuado
   a un contexto, y esa elección se justifica.
3. **Las herramientas no definen el proceso.** Definen dónde se pone el esfuerzo, y qué tan
   caro resulta equivocarse.

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
