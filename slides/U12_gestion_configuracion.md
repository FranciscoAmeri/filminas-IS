---
title: Gestión de la Configuración
theme: solarized
slideNumber: true
---

#### Ingeniería de Software

## Gestión de la Configuración y
## Control de Versiones

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

- Introducción
- Alcance
- Objetivos
- Roles y Responsabilidades
- Actividades de Gestión de Configuración
- Identificación de Elementos de Configuración
- Mantenimiento y control de la gestión de la configuración

</div>
<div class="grid-item">

- Proceso de control de cambios
- Recuperación de los elementos de configuración
- Informe del estado de los elementos de configuración
- Verificación y Auditoría
- Gestión de la liberación del Software
- Identificación de Versiones
- Herramientas

</div>
</div>

---

### Alcance de esta unidad
<!-- .slide: style="font-size: 0.80em" -->

Quedan **4 clases** y el programa no entra completo, asi que parte del material
de esta unidad no se desarrolla en el cursado.

<div class="grid-item">

Lo que **no se dicta en clase** esta completo en un mazo aparte:
**[Gestión de la Configuración: material de examen final](U12_gestion_configuracion_final.html)**

Es material de estudio y **se evalua en el examen final**.

</div>

Todo lo que sigue aca **si se dicta**, y es la base para el trabajo practico.

---

<!--https://unpsjb.github.io/ids3t/configuracion.html-->

### Gestión de la configuración: Introducción
Tiene como objetivo asegurar que el producto de software sea consistente, trazable y controlado durante todo su ciclo de vida.

Podemos definir **SCM – Software Configuration Management** como el conjunto de actividades destinadas a:
- Identificar
- Controlar
- Auditar
- Registrar los cambios 
que se realizan sobre los artefactos del software.

---

### Gestión de la Configuración: Objetivos
- Determinar cuál es la versión actual de cada uno de los componentes.
- Determinar el proceso cambios.
- Determinar la política de releases.
- Roles y Responsabilidades

---

### Gestión de la Configuración: Roles
1. Gestor de configuración	
2. Coordinador de configuración
3. Responsable de elementos de configuración
4. Gestor de cambio

---

### Actividades de Gestión de Configuración
<!-- .slide: style="font-size: 0.50em" -->

<table>
    <thead>
        <tr>
            <th>Actividad</th>	
            <th>Rol Responsable</th>
            <th>Descripción</th>
            <th>Entradas</th>
            <th>Salidas</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Gestión del proceso de gestión de configuración.</td>
            <td>Gestor de configuración.</td>
            <td>Documentar el plan de gestión de configuración.</td>
            <td>Necesidades del proyecto. Plan de proyecto.</td>
            <td>Plan de gestión de configuración aprobado.</td>
        </tr>
        <tr>
            <td>Identificación de elementos de configuración.</td>
            <td>Gestor de configuración.</td>
            <td>Identificar elementos de configuración. Crear estructura del directorio de gestión de configuración.</td>
            <td>Productos del proyecto.</td>
            <td>Elementos de configuración identificados. Línea base. Estructura del directorio de gestión de configuración.</td>
        </tr>
        <tr>
            <td>Mantenimiento y control de la gestión de configuración.</td>
            <td>Responsable del elemento de configuración.</td>
            <td>Control de cambios sobre elementos de configuración y líneas base. Obtener aprobación de solicitudes de cambio sobre productos de trabajo de línea base.</td>
            <td>Peticiones de cambio.</td>
            <td>Registro de solicitud de cambio. Solicitud de cambio aprobada. Línea base.</td>
        </tr>
    </tbody>
</table>

---
<!-- .slide: style="font-size: 0.52em" -->

### Identificación de Elementos de Configuración

Se debe identificar los elementos que van a ser controlados, establecer esquemas para la identificación de los elementos y sus versiones, y establece las herramientas y técnicas a usar para adquirir y gestionar los elementos controlados. 

Estas actividades proporcionan la base para otras actividades de gestión de configuración. 

----

### Identificación de Elementos de Configuración: criterios para seleccionar elementos
- Productos de trabajo que vayan a ser utilizados por dos o más grupos.
- Productos de trabajo que puedan cambiar con el tiempo debido a cambios en requisitos o errores.
- Productos que dependan de otros en el sentido de que un cambio en uno de ellos implique un cambio en los otros.
- Productos de trabajo que sean críticos para el proyecto.

---

### Mantenimiento y control de la gestión de la configuración
Cuando se solicita un cambio que afecta a algún producto bajo gestión de configuración (línea base), entrará en funcionamiento el proceso de control de cambios. 

En este proceso se deben identificar y valorar los cambios y, si son admitidos, modificar los productos afectados, siguiendo el procedimiento establecido. 

Estos cambios realizados deben comunicarse a todas las personas que resulten afectadas por los mismos.

---

### Proceso de control de cambios

![Proceso de Control de Cambios](images/unidad12/controldecambios.png)

---

### Proceso de control de cambios (1)
<!-- .slide: style="font-size: 0.90em" -->
Como primer paso para gestionar los cambios sobre los elementos controlados es **determinar los cambios que se van a realizar**. 

El proceso de petición de cambios proporciona procedimientos formales para enviar y registrar peticiones de cambio, evaluar el **coste e impacto** potencial del cambio propuesto, y aceptar, modificar, o rechazar el cambio propuesto.

Los cambios solicitados o los errores detectados deberán ser identificados a través de los canales preestablecidos (personas, herramientas, etc.). Una vez recibidos serán documentados para su posterior estudio.

---

### Recuperación de los elementos de configuración
Es preciso la definición de un repositorio general del proyecto que posea interfaz vía línea de comandos y/o gráfica y/o interfaz web que facilite su uso. Además, la herramienta de repositorio deberá contar con una política de branching que no resulte dificultosa para el equipo.

----

![Branching](images/unidad12/branches.png)

----

### Reglas de Branching: Feature
<!-- .slide: style="font-size: 0.80em" -->
Se utilizan para desarrollar las nuevas características del servicio que, una vez terminadas, se incorporan a la rama develop. Se dispara la creación de estas ramas a partir de nuevas funcionalidades que se espera del producto.
- Se originan a partir de la rama develop, dado que se emplea el código que actualmente se está empleando.
- Se incorporan siempre a la rama develop. Una vez hecho esto, se deberán eliminar las ramas ya no trabajaran sobre esa feature. De esta forma se busca un esquema de trabajo limpio en donde no se tenga constantemente múltiples ramas, sino que existan las ramas master y develop, y que el resto sean temporales.
- El nombrado de esta rama puede ser cualquiera, pero no debe entrar en conflicto con el nombre de master, develop, relese o hotfix.

----

### Reglas de Branching: Release
<!-- .slide: style="font-size: 0.75em" -->
Estas ramas se utilizan para preparar el siguiente código en producción. Estas ramas son las que se vuelcan en los servidores de pre-producción para hacer el testing final: corrección de bugs, corrección de documentación, mejora de las GUI, etc. Se hace la puesta a punto final de la aplicación antes de liberar la versión definitiva, que irá a parar a la rama master y a la rama develop.
- El nombrado de la rama deberá corresponder con un tag que se ajuste al esquema de identificación de versiones definido por el equipo.
- Se originan a partir de la rama develop.
- Se incorporan a master y develop. La rama dejará de existir una vez que se efectúe el merge sobre dichas ramas, con lo cual las versiones estables quedarán sobre la rama master y el trabajo en curso sobre la rama develop. 
- En caso de existir bugs de último momento, se creará la rama de tipo Hotfix.

----

### Reglas de Branching: Hotfix
<!-- .slide: style="font-size: 0.80em" -->
Estas ramas ayudan a hacer las modificaciones de forma más eficiente y a corregir el problema con el mínimo impacto sobre el resto del trabajo que se está haciendo. El uso de estas ramas permite:
- Interrumpir el trabajo que se está haciendo en la rama develop para una versión nueva del servicio.
- Resolver el bug.
- Incorporar la corrección del bug en la rama master para desplegarlo en producción lo más rápido posible.
- Identificar sobre la rama master que ha habido una corrección, modificando el número de patch en el identificador de la versión.
- Incorporar la corrección del bug en la rama develop, si es necesario.
- Retomar el trabajo en la rama develop.

---

### Informe del estado de los elementos de configuración
Reporta la información necesaria para gestionar de forma efectiva la configuración de software. En esta actividad se deberá diseñar y operar un sistema para la captura y reporte de la información necesaria a medida que avanza el proceso de desarrollo.

La información sobre el estado de la configuración que se quiere gestionar debe ser identificada, recogida y mantenida. Son necesarias diversas métricas e información para dar soporte al proceso de gestión de configuración. 

---

### Verificación y Auditoría
<!-- .slide: style="font-size: 0.90em" -->
Una auditoría de software es una actividad llevada a cabo para evaluar, de forma independiente y objetiva, la conformidad de los productos y procesos software con respecto a las regulaciones, estándares, guías, planes y procedimientos aplicables (IEEE1028-97).

Las auditorías se llevarán a cabo de acuerdo a un proceso bien definido que detalla los roles y responsabilidades de los auditores. Cada auditoría debe ser cuidadosamente planificada, en función de la naturaleza del proyecto y de los requisitos. 

El uso de herramientas que ayuden en la planificación y realización de auditorías facilitan en gran medida el proceso.

----

### Auditoría
<!-- .slide: style="font-size: 0.80em" -->
- **Objetivo:** Verificar que en un momento dada, la línea base se compone de una colección consistente y bien definida de productos.
- **Elementos de configuración bajo auditoría:** se elegirán uno o más elementos de configuración de mayor prioridad en la línea base.
- **Agenda de auditorías:** antes de la liberación o actualización.
- **Conducción:** las auditorías serán dirigidas por el SCMR.
- **Participantes:** SCMR y los autores de los elementos de configuración a auditar.
- **Documentos requeridos**: documentos de SCR y reportes de estado de la configuración generados.
- **Reportes de deficiencias y acciones correctivas:** determinadas por los participantes.
- **Criterio de aprobación:** lo determina el SCMR.

---

### Gestión de la liberación del Software
El término **liberación** se utiliza en este contexto para referirse a la distribución del elemento de configuración de software fuera de la actividad de desarrollo. Esto incluye tanto liberaciones internas como distribuciones al cliente.

Implica la identificación, empaquetado y entrega de los elementos del producto, por ejemplo, programas ejecutables, documentación, notas de versión, y datos de configuración. 

---

### Identificación de Versiones
<!-- .slide: style="font-size: 0.90em" -->
El esquema sugerido para la identificación de las distintas versiones del producto, es un esquema numérico conformado de la siguiente manera:

**major_version** . **minor_version** . **patch_number**

- **Major Version:** indica un cambio de funcionalidad sustancial a otras versiones del sistema
- **Minor Version:** indica que el sistema es funcionalmente idéntico, pero es distinto desde el punto de vista no-funcional a otras versiones
- **Patch Version:** indica el número de un parche aplicado al sistema, que significa la corrección de un defecto encontrado

---

### Herramientas
- **Git:** Sistema de control de versiones.
- **Github o BitBucket:** Sistema web de control colaborativo de revisión y desarrollo de software utilizado para alojar proyectos que sean gestionados con Git.
- **Gitflow:** Conjunto de extensiones de git que facilitan la gestión de ramas y flujos de trabajo. Provee una serie de hooks que automatizan la gestión de ramas en un repositorio git, permitiendo así trabajar con la estructura de ramas descrita en el plan.

---

## ¿Dudas, Preguntas, Comentarios?

![DUDAS](images/pregunta.gif)
