
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

.exercise-slide {
  border: 2px dashed #b58900;
  border-radius: 12px;
  padding: 20px;
}

.fuente {
  border-top: 2px solid rgba(121, 177, 217, 0.6);
  padding-top: 8px;
  margin-top: 14px;
  font-size: 0.80em;
}

.alerta {
  border-left: 5px solid #b58900;
  padding-left: 14px;
  text-align: left !important;
}
</style>
## Temario
<div class="grid-container2">
<div class="grid-item">

### Calidad del Software
* Definición
* Manejo de la calidad
* Qué es calidad?
* Compromiso de Calidad
* Actividades de manejo de calidad
* Atributos de la calidad del software
* Calidad basada en procesos
* Estándares de Software
* Importancia de los estándares
* Problemas con estándares

</div>
<div class="grid-item">

* ISO 9000-9001
* Certificación ISO
* Revisión
* Procedimientos de Revisión
* Revisiones de Calidad
* Tipos de Revisiones
* Inspecciones del programa
* Métricas de calidad del producto
* Suposición de métricas
* Métricas estáticas de productos de software
* Métricas Orientadas a Objetos
* Métricas de acoplamiento
* Madures de las métricas
</div>
</div>

---

### Alcance de esta unidad
<!-- .slide: style="font-size: 0.80em" -->

Quedan **4 clases** y el programa no entra completo, asi que parte del material no se va a
desarrollar en el cursado.

<div class="grid-item">

Las filminas marcadas con **&#9761; No se dicta en clase** estan completas aca y
**se evaluan en el examen final**. Son material de estudio: nadie las va a explicar en clase.

Todo lo demas se dicta, y es la base para el trabajo practico.

</div>

**Como estudiarlas:** la filmina marcada siempre viene despues de la que si se dicta sobre el
mismo tema. Si entendiste la que se dicto, la marcada es la profundizacion.

---

#### Ingeniería de Software
#### Ian Sommerville

![Bibliografia](images/unidad11/somerville.png)

---
### CALIDAD
* **Asegurar la calidad:** definición de procesos y estándares que deben conducir
a la obtención de productos de alta calidad
* **Control de calidad:** aplicación de procesos para eliminar productos que no
cuentan con el nivel de calidad requerido

---
### MANEJO DE LA CALIDAD DEL SOFTWARE
* Se refiere a lograr un nivel de calidad requerido en el producto de software
* Involucra a la definición de estándares de calidad apropiados y procedimientos que
permitan asegurar que estos se cumplan.
* Debe llevar a desarrollar una cultura de calidad en donde la calidad es responsabilidad de todos

---
### ¿QUÉ ES CALIDAD?
**Calidad significa que un producto debe cumplir con sus especificaciones.**

Para sistemas de software
* Algunos requerimientos de calidad son difíciles de especificar (eficiencia, mantenibilidad,
reusabilidad, etc.)
* Las especificaciones del Software son usualmente incompletos y a menudo inconsistentes

---
### EL COMPROMISO DE CALIDAD
<!-- .slide: class="final" -->
* No podemos esperar a que las especificaciones mejoren para poner atención al manejo de la calidad
* Debe haber procedimientos que permitan mejorar la calidad aunque la especificaciones no sean perfectas
* El manejo de la calidad no solo se refiere a reducir defectos sino también a mejorar otras cualidades del producto

---
### ACTIVIDADES DE MANEJO DE CALIDAD
* **Asegurar la calidad:** Establecer procedimientos organizacionales y estándares para la calidad
* **Planear la calidad:** Seleccionar procedimientos aplicables y estándares para un proyecto en particular y
modificar estos como sean requeridos
* **Controlar la calidad:** Garantizar que procedimientos y estándares son seguidos por el equipo de desarrollo de
software

---
### ACTIVIDADES DE MANEJO DE CALIDAD
<!-- .slide: class="final" -->
El manejo de calidad debe ser separado del manejo del proyecto
para asegurar independencia

---

### Plan de Calidad
<!-- .slide: style="font-size: 0.80em" -->
Un plan de calidad (Humphrey) suele incluir:
1. **Introducción del producto:** Descripción del producto, su mercado y expectativas de calidad. 
2. **Planes del Producto:** Indican las fechas de entrega críticas y las responsabilidades para el producto, planes para distribución y servicio al producto.
3. **Descripciones de procesos:** Describen los procesos y estándares de desarrollo y 
servicio que deben usarse para diseño y gestión del producto.
4. **Metas de calidad:** Identificación y justificación de los atributos esenciales de calidad del 
producto.
5. **Riesgos y gestión del riesgo:** Los riesgos pueden afectar la calidad del 
producto y las acciones a tomar para enfrentar dichos riesgos

---
### ATRIBUTOS DE LA CALIDAD DEL SOFTWARE
<!-- .slide: style="font-size: 0.60em" -->
<!--
|              |                  |                                                    |
|:-------------|:-----------------|:---------------------------------------------------|
| Protección   | Comprensibilidad | Portabilidad                                       |
| Seguridad    | Comprobabilidad  | Usabilidad                                         |
| Fiabilidad   | Adaptabilidad    | Reusabilidad                                       |
| Flexibilidad | Modularidad      | Eficiencia                                         |
| Robustez     | Complejidad      | Facilidad para que el usuario aprenda a utilizarlo |
-->
<table>
<thead>
<tr>
<th style="text-align:left"></th>
<th style="text-align:left"></th>
<th style="text-align:left"></th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Protección</td>
<td style="text-align:left">Comprensibilidad</td>
<td style="text-align:left">Portabilidad</td>
</tr>
<tr>
<td style="text-align:left">Seguridad</td>
<td style="text-align:left">Comprobabilidad</td>
<td style="text-align:left">Usabilidad</td>
</tr>
<tr>
<td style="text-align:left">Fiabilidad</td>
<td style="text-align:left">Adaptabilidad</td>
<td style="text-align:left">Reusabilidad</td>
</tr>
<tr>
<td style="text-align:left">Flexibilidad</td>
<td style="text-align:left">Modularidad</td>
<td style="text-align:left">Eficiencia</td>
</tr>
<tr>
<td style="text-align:left">Robustez</td>
<td style="text-align:left">Complejidad</td>
<td style="text-align:left">Facilidad para que el usuario aprenda a utilizarlo</td>
</tr>
</tbody>
</table>

----

### ATRIBUTOS DE LA CALIDAD DEL SOFTWARE
<!-- .slide: class="final" -->

1. **Protección:** Capacidad del sistema para evitar accesos no autorizados o acciones maliciosas. Incluye control de acceso, manejo de roles, autenticación y autorización.

2. **Seguridad:** Abarca confidencialidad, integridad y disponibilidad de la información.

3. **Robustez:** Capacidad del software de mantenerse operativo ante fallas o entradas inválidas.

----

### ATRIBUTOS DE LA CALIDAD DEL SOFTWARE
<!-- .slide: class="final" -->

4. **Comprensibilidad:** Qué tan fácil es entender el código o la lógica del sistema.

5. **Complejidad:** Grado de dificultad en la estructura o lógica del software. Cuanto mayor la complejidad, más difícil de mantener.

6. **Modularidad:** Grado en que el sistema está dividido en módulos independientes y cohesivos.

7. **Comprobabilidad:** Facilidad con la que se puede verificar y probar el sistema para confirmar que cumple requisitos.

----

### ATRIBUTOS DE LA CALIDAD DEL SOFTWARE
<!-- .slide: class="final" -->

8. **Eficiencia:** Uso óptimo de recursos (CPU, memoria, red, tiempo de respuesta).

9. **Fiabilidad:** Capacidad del software para funcionar correctamente durante un tiempo determinado sin fallar.

10. **Flexibilidad:** Facilidad con la que el software puede adaptarse a nuevos requerimientos sin grandes cambios estructurales.

----

### ATRIBUTOS DE LA CALIDAD DEL SOFTWARE
<!-- .slide: class="final" -->

11. **Portabilidad:** Capacidad del sistema para ejecutarse en diferentes entornos o plataformas.

12. **Adaptabilidad:** Facilidad de ajustar el software a distintos contextos o necesidades.

13. **Reusabilidad:** Grado en que los componentes pueden ser reutilizados en otros proyectos o módulos.

----

### ATRIBUTOS DE LA CALIDAD DEL SOFTWARE
<!-- .slide: class="final" -->

14. **Usabilidad:** Facilidad con la que el usuario puede utilizar el sistema de forma efectiva, eficiente y satisfactoria.

15. **Facilidad de uso:** Relacionado con la usabilidad, pero enfocado en el tiempo y esfuerzo necesarios para aprender.

---

### Ejercicio: Atributos de Calidad
<!-- .slide: class="final" style="font-size: 0.80em" -->
Para cada uno de los siguientes ejemplos determine el atributo de calidad principal:

<p class="fragment">3. Robustez</p>
- Una API que responde con un error controlado (HTTP 400) en lugar de colapsar ante un input inesperado.

<p class="fragment">9. Fiabilidad</p>
- Un sistema de monitoreo que no pierde datos durante una semana de ejecución continua.

<p class="fragment">2. Seguridad</p>
- Cifrar contraseñas y asegurar conexiones con HTTPS.

----

### Ejercicio: Atributos de Calidad
<!-- .slide: class="final" style="font-size: 0.80em" -->
<p class="fragment">14. Usabilidad</p>
- Una interfaz clara con botones y mensajes comprensibles.

<p class="fragment">10. Flexibilidad</p>
- Agregar nuevos métodos de pago sin reescribir toda la lógica de facturación.

<p class="fragment">12. Adaptabilidad</p>
- Cambiar el idioma o la moneda sin reescribir el código fuente.

----

### Ejercicio: Atributos de Calidad
<!-- .slide: class="final" style="font-size: 0.80em" -->
<p class="fragment">13. Reusabilidad</p>
- Una librería de autenticación usada en varios microservicios.

<p class="fragment">5. Complejidad</p>
- Una función con 200 líneas y múltiples condicionales tiene alta complejidad ciclomática.

<p class="fragment">1. Protección</p>
- Un sistema que solo permite que los administradores borren datos críticos.

----

### Ejercicio: Atributos de Calidad
<!-- .slide: class="final" style="font-size: 0.80em" -->
<p class="fragment">4. Comprensibilidad</p>
- Un código bien comentado, con nombres descriptivos y arquitectura clara.
<p class="fragment">11. Portabilidad</p>
- Una aplicación que corre tanto en Linux como en Windows sin modificaciones.
<p class="fragment">8. Eficiencia</p>
- Una consulta SQL optimizada que evita cargar toda la tabla en memoria.

----

### Ejercicio: Atributos de Calidad
<!-- .slide: class="final" style="font-size: 0.80em" -->
<p class="fragment">7. Comprobabilidad</p>
- Tener tests automatizados, logs y trazas claras que faciliten la validación de comportamientos.

<p class="fragment">15. Facilidad de Uso</p>
- Una app intuitiva que un usuario nuevo puede dominar sin leer un manual.

<p class="fragment">6. Modularidad</p>
- Un backend dividido en servicios (auth, usuarios, pagos) que pueden desarrollarse y probarse por separado.

---

### [ISO 25010](https://iso25000.com/index.php/normas-iso-25000/iso-25010)
<!-- .slide: style="font-size: 0.80em" -->
La calidad del producto software se puede interpretar como el grado en que dicho producto satisface los requisitos de sus usuarios aportando de esta manera un valor.

El modelo de calidad del producto definido por la ISO/IEC 25010 se encuentra compuesto por las nueve características de calidad:

![Iso 25010](images/unidad11/iso25010.png)

----

### Las nueve características
<!-- .slide: style="font-size: 0.64em" -->

| Característica | Qué pregunta responde |
|---|---|
| **Adecuación funcional** | ¿Hace lo que tiene que hacer, completo y correcto? |
| **Eficiencia de desempeño** | ¿Responde a tiempo y usa bien los recursos bajo la carga esperada? |
| **Compatibilidad** | ¿Convive e interopera con los otros sistemas? |
| **Capacidad de interacción** | ¿Las personas lo pueden usar? Incluye **inclusividad** y asistencia al usuario |
| **Fiabilidad** | ¿Sigue funcionando a lo largo del tiempo y se recupera de las fallas? |
| **Seguridad** | ¿Protege la información y resiste el ataque? Incluye **resistencia** |
| **Mantenibilidad** | ¿Se puede entender, modificar y probar sin romperlo? |
| **Flexibilidad** | ¿Se adapta a otros entornos y crece? Incluye **escalabilidad** |
| **Seguridad operacional** *(safety)* | ¿Evita daños a personas, bienes o al ambiente? |

----

### Lo que cambió en 2023
<!-- .slide: style="font-size: 0.74em" -->

La versión vigente es **ISO/IEC 25010:2023**, publicada en noviembre de 2023, que reemplazó a la
de 2011. Los cambios no son cosméticos:

| 2011 | 2023 | Por qué |
|---|---|---|
| *Usabilidad* | **Capacidad de interacción** | El término viejo se confundía con "fácil de usar". Lo que se mide es la **capacidad del producto de sostener la interacción** |
| *Portabilidad* | **Flexibilidad** | Ya no se trata de mover software entre máquinas, sino de adaptarse y **escalar** |
| — | **Seguridad operacional** *(safety)* | Característica **nueva** de primer nivel. En 2011 no existía, y hoy el software gobierna autos, equipos médicos y redes eléctricas |
| *Accesibilidad* | **Inclusividad** + **asistencia al usuario** | Se partió en dos, y la inclusividad pasó a tener peso propio |
| *Estética de la interfaz* · *Madurez* | **Compromiso del usuario** · **Ausencia de fallas** | Nombres medibles en lugar de nombres opinables |

<div class="alerta">

**La lista de atributos de Sommerville que vimos antes es anterior a este modelo.** Sirve para
entender los conceptos, pero **lo que se usa en un contrato o en un plan de calidad es ISO 25010**,
porque tiene subcaracterísticas definidas y métricas asociadas en la familia ISO 25000.

</div>

<div class="fuente">

📎 [ISO 25010 en iso25000.com](https://iso25000.com/index.php/normas-iso-25000/iso-25010) ·
[Qué cambió en la versión 2023](https://quality.arc42.org/articles/iso-25010-update-2023)

</div>

---
### CALIDAD BASADA EN PROCESOS
* Relación directa entre procesos y productos
* Más complejo para software debido a:
  * Se requiere la aplicación de habilidades individuales y experiencia, lo cual es importante para el desarrollo de software 
  * Factores externos en las que una aplicación es novedosa o la necesidad para acelerar el
    calendario de desarrollo puede empeorar la calidad del producto
* Debe tenerse especial cuidado de no imponer estándares inapropiados

---
### CALIDAD DE PROCESOS PRACTICA
<!-- .slide: class="final" -->
* Definir procesos de estándares que indiquen como llevar a cabo las
  revisiones, la administración de la configuración, etc.
* Monitoriear el proceso de desarrollo para asegurar que se están siguiendo los estándares.
* Reportar estos procesos a la administración del proyecto.

---
### CALIDAD BASADA EN PROCESOS
<!-- .slide: class="final" -->
![Calidad Basada en Procesos](images/unidad11/proceso-de-calidad.png)

---
### ESTÁNDARES DE SOFTWARE
* Son clave para un efectivo manejo de calidad
* Puede ser un proyecto internacional, nacional, o organizacional
* Los estándares de producto definen características que todos los componentes deberán tener

---
### IMPORTANCIA DE LOS ESTÁNDARES
<!-- .slide: class="final" -->
* Reúne las mejores practicas
* Evita la repetición de errores pasados 
* Proporciona un marco para el análisis de calidad - involucra verificar la conformidad con estándares
* Proporcionar continuidad. El personal nuevo puede entender a la organización entendiendo a los estándares aplicados

---
### ESTÁNDARES DE PRODUCTOS Y PROCESOS
<!-- .slide: class="final" style="font-size: 0.80em" -->
<!--
| Estándares de producto                    | Estándares de proceso                             |
|:------------------------------------------|:--------------------------------------------------|
| Formato de revisión de diseño             | Realizar revisión del diseño                      |
| Estructura de documento de requerimientos | Enviar nuevo código para construcción del sistema |
| Formato de encabezado por método          | Proceso de liberación de versión                  |
| Estilo de programación Java               | Proceso de aprobación del plan del proyecto       |
| Formato de plan de proyecto               | Proceso de control de cambio                      |
| Formato de solicitud de cambio            | Proceso de registro de prueba                     |
-->
<table>
<thead>
<tr>
<th style="text-align:left">Estándares de producto</th>
<th style="text-align:left">Estándares de proceso</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Formato de revisión de diseño</td>
<td style="text-align:left">Realizar revisión del diseño</td>
</tr>
<tr>
<td style="text-align:left">Estructura de documento de requerimientos</td>
<td style="text-align:left">Enviar nuevo código para construcción del sistema</td>
</tr>
<tr>
<td style="text-align:left">Formato de encabezado por método</td>
<td style="text-align:left">Proceso de liberación de versión</td>
</tr>
<tr>
<td style="text-align:left">Estilo de programación Java</td>
<td style="text-align:left">Proceso de aprobación del plan del proyecto</td>
</tr>
<tr>
<td style="text-align:left">Formato de plan de proyecto</td>
<td style="text-align:left">Proceso de control de cambio</td>
</tr>
<tr>
<td style="text-align:left">Formato de solicitud de cambio</td>
<td style="text-align:left">Proceso de registro de prueba</td>
</tr>
</tbody>
</table>

---
### PROBLEMAS CON ESTÁNDARES
* No son vistos como relevantes ni se encuentran actualizados por los ingenieros de software
* Involucra actividades burocráticas
* No soportado por herramientas de software por lo que se requieren actividades manuales para mantener los estándares

----

### PROBLEMAS CON ESTÁNDARES
<!-- .slide: class="final" -->
* Involucrar a los desarrolladores. Los Ingenieros deberán entender la racionalidad bajo un estándar.
* Revisión de estándares y su uso regularmente. Los estándares pueden rápidamente estar desactualizados lo cual reduce su credibilidad entre sus usuarios
* Los estándares detallados deberán tener asociado una herramienta de soporte

---
### PROBLEMAS CON ESTÁNDARES
<!-- .slide: class="final" -->
**Excesivo trabajo manual es el más significante reclamo en contra de los estándares**

---

### Estándares Hoy

Muchos aspectos de los estándares están automatizados o integrados en herramientas de desarrollo.
Eso redujo la burocracia, ya que se vigilan o aplican automáticamente.

----

### Estándares Hoy
<!-- .slide: style="font-size: 0.80em" -->
Algunos ejemplos concretos:
- **Estándares de codificación y estilo:**	ESLint, Prettier, SonarLint, Pylint, Checkstyle
- **Control de calidad estática:** [SonarQube](https://www.sonarsource.com/es/products/sonarqube/), Code Climate, Codacy
- **Gestión de pruebas y trazabilidad:** Xray, Zephyr, TestRail, GitHub Actions con reportes de test
- **Integración continua y revisión:** Jenkins, GitHub Actions, GitLab CI/CD
- **Seguridad y cumplimiento:** Snyk, OWASP Dependency-Check, GitHub Dependabot
- **Mantenibilidad y métricas:** [SonarQube](https://www.sonarsource.com/es/products/sonarqube/), CodeScene, K6, Lighthouse

---
### ISO 9000 - ISO 9001
* Conjunto de estándares internacionales para el manejo de calidad
* Aplicable a un rango de organizaciones desde industrias de servicio a industrias de manufactura
* La ISO 9001 es aplicable a organizaciones que diseñan, desarrollan y mantienen productos
* ISO 9001 es un modelo genérico del proceso de calidad. Está instanciado para cada organización

----

### ISO 9001: la versión vigente
<!-- .slide: style="font-size: 0.76em" -->

<div class="alerta">

**Atención a la fecha.** La versión que rigió durante una década fue **ISO 9001:2015**. El
**16 de septiembre de 2026** se publicó **ISO 9001:2026**, sexta edición, que reemplaza a la de
2015 e incorpora la enmienda de **acción climática** de 2024.

</div>

* Las organizaciones ya certificadas tienen un **período de transición** —del orden de tres años—
  para migrar sus certificados. Conviene confirmarlo con el organismo certificador.
* La estructura de alto nivel y el enfoque a procesos se mantienen: lo que cambia es el énfasis en
  el **contexto**, el **riesgo** y, ahora, las **cuestiones climáticas** como parte del contexto de
  la organización.

**Lo importante como ingenieros:** ISO 9001 certifica que la organización **tiene un proceso y lo
sigue**. No certifica que el producto sea bueno. Una empresa puede estar certificada y entregar
software malo de manera perfectamente documentada y repetible.

----

### Madurez de procesos: CMMI
<!-- .slide: style="font-size: 0.76em" -->

Donde ISO 9001 pregunta *"¿tenés un proceso?"*, **CMMI** pregunta *"¿qué tan bueno es?"*.

* La versión vigente es **CMMI v3.0**, de 2023. Desde enero de 2024 **solo se evalúa con v3.0**:
  las versiones anteriores quedaron fuera de servicio.
* v3.0 amplió el alcance más allá del desarrollo: incorpora **seguridad**, **safety**, **gestión de
  datos**, gestión de personas y **trabajo remoto**.
* Existe además un modelo complementario de **madurez en IA** para organizaciones que incorporan
  sistemas de inteligencia artificial a sus procesos.

**Cuidado con el nombre:** el viejo **CMM** ya no existe. Si una bibliografía dice "nivel CMM 3",
está hablando de un modelo retirado.

---
### CERTIFICACIÓN ISO
<!-- .slide: class="final" -->
* Los Estándares de calidad y procedimientos deberán ser documentados en un manual organizacional de calidad
* Personal externo puede certificar que una organización conforma con los estándares ISO 9000/9001
* Los clientes demandan cada vez mas que los productos tengan la certificación ISO 9000/9001

---
### ISO 9001
<!-- .slide: class="final" -->
![ISO 9001](images/unidad11/iso9001.png)

---
### ISO 9001 Y MANEJO DE CALIDAD
<!-- .slide: class="final" -->
![Manejo de Calidad](images/unidad11/manejo-de-calidad.png)

---
### REVISIÓN
<!-- .slide: style="font-size: 0.90em" -->
* Es el principal método de validación de la calidad de un proceso o de un producto
* Un grupo debe examinar parte o toda su documentación para buscar problemas potenciales
* Hay diferentes tipos de revisiones con diferentes objetivos
  * Inspecciones para remover defectos (producto)
  * Revisiones para estimación de progresos (procesos y producto)
  * Revisiones de calidad (estándares y producto)

---
### PROCEDIMIENTOS DE REVISIÓN
<!-- .slide: class="final" -->
* Función de calidad - Es parte del proceso general de administración de calidad
* Función de administración del proyecto - proveen información para los administradores del proyecto
* Funciones de comunicación. Paso de conocimientos entre miembros del equipo

---
### REVISIONES DE CALIDAD
* Un grupo de personas cuidadosamente examinará cada parte o todo un sistema de software y su documentación asociada
* Código, diseños, especificaciones, planes de prueba, estándares, etc. todo puede ser revisado
* Documentos o Software puede ser “firmados” en cada revisión lo cual significa que la administración ha
aprobado el progreso de la siguiente etapa del desarrollo

---
### REVISIONES DE CALIDAD
<!-- .slide: class="final" -->
* El objetivo es descubrir defectos en el sistema e inconsistencias
* Cualquier documento producido en el proceso puede ser revisado
* El equipo de revisión deberá ser relativamente pequeño y las revisiones deberán ser relativamente cortas
* La revisión deberá ser grabada y almacenada

---
### TIPOS DE REVISIONES
<!-- .slide: style="font-size: 0.60em" -->
<!--
| Tipo de Revisión                  | Propósito Principal                                                                                                                                                                                                                                                                                                     |
|:----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inspecciones de diseño o programa | Detectar errores detallados en el diseño o código y comprobar si se han seguido las normas. La revisión debe basarse en una lista de verificación de posibles errores.                                                                                                                                                  |
| Revisiones de progreso            | Proporcionar información a la dirección sobre el progreso general del proyecto. Se trata de un proceso y una revisión del producto y se ocupa de costos, planes y cronogramas.                                                                                                                                          |
| Revisiones de calidad             | Realizar un análisis técnico de los componentes o la documentación del producto para encontrar fallas o desajustes entre la especificación y el diseño, código o documentación. También puede estar relacionado con cuestiones de calidad más amplias, como el cumplimiento de estándares y otros atributos de calidad. |
-->
<table>
<thead>
<tr>
<th style="text-align:left">Tipo de Revisión</th>
<th style="text-align:left">Propósito Principal</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Inspecciones de diseño o programa</td>
<td style="text-align:left">Detectar errores detallados en el diseño o código y comprobar si se han seguido las normas. La revisión debe basarse en una lista de verificación de posibles errores.</td>
</tr>
<tr>
<td style="text-align:left">Revisiones de progreso</td>
<td style="text-align:left">Proporcionar información a la dirección sobre el progreso general del proyecto. Se trata de un proceso y una revisión del producto y se ocupa de costos, planes y cronogramas.</td>
</tr>
<tr>
<td style="text-align:left">Revisiones de calidad</td>
<td style="text-align:left">Realizar un análisis técnico de los componentes o la documentación del producto para encontrar fallas o desajustes entre la especificación y el diseño, código o documentación. También puede estar relacionado con cuestiones de calidad más amplias, como el cumplimiento de estándares y otros atributos de calidad.</td>
</tr>
</tbody>
</table>


---
### INSPECCIONES DEL PROGRAMA
<!-- .slide: class="final" style="font-size: 0.60em" -->
<!--
| Clase de falla    | Comprobación de inspección                                                               |
|:------------------|:-----------------------------------------------------------------------------------------|
| Fallas de datos   | * ¿Todas las variables del programa se inician antes de usar sus valores?                |
|                   | * ¿Todas las constantes tienen nombre?                                                   |
|                   | * ¿La cota superior de los arreglos es igual al tamaño del arreglo o Valor - 1?          |
|                   | * Si se usan cadenas de caracteres, ¿se asigna explicitamente un delimitador?            |
|                   | * ¿Existe alguna posibilidad de desbordamiento de buffer?                                |
| Fallas de control | * Para cada enunciado condicional, ¿la condición es correcta?                            |
|                   | * ¿Hay certeza de que termine cada ciclo?                                                |
|                   | * ¿Los enunciados compuestos están correctamente colocados entre paréntesis?             |
|                   | * En caso de enunciados, ¿se justifican todos los casos posibles?                        |
|                   | * Si después de cada caso en los enunciados se requiere un paréntesis, ¿éste se incluyó? |
-->
<table>
<thead>
<tr>
<th style="text-align:left">Clase de falla</th>
<th style="text-align:left">Comprobación de inspección</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Fallas de datos</td>
<td style="text-align:left">* ¿Todas las variables del programa se inician antes de usar sus valores?</td>
</tr>
<tr>
<td style="text-align:left"></td>
<td style="text-align:left">* ¿Todas las constantes tienen nombre?</td>
</tr>
<tr>
<td style="text-align:left"></td>
<td style="text-align:left">* ¿La cota superior de los arreglos es igual al tamaño del arreglo o Valor - 1?</td>
</tr>
<tr>
<td style="text-align:left"></td>
<td style="text-align:left">* Si se usan cadenas de caracteres, ¿se asigna explicitamente un delimitador?</td>
</tr>
<tr>
<td style="text-align:left"></td>
<td style="text-align:left">* ¿Existe alguna posibilidad de desbordamiento de buffer?</td>
</tr>
<tr>
<td style="text-align:left">Fallas de control</td>
<td style="text-align:left">* Para cada enunciado condicional, ¿la condición es correcta?</td>
</tr>
<tr>
<td style="text-align:left"></td>
<td style="text-align:left">* ¿Hay certeza de que termine cada ciclo?</td>
</tr>
<tr>
<td style="text-align:left"></td>
<td style="text-align:left">* ¿Los enunciados compuestos están correctamente colocados entre paréntesis?</td>
</tr>
<tr>
<td style="text-align:left"></td>
<td style="text-align:left">* En caso de enunciados, ¿se justifican todos los casos posibles?</td>
</tr>
<tr>
<td style="text-align:left"></td>
<td style="text-align:left">* Si después de cada caso en los enunciados se requiere un paréntesis, ¿éste se incluyó?</td>
</tr>
</tbody>
</table>


----

### INSPECCIONES DEL PROGRAMA
<!-- .slide: class="final" style="font-size: 0.50em" -->
<!--
| Clase de falla                      | Comprobación de inspección                                                                                      |
|:------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| Fallas de entrada/salida            | * ¿Se usan todas las variables de entrada?                                                                      |
|                                     | * ¿A todas las variables de salida se les asigna un valor antes de que se produzcan?                            |
|                                     | * ¿Entradas inesperadas pueden causar corrupción?                                                               |
| Fallas de interfaz                  | * ¿Todas las llamadas a función y método tienen el número correcto de parámetros?                               |
|                                     | * ¿Los tipos de parámetro formal y real coinciden?                                                              |
|                                     | * ¿Los parámetros están en el orden correcto?                                                                   |
|                                     | * Si los componentes acceden a memoria compartida, ¿tienen el mismo modelo de estructura de memoria compartida? |
| Fallas de gestión de almacenamiento | * Si se modifica una estructura vinculada, ¿todos los vinculos se reasignan correctamente?                      |
|                                     | * Si se usa almacenamiento dinámico, ¿el espacio se asignó correctamente.                                       |
|                                     | * ¿El espacio se cancela explícitamente después de que ya no se requiere?                                       |
| Fallas de gestión de excepción      | * ¿Se tomaron en cuenta todas las posibles condiciones de error?                                                |
-->
<table>
<thead>
<tr>
<th style="text-align:left">Clase de falla</th>
<th style="text-align:left">Comprobación de inspección</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Fallas de entrada/salida</td>
<td style="text-align:left">* ¿Se usan todas las variables de entrada?</td>
</tr>
<tr>
<td style="text-align:left"></td>
<td style="text-align:left">* ¿A todas las variables de salida se les asigna un valor antes de que se produzcan?</td>
</tr>
<tr>
<td style="text-align:left"></td>
<td style="text-align:left">* ¿Entradas inesperadas pueden causar corrupción?</td>
</tr>
<tr>
<td style="text-align:left">Fallas de interfaz</td>
<td style="text-align:left">* ¿Todas las llamadas a función y método tienen el número correcto de parámetros?</td>
</tr>
<tr>
<td style="text-align:left"></td>
<td style="text-align:left">* ¿Los tipos de parámetro formal y real coinciden?</td>
</tr>
<tr>
<td style="text-align:left"></td>
<td style="text-align:left">* ¿Los parámetros están en el orden correcto?</td>
</tr>
<tr>
<td style="text-align:left"></td>
<td style="text-align:left">* Si los componentes acceden a memoria compartida, ¿tienen el mismo modelo de estructura de memoria compartida?</td>
</tr>
<tr>
<td style="text-align:left">Fallas de gestión de almacenamiento</td>
<td style="text-align:left">* Si se modifica una estructura vinculada, ¿todos los vinculos se reasignan correctamente?</td>
</tr>
<tr>
<td style="text-align:left"></td>
<td style="text-align:left">* Si se usa almacenamiento dinámico, ¿el espacio se asignó correctamente.</td>
</tr>
<tr>
<td style="text-align:left"></td>
<td style="text-align:left">* ¿El espacio se cancela explícitamente después de que ya no se requiere?</td>
</tr>
<tr>
<td style="text-align:left">Fallas de gestión de excepción</td>
<td style="text-align:left">* ¿Se tomaron en cuenta todas las posibles condiciones de error?</td>
</tr>
</tbody>
</table>

---

### Lo que hoy revisa una máquina
<!-- .slide: style="font-size: 0.66em" -->

Las listas de verificación de las dos slides anteriores son de la era de C: punteros,
delimitadores de cadena, desbordamiento de *buffer*, liberación manual de memoria. **Casi todo eso
hoy lo detecta una herramienta antes de que el código llegue a una revisión humana.**

| Lo que antes se revisaba a mano | Quién lo hace hoy |
|---|---|
| Estilo, formato, nombres | *Linters* y formateadores automáticos (ESLint, Prettier, Pylint) |
| Variables sin inicializar, código muerto, complejidad | Análisis estático: **SAST**, SonarQube |
| Vulnerabilidades en dependencias | **SCA** y alertas automáticas de dependencias |
| Secretos filtrados en el repositorio | Escaneo de secretos en el *pipeline* |
| Que los tests pasen y la cobertura no baje | Integración continua, obligatoria antes de fusionar |

----

### Entonces, ¿qué revisa una persona?
<!-- .slide: style="font-size: 0.70em" -->

La revisión humana se corrió hacia **lo que ninguna herramienta puede juzgar**:

<div class="grid-item">

1. **¿Resuelve el problema correcto?** Es la pregunta que más defectos encuentra, y ninguna
   herramienta la puede hacer.
2. **¿Las reglas de negocio están bien interpretadas?** Comparar el código contra la
   especificación, no contra sí mismo.
3. **¿Los casos borde están contemplados?** Concurrencia, valores límite, qué pasa cuando el
   sistema externo no responde.
4. **¿Se entiende?** Si el revisor necesita que le expliquen, el próximo que lo lea tampoco va a
   entender.
5. **¿El diseño es el adecuado**, o resuelve hoy y complica mañana?
6. **¿Los tests prueban el comportamiento** o prueban la implementación?

</div>

**La regla que cambió:** si una observación de una revisión se puede automatizar, **se automatiza**
y no se vuelve a discutir nunca más. Discutir comas en una revisión es desperdiciar el recurso más
caro del proceso.

<div class="fuente">

📎 El reclamo de la slide anterior —*"excesivo trabajo manual"*— se resolvió justamente así.

</div>

---

### Proceso de Revisión de Software
<!-- .slide: class="final" -->

![Proceso de Revisión de Software](images/unidad11/proceso-de-revision.png)

---
### MÉTRICAS DE LA CALIDAD DEL PRODUCTO
* Una métrica de calidad deberá ser una forma de predicción de la calidad del producto
* La mayoría de las métricas de calidad existentes son las métricas de la calidad
  del diseño las cuales se relacionan con la medición del acoplamiento o la complejidad del diseño

---
### MÉTRICAS DE CONTROL Y PREDICCIÓN
<!-- .slide: class="final" -->
![Métricas de Control y Predicción](images/unidad11/metricas-control-prediccion.png)

---
### SUPOSICIÓN DE MÉTRICAS
* Una propiedad del software puede ser medida
* Existe una relación entre lo que se puede medir y que se quiere conocer
* Esta relación ha sido formalizada y validada
* Puede ser difícil relacionar que puede ser medido en cuanto a atributos deseables de calidad

---
### ATRIBUTOS INTERNOS Y EXTERNOS
<!-- .slide: class="final" -->
![Atributos Internos y Externos](images/unidad11/atributos-internos-externos.png)

---
### MÉTRICAS ESTÁTICAS DE PRODUCTOS DE SOFTWARE
* Fan-in/Fan-Out
* Longitud de código
* Complejidad Ciclomática
* Longitud de identificadores
* Profundidad de anidado condicional
* Índice Fog

----

### MÉTRICAS ESTÁTICAS DE PRODUCTOS DE SOFTWARE
<!-- .slide: class="final" style="font-size: 0.70em" -->
* **Fan-in/Fan-Out:** Fan-in (abanico de entrada) es una medida del número de funciones o métodos que llaman a otra 
función o método (por ejemplo, X). Fan-out (abanico de salida) es el número de funciones a las que llama la función X. 
Un valor alto para fan-in significa que X está estrechamente acoplado con el resto del diseño y que los cambios a X 
tendrán extensos efectos dominó. Un valor alto de fan-out sugiere que la complejidad global de X puede ser alta debido 
a la complejidad de la lógica de control necesaria para coordinar los componentes llamados.
* **Longitud de código:** Ésta es una medida del tamaño de un programa. Por lo general, cuanto más grande sea el tamaño 
del código de un componente, más probable será que el componente sea complejo y proclive a errores. Se ha demostrado que 
la longitud del código es una de las métricas más fiables para predecir la proclividad al error en los componentes.

----

### MÉTRICAS ESTÁTICAS DE PRODUCTOS DE SOFTWARE
<!-- .slide: class="final" -->
* **Complejidad Ciclomática:** Ésta es una medida de la complejidad del control de un programa. Tal complejidad del 
control puede relacionarse con la comprensibilidad del programa.
* **Longitud de identificadores:** Ésta es una medida de la longitud promedio de los identificadores (nombres para 
variables, clases, métodos, etc) en un programa. Cuanto más largos sean los identificadores, es más probable que 
sean significativos y, por ende, más comprensible será el programa.

----

### MÉTRICAS ESTÁTICAS DE PRODUCTOS DE SOFTWARE
<!-- .slide: class="final" -->
* **Profundidad de anidado condicional:** Ésta es una medida de la profundidad de anidado de los enunciados if en un 
programa. Los enunciados if profundamente anidados son difíciles de entender y proclives potencialmente a errores.
* **Índice Fog:** Ésta es una medida de la longitud promedio de las palabras y oraciones en los documentos. Cuanto más 
alto sea el valor del índice Fog de un documento, más difícil será entender el documento.

---
### MÉTRICAS ORIENTADAS a OBJETOS
<!-- .slide: class="final" -->
* Métodos ponderados por clase
* Profundidad de árbol de herencia
* Número de hijos
* Acoplamiento entre clases de objetos
* Respuesta por clase
* Falta de cohesión en métodos

----

### MÉTRICAS ORIENTADAS a OBJETOS
<!-- .slide: class="final" style="font-size: 0.75em" -->
* **Métodos ponderados por clase:** Éste es el número de métodos en cada clase, ponderado por la complejidad de cada 
método. Por lo tanto, un método simple puede tener una complejidad de 1, y un método grande y complejo tendrá un valor 
mucho mayor. Cuanto más grande sea el valor para esta métrica, más compleja será la case de objeto. Es más probable que 
los objetos complejos sean más dificiles de entender. Tal vez no sean lógicamente cohesivos, por lo que no pueden 
reutilizarse de manera efectiva como supercases en un árbol de herencia.
* **Profundidad de árbol de herencia:** Esto representa el número de niveles discretos en el árbol de herencia en que 
las subclases heredan atributos y operaciones (métodos) de las superclases. Cuanto más profundo sea el árbol de herencia, 
más complejo será el diseño. Es posible que tengan que comprenderse muchas clases de objetos para entender las clases de 
objetos en las hojas del árbol.

----

### MÉTRICAS ORIENTADAS a OBJETOS
<!-- .slide: class="final" style="font-size: 0.75em" -->
* **Número de hijos:** Ésta es una medida del número de subclases inmediatas en una clase. Mide la amplitud de una 
jerarquia de clase, mientras que DIT mide su profundidad. Un valor alto de NOC puede indicar mayor reutilización. Podria 
significar que debe realizarse más esfuerzo para validar las clases base, debido al número de subclases que dependen 
de ellas.
* **Acoplamiento entre clases de objetos:** Las clases están acopladas cuando los métodos en una clase usan los métodos o 
variables de instancia definidos en una clase diferente. CBO es una medida de cuánto acoplamiento existe. Un valor alto 
para CBO significa que las clases son estrechamente dependientes y, por lo tanto, es más probable que el hecho de cambiar 
una clase afecte a otras clases en el programa.

----

### MÉTRICAS ORIENTADAS a OBJETOS
<!-- .slide: class="final" style="font-size: 0.75em" -->
* **Respuesta por clase:** RFC es una medida del número de métodos que potencialmente podrían ejecutarse en respuesta a 
un mensaje recibido por un objeto de dicha clase. Nuevamente, RFC se relaciona con la complejidad. Cuanto más alto sea 
el valor para RFC, más compleja será una case y, por ende, es más probable que incluya errores.
* **Falta de cohesión en métodos:** LCOM se calcula al considerar pares de métodos en una clase. LCOM es la diferencia 
entre el número de pares de método sin compartir atributos y el número de pares de método con atributos compartidos. El 
valor de esta métrica se debate ampliamente y existe en muchas variaciones. No es claro si realmente agrega alguna 
información útil además de la proporcionada por otras métricas.

---
### PROCESO DE MEDICIÓN DEL PRODUCTO
<!-- .slide: class="final" -->
![Medición del Producto](images/unidad11/medicion-del-producto.png)

---
### MANTENIBILIDAD DEL DISEÑO
* **Cohesión:** Cuanto están relacionadas las partes forman un componente.
* **Acoplamiento:** Que tan independiente es un componente.
* **Entendibilidad:** Que tan fácil es entender las funciones de un componente.
* **Adaptabilidad:** Que tan fácil es cambiar un componente.

---
### MÉTRICAS DE ACOPLAMIENTO
<!-- .slide: class="final" -->
* Asociado con la medida ‘fan-in y fan-out’.
* Alta entrada (fan-in)- implica un alto acoplamiento debido a las dependencias de los módulos.
* Alta salida (fan-out)- implica un alto acoplamiento debido a la complejidad del control

---
### MÉTRICAS DE CALIDAD EN UN PROGRAMA
<!-- .slide: class="final" style="font-size: 0.85em" -->
* Las métricas de diseño son también aplicables a programas.
* Otras métricas incluyen:
  * Longitud. El tamaño del código fuente del programa.
  * Complejidad ciclomatica. La complejidad de control de un programa.
  * Longitud de identificadores 
  * Profundidad de condicionales anidados
* Los valores anómalos de las métricas sugieren que un componente presenta defectos o es difícil de entender

---
### CONSIDERACIONES PARA LAS MÉTRICAS
<!-- .slide: class="final" -->
* La longitud del código es simple pero la experimentación ha sugerido que
representa un buen predictor de problemas
* La complejidad ciclomatica puede ser engañosa
* Nombres largos deberán incrementar la entendibilidad de un programa
* Condicionales profundamente anidadas son difíciles de entender.

---
### MÉTRICAS DE COMPLEJIDAD
La complejidad ciclomatica es una medida de cuanto una estructura es compleja:

M = Complejidad ciclomática.

A = Número de arcos del grafo.

N = Número de nodos del grafo

M = A − N + 2

---
![Grafos](images/unidad11/grafo.jpg)
<!-- .slide: class="final" -->

---

Grafo numerando nodos y aristas. **M=8-7+2**
<!-- .slide: class="final" -->

---
### MÉTRICAS DE CALIDAD DE LA DOCUMENTACIÓN
<!-- .slide: class="final" -->
* La legibilidad es importante en la documentación
* El índice “Gunnings Fog” es una medida de la legibilidad
  * Basada en la longitud de las frases y el número de sílabas en una palabra
  * Esto puede causar malas interpretaciones cuando se aplica a la documentación técnica.

---
### MADUREZ DE LAS MÉTRICAS
* Las métricas de **producto** todavía tienen un valor limitado y no ampliamente aceptado.
* Las relaciones entre lo que se puede medir y lo que se quiere conocer no están bien
  comprendidas aún.
* Hace falta poner de acuerdo a las organizaciones sobre las métricas necesarias en el proceso de
  software.

<div class="alerta">

**Esto era cierto para las métricas de producto, y en buena medida lo sigue siendo.** Pero entre
2011 y hoy aparecieron métricas de **proceso de entrega** que sí tienen consenso y evidencia
empírica. Ver las dos slides siguientes.

</div>

----

### Métricas DORA
<!-- .slide: style="font-size: 0.70em" -->

Surgieron de un programa de investigación con decenas de miles de respuestas a lo largo de una
década. Son **cuatro** métricas, y la clave es que se miden **en el sistema**, no se opinan:

| Métrica | Qué mide | Por qué importa |
|---|---|---|
| **Frecuencia de despliegue** | Cada cuánto se pone algo en producción | Lotes chicos fallan menos y se arreglan más rápido |
| **Lead time del cambio** | Desde que se *commitea* hasta que está en producción | Mide la capacidad real de responder |
| **Tasa de fallas del cambio** | Qué porcentaje de despliegues provoca una falla | Es el contrapeso: desplegar rápido y mal no cuenta |
| **Tiempo de recuperación** | Cuánto se tarda en recuperarse de un despliegue fallido | Asume que va a fallar, y mide la resiliencia |

En el informe de **2025** se agregó una quinta, la **tasa de retrabajo**, y se dejó de clasificar a
los equipos en *bajo / medio / alto / elite* para describirlos en **siete perfiles** distintos.

<div class="alerta">

**El hallazgo contraintuitivo:** velocidad y estabilidad **no** se oponen. Los equipos que
despliegan más seguido tienen además **menos** fallas, porque los cambios son más chicos y el
problema se localiza antes.

</div>

----

### Medir personas es otra cosa
<!-- .slide: style="font-size: 0.72em" -->

DORA mide **el sistema de entrega**. Para la productividad de las personas y los equipos se usa el
marco **SPACE**, que insiste en una idea simple: **ninguna métrica aislada sirve**, y hay que mirar
al menos tres dimensiones a la vez.

<div class="grid-item">

**S**atisfacción y bienestar · **P**erformance (resultado, no actividad) ·
**A**ctividad · **C**omunicación y colaboración · **E**ficiencia y flujo

</div>

**La trampa clásica** —y el motivo por el que el marco existe— es medir **actividad** y llamarla
productividad: líneas de código, cantidad de *commits*, puntos de historia por persona. Todas se
pueden inflar sin producir nada de valor, y en cuanto se usan para evaluar personas, se inflan.

<div class="alerta">

**Ley de Goodhart:** cuando una medida se convierte en objetivo, deja de ser una buena medida.
Vale para la cobertura de tests, para la *velocity* y para las métricas DORA también.

</div>

---

## Temas que el libro no cubre
### Y que hoy son parte del plan de calidad

<!-- .slide: style="font-size: 0.68em" -->

| Tema | De qué se trata |
|---|---|
| **Deuda técnica** | Lo que se decide **no** hacer bien para entregar antes. No es un defecto: es un préstamo con intereses. Se mide y se gestiona; se vuelve problema cuando es invisible |
| **Shift-left** | Mover la verificación lo más temprano posible. Un defecto encontrado en requerimientos cuesta **órdenes de magnitud** menos que en producción |
| **DevSecOps** | La seguridad deja de ser una auditoría final y pasa a ser una etapa del *pipeline*: SAST, DAST, SCA y escaneo de secretos en cada cambio |
| **SBOM** | El inventario de todo lo que tu software incluye de terceros. Responde *"¿estoy afectado por esta vulnerabilidad?"* en minutos y no en semanas |
| **Accesibilidad** | **WCAG 2.2** como estándar técnico. En la Unión Europea es **exigible desde 2025** para productos y servicios digitales. Es la subcaracterística *inclusividad* de ISO 25010 |
| **Observabilidad** | Logs, métricas y trazas. La calidad en producción no se infiere: se observa |

<div class="alerta">

**El corrimiento de fondo:** en 2011 la calidad se verificaba **antes** de entregar. Hoy, con
entregas continuas, se verifica **durante** y se **observa después**. El plan de calidad ya no
termina en la puesta en producción.

</div>

---

## Ejercitación
### La calidad de TicketFr

<!-- .slide: style="font-size: 0.76em" -->

<div class="grid-item">

**Contexto.** Portal de eventos y venta de entradas. Entre los requisitos no funcionales
declarados hay uno explícito: sostener **5.000 compradores concurrentes** durante los primeros 10
minutos de una preventa, con respuesta **menor a 3 segundos** en la búsqueda y en la selección de
butacas. Maneja **pagos** por pasarela externa, **datos personales** y una **blacklist de
personas**.

</div>

<div class="fuente">

📎 [Caso integrador: portal de venta de entradas](U5_caso_integrador_ticketera.html)

</div>

----

### 💡 Ejercicio 1: Priorizar atributos de calidad
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.70em" -->

1. Tomá las **nueve características de ISO 25010:2023** y ordenalas por prioridad para TicketFr.
   Justificá las **tres primeras** y las **dos últimas** con una frase del enunciado.
2. Para cada una de las tres primeras, definí **una métrica concreta y un umbral**. No vale
   "que sea rápido": tiene que poder medirse y fallar.
3. ¿Aplica la característica **seguridad operacional** *(safety)* a este sistema? Argumentá las dos
   posiciones.
4. La **inclusividad** —subcaracterística de capacidad de interacción— ¿es un requisito deseable o
   exigible? ¿Cambia la respuesta según dónde se publique el portal?

<!--
1. Primeras esperables: eficiencia de desempeño (el RNF de la preventa es explicito), seguridad
   (pagos, datos personales, blacklist) y fiabilidad (si cae durante la preventa, el daño es
   irreversible: esa venta no vuelve). Ultimas: seguridad operacional y compatibilidad.
2. Lo que se corrige es que el umbral sea verificable. Bien: "percentil 95 del tiempo de
   respuesta de la seleccion de butacas por debajo de 3 s con 5.000 usuarios concurrentes,
   medido en prueba de carga". Mal: "buen rendimiento".
3. A favor de que NO aplica: no hay riesgo de dano fisico. A favor de que SI: el control de
   aforo. Si el sistema permite ingresar mas personas que la capacidad de la sala, hay riesgo
   real para la integridad de las personas. RN-056 del sistema existe por eso. Es el ejercicio
   que mas discusion genera y la respuesta correcta es la segunda.
4. Exigible. En la UE lo es desde 2025; y ademas es la via de acceso de personas con
   discapacidad a un servicio de venta al publico. La respuesta "deseable" se corrige.
-->

----

### 💡 Ejercicio 2: Plan de calidad
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.70em" -->

Redactá el **plan de calidad** de TicketFr siguiendo la estructura de Humphrey que vimos.
Mínimos exigidos:

1. **Metas de calidad:** las tres del ejercicio anterior, con métrica y umbral.
2. **Estándares de producto y de proceso:** uno de cada tipo, y **con qué herramienta** se verifica
   cada uno automáticamente.
3. **Revisiones:** qué artefactos se revisan, quién los revisa y con qué lista de verificación.
   ¿Qué de esa lista se puede automatizar?
4. **Riesgos de calidad:** tres, tomados del registro de riesgos de
   [Gestión de Proyectos](U10_gestion_de_proyectos.html).
5. **Métricas del proceso:** elegí dos métricas DORA con su objetivo, y justificá por qué esas.

<!--
2. Lo que se busca: que distingan producto de proceso. Producto: "toda funcion publica tiene
   prueba automatizada del camino feliz y de al menos una excepcion". Proceso: "ningun cambio se
   fusiona sin revision de otra persona y sin que el pipeline pase en verde".
3. La lista de verificacion mas valiosa para este sistema es la de consistencia entre la
   especificacion y el codigo: la reserva de 10 minutos, el limite de 6 entradas, el tratamiento
   de la pasarela sin respuesta. Nada de eso lo detecta una herramienta.
5. Lead time y tasa de fallas del cambio son la eleccion defendible: la primera porque el
   proyecto esta comprimido, la segunda porque una falla durante una preventa no se puede
   deshacer. Si eligen solo frecuencia de despliegue, hay que marcar que falta el contrapeso de
   estabilidad.
-->

----

### 💡 Ejercicio 3: Inspección de un requerimiento
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.66em" -->

Hacé una **inspección** del requerimiento **"Comprar entradas"** con esta especificación:

> **Precondición:** el comprador está autenticado, la función está publicada y tiene butacas
> reservadas con la reserva vigente.
> **Flujo:** verificar la reserva → verificar el límite de 6 entradas por función → calcular el
> total con descuentos → solicitar el pago a la pasarela → marcar las butacas como vendidas →
> emitir una entrada con QR por butaca → enviar por correo.
> **Excepciones:** reserva vencida · límite superado · pago rechazado · **pasarela sin respuesta**.

1. Para cada excepción, ¿el comportamiento está completamente definido? ¿Qué pasa con las butacas
   en cada caso?
2. **Dos compradores confirman la última butaca en el mismo instante.** ¿La especificación lo
   resuelve? ¿Qué atributo de calidad está en juego?
3. La pasarela **aprueba** un pago cuya reserva ya venció y cuyas butacas se revendieron.
   Clasificá el defecto: ¿es de requerimientos, de diseño o de implementación? ¿En qué etapa se
   debería haber detectado?
4. ¿Cuántos **casos de prueba** hacen falta para cubrir este requerimiento? Listalos.
5. ¿Cuáles de los defectos que encontraste los hubiera detectado una herramienta automática?

<!--
1. Reserva vencida: se liberan. Limite superado: se mantienen (no se consumio nada). Pago
   rechazado: se mantienen por el tiempo restante. Pasarela sin respuesta: NO se venden NI se
   liberan, y la compra queda pendiente. Ese ultimo es el unico que los alumnos suelen resolver
   mal, y es el que evita la sobreventa.
2. No lo resuelve el texto: hace falta decir explicitamente que la operacion es atomica y que
   solo una prospera. Atributos en juego: fiabilidad y adecuacion funcional (correccion).
3. De requerimientos. Es un hueco de especificacion, no un error de codigo: nadie definio que
   hacer. Se deberia haber detectado en la revision de la especificacion, que es justamente el
   argumento del shift-left: ahi cuesta una conversacion, en produccion cuesta una sobreventa
   con dinero cobrado.
4. Minimo 6: camino feliz, reserva vencida, limite superado, pago rechazado, pasarela sin
   respuesta, y concurrencia por la ultima butaca. Si alguien dice "uno por excepcion" le faltan
   el feliz y el de concurrencia.
5. Ninguno. Todos son defectos de especificacion y de reglas de negocio. Es el punto de la clase:
   la automatizacion se quedo con lo mecanico y le dejo a las personas exactamente esto.
-->

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)