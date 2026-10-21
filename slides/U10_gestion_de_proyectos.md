---
title: Gestión de Proyectos
theme: solarized
slideNumber: true
---

#### Ingeniería de Software
# Gestión de Proyectos
Created by <i class="fab fa-telegram"></i>
[edme88]("https://t.me/edme88")
Edit by F.A <!-- compelta aca con mi github -->

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

  .alta {
      background-color: #f8d7da; /* rojo claro */
      color: #721c24;
      font-weight: bold;
  }
  .moderada {
      background-color: #fff3cd; /* amarillo */
      color: #856404;
      font-weight: bold;
  }
  .grave {
      background-color: #f5c6cb; /* rojo más intenso */
      color: #721c24;
      font-weight: bold;
  }

  .catastrofico {
      background-color: #f5c6cb; /* rojo más intenso */
      color: #ff0019ff;
      font-weight: bold;
  }
  .tolerable {
      background-color: #cce5ff; /* azul claro */
      color: #004085;
      font-weight: bold;
  }
  .insignificante, .baja {
      background-color: #d4edda; /* verde claro */
      color: #155724;
      font-weight: bold;
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

# Ingeniería de Software
## Ian Sommerville

![Bibliografia](images/unidad10/ian-sommerville.png)

---
<!-- .slide: style="font-size: 0.78em" -->

## Temario
<div class="grid-container2">
<div class="grid-item">

### Gestión de Proyectos
* Proyecto
* Definición
* Elementos que incluye
* Cómo se gestiona
* Criterios de Éxito
* Gestión de proyectos de Software
* Actividades de los administradores
* Gestión del Riesgo
* Identificación del Riesgo

</div>
<div class="grid-item">

* Planeación del Riesgo
* Monitoreo del Riesgo
* Indicadores de Riesgo
* Gestión de Personal
* Factores
* Motivación del Personal
* Jerarquía de Necesidades Humanas
* Trabajo en Equipo
* Calendarización de Proyectos
</div>
</div>

---
### PROYECTO
Un proyecto es un esfuerzo temporal que se lleva a cabo para crear un producto, servicio o resultado único.

---
### PROYECTO
<!-- .slide: style="font-size: 0.90em" -->
* La naturaleza temporal de los proyectos implica que un proyecto tiene un principio y un final definidos.
* El final se alcanza cuando se logran los objetivos del proyecto, cuando se termina el proyecto porque sus objetivos 
no se cumplirán o no pueden ser cumplidos, o cuando ya no existe la necesidad que dio origen al proyecto.
* Implica la ejecución de un conjunto de actividades coordinadas y controladas para lograr un objetivo conforme a 
requisitos específicos, contemplando limitaciones de tiempo, costos y recursos.

---
![Gestión de Proyectos](images/unidad10/gestion-de-proyectos.jpg)

---
### GESTIÓN DE PROYECTOS DE SOFTWARE
* Actividades que aseguran que el software será entregado en el tiempo justo y estará de acuerdo
con los requerimientos del cliente.
* Es necesario porque el desarrollo estará siempre sujeto a las limitaciones de costos y tiempos de la empresa

---
![Administración de Proyecto](images/unidad10/proyecto-administracion.jpg)

---
![Dirección de Proyectos](images/unidad10/direccion-de-proyectos.jpg)

---
### ¿QUÉ INCLUYE LA DIRECCIÓN DE PROYECTOS?
* Identificar los requisitos
* Establecer objetivos claros y posibles de realizar
* Equilibrar las demandas concurrentes de calidad, alcance, tiempo y costos
* Adaptar las especificaciones, los planes y el enfoque a las diversas inquietudes y
expectativas de los diferentes interesados

---
### ¿CÓMO SE GESTIONA?
Siguiendo una metodología:
* Se proporciona una guía para conocer todo el camino a recorrer antes de iniciar.
* Se asegura la calidad del producto final
* Se asegura el cumplimiento de los tiempos establecidos
* Se asegura la utilización de los recursos limitados definidos

----

### Los marcos de referencia hoy
<!-- .slide: style="font-size: 0.72em" -->

| Marco | Qué es | Estado 2026 |
|---|---|---|
| **PMBOK Guide** (PMI) | El cuerpo de conocimiento más difundido | **8.ª edición**, publicada a fines de 2025. Reduce los principios de 12 a **6**, mantiene **7 dominios de desempeño**, reintroduce los grupos de proceso como **áreas de enfoque** y agrega por primera vez un **apéndice sobre IA** |
| **ISO 21502** | Norma internacional de dirección de proyectos | Vigente. PMBOK 8 se alinea con ella: el eje pasa a ser la **generación de valor** |
| **Scrum / Kanban** | Marcos de trabajo ágiles | Dominantes en software. Ver [Desarrollo Ágil](U4_1_desarrollo_agil.html) y [Scrum: Práctico](U4P_scrum_jira.html) |
| **CMMI** | Modelo de madurez de procesos | **v3.0** desde 2023. Desde 2024 solo se evalúa con v3.0, e incorpora seguridad, gestión de datos y trabajo remoto |

<div class="alerta">

**El cambio de fondo de PMBOK 7 y 8:** se dejó de describir el proyecto como una secuencia de
procesos a ejecutar y se pasó a **principios y dominios de desempeño**. La razón es que ninguna
secuencia única sirve para todos los proyectos: en software conviven lo predictivo y lo ágil.

</div>

---
![Fases del Proyecto](images/unidad10/fases-del-proyecto.jpg)

---
### CRITERIOS DE ÉXITO PARA LA GESTIÓN DEL PROYECTO
* Entregar el software al cliente en el tiempo acordado.
* Mantener costos dentro del presupuesto general.
* Entregar software que cumpla con las expectativas del cliente.
* Mantener un equipo de desarrollo óptimo y con buen funcionamiento

---
### CRITERIOS DE ÉXITO DEL PROYECTO
Lo importante es que las restricciones del proyecto esten en equilibrio.

![Restricciones](images/unidad10/restricciones.jpg)

---
### GESTIÓN DE PROYECTOS DE SOFTWARE
* El producto es intangible.
  * Los administradores de proyectos de software no pueden constatar el progreso con sólo
observar el artefacto que se construye.
* Los grandes proyectos de software con frecuencia son proyectos excepcionales. 
  * Los grandes proyectos de software en general son diferentes de los proyectos anteriores. 
* Los procesos de software son variables y específicos de la organización

---
### ACTIVIDADES DE LOS ADMINISTRADORES
<!-- .slide: style="font-size: 0.90em" -->
1. **Planeación del proyecto:** Son responsables de la planeación, estimación y
calendarización del desarrollo del proyecto, así como de la asignación de tareas a las personas. Supervisa
el trabajo y estandares. Monitorea el avance.
2. **Informes:** Son responsables de informar del avance de un proyecto a los clientes y administradores de la
compañía que desarrolla el software.
3. **Gestión del riesgo:** Tienen que valorar los riesgos que pueden afectar un proyecto, monitorizar dichos riesgos
y emprender acciones cuando surjan problemas.

---
### ACTIVIDADES DE LOS ADMINISTRADORES
4. **Gestión de personal:** Son responsables de administrar el equipo de personas. Deben elegir a los integrantes y 
establecer formas de trabajo que conduzcan a un desempeño efectivo del equipo.
5. **Redactar propuestas:** La propuesta describe los objetivos del proyecto y cómo se realizará. Por lo general,
incluye estimaciones de costo y calendarización, además de justificar por qué
el contrato del proyecto debería concederse a una organización o un equipo particular

---
### GESTIÓN DE PROYECTOS
![Proceso de Gestión de Proyectos](images/unidad10/proceso-gestion-proyectos.jpg)

---
### GESTIÓN DEL RIESGO
Un riesgo es la posibilidad de que una circunstancia adversa se pueda presentar.
1. **Riesgos del proyecto:** alteran el calendario o los recursos del proyecto.
2. **Riesgos del producto:** afectan la calidad o el rendimiento del software a desarrollar.
3. **Riesgos empresariales:** afectan a la organización que desarrolla o adquiere el software.

---
### GESTIÓN DEL RIESGO
Gestion del riesgo implica identificar los riesgos y generar planes para
minimizar sus efectos sobre el proyecto.

---
### EJEMPLOS
<!-- .slide: style="font-size: 0.60em" -->
<!--
| Riesgo                                    | Repercute en           | Descripción                                                                                       |
|:------------------------------------------|:-----------------------|:--------------------------------------------------------------------------------------------------|
| Rotación de personal                      | Proyecto               | Personal experimentado abandonará el proyecto antes de que éste termine.                          |
| Cambio administrativo                     | Proyecto               | Habrá un cambio de gestión en la organización con diferentes prioridades.                         |
| Indisponibilidad de hardware              | Proyecto               | Hardware, que es esencial para el proyecto, no se entregará a tiempo.                             |
| Cambio de requerimientos                  | Proyecto y producto    | Habrá mayor cantidad de cambios a los requerimientos que los anticipados.                         |
| Demoras en la especificación              | Proyecto y producto    | Especificaciones de interfaces esenciales no están disponibles a tiempo.                          |
| Subestimación del tamaño                  | Proyecto y producto    | Se subestimó el tamaño del sistema.                                                               |
| Obsolescencia tecnológica | Empresa                | La tecnología subyacente sobre la cual se construye el sistema se sustituye con nueva tecnología. |
| Competencia de productos                  | Empresa                | Un producto competitivo se comercializa antes de que el sistema está completo.                    |
-->
<table>
<thead>
<tr>
<th style="text-align:left">Riesgo</th>
<th style="text-align:left">Repercute en</th>
<th style="text-align:left">Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Rotación de personal</td>
<td style="text-align:left">Proyecto</td>
<td style="text-align:left">Personal experimentado abandonará el proyecto antes de que éste termine.</td>
</tr>
<tr>
<td style="text-align:left">Cambio administrativo</td>
<td style="text-align:left">Proyecto</td>
<td style="text-align:left">Habrá un cambio de gestión en la organización con diferentes prioridades.</td>
</tr>
<tr>
<td style="text-align:left">Indisponibilidad de hardware</td>
<td style="text-align:left">Proyecto</td>
<td style="text-align:left">Hardware, que es esencial para el proyecto, no se entregará a tiempo.</td>
</tr>
<tr>
<td style="text-align:left">Cambio de requerimientos</td>
<td style="text-align:left">Proyecto y producto</td>
<td style="text-align:left">Habrá mayor cantidad de cambios a los requerimientos que los anticipados.</td>
</tr>
<tr>
<td style="text-align:left">Demoras en la especificación</td>
<td style="text-align:left">Proyecto y producto</td>
<td style="text-align:left">Especificaciones de interfaces esenciales no están disponibles a tiempo.</td>
</tr>
<tr>
<td style="text-align:left">Subestimación del tamaño</td>
<td style="text-align:left">Proyecto y producto</td>
<td style="text-align:left">Se subestimó el tamaño del sistema.</td>
</tr>
<tr>
<td style="text-align:left">Obsolescencia tecnológica</td>
<td style="text-align:left">Empresa</td>
<td style="text-align:left">La tecnología subyacente sobre la cual se construye el sistema se sustituye con nueva tecnología.</td>
</tr>
<tr>
<td style="text-align:left">Competencia de productos</td>
<td style="text-align:left">Empresa</td>
<td style="text-align:left">Un producto competitivo se comercializa antes de que el sistema está completo.</td>
</tr>
</tbody>
</table>

---
### GESTIÓN DEL RIESGO
1. **Identificación del riesgo:** identificar posibles riesgos para el proyecto, el producto y la empresa.
2. **Análisis de riesgos:** valorar la probabilidad y las consecuencias de dichos riesgos.
3. **Planeación del riesgo:** elaborar planes para enfrentar el riesgo, evitarlo o minimizar sus efectos en el proyecto.
4. **Monitorización del riesgo:** valorar regularmente el riesgo y los planes para atenuarlo.

---
### GESTION DEL RIESGO – EL PROCESO
![Gestión del Riesgo](images/unidad10/gestion-del-riesgo.png)

---
### 1. IDENTIFICACIÓN DEL RIESGO
<!-- .slide: style="font-size: 0.80em" -->
1. **Riesgos tecnológicos:** Se derivan de las tecnologías de software o hardware usadas para desarrollar el sistema.
2. **Riesgos personales:** Se asocian con las personas en el equipo de desarrollo.
3. **Riesgos organizacionales:** Se derivan del entorno organizacional donde se desarrolla el software.
4. **Riesgos de herramientas:** Resultan de las herramientas de software y otro software de soporte
que se usa para desarrollar el sistema.
5. **Riesgos de requerimientos:** Proceden de cambios a los requerimientos del cliente y del proceso de gestionarlos.
6. **Riesgos de estimación:** Surgen de las estimaciones administrativas de los recursos requeridos para construir el sistema.

---
### EJEMPLOS
<!-- .slide: style="font-size: 0.40em" -->
<!--
| Tipo de riesgo  | Riesgos posibles                                                                                                                                                                                                                                |
|:----------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tecnología      | La base de datos que se usa en el sistema no puede procesar tantas transacciones por segundo como se esperaba. (1) <br> Los componentes de software de reutilización contienen defectos que haen que no puedan reutilizarse como se planeó. (2) |
| Personal        | Es imposible reclutar personal con las habilidades requeridas. (3) <br> El personal clave está enfermo e indispuesto en momentos críticos. (4) <br> No está disponible la capacitación requerida para el personal. (5)                          |
| De organización | La organización se reestructura de modo que diferentes administraciones son responsables del proyecto. (6) <br> Problemas financieros de la organización fuerzan reducciones en el presupuesto del proyecto. (7)                                |
| Herramientas    | El código elaborado por las herramientas de generación de código de software es ineficiente. (8) <br> Las herramientas de software no pueden trabajar en una forma integrada. (9)                                                               |
| Requerimientos  | Se proponen cambios a los requerimientos que demandan mayor trabajo de rediseño. (10) <br> Los clientes no entienden las repercusiones de los cambios a los requerimientos. (11)                                                                |
| Estimación      | Se subestima el tiempo requerido para desarrollar el software. (12) <br> Se subestima la tasa de reparación de defectos. (13) <br> Se subestima el tamaño del software. (14)                                                                    |
-->
<table>
<thead>
<tr>
<th style="text-align:left">Tipo de riesgo</th>
<th style="text-align:left">Riesgos posibles</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Tecnología</td>
<td style="text-align:left">La base de datos que se usa en el sistema no puede procesar tantas transacciones por segundo como se esperaba. (1) <br> Los componentes de software de reutilización contienen defectos que hacen que no puedan reutilizarse como se planeó. (2)</td>
</tr>
<tr>
<td style="text-align:left">Personal</td>
<td style="text-align:left">Es imposible reclutar personal con las habilidades requeridas. (3) <br> El personal clave está enfermo e indispuesto en momentos críticos. (4) <br> No está disponible la capacitación requerida para el personal. (5)</td>
</tr>
<tr>
<td style="text-align:left">De organización</td>
<td style="text-align:left">La organización se reestructura de modo que diferentes administraciones son responsables del proyecto. (6) <br> Problemas financieros de la organización fuerzan reducciones en el presupuesto del proyecto. (7)</td>
</tr>
<tr>
<td style="text-align:left">Herramientas</td>
<td style="text-align:left">El código elaborado por las herramientas de generación de código de software es ineficiente. (8) <br> Las herramientas de software no pueden trabajar en una forma integrada. (9)</td>
</tr>
<tr>
<td style="text-align:left">Requerimientos</td>
<td style="text-align:left">Se proponen cambios a los requerimientos que demandan mayor trabajo de rediseño. (10) <br> Los clientes no entienden las repercusiones de los cambios a los requerimientos. (11)</td>
</tr>
<tr>
<td style="text-align:left">Estimación</td>
<td style="text-align:left">Se subestima el tiempo requerido para desarrollar el software. (12) <br> Se subestima la tasa de reparación de defectos. (13) <br> Se subestima el tamaño del software. (14)</td>
</tr>
</tbody>
</table>

---
### Riesgos que el libro no trae
<!-- .slide: style="font-size: 0.64em" -->

La taxonomía de arriba es de **2011**. Un proyecto de 2026 tiene además estas categorías, y son
las que más seguido aparecen en los postmortems:

| Tipo | Riesgo concreto | Caso real |
|---|---|---|
| **Cadena de suministro** | Una dependencia de terceros queda comprometida o deja de mantenerse | `xz-utils` (2024): una puerta trasera en una librería de compresión usada por medio mundo |
| **Proveedor de nube** | Caída de una región, cambio de precios, bloqueo de cuenta | Toda caída de una región mayor arrastra miles de sistemas |
| **Regulatorio** | Cambia la normativa de datos personales, accesibilidad o IA | Reglamento europeo de IA; accesibilidad obligatoria desde 2025 en la UE |
| **IA generativa** | Código asistido por IA con defectos, licencias dudosas o filtración de datos | Deuda técnica generada más rápido de lo que se revisa |
| **Seguridad** | Vulnerabilidad explotada antes del parche | Dependencias desactualizadas son el vector más común |
| **Escala** | El sistema funciona en pruebas y cae en producción con carga real | El riesgo central de una preventa de entradas |
| **Dato** | Pérdida, corrupción o migración fallida | Un backup que nunca se probó restaurar |

<div class="alerta">

**Por qué importa el encuadre:** los riesgos de Sommerville son casi todos **internos** al equipo.
Los de esta tabla son **externos** y en su mayoría no se pueden evitar, solo mitigar y monitorear.
Eso cambia la estrategia: de *evitación* a *contingencia*.

</div>

----

### 2. ANÁLISIS DEL RIESGO
Para cada riesgo identificado estimar la probabilidad de ocurrencia y gravedad en caso de ocurrir.
* La probabilidad del riesgo puede valorarse como muy baja (< 10%), baja (del 10 al 25%), moderada
(del 25 al 50%), alta (del 50 al 75%) o muy alta (> 75%).
* Los efectos del riesgo pueden estimarse como catastróficos (amenazan la supervivencia del proyecto), graves (causarían 
grandes demoras), tolerables (demoras dentro de la contingencia permitida) o insignificantes.

---
### EJEMPLOS
<!-- .slide: style="font-size: 0.60em" -->
<!--
| Riesgo                                                                                                                    | Probabilidad | Efectos        |
|:--------------------------------------------------------------------------------------------------------------------------|:-------------|:---------------|
| Problemas financieros de la organización fuerzan reducciones en el presupuesto del proyecto. (7)                          | Baja         | Catastrófico   |
| Es imposible reclutar personal con las habilidades requeridas. (3)                                                        | Alta         | Catastrófico   |
| El personal clave está enfermo e indispuesto en momentos críticos. (4)                                                    | Moderada     | Grave          |
| Los componentes de software de reutilización contienen defectos que hacen que no puedan reutilizarse como se planeó. (2)  | Moderada     | Grave          |
| Se proponen cambios a los requerimientos que demandan mayor trabajo de rediseño. (10)                                     | Moderada     | Grave          |
| La organización se reestructura de modo que diferentes administraciones son responsables del proyecto. (6)                | Alta         | Grave          |
| La base de datos que se usa en el sistema no puede procesar tantas transacciones por segundo como se esperaba. (1)        | Moderada     | Grave          | 
-->
<table>
<thead>
<tr>
<th style="text-align:left">Riesgo</th>
<th style="text-align:left">Probabilidad</th>
<th style="text-align:left">Efectos</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Problemas financieros de la organización fuerzan reducciones en el presupuesto del proyecto. (7)</td>
<td style="text-align:left" class="baja">Baja</td>
<td style="text-align:left" class="catastrofico">Catastrófico</td>
</tr>
<tr>
<td style="text-align:left">Es imposible reclutar personal con las habilidades requeridas. (3)</td>
<td style="text-align:left" class="alta">Alta</td>
<td style="text-align:left" class="catastrofico">Catastrófico</td>
</tr>
<tr>
<td style="text-align:left">El personal clave está enfermo e indispuesto en momentos críticos. (4)</td>
<td style="text-align:left" class="moderada">Moderada</td>
<td style="text-align:left" class="grave">Grave</td>
</tr>
<tr>
<td style="text-align:left">Los componentes de software de reutilización contienen defectos que hacen que no puedan reutilizarse como se planeó. (2)</td>
<td style="text-align:left" class="moderada">Moderada</td>
<td style="text-align:left" class="grave">Grave</td>
</tr>
<tr>
<td style="text-align:left">Se proponen cambios a los requerimientos que demandan mayor trabajo de rediseño. (10)</td>
<td style="text-align:left" class="moderada">Moderada</td>
<td style="text-align:left" class="grave">Grave</td>
</tr>
<tr>
<td style="text-align:left">La organización se reestructura de modo que diferentes administraciones son responsables del proyecto. (6)</td>
<td style="text-align:left" class="alta">Alta</td>
<td style="text-align:left" class="grave">Grave</td>
</tr>
<tr>
<td style="text-align:left">La base de datos que se usa en el sistema no puede procesar tantas transacciones por segundo como se esperaba. (1)</td>
<td style="text-align:left" class="moderada">Moderada</td>
<td style="text-align:left" class="grave">Grave</td>
</tr>
</tbody>
</table>


----

### EJEMPLOS
<!-- .slide: style="font-size: 0.60em" -->
<!--
| Riesgo                                                                                           | Probabilidad | Efectos        |
|:-------------------------------------------------------------------------------------------------|:-------------|:---------------|
| Se subestima el tiempo requerido para desarrollar el software. (12)                              | Altab        | Grave          |
| Las herramientas de software no pueden trabajar en una forma integrada. (9)                      | Alta         | Tolerable      |
| Los clientes no entienden las repercusiones de los cambios a los requerimientos. (11)            | Moderada     | Tolerable      |
| No está disponible la capacitación requerida para el personal. (5)                               | Moderada     | Tolerable      |
| Se subestima la tasa de reparación de defecto. (13)                                              | Moderada     | Tolerable      |
| Se subestima el tamaño del software. (14)                                                        | Alta         | Tolerable      |
| El código elaborado por las herramientas de generación de código de software es ineficiente. (8) | Moderada     | Insignificante |
-->

<table>
<thead>
<tr>
<th style="text-align:left">Riesgo</th>
<th style="text-align:left">Probabilidad</th>
<th style="text-align:left">Efectos</th>
</tr>
</thead>
<tbody>
<tr>
<td>Se subestima el tiempo requerido para desarrollar el software. (12)</td>
<td class="alta">Alta</td>
<td class="grave">Grave</td>
</tr>
<tr>
<td>Las herramientas de software no pueden trabajar en una forma integrada. (9)</td>
<td class="alta">Alta</td>
<td class="tolerable">Tolerable</td>
</tr>
<tr>
<td>Los clientes no entienden las repercusiones de los cambios a los requerimientos. (11)</td>
<td class="moderada">Moderada</td>
<td class="tolerable">Tolerable</td>
</tr>
<tr>
<td>No está disponible la capacitación requerida para el personal. (5)</td>
<td class="moderada">Moderada</td>
<td class="tolerable">Tolerable</td>
</tr>
<tr>
<td>Se subestima la tasa de reparación de defecto. (13)</td>
<td class="moderada">Moderada</td>
<td class="tolerable">Tolerable</td>
</tr>
<tr>
<td>Se subestima el tamaño del software. (14)</td>
<td class="alta">Alta</td>
<td class="tolerable">Tolerable</td>
</tr>
<tr>
<td>El código elaborado por las herramientas de generación de código de software es ineficiente. (8)</td>
<td class="moderada">Moderada</td>
<td class="insignificante">Insignificante</td>
</tr>
</tbody>
</table>

---
### 3. PLANEACIÓN DEL RIESGO
Considerar cada riesgo y generar estrategias para gestionarlo.

* **Estrategias de evitación:** reducir la probabilidad de que surja el riesgo.
* **Estrategias de minimización:** reducir el efecto del riesgo.
* **Planes de contingencia:** hacer frente y tener una estrategia para a ello.

---
### ESTRATEGIAS PARA GESTIÓN DEL RIESGO
<!-- .slide: style="font-size: 0.40em" -->
<!--
| Riesgo                                   | Estrategia                                                                                                                                                                                                                                                      |
|:-----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Problemas financieros de la organización | Prepare un documento informativo para altos ejecutivos en el que muestre cómo el proyecto realiza una aportación muy importante a las metas de la empresa y presente razones por las que los recortes al presupuesto del proyecto no serían efectivos en costo. |
| Problemas de reclutamiento               | Alerte al cliente de dificultades potenciales y de la posibilidad de demoras; investigue la compra de componentes.                                                                                                                                              |
| Enfermedad del personal                  | Reorganice los equipos de manera que haya más traslape de trabajo y, así, las personas comprendan las labores de los demás.                                                                                                                                     |
| Componentes defectuosos                  | Sustituya los componentes potencialmente defectuosos con la compra de componentes de conocida fiabilidad.                                                                                                                                                       |
| Cambios de requerimientos                | Obtenga información de seguimiento para valorar el efecto de cambiar los requerimientos; maximice la información que se oculta en el diseño.                                                                                                                    |
| Reestructuración de la organización      | Prepare un documento informativo para altos ejecutivos en el que muestre cómo el proyecto realiza una aportación muy importante a las metas de la empresa.                                                                                                      |
| Rendimiento de la base de datos          | Investigue la posibilidad de comprar una base de datos de mayor rendimiento.                                                                                                                                                                                    |
| Subestimación del tiempo de desarrollo   | Investigue los componentes comprados; indague el uso de un generador de programa.                                                                                                                                                                               |
-->
<table>
<thead>
<tr>
<th style="text-align:left">Riesgo</th>
<th style="text-align:left">Estrategia</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Problemas financieros de la organización</td>
<td style="text-align:left">Prepare un documento informativo para altos ejecutivos en el que muestre cómo el proyecto realiza una aportación muy importante a las metas de la empresa y presente razones por las que los recortes al presupuesto del proyecto no serían efectivos en costo.</td>
</tr>
<tr>
<td style="text-align:left">Problemas de reclutamiento</td>
<td style="text-align:left">Alerte al cliente de dificultades potenciales y de la posibilidad de demoras; investigue la compra de componentes.</td>
</tr>
<tr>
<td style="text-align:left">Enfermedad del personal</td>
<td style="text-align:left">Reorganice los equipos de manera que haya más traslape de trabajo y, así, las personas comprendan las labores de los demás.</td>
</tr>
<tr>
<td style="text-align:left">Componentes defectuosos</td>
<td style="text-align:left">Sustituya los componentes potencialmente defectuosos con la compra de componentes de conocida fiabilidad.</td>
</tr>
<tr>
<td style="text-align:left">Cambios de requerimientos</td>
<td style="text-align:left">Obtenga información de seguimiento para valorar el efecto de cambiar los requerimientos; maximice la información que se oculta en el diseño.</td>
</tr>
<tr>
<td style="text-align:left">Reestructuración de la organización</td>
<td style="text-align:left">Prepare un documento informativo para altos ejecutivos en el que muestre cómo el proyecto realiza una aportación muy importante a las metas de la empresa.</td>
</tr>
<tr>
<td style="text-align:left">Rendimiento de la base de datos</td>
<td style="text-align:left">Investigue la posibilidad de comprar una base de datos de mayor rendimiento.</td>
</tr>
<tr>
<td style="text-align:left">Subestimación del tiempo de desarrollo</td>
<td style="text-align:left">Investigue los componentes comprados; indague el uso de un generador de programa.</td>
</tr>
</tbody>
</table>


---
### 4. MONITOREO DEL RIESGO
Hay que valorar regularmente cada uno de los riesgos identificados para
decidir si este riesgo se vuelve más o menos probable.

---
### INDICADORES DE RIESGO
<!-- .slide: style="font-size: 0.60em" -->
<!--
| Tipo de riesgo  | Indicadores potenciales                                                                                                                                  |
|:----------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tecnológico     | Entrega tardía de hardware o software de soporte; muchos problemas tecnológicos reportados.                                                              |
| Personal        | Baja moral de personal; malas relaciones entre miembros del equipo; alta rotación de personal.                                                           |
| De organización | Chismes en la organización; falta de acción de los altos ejecutivos.                                                                                     |
| Herramientas    | Renuencia de los miembros del equipo para usar herramientas; quejas acerca de las herramientas CASE; demandas por estaciones de trabajo mejor equipadas. |
| Requerimientos  | Muchas peticiones de cambio de requerimientos; quejas de los clientes.                                                                                   |
| Estimación      | Falla para cumplir con el calendario acordado; falla para corregir los defectos reportados.                                                              |
-->
<table>
<thead>
<tr>
<th style="text-align:left">Tipo de riesgo</th>
<th style="text-align:left">Indicadores potenciales</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Tecnológico</td>
<td style="text-align:left">Entrega tardía de hardware o software de soporte; muchos problemas tecnológicos reportados.</td>
</tr>
<tr>
<td style="text-align:left">Personal</td>
<td style="text-align:left">Baja moral de personal; malas relaciones entre miembros del equipo; alta rotación de personal.</td>
</tr>
<tr>
<td style="text-align:left">De organización</td>
<td style="text-align:left">Chismes en la organización; falta de acción de los altos ejecutivos.</td>
</tr>
<tr>
<td style="text-align:left">Herramientas</td>
<td style="text-align:left">Renuencia de los miembros del equipo para usar herramientas; quejas acerca de las herramientas CASE; demandas por estaciones de trabajo mejor equipadas.</td>
</tr>
<tr>
<td style="text-align:left">Requerimientos</td>
<td style="text-align:left">Muchas peticiones de cambio de requerimientos; quejas de los clientes.</td>
</tr>
<tr>
<td style="text-align:left">Estimación</td>
<td style="text-align:left">Falla para cumplir con el calendario acordado; falla para corregir los defectos reportados.</td>
</tr>
</tbody>
</table>

---

### Ejercicio de Riesgo

[Matriz de Riesgos](https://docs.google.com/spreadsheets/d/1-Nlu84CVFm2XJ2WK3sqCNiwntB-BbRE8sJ7sl2-pUyY/edit?gid=0#gid=0)

![QR](images/unidad10/QR.png)

---
### GESTIÓN DE PERSONAL
* Las personas son el principal capital de la empresa.
* Una incorrecta gestión del personal garantiza la falla del proyecto.
* Se debe designar a las personas responsabilidades acordes a sus habilidades.

---
### FACTORES
* **Consistencia:** Todas las personas en un equipo de proyecto deben recibir un trato similar.
* **Respeto:** Las personas tienen distintas habilidades y los administradores deben respetar esas diferencias.
* **Inclusión:** Las personas contribuyen mejor si sienten que las toman en cuenta.
* **Honestidad:** El administrador, debe ser honesto sobre lo que está bien o mal en el equipo.

---
### MOTIVACIÓN DEL PERSONAL
* Un rol importante del administrador es motivar al personal.
* Organizar el trabajo y el entorno laboral para alentar a las personas a trabajar mejor. 
  * Si las personas no están motivadas, no desarrollarán su trabajo apropiadamente. 
  * Hay diferentes tipos de motivación basada en 
    * Necesidades básicas (comer, dormir, etc.); 
    * Necesidades Personales (respeto)
    * Necesidades Sociales (aceptación por parte del grupo).

---

![Jerarquía de Necesidades Humanas](images/unidad10/jerarquia-necesidades-humanas.png)

---
### SATISFACCIÓN DE NECESIDADES
* En desarrollo de software las necesidades fisiológicas y de seguridad están cubiertas. 
* Satisfacción de necesidades **sociales** 
  * Generar facilidades de comunicación;
  * Favorecer la comunicación informal 
* Satisfacción de necesidades de **Estima** 
  * Reconocimiento de logros. 
  * Justa recompensa económica. 
* Satisfacción de necesidades **Autorrealización** 
  * Favorecer la capacitación.

---

### Personalidad y motivación

1. Personas **orientadas a las tareas**, que están motivadas por el reto 
intelectual de desarrollar software.
2. Personas **orientadas hacia sí mismas**, que están motivadas por el 
éxito y el reconocimiento personales.
3. Personas **orientadas a la interacción**, están motivadas por la presencia y 
las acciones de los compañeros de trabajo.

----

### Qué dice la evidencia hoy
<!-- .slide: style="font-size: 0.70em" -->

<div class="alerta">

**La pirámide de Maslow hay que darla con una advertencia.** Maslow nunca la dibujó como pirámide
—eso lo agregaron divulgadores posteriores— y nunca sostuvo que haya que satisfacer un nivel
completo antes de pasar al siguiente. La evidencia empírica de la jerarquía estricta es débil.
Sirve como **vocabulario** para hablar de distintos tipos de necesidad, no como modelo predictivo.

</div>

Los modelos que hoy se usan para equipos de software:

| Modelo | Qué sostiene |
|---|---|
| **Autodeterminación** (Deci y Ryan) | La motivación intrínseca necesita tres cosas: **autonomía** (decidir cómo trabajo), **competencia** (mejorar en algo que me importa) y **vínculo** (pertenecer a un equipo) |
| **Herzberg** | El sueldo, la oficina y las herramientas son **factores de higiene**: su ausencia desmotiva, pero su presencia no motiva. Lo que motiva es el logro, el reconocimiento y el trabajo en sí |
| **Seguridad psicológica** (Edmondson) | El predictor más fuerte de desempeño de equipo encontrado por Google en su estudio interno: poder decir "no entiendo" o "me equivoqué" sin costo |

**La traducción práctica:** un equipo al que se le dicta todo, que no ve el efecto de su trabajo y
donde admitir un error se castiga, no se arregla con una fruta en la cocina.

---

### TRABAJO EN EQUIPO
* El desarrollo de software implica trabajo en equipo.
* En un grupo cohesivo, los miembros piensan que el equipo es más importante que los individuos.
* Los miembros de un grupo cohesivo bien liderado son leales al equipo.
* Se identifican con las metas del grupo y con los demás miembros.

---
### GRUPO COHESIVO
* **El grupo puede establecer sus propios estándares de calidad**, puesto que dichos estándares se establecen por
consenso, éstos tienen más probabilidad de respetarse que los estándares externos impuestos sobre el grupo.
* **Los individuos aprenden de los demás y se apoyan mutuamente**. Las personas en el grupo aprenden de los
demás. Las inhibiciones causadas por la ignorancia se minimizan mientras se promueve el aprendizaje mutuo.

----

### GRUPO COHESIVO
* **El conocimiento se comparte**. Puede mantenerse la continuidad si sale un miembro del grupo. Otros en el
grupo pueden tomar el control de las tareas críticas para asegurar que el proyecto no se altere en forma considerable.
* **Se alientan la refactorización y el mejoramiento continuo**. Los miembros del grupo trabajan de manera colectiva 
para entregar resultados de alta calidad y corregir problemas, sin importar quiénes crearon originalmente el diseño o
programa

---
### LA EFICIENCIA DEL GRUPO
<!-- .slide: style="font-size: 0.90em" -->
* Se necesita una combinación de personas en un grupo de proyecto, puesto que el desarrollo de
software implica diversas actividades, como negociación con clientes, programación, pruebas y documentación.
* El grupo debe organizarse de forma que los individuos puedan contribuir con sus mejores
habilidades y completar las tareas como se esperaba.
* Es esencial la óptima comunicación entre los miembros del grupo, y entre el equipo de
ingeniería de software y otras partes interesadas en el proyecto.

---
### RESPONSABILIDAD DEL ADMINISTRADOR DEL PROYECTO
* Un administrador de proyecto debe crear un grupo que logre trabajar de manera eficiente.
* El grupo debe estar formado por diferentes perfiles, tanto desde el punto de vista técnico como en cuanto a la personalidad.

<small> (las personas motivadas por el trabajo son más fuertes técnicamente. Las personas orientadas hacia sí mismas 
son mejores para impulsar el trabajo hacia delante para terminar la tarea. Las personas orientadas a la interacción ayudan a facilitar las comunicaciones dentro del grupo.) </small>

---

### Organización del Grupo
<!-- .slide: style="font-size: 0.80em" -->
Influye en las decisiones que toma dicho grupo, en cómo se intercambia la información y las interacciones entre el grupo de desarrollo y los participantes externos del proyecto. 

Algunas preguntas organizacionales son:
1. ¿El administrador del proyecto debe ser el líder técnico del grupo?
2. ¿Quién se encargará de tomar las decisiones técnicas críticas, y cómo se tomarán?
3. ¿Cómo se manejarán las interacciones con los participantes externos y los altos directivos de la compañía?
4. ¿Cómo lograr cohesión en equipos remotos?
5. ¿Cómo puede compartirse el conocimiento a través del grupo?

---

### Comunicaciones grupales

El equipo debe  intercambiar información acerca de:
- El estatus de su trabajo
- Las decisiones de diseño 
- Los cambios que deben implementarse
- Problemas que pueden surgir

----

### Comunicaciones grupales

La efectividad y la eficiencia de las comunicaciones están influidas por:
1. **Tamaño del grupo:** Conforme el grupo crece, se hace más difícil que los miembros
se comuniquen de manera efectiva. La cantidad de **canales** entre pares crece de forma
cuadrática: **n·(n−1)/2**. Con 5 personas hay 10 canales; con 8 hay **28**; con 15 hay 105.
*(Si se cuentan las dos direcciones de cada canal, n·(n−1), con 8 personas son 56.)*
2. **Estructura del grupo:** Grupos "informales" se comunican más que "grupos de estructura jerárquica" 
(comunicación de arriba hacia abajo).

----

### Comunicaciones grupales

3. **Composición del grupo:** Personas con los mismos tipos de personalidad a veces se 
inhiben.
4. **Ambiente laboral:** El espacio y la forma de la oficina física, o las herramientas de
comunicación pueden facilitar o inhibir las comunicaciones.
5. **Canales de comunicación:** Cara a cara, email, documentos formales, teléfono, 
redes sociales, wikis, etc.

---

## Ejercitación
### El proyecto TicketFr

<!-- .slide: style="font-size: 0.78em" -->

Los ejercicios que siguen son sobre **el mismo sistema** que venimos modelando: el portal de
gestión de eventos y venta de entradas.

<div class="grid-item">

**Contexto para todos los ejercicios.** Una productora contrata el desarrollo del portal.
Alcance: configuración de salas con **varias distribuciones**, programación de funciones, venta al
público con reserva temporal, transferencia y reembolso de entradas, red de **RRPP** con cupos
VIP, servicios de **transporte**, **merchandising**, control de **acceso** por QR y **blacklist**
de personas. Integra una **pasarela de pagos** externa y un **servicio de mailing** ya contratado.
Primera preventa comprometida: **5.000 compradores concurrentes** en los primeros 10 minutos.

Equipo: **6 personas** (1 líder técnico, 3 desarrolladores, 1 QA, 1 diseñador). Plazo: **9 meses**.

</div>

<div class="fuente">

📎 El caso completo está en
[Caso integrador: portal de venta de entradas](U5_caso_integrador_ticketera.html)

</div>

----

### 💡 Ejercicio 1: Identificar riesgos
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.74em" -->

Armá el **registro de riesgos** del proyecto TicketFr con **al menos 10 riesgos**. Para cada uno:

1. Clasificalo en **proyecto / producto / empresa** y además por tipo (tecnológico, personal,
   organizacional, de requerimientos, de estimación, y las categorías nuevas: cadena de
   suministro, regulatorio, escala).
2. Escribilo como una **condición observable**, no como un miedo. Mal: *"que falle el pago"*.
   Bien: *"la pasarela no responde durante la preventa y quedan compras en estado pendiente"*.
3. Indicá **quién** lo detectaría y **con qué indicador**.

**Pista:** mirá la especificación del sistema. Cada pendiente de definición sin resolver **es** un
riesgo de requerimientos, y hay 15 críticos.

<!--
Lo que se evalua:
- Que aparezcan riesgos de las tres categorias y no solo tecnologicos.
- Riesgos esperables: la preventa de 5.000 concurrentes (escala, producto); la pasarela sin
  respuesta y la sobreventa (producto); las wallets de iOS y Android que requieren cuentas de
  desarrollador y certificados (tecnologico + empresa); la blacklist y los datos personales
  (regulatorio); el equipo de 6 personas para 15 modulos (estimacion); los 15 PD criticos sin
  resolver (requerimientos); un solo QA para todo el alcance (personal); dependencia del
  servicio de mailing contratado que no eligieron ellos (cadena de suministro).
- El punto 2 es el que mas rinde al corregir: un riesgo que no se puede observar no se puede
  monitorear, y por lo tanto no se puede gestionar.
-->

----

### 💡 Ejercicio 2: Matriz de riesgo
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.74em" -->

Tomá los 10 riesgos del ejercicio anterior y completá el cuadro:

| Riesgo | Probabilidad | Efecto | Exposición | Estrategia | Dueño |
|---|---|---|---|---|---|
| | muy baja … muy alta | insignificante · tolerable · grave · catastrófico | | evitación · minimización · contingencia | |

1. Justificá la probabilidad con un **dato o un supuesto explícito**, no con una intuición.
2. Ordená por **exposición** y marcá los **tres** que atacarías primero.
3. Para esos tres, escribí la estrategia con una **acción concreta y fechada**, no un deseo.
4. ¿Cuál de los riesgos **no se puede evitar**, solo mitigar? ¿Qué implica eso?

<!--
Lo que se evalua:
- Que distingan probabilidad de impacto: el riesgo catastrofico improbable y el tolerable casi
  seguro requieren tratamientos distintos.
- Que las tres estrategias no sean "monitorear de cerca". Evitacion de la preventa: prueba de
  carga a los 3 meses con el doble del volumen esperado. Contingencia de la pasarela: cola de
  conciliacion y no liberar las ubicaciones. Minimizacion del alcance: cerrar los PD criticos
  antes de empezar los modulos que dependen de ellos.
- Punto 4: la caida de la pasarela externa y el cambio regulatorio no se evitan. Eso obliga a
  plan de contingencia, que es la categoria que los alumnos siempre dejan vacia.
- Vale discutir que el riesgo de mayor exposicion probablemente no sea tecnico sino los 15 PD
  criticos: empezar a construir sin definiciones es el camino directo al retrabajo.
-->

----

### 💡 Ejercicio 3: Organizar el equipo
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.74em" -->

Con 6 personas y 15 módulos:

1. ¿Cuántos **canales de comunicación** hay en el equipo? Si se suman 4 personas más, ¿cuántos?
   ¿Qué le pasa al costo de coordinación?
2. Proponé una **organización** del equipo y justificá: ¿por módulos, por capas, o por recorridos
   completos de funcionalidad? ¿Quién decide la arquitectura?
3. El líder técnico es la única persona que entiende el modelo de distribuciones de sala.
   Nombrá el riesgo y proponé **dos** mitigaciones distintas.
4. El diseñador trabaja desde otra provincia y en otra franja horaria. ¿Qué tres decisiones
   concretas tomarías para que eso no degrade la comunicación?

<!--
1. 6 personas: 15 canales. 10 personas: 45. Triplica. Es el argumento de Brooks: agregar gente a
   un proyecto atrasado lo atrasa mas.
2. La respuesta interesante es por recorridos completos (feature teams): un equipo que lleva
   "comprar entrada" de punta a punta entrega valor, mientras uno organizado por capas necesita
   que las tres capas terminen para que algo funcione. Ley de Conway: la arquitectura va a
   terminar pareciendose a la estructura del equipo.
3. Riesgo personal de concentracion de conocimiento (factor camion). Mitigaciones: programacion
   en pares o revision obligatoria de ese modulo por otra persona, y documentar la decision en
   la wiki del proyecto (que es justamente para que sirve la SSOT).
4. Asincronia por defecto: decisiones escritas en lugar de conversadas, una franja de
   solapamiento acordada, y nada critico que dependa de una sola conversacion en vivo.
-->

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)