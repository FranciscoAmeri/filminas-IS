---
title: Desarrollo Ágil de Software
theme: solarized
slideNumber: true
---

# Ingeniería de Software
## Desarrollo Ágil de Software
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

### Desarrollo Ágil de Software
* Definición
* Manifiesto Ágil
* Aplicabilidad
* Problemas
* Mantenimiento
* Desarrollo Guiado por Plan
* Cuestiones técnicas, humanas y organizacionales
* Programación Extrema
* Escenarios de Requerimientos
* Refactorización
* Pruebas

</div>
<div class="grid-item">

* Automatización de Pruebas
* Programación en pares
* Gestión Ágil
* Scrum
* Ciclo Sprint
* Beneficios de Scrum
* Desarrollo de Sistemas Grandes
</div>
</div>

---
### Desarrollo ágil de software
<!-- .slide: style="font-size: 0.80em" -->
* El rápido desarrollo y la entrega son ahora los
requisitos más importantes para los sistemas de software
  * Los requisitos de las empresas cambian rápidamente y es
prácticamente imposible producir un conjunto de requerimientos de software estable.
  * El Software tiene que evolucionar rápido para reflejar los cambios en las necesidades del negocio.

---
### Desarrollo ágil de software
<!-- .slide: style="font-size: 0.90em" -->
Aunque existen muchos enfoques para el desarrollo ágil, todos comparten ciertas características:
1. Especificación, diseño e implementación están entrelazados
2. El sistema se desarrolla en diferentes versiones. Se pueden proponer cambios y nuevos requerimientos en versiones posteriores.
3. Las interfaces del usuario se desarrollan a menudo utilizando un IDE y herramientas gráficas
4. Se emplea desarrollo incremental
5. Se involucra al cliente en el desarrollo
6. Poca documentación

---
### Métodos Ágiles
<!-- .slide: style="font-size: 0.80em" -->
* La insatisfacción con los gastos involucrados en los métodos
de diseño de software de los años 1980 y 1990 dieron lugar a la
creación de métodos ágiles. Estos métodos:
  * Se enfocan en el código en lugar del diseño
  * Se basan en un enfoque iterativo para el desarrollo de software
  * Tienen la intención de ofrecer software de trabajo de forma rápida y
evolucionar rápidamente para satisfacer las cambiantes necesidades.
* El objetivo de los métodos ágiles es reducir los gastos
generales del proceso de software (por ejemplo, limitando la
documentación) y ser capaces de responder rápidamente a las
necesidades cambiantes sin rehacer trabajo de manera
excesiva

---

#### Cambio de los costos como función del tiempo transcurrido en el desarrollo

![Costo del Cambio](images/unidad4/costo-del-cambio.png)

---
#### Manifiesto Ágil: Valores

![Valores Agile](images/unidad4/valores-agile.png)

----

### Los 4 valores del Manifiesto Ágil
<!-- .slide: style="font-size: 0.80em" -->

> Estamos descubriendo formas mejores de desarrollar software tanto por nuestra propia
> experiencia como ayudando a terceros. A través de este trabajo hemos aprendido a valorar:

1. **Individuos e interacciones** sobre procesos y herramientas
2. **Software funcionando** sobre documentación extensiva
3. **Colaboración con el cliente** sobre negociación contractual
4. **Respuesta ante el cambio** sobre seguir un plan

**La frase que casi siempre se olvida:** *"Esto es, aunque valoramos los elementos de la derecha,
valoramos más los de la izquierda."* El Manifiesto no dice que la documentación o los contratos
no sirvan: dice qué priorizar cuando hay que elegir.

(Utah, 2001 — 17 firmantes, entre ellos Kent Beck, Ken Schwaber, Martin Fowler y Alistair Cockburn)

----

### Los 12 principios (1 a 6)
<!-- .slide: style="font-size: 0.68em" -->

1. Nuestra mayor prioridad es satisfacer al cliente mediante la **entrega temprana y continua** de software con valor.
2. Aceptamos que los **requisitos cambien**, incluso en etapas tardías. Los procesos ágiles aprovechan el cambio para dar ventaja competitiva al cliente.
3. Entregamos software funcional **frecuentemente**, entre dos semanas y dos meses, con preferencia al periodo más corto posible.
4. Los responsables de negocio y los desarrolladores trabajan **juntos de forma cotidiana** durante todo el proyecto.
5. Los proyectos se desarrollan en torno a **individuos motivados**: hay que darles el entorno y el apoyo que necesitan, y confiarles la ejecución del trabajo.
6. El método más eficiente de comunicar información dentro del equipo es la **conversación cara a cara**.

----

### Los 12 principios (7 a 12)
<!-- .slide: style="font-size: 0.68em" -->

7. El **software funcionando** es la medida principal de progreso.
8. Los procesos ágiles promueven el **desarrollo sostenible**: todos deben poder mantener un ritmo constante de forma indefinida.
9. La atención continua a la **excelencia técnica** y al buen diseño mejora la agilidad.
10. La **simplicidad** —el arte de maximizar la cantidad de trabajo no realizado— es esencial.
11. Las mejores arquitecturas, requisitos y diseños emergen de **equipos auto-organizados**.
12. A intervalos regulares el equipo **reflexiona** sobre cómo ser más efectivo, y ajusta su comportamiento en consecuencia.

<!--
Notar el 8 y el 12: el ritmo sostenible y la retrospectiva son los dos principios que más
se saltean las empresas que dicen "hacer ágil". Sin retrospectiva no hay mejora del proceso.
-->

---
### Métodos Ágiles: Ejemplos
* Programación Extrema (Beck)
* Scrum (Cohn, Schwaber, Beedle)
* Crystal (Cockburn)
* ASD - Desarrollo de Software Adaptativo (Highsmith)
* DSDM - Desarrollo de Sistemas Dinámicos (Stapleton)
* FDD - Desarrollo dirigido por características (Palmer y Felsing)


---

### Principios de los métodos ágiles
<!-- .slide: style="font-size: 0.60em" -->
<!--
| Principio | Descripción                                                                                                                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Participación del Cliente | Los clientes deben intervenir estrechamente durante el proceso de desarrollo. Su función consiste en ofrecer y priorizar nuevos requerimientos del sistema y evaluar las iteraciones del mismo. |
| Entrega Incremental | El software se desarrolla en incrementos y el cliente especifica los requerimientos que se van a incluir en cada incremento.                                                                    |
| Personas, no procesos | Tienen que reconocerse y aprovecharse las habilidades del equipo de desarrollo. Debe permitirse a los miembros del equipo desarrollar sus propias formas de trabajar sin procesos establecidos. |
| Adoptar el cambio | Esperar a que cambien los requerimientos del sistema y, de este modo, diseñar el sistema para adaptar dichos cambios |
| Mantener simplicidad | Enfocarse en la simplicidad tanto en el software a desarrollar como en el proceso de desarrollo. Siempre que sea posible, trabajar de manera activa para eliminar la complejidad del sistema |
-->
<table>
<thead>
<tr>
<th>Principio</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Participación del Cliente</strong></td>
<td>Los clientes deben intervenir estrechamente durante el proceso de desarrollo. Su función consiste en ofrecer y <strong>priorizar</strong> nuevos requerimientos del sistema y <strong>evaluar</strong> las iteraciones del mismo.</td>
</tr>
<tr>
<td><strong>Entrega Incremental</strong></td>
<td>El software se desarrolla en incrementos y el cliente especifica los <strong>requerimientos</strong> que se van a incluir en cada incremento.</td>
</tr>
<tr>
<td><strong>Personas, no procesos</strong></td>
<td>Tienen que reconocerse y aprovecharse las habilidades del equipo de desarrollo. Debe permitirse a los miembros del equipo desarrollar sus propias <strong>formas de trabajar</strong> sin procesos establecidos.</td>
</tr>
<tr>
<td><strong>Adoptar el cambio</strong></td>
<td><strong>Esperar</strong> a que cambien los requerimientos del sistema y, de este modo, diseñar el sistema para adaptar dichos cambios</td>
</tr>
<tr>
<td><strong>Mantener simplicidad</strong></td>
<td>Enfocarse en la simplicidad tanto en el <strong>software</strong> a desarrollar como en el <strong>proceso</strong> de desarrollo. Siempre que sea posible, trabajar de manera activa para eliminar la complejidad del sistema</td>
</tr>
</tbody>
</table>

---
### Aplicabilidad del método ágil
* Desarrollo de productos, donde una compañía de software está desarrollando un producto de pequeño o mediano tamaño para la venta.
* El desarrollo de sistemas a medida para una organización, donde hay un claro compromiso por parte del cliente para participar en el proceso de desarrollo y donde
no hay muchas reglas y regulaciones externas que afectarán el software.
* Pequeños equipos, bien integrados. Hay problemas en la ampliación de los métodos ágiles a grandes sistemas

---
### Problemas con métodos ágiles
* Puede ser difícil mantener el interés de los clientes que están involucrados en el proceso.
* Los miembros del equipo pueden ser inadecuados para la intensa participación que caracteriza a los métodos ágiles.
* Priorizar cambios puede ser difícil donde hay múltiples partes interesadas.
* Mantener simplicidad requiere un trabajo extra
* Los contratos pueden ser un problema

---
### Los métodos ágiles y el mantenimiento de Software
<!-- .slide: style="font-size: 0.80em" -->
* La mayoría de las organizaciones gastan más en el mantenimiento del software existente que en el desarrollo de nuevo software.
* Los métodos ágiles deben facilitar tanto el mantenimiento como el desarrollo inicial.
* Dos problemas fundamentales:
  * ¿Son mantenibles los sistemas desarrollados con metodologías ágiles?
  * ¿Se pueden utilizar los métodos ágiles con eficacia para la evolución de un sistema?

**Pueden surgir problemas si el equipo de desarrollo original no puede mantenerse.**

---

### Ejercicio
<!-- .slide: style="font-size: 0.90em" -->
De los siguientes sistemas, piense qué metodología se adapta mejor a su desarrollo, ágil o dirigida por plan:
1. Sistema de Control de Tráfico Aéreo <!--Dirigida por plan-->
2. Aplicación Móvil de Redes Sociales <!--Ágil-->
3. Sistema de Gestión de Historias Clínicas Electrónicas (HCE) <!--Dirigida por plan-->
4. Sitio Web de Comercio Electrónico para una Startup <!--Ágil-->
5. Software de Navegación para Vehículos Autónomos <!--Dirigida por plan-->
6. Aplicación para la Gestión de Proyectos en una Empresa <!--Ágil-->
7. Sistema de Control de Calidad en una Planta de Manufactura <!--Dirigida por plan-->
8. Plataforma de Educación en Línea <!--Ágil-->

<img src="images/question.png" style="float: right; position: absolute">

---
### Desarrollo guiado por plan y el desarrollo ágil
<!-- .slide: style="font-size: 0.80em" -->
#### Desarrollo guiado por plan:
* Identifica etapas separadas en el proceso de software con salidas asociadas a cada etapa. 
* Las salidas de una etapa se usan como base para planear la siguiente actividad del proceso. 
* Las iteraciones se producen dentro de las actividades.

#### Desarrollo Ágil
* Especificación, diseño, implementación y pruebas están intercalados.

**La mayoría de los proyectos de software incluyen prácticas de los enfoques ágil y basado en plan**

----

### Desarrollo guiado por plan y el desarrollo ágil
![Plan vs Agil](images/unidad4/plan-vs-agil.png)

---
### Cuestiones técnicas, humanas y organizacionales
<!-- .slide: style="font-size: 0.75em" -->
* La mayoría de los proyectos incluyen elementos del guiado por plan y procesos ágil.
* La decisión depende de:
  1. ¿Es importante contar con una **especificación y diseño muy detallado** antes de pasar a la implementación? 
  <p class="fragment"> Si es así, utilizar un enfoque guiado por plan. </p>
  2. ¿Puede realizarse una estrategia de **entrega incremental**? 
  <p class="fragment"> Si es así, considere el uso de los métodos ágiles. </p>
  3. ¿Qué tan **grande es el sistema** que se está desarrollando? 
  <p class="fragment"> Los métodos ágiles son más eficaces cuando el sistema se puede
desarrollar con un equipo pequeño que pueda comunicarse de manera informal. Esto puede no ser posible para los grandes sistemas que requieren equipos de desarrollo grandes y distribuidos. </p>

----

### Cuestiones técnicas, humanas y organizacionales
<!-- .slide: style="font-size: 0.65em" -->
4. ¿Qué **tipo de sistema** se está desarrollando?
<p class="fragment"> Los enfoques guiado por plan pueden ser necesarios para los sistemas que requieren una gran cantidad de análisis antes de la aplicación (por ejemplo, sistema en tiempo real con complejos Requisitos de temporización). </p>
5. ¿Cuál es la **expectativa de vida** del sistema?
<p class="fragment"> Los sistemas de larga vida requieren más documentación de diseño para comunicar las intenciones originales de los desarrolladores del sistema al equipo de soporte. </p>
6. ¿Qué **tecnologías** están disponibles para apoyar el desarrollo del sistema?
<p class="fragment"> Los métodos ágiles se basan en buenas herramientas para realizar un seguimiento de la evolución de un diseño </p>
7. ¿Cómo se **organiza** el equipo de desarrollo?
<p class="fragment"> Si el equipo de desarrollo se distribuye o si parte del desarrollo se subcontrata, entonces son necesarios los documentos de diseño para comunicar a los equipos de desarrollo. </p>

----

### Cuestiones técnicas, humanas y organizacionales

<!-- .slide: style="font-size: 0.70em" -->

8. ¿Hay cuestiones **culturales o de organización** que puedan afectar al desarrollo del sistema?
<p class="fragment"> Las organizaciones tradicionales tienen una cultura basada en planes.</p>
9. ¿Qué tan **buenos** son los diseñadores y **programadores** del equipo de desarrollo?
<p class="fragment"> A veces se argumenta que los métodos ágiles requieren niveles más altos de capacitación que los enfoques basados en planes, en el que los programadores simplemente traducen un diseño detallado en código. </p>
10. ¿El sistema está sujeto a **regulación externa**?
<p class="fragment"> Si un sistema tiene que ser aprobado por un regulador externo (por ejemplo, que la FAA apruebe el software crítico para el funcionamiento de una aeronave) entonces se debe producir documentación detallada. </p>

---

### Programación extrema
Tal vez el más conocido y más utilizado método ágil.

Extreme Programming (XP) :
* Las nuevas versiones se pueden construir varias veces al día;
* Los incrementos se entregan a los clientes cada 2 semanas;
* Todas las pruebas se deben ejecutar para cada iteración y la integración sólo se acepta si las pruebas resultan satisfactorias.

---

### Valores en XP

![Valores en XP](images/unidad4/valores-extreme-programming-1.webp)

----

### Valores en XP
<!-- .slide: style="font-size: 0.75em" -->
- **Comunicación:** Debe ser eficaz para lograr una colaboración estrecha pero informal (verbal) entre los clientes y los desarrolladores.
Se establecen **metáforas** para comunicar conceptos. Ejemplo de un *sistema de mensajería*: “El sistema funciona como un servicio postal: 
cada usuario tiene un buzón, los mensajes son cartas, y el servidor de correo es la oficina de correos que se encarga de distribuirlas.”

- **Simplicidad:** Se diseña sólo la necesidad inmediata.

- **Retroalimentación:** Se obtiene de **3** fuentes:
  1. software implementado (pruebas unitarias)
  2. el cliente
  3. otros miembros del equipo 

Las historias del usuario o casos de uso son la base para las pruebas de aceptación. 

----

### Valores en XP
- **Valentía o disciplina:** Diseñar para hoy. Reconocer que los requerimientos futuros tal vez cambien mucho.
- **Respeto:** Entre los miembros del equipo, con el software y con el proceso XP.

---

![Programacion Extrema](images/unidad4/programacion-extrema.png)

----

#### Proceso de la programación extrema
![Proceso XP](images/unidad4/proceso-xp.png)

CRC = Clase - Responsabilidad - Colaboraciones

---
### XP y principios ágiles
1. **Participación del cliente:** un compromiso a tiempo completo del cliente con el equipo
2. **Entrega incremental:** el desarrollo incremental es apoyado a través pequeños sistemas de comunicación frecuentes.
3. **Personas no procesos:** a través de la programación en pares y propiedad colectiva del código.
4. **Adoptar el cambio:** Cambios soportados a través sistemas regulares de comunicación.
5. **Mantener la simplicidad:** refactorización constante de código.

---
### Prácticas de Extreme programming

<!-- .slide: style="font-size: 0.60em" -->

<table>
<thead>
<tr>
<th>Principio o práctica</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Planificación Incremental</strong></td>
<td>Los requisitos se escriben como <strong>historias de usuario</strong> que son incluidas en una publicación determinada por el tiempo disponible y su prioridad. Se subdivide en <strong>tareas</strong>.</td>
</tr>
<tr>
<td><strong>Incrementos pequeños</strong></td>
<td>Primero se desarrolla el <strong>MVP</strong> (Producto Mínimo Viable). Posteriormente se añaden funcionalidades o mejoras en cada versión.</td>
</tr>
<tr>
<td><strong>Diseño Simple</strong></td>
<td>El diseño solo satisface las necesidades actuales y no más.</td>
</tr>
<tr>
<td><strong>Desarrollo de las pruebas primero</strong></td>
<td>Se desarrollan las <strong>pruebas unitarias</strong> automatizadas antes de implementar la funcionalidad.</td>
</tr>
<tr>
<td><strong>Refactorización</strong></td>
<td>Se implementan mejoras constantes en el código para que sea simple y mantenible.</td>
</tr>
</tbody>
</table>

----

### Prácticas de Extreme programming
<!-- .slide: style="font-size: 0.70em" -->

<table>
<thead>
<tr>
<th>Principio o práctica</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Programación en pares</strong></td>
<td>Los desarrolladores trabajan en parejas, revisando el trabajo mutuamente y dándose apoyo para hacer un buen trabajo.</td>
</tr>
<tr>
<td><strong>Propiedad colectiva del código</strong></td>
<td>La pareja de desarrolladores trabaja en todas las áreas del sistema, para que no queden islas de conocimiento y todos los desarrolladores asumen responsabilidad por todo el código.</td>
</tr>
<tr>
<td><strong>Integración continua</strong></td>
<td>Tan pronto como el trabajo en una tarea está completo, es integrado en el sistema y se ejecutan todas las pruebas unitarias.</td>
</tr>
<tr>
<td><strong>Ritmo sostenible</strong></td>
<td>No se trabajan horas extras. El cansancio reduce la calidad del código y la productividad</td>
</tr>
<tr>
<td><strong>Cliente en el sitio</strong></td>
<td>El cliente debe estar disponible a tiempo completo para el equipo XP. Es responsable de llevar requisitos del sistema para el equipo de implementación.</td>
</tr>
</tbody>
</table>

----

### 💡 Ejercicio: ¿Qué práctica de XP faltó?
<!-- .slide: style="font-size: 0.70em" -->

En cada situación el equipo dice "hacemos XP". Identifiquen **qué práctica se están salteando**:

1. Nadie se anima a tocar el módulo de facturación porque "eso lo hizo Martín y solo él lo entiende". <!--Propiedad colectiva del código + programación en pares-->
2. El lunes integran tres semanas de trabajo de cinco personas y se pasan dos días arreglando conflictos. <!--Integración continua-->
3. El equipo entrega el sprint trabajando dos fines de semana seguidos; el siguiente sprint rinde la mitad. <!--Ritmo sostenible-->
4. Programaron un sistema de permisos configurable "por si algún día lo piden". Nunca lo pidieron. <!--Diseño simple: se diseña solo la necesidad inmediata-->
5. Cada cambio rompe algo distinto y se enteran cuando el cliente lo reporta. <!--Desarrollo de las pruebas primero / pruebas automatizadas-->
6. El cliente responde los mails una vez por semana y el equipo avanza suponiendo. <!--Cliente en el sitio-->

<!--
Cierre de la discusión: las prácticas de XP se sostienen entre sí. La propiedad colectiva del
código no funciona sin pruebas automatizadas (nadie toca lo ajeno sin red), y la integración
continua no sirve de nada si las pruebas no corren solas.
-->

---
### Escenarios de los requerimientos
* En XP, el cliente o usuario es parte del equipo y es responsable de tomar decisiones sobre los requisitos
* Solicitudes de los usuarios se expresan como escenarios o historias del usuario.
* Las historias de Usuario se dividen y plasman en tareas. Estas tareas son la base del calendario y de la estimación de los costos.
* El cliente elige las historias para su inclusión en el próximo incremento en base a sus prioridades y calendario.

---

<!-- .slide: style="font-size: 0.57em" -->

### Una historia para “Prescripción de medicamentos”
Kate es una médica que quiere prescribir fármacos a un paciente que se atiende en una clínica. El archivo del paciente
ya se desplegó en su computadora, de manera que da click en el campo del medicamento y luego puede seleccionar 
"medicamento actual", "medicamento nuevo" o "formulario".

Si selecciona "medicamento actual", el sistema le puede comprobar la dosis. Si quiere cambiar la dosis, ingresa la dosis
y luego confirma la prescripción.

Si elige "medicamento nuevo", el sistema supone que Kate sabe cuál medicamento prescribir. Ella teclea las primeras
letras del nombre del medicamento. El sistema muestra una lista de medicamentos posibles cuyo nombre inicia con esas
letras. Posteriormente elige el fármaco requerido y el sistema responde solicitándole que verifique que el medicamento
seleccionado sea el correcto. Ella ingresa la dosis y luego confirma la prescripción.
Si Kate elige "formulario", el sistema muestra un recuadro de búsqueda para el formulario aprobado. Entonces busca el
medicamento requerido. Ella selecciona un medicamento y el sistema le pide comprobar que éste sea el correcto. Luego
ingresa la dosis y confirma la prescripción.

El sistema siempre verifica que la dosis esté dentro del rango aprobado. Si no es así, le pide a Kate que la modifique.
Después de que ella confirma la prescripción, se desplegará para su verificación. Kate hace click o en "OK" o en "Cambiar".
Si hace click en "OK", la prescripción se registra en la base de datos de auditoría. Si hace click en "Cambiar", 
reingresa al proceso de "prescripción de medicamento".

---
### Ejemplos de tarjetas de tareas para la prescripción de medicamentos
<!-- .slide: style="font-size: 0.80em" -->
1. Cambiar dosis del medicamento prescripto
2. Selección de formulario
3. Validación de dosis

La verificación de dosis es una prevención de seguridad para comprobar que el médico no prescribe una dosis
riesgosamente pequeña o grande.
Al usar el ID del formulario para el nombre genérico del medicamento, busca el formulario y recupera las dosis, máxima
y mínima, recomendadas.
Verifica la dosis prescrita contra el mínimo y el máximo. Si está fuera de rango, emite un mensaje de error señalando
que la dosis es muy alta o muy baja.
Si está dentro del rango, habilita el botón "Confirmar".

---
### XP y el cambio
* La sabiduría convencional en la ingeniería de software es diseñar para el cambio. Sostiene que vale la pena el gasto de
tiempo y esfuerzo anticipando los cambios ya que esto reduce costos más tarde.
* XP sostiene que no vale la pena anticipar los cambios ya que cambios no se pueden prever de forma fiable
* Propone la mejora constante de código (refactorización) para poder realizar cambios más fácilmente.

---
### Refactorización
* El equipo de programación busca posibles mejoras de código y realiza las mejoras aunque no sean de inmediata necesidad.
* Esto mejora la comprensibilidad del software y reduce la necesidad de documentación.
* Los cambios son más fáciles de hacer ya que el código está bien estructurado y claro.
* Sin embargo, algunos cambios requieren reconstrucción de la arquitectura y esto es mucho más caro

---
### Ejemplos de Refactorización
* Re-organización de una jerarquía de clases para eliminar código duplicado.
* Ordenar y cambiar el nombre de los atributos y métodos para facilitar su comprensión.
* La sustitución de líneas de código con llamadas a métodos que se han incluido en una biblioteca de programas.

----

### Refactorizar: antes y después
<!-- .slide: style="font-size: 0.62em" -->

**Antes** — funciona, pero nadie entiende qué hace:

```javascript
function calc(l, t) {
  let r = 0;
  for (let i = 0; i < l.length; i++) {
    if (t == 1) { r = r + l[i].p * l[i].c * 0.9; }
    else { r = r + l[i].p * l[i].c; }
  }
  return r;
}
```

**Después** — mismo comportamiento, otra legibilidad:

```javascript
const DESCUENTO_MAYORISTA = 0.10;

function calcularTotal(items, esMayorista) {
  const subtotal = items.reduce(
    (acum, item) => acum + item.precio * item.cantidad, 0
  );
  return esMayorista ? subtotal * (1 - DESCUENTO_MAYORISTA) : subtotal;
}
```

**Qué cambió:** nombres que se leen, el número mágico `0.9` pasó a ser una constante con nombre,
y desapareció la duplicación de la multiplicación. **Ni una funcionalidad nueva** — eso es
exactamente refactorizar.

----

### 💡 Ejercicio: Detectar qué refactorizar
<!-- .slide: style="font-size: 0.68em" -->

```javascript
function proc(u) {
  if (u.t == "a") {
    console.log(u.n + " admin");
    return u.n.toUpperCase() + " [ADMIN]";
  } else if (u.t == "m") {
    console.log(u.n + " moderador");
    return u.n.toUpperCase() + " [MOD]";
  } else {
    console.log(u.n + " usuario");
    return u.n.toUpperCase() + " [USER]";
  }
}
```

1. Señalen **tres problemas** distintos de este código.
2. Propongan cómo lo refactorizarían.
3. ¿Qué necesitan tener antes de animarse a tocarlo?

<!--
1. Nombres sin significado (proc, u, t, n); código duplicado en las tres ramas (el
   toUpperCase y el console.log se repiten); condicionales encadenados con literales
   mágicos ("a", "m") que deberían ser un mapa o un enum.
2. Extraer la etiqueta a un objeto {admin:"[ADMIN]", ...}, renombrar todo, dejar una sola
   línea de formateo y sacar el console.log (efecto colateral escondido en una función que
   dice devolver un texto).
3. PRUEBAS. Sin pruebas automatizadas no se refactoriza: no hay forma de saber si
   se rompió algo. Esta es la respuesta que interesa.
-->

---
### Las pruebas en XP
<!-- .slide: style="font-size: 0.90em" -->
* Las Pruebas son fundamentales para XP. El software se comprueba después de cada cambio.
* Funciones de prueba de XP:
  * Desarrollo de las pruebas en primer lugar
  * Desarrollo de pruebas incrementales de escenarios.
  * Participación de los usuarios en el desarrollo de la prueba y validación.
  * Juego de pruebas automatizadas que se utilizan para ejecutar todas las pruebas de componentes cada vez que una nueva versión está construida.

---
### Desarrollo de las pruebas primero
<!-- .slide: style="font-size: 0.90em" -->
* Escribir pruebas antes del código aclara los requisitos para ser implementados.
* Las pruebas se escriben como programas en lugar de datos de manera que se pueden ejecutar de forma automática. La prueba incluye una comprobación de que se ha ejecutado correctamente.
  * Por lo general, se usan frameworks de pruebas como JUnit o Jest.
* Todas las pruebas anteriores y las nuevas se ejecutan automáticamente cuando se añade una nueva funcionalidad, comprobando así que la nueva funcionalidad no ha introducido errores.

----

### El ciclo rojo - verde - refactor
<!-- .slide: style="font-size: 0.62em" -->

**1. Rojo** — se escribe la prueba de algo que todavía no existe. Falla, y está bien que falle:

```javascript
test('rechaza una dosis por encima del máximo', () => {
  expect(validarDosis(500, 3, { max: 1000 })).toBe(false);
});
```

**2. Verde** — se escribe el código *mínimo* que hace pasar la prueba:

```javascript
function validarDosis(dosis, frecuencia, limites) {
  return dosis * frecuencia <= limites.max;
}
```

**3. Refactor** — con la prueba en verde, ahora sí se mejora el código sin miedo.

**Por qué importa el orden:** escribir la prueba primero obliga a definir *qué* tiene que hacer
la función antes de pensar en *cómo*. Si no podés escribir la prueba, no entendiste el requisito.

----

### 💡 Ejercicio: Escribir la prueba primero
<!-- .slide: style="font-size: 0.75em" -->

Un requisito de la app de gestión de tareas: *"una tarea no puede marcarse como completada
si tiene subtareas pendientes"*.

**Antes de escribir una línea de implementación**, escriban los casos de prueba:

1. ¿Cuáles son los casos donde debe **permitir** completar?
2. ¿Cuáles son los casos donde debe **rechazar**?
3. ¿Qué casos límite aparecen que el requisito no aclara?

<!--
El punto 3 es el que importa: ¿una tarea sin subtareas se puede completar? ¿Y si las subtareas
están canceladas en vez de completadas? ¿Y si tiene sub-subtareas?
Escribir las pruebas hace visibles los agujeros del requisito ANTES de programar,
que es exactamente el argumento de XP para hacerlo en ese orden.
-->

---
### Participación de los clientes
<!-- .slide: style="font-size: 0.90em" -->
* El papel del cliente en el proceso de pruebas es ayudar a desarrollar pruebas de aceptación de las historias que han de
ser implementadas en la próxima versión del sistema
* El cliente que es parte del equipo de pruebas, escribe pruebas simultáneamente al desarrollo. Por consiguiente, todo nuevo
código es validado para asegurarse de que es lo que necesita el cliente.
* Problemas: las personas que adoptan el papel de clientes disponen de limitado tiempo. Ellos pueden sentir que la
presentación de los requisitos era suficiente contribución y por tanto pueden ser reacios a involucrarse en el proceso de
prueba.

---
### Descripción del caso de prueba para la comprobación de dosis
<!-- .slide: style="font-size: 0.70em" -->
Prueba 4: Comprobación de dosis
Entrada: 
1. Un número en mg que represente una sola dosis del medicamento.
2. Un número que signifique el número de dosis individuales por día.

Pruebas:
1. Probar las entradas donde la dosis individual sea correcta, pero la frecuencia muy elevada.
2. Probar las entradas donde la dosis individual sea muy alta y muy baja.
3. Probar las entradas donde la dosis individual x frecuencia sea muy alta o muy baja.
4. Probar las entradas donde la dosis individual x frecuencia esté en el rango permitido.

Salida: 
OK o mensaje de error que indique que la dosis está fuera del rango de seguridad.

---
### La automatización de pruebas
<!-- .slide: style="font-size: 0.80em" -->
* La automatización de pruebas significa que las pruebas se escriben como componentes ejecutables antes de que la tarea se implemente
  * Estos componentes de prueba deben ser independientes, deberían
simular la presentación de la entrada para ser probado y debe comprobar que el resultado cumple con las especificaciones de salida.
* Cuando se automatizan las pruebas, siempre hay un conjunto de pruebas que puede ser rápida y fácilmente ejecutado
  * Siempre que se agrega alguna funcionalidad al sistema, las pruebas de
regresión se deben correr y si el nuevo código introdujo problemas se identifican inmediatamente

---
### Dificultades en pruebas XP
<!-- .slide: style="font-size: 0.80em" -->
* Los programadores prefieren la programación a las pruebas y a veces se toman atajos al escribir pruebas. Por
ejemplo, pueden escribir pruebas incompletas que no comprueban todas las posibles excepciones que puedan ocurrir.
* Algunas pruebas pueden ser muy difíciles de escribir de forma incremental. Por ejemplo, en una interfaz de usuario
compleja, es a menudo difícil de escribir pruebas unitarias para el código que implementa la 'lógica de visualización' 
y flujo de trabajo entre las pantallas
* Es difícil juzgar la integridad de un conjunto de pruebas. Aunque se tengan muchas pruebas, la prueba de conjunto
puede no proporcionar una cobertura completa.

---
### Programación en pares
* En XP, los programadores trabajan en parejas, sentados juntos a desarrollar código.
* Esto ayuda a desarrollar la propiedad común de código y difunde el conocimiento a través del equipo.
* Sirve como un proceso de revisión informal, ya que cada línea de código es vista por más de una persona.
* Alienta a la refactorización.
* Las mediciones muestran que la productividad de desarrollo con la programación par es similar a la de dos
personas trabajando en paralelo

---
### Programación en pares
<!-- .slide: style="font-size: 0.80em" -->
* En la programación en pares, los programadores se sientan juntos en la misma estación de trabajo para desarrollar el
software.
* Las parejas se crean dinámicamente para que todos los miembros del equipo trabajen unos con otros durante el proceso
de desarrollo.
* El intercambio de conocimientos que sucede entre la pareja durante la programación es muy importante, ya que reduce
riesgos para el proyecto cuando algún miembro del equipo se va.
* La programación en pares **no es necesariamente ineficiente**: las mediciones muestran que la productividad de una
pareja es comparable a la de dos programadores trabajando por separado, con la ventaja de la revisión permanente y la
difusión del conocimiento.

---
### Ventajas de la programación en parejas
<!-- .slide: style="font-size: 0.80em" -->
* Apoya la idea de la propiedad y responsabilidad colectiva.
  * Los individuos no son responsables de los problemas con el código. En su lugar, el equipo tiene la responsabilidad 
colectiva para resolver estos problemas
  * Actúa como un proceso de revisión informal, ya que cada línea de código se mira por al menos dos personas.
* Ayuda apoyando a la refactorización, que es un proceso de mejora de software.
  * Cuando se utiliza la programación en pares y la propiedad
colectiva, otros se benefician inmediatamente de la refactorización de modo que es probable que apoyen el proceso.

---

### Ejercicio: Historias de Usuario y Estimación

1. Emplear Jira para redactar historias de usuario para la app de **gestión de tareas** siguiendo el formato “Como [rol], quiero [funcionalidad] para [beneficio]”.
Ejemplos:
<p class="fragment"> Como usuario, quiero crear una nueva tarea, para recordar lo que tengo que hacer. </p>
<p class="fragment"> Como usuario, quiero marcar una tarea como completada, para llevar un control de lo que ya hice. </p>

2. Realizar una estimación empleando [poker planning](https://planningpokeronline.com/8eCdPtjVtv9hVj75aXsc/)

---
### Gestión de proyectos ágil
<!-- .slide: style="font-size: 0.90em" -->
* La principal responsabilidad de los directores de proyectos de software es la gestión del proyecto para que
el software se entregue a tiempo y dentro del presupuesto previsto para el proyecto
* El enfoque estándar para la gestión de proyectos es dirigido por plan. Gerentes elaboran un plan para el
proyecto determinando qué debería ser entregado, cuándo debería ser entregado y quién trabajara en el desarrollo del
proyecto
* La gestión de proyectos ágil requiere un enfoque diferente, adaptado para desarrollo incremental y la
fortalezas particulares de los métodos ágiles.

---
### Scrum
<!-- .slide: style="font-size: 0.80em" -->
El enfoque de Scrum es un método ágil, su atención se centra en la gestión del desarrollo iterativo

Hay tres fases en Scrum.
1. La **fase inicial** es un anteproyecto: se establecen los objetivos generales del proyecto y se diseña la
arquitectura de software.
2. Esto es seguido por una serie de **ciclos**, donde cada ciclo desarrolla un incremento del sistema.
3. La **fase de cierre** del proyecto concluye el proyecto, completa documentación requerida, tales como marcos de ayuda del
sistema y manuales de usuario y evalúa las lecciones aprendidas del proyecto.

---
### El Ciclo de Sprint
* Los Sprints son de longitud fija, normalmente 2-4 semanas. Ellos corresponden al desarrollo de una versión del sistema en XP.
* El punto de partida para la planificación es la lista de tareas a realizar en el proyecto.
* La fase de selección involucra a todo el equipo del proyecto, que trabajan con el cliente para seleccionar las
funcionalidades que se desarrollarán durante el sprint.

----

### El Ciclo de Sprint
* Una vez que éstos están de acuerdo, el equipo se organiza para desarrollar el software. Durante esta etapa,
el equipo está aislado del cliente y la organización, con todas las comunicaciones canalizadas a través del denominado
'Scrum Master'.
* El papel del Scrum Master es proteger el equipo de desarrollo de las distracciones externas.
* Al final del sprint, el trabajo realizado es revisado y se presenta a las partes interesadas. El siguiente ciclo de
sprint comienza entonces

---
### Trabajo en equipo en Scrum
<!-- .slide: style="font-size: 0.90em" -->
* El 'Scrum Master' es un facilitador que organiza reuniones diarias, rastrea la lista de trabajos por hacer,
registra las decisiones, mide el progreso y se comunica con los clientes y la gestión fuera del equipo.
* Todo el equipo asiste a las reuniones diarias cortas donde todos los miembros del equipo comparten
información, describen su progreso desde la última reunión, los problemas que han surgido y que se ha
previsto para el día siguiente.

**Esto significa que todos en el equipo saben lo que está pasando y, si surgen problemas, puede volver a planear el
trabajo a corto plazo para hacer frente a ellos.**

----

![Reuniones cortas](images/unidad4/reuniones-cortas.png)

---
### Beneficios de Scrum
* El producto se divide en un conjunto de fragmentos manejables y comprensibles.
* Los requisitos inestables son más manejables.
* Todo el equipo tiene visibilidad de todo y por lo tanto se mejora la comunicación del equipo.
* Los clientes ven la entrega a tiempo y se obtiene retroalimentación sobre cómo funciona el producto.
* Se genera confianza entre los clientes y los desarrolladores. Se crea una cultura positiva en la que
todos esperan que el proyecto tenga éxito.

---
### El Proceso Scrum
![Scrum](images/unidad4/03-scrum.png)

----

### Flujo Scrum

![Scrum](images/unidad4/proceso-scrum.png)

---
### Escala métodos ágiles
<!-- .slide: style="font-size: 0.90em" -->
* Los métodos ágiles han demostrado ser un éxito para los proyectos pequeños y medianos que pueden ser
desarrollados por un equipo pequeño co-ubicado.
* A veces se argumenta que el éxito de estos métodos viene a causa de la mejora de las comunicaciones, que
es posible cuando todos trabajan juntos.
* La ampliación de los métodos ágiles implica el cambio de éstos para hacer frente a grandes proyectos, más
largos, en los que hay varios equipos de desarrollo, tal vez trabajando en diferentes lugares.

---
### Desarrollo de sistemas grandes
<!-- .slide: style="font-size: 0.80em" -->
* Los grandes sistemas suelen ser colecciones de sistemas independientes en los que equipos separados desarrollan cada
sistema. Con frecuencia, estos equipos están trabajando en diferentes lugares, a veces en diferentes zonas horarias.
* Los sistemas grandes suelen ser **sistemas *brownfield***: no nacen en el vacío, sino que deben convivir e interactuar con
una serie de sistemas que ya existen. Muchos de sus requisitos tienen que ver con esa interacción, y por eso no se prestan
bien a la flexibilidad ni al desarrollo incremental.
* Si varios sistemas se integran para crear un sistema, una parte importante del desarrollo tiene que ver con la configuración del sistema
en lugar de desarrollo de código inicial.

----

### El desarrollo del sistemas grandes
<!-- .slide: style="font-size: 0.90em" -->
* Grandes sistemas y sus procesos de desarrollo están a menudo limitados por las reglas y regulaciones externas
que limitan la forma en que se pueden desarrollar.
* Los sistemas grandes tienen un tiempo de desarrollo largo. Es difícil mantener equipos coherentes que conocen
el sistema a lo largo de ese período ya que, inevitablemente, la gente se mueve a otros trabajos y proyectos.
* Los sistemas grandes suelen tener un conjunto diverso de partes interesadas. Es prácticamente imposible incluir
todas estas diferentes partes interesadas en el proceso de desarrollo.

---
### El escalado horizontal y la ampliación
<!-- .slide: style="font-size: 0.90em" -->
* La "expansión" tiene que ver con el uso de los métodos ágiles de desarrollo de sistemas de software grandes que
no pueden ser desarrollados por un equipo pequeño.
* La "ampliación“ se refiere a cómo los métodos ágiles pueden introducirse a través de una gran organización con
muchos años de experiencia en desarrollo de software.
* Al escalar los métodos ágiles es esencial mantener los fundamentos ágiles
  * Planificación flexible, versiones frecuentes del sistema, integración continua, desarrollo basado en pruebas y
las buenas comunicaciones del equipo.

---
### La expansión para los grandes sistemas
<!-- .slide: style="font-size: 0.90em" -->
* Para el desarrollo de grandes sistemas, no es posible centrarse únicamente en el código del sistema. Se tiene
que hacer diseño y documentación.
* Mecanismos de comunicación entre los equipos tienen que ser diseñados y utilizados. Este procedimiento incluirá
conferencias telefónicas y de vídeo regulares y frecuentes donde los equipos se actualizan entre sí sobre los
progresos.
* La integración continua —reconstruir el sistema completo cada vez que un desarrollador integra un cambio— es
prácticamente imposible a esta escala. Cada equipo integra de forma continua su propio subsistema, y la integración
del conjunto se hace con menor frecuencia.

---
### La ampliación a grandes empresas
<!-- .slide: style="font-size: 0.80em" -->
* Los administradores de proyectos que no cuentan con experiencia en métodos ágiles pueden ser reacios a aceptar el 
riesgo de un nuevo enfoque.
* Las grandes organizaciones suelen tener procedimientos y normas de calidad que se espera que todos los proyectos sigan 
y, por su carácter burocrático, éstos tienden a ser incompatibles con los métodos ágiles.
* Los métodos ágiles parecen funcionar mejor cuando los miembros del equipo tienen un nivel relativamente alto de 
habilidad. Sin embargo, dentro de las grandes organizaciones, lo más probable es que se tenga
una amplia gama de habilidades y capacidades.
* Existe resistencia cultural a los métodos ágiles, especialmente en aquellas organizaciones que tienen una larga 
historia de uso de los procesos de ingeniería de sistemas convencionales.

---

### 📝 Cuestionario para resolver
<!-- .slide: style="font-size: 0.90em" -->

Este cuestionario es **para llevarse y resolver en casa**.

* **Parte A:** 8 preguntas de opción múltiple (una sola correcta).
* **Parte B:** 3 casos para analizar y justificar.

Lo repasamos al inicio de la próxima clase.

----

### Parte A — Opción múltiple (1 a 4)
<!-- .slide: style="font-size: 0.60em" -->

**1.** Que el Manifiesto valore "software funcionando sobre documentación extensiva" significa que:
a) No hay que documentar nada
b) Cuando hay que elegir se prioriza el software que funciona, sin que eso anule el valor de documentar
c) La documentación se hace toda al final
d) Documentar es responsabilidad del cliente
<!--Correcta: b. La frase clave del Manifiesto es "valoramos más los de la izquierda", no "descartamos los de la derecha".-->

**2.** ¿Cuál **NO** es una característica común de los enfoques ágiles?
a) Especificación, diseño e implementación entrelazados
b) Desarrollo incremental
c) Congelar los requisitos antes de empezar a programar
d) Involucrar al cliente en el desarrollo
<!--Correcta: c-->

**3.** En XP, las historias de usuario:
a) Reemplazan al código fuente
b) Las redacta el arquitecto al inicio del proyecto
c) Las elige el cliente para cada incremento según su prioridad
d) Son diagramas UML
<!--Correcta: c-->

**4.** "Desarrollo de las pruebas primero" significa:
a) Probar manualmente antes de entregar
b) Escribir las pruebas automatizadas antes de implementar la funcionalidad
c) Que el cliente pruebe antes que el equipo
d) Hacer pruebas de carga al comienzo del proyecto
<!--Correcta: b-->

----

### Parte A — Opción múltiple (5 a 8)
<!-- .slide: style="font-size: 0.60em" -->

**5.** Refactorizar es:
a) Agregar funcionalidad nueva de forma incremental
b) Corregir errores detectados en producción
c) Mejorar la estructura del código sin cambiar su comportamiento
d) Reescribir el sistema desde cero
<!--Correcta: c. Si cambia el comportamiento, no es refactorización.-->

**6.** La propiedad colectiva del código en XP significa que:
a) El código es de dominio público
b) Todos los desarrolladores trabajan en todas las áreas y asumen responsabilidad por todo el código
c) Cada módulo tiene un dueño responsable de aprobarlo
d) El cliente es dueño del código fuente
<!--Correcta: b. Es lo que evita las "islas de conocimiento" y se apoya en la programación en pares.-->

**7.** Un argumento en contra de aplicar métodos ágiles a un sistema grande y distribuido es:
a) Que en esos sistemas no se pueden hacer pruebas
b) Que la comunicación informal deja de alcanzar y se vuelven necesarios el diseño y la documentación
c) Que no existe el desarrollo incremental
d) Que los sprints tendrían que durar más de un año
<!--Correcta: b-->

**8.** Respecto del cambio, XP sostiene que:
a) Conviene anticiparlo con un diseño detallado por adelantado
b) No vale la pena anticiparlo porque no se puede prever de forma fiable; conviene refactorizar constantemente
c) Los cambios se posponen a la etapa de mantenimiento
d) Los cambios los decide el arquitecto del sistema
<!--Correcta: b. Es la postura opuesta a la "sabiduría convencional" de diseñar para el cambio.-->

----

### Parte B — Casos para analizar
<!-- .slide: style="font-size: 0.68em" -->

**Caso 1.** Un banco va a rehacer su home banking. Son 30 personas en tres ciudades y el
sistema debe pasar auditorías del Banco Central. ¿Ágil, dirigido por plan o híbrido?
Justificá usando **tres** de los diez factores vistos en la unidad.

**Caso 2.** Un equipo XP viene atrasado y el líder propone eliminar la programación en pares
"para que rindan el doble". ¿Qué le responderías? Dá **dos** argumentos y admití **un** costo
real de la práctica.

**Caso 3.** Escribí **tres historias de usuario** para una app de reserva de canchas de fútbol
en el formato *"Como [rol], quiero [funcionalidad] para [beneficio]"*, y dividí una de ellas
en las tareas necesarias para implementarla.

<!--
Caso 1: híbrido. Factores que empujan a plan: regulación externa (auditoría del BCRA exige
documentación y trazabilidad), tamaño y distribución del equipo (30 personas en tres ciudades,
la comunicación informal no escala), expectativa de vida larga del sistema. Factores que
empujan a ágil: entrega incremental posible por módulos, alta expectativa de cambio en la
experiencia de usuario. Salida razonable: arquitectura y contratos de integración dirigidos
por plan, desarrollo de cada módulo en sprints.

Caso 2: la productividad de una pareja es comparable a la de dos programadores separados,
y encima incorpora revisión permanente y difusión del conocimiento (menos riesgo si alguien
se va). Sacarla suele empeorar la calidad justo cuando el equipo está apurado, que es cuando
más errores se cometen. Costo real a admitir: es agotadora y no todos los perfiles la toleran;
tampoco rinde para tareas triviales o repetitivas.

Caso 3: revisar que las tres historias tengan los tres componentes y que el beneficio no sea
una repetición de la funcionalidad ("quiero reservar una cancha para reservar una cancha" no
es un beneficio). Las tareas deben ser técnicas: modelo de datos, endpoint, pantalla, validación,
pruebas.
-->

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
