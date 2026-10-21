---
title: Gestión de la Configuración - Material de examen final
theme: solarized
slideNumber: true
---

#### Ingenieria de Software
# Gestión de la Configuración
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
**[Gestión de la Configuración](U12_gestion_configuracion.html)**. Conviene estudiarlas despues de ese mazo,
no antes.

</div>

Son **23 filminas**.

---

### Plan de la Gestión de la Configuración: Supuestos
<!-- .slide: style="font-size: 0.80em" -->
- Tener control sobre cada una de las iteraciones y fases de los productos generados durante estas y de los cambios surgidos, evaluados y aprobados.
- Incluir en control de configuración la mayor cantidad de productos posibles, tomando en cuenta las restricciones de duración del proyecto y de capacidad organizativa del equipo.
- Si es necesario, realizar modificaciones que el cliente ha pedido y actuar con las estrategias pertinentes.
- Elección de los elementos de configuración en base a los entregables, siendo esta responsabilidad del Responsable de SCM, apoyado por los integrantes de cada disciplina.
- Al concluir cada una de las iteraciones, se llevar a cabo una prueba de verificación de la funcionalidad.

---

### ROL: 1. Gestor de configuración	
<!-- .slide: style="font-size: 0.75em" -->
- Gestionar la planificación, identificación, control, seguimiento y auditoría de todos los elementos de configuración en la base de datos de configuración.
- Desarrollar el plan de gestión de configuración.
- Promover el uso efectivo de la base de datos de configuración dentro de la organización.
- Monitorear y reportar los cambios no autorizados sobre los elementos de configuración.
- Asegurar la consistencia e integridad de los datos de la base de datos de configuración a través de la ejecución de procedimientos de verificación y auditoría.
- Liderar las actividades de evaluación del proceso: revisar tipos de elementos de configuración, relaciones, atributos y valores asociados, estructura de la base de datos, derechos de acceso.
- Aprobar cambios estructurales en la base de datos de configuración.

---

### ROL: 2. Coordinador de configuración
<!-- .slide: style="font-size: 0.95em" -->
- Asegurar que todos los elementos de configuración están registrados de forma adecuada en la base de datos de configuración.
- Asegurar la consistencia e integridad de los datos de la base de datos de configuración y la estructura del sistema a través de la ejecución de procedimientos de verificación y auditoría.
- Reportar cualquier discrepancia o no conformidad en los elementos de configuración al gestor de configuración.
- Participar en la mejora continua del proceso de gestión de configuración.

---

### ROL: 3. Responsable de elementos de configuración
<!-- .slide: style="font-size: 0.95em" -->
- Asegurar que los elementos de configuración de los que es responsable están registrados en la base de datos de configuración con el estado y datos de configuración apropiados.
- Verificar que los cambios sobre los elementos de configuración siguen el proceso de cambios definido.
- Asegurar la idoneidad e integridad de los elementos de configuración de los que es responsable.
- Trabajar conjuntamente con el gestor de configuración para identificar las causas de cualquier discrepancia identificada en las auditorías e implementar las acciones correctivas.

---

### ROL: 4. Gestor de cambio	

- Evaluar el impacto y riesgo de los cambios.
- Asegurar que los responsables de los elementos de configuración actualizan los históricos de estos elementos con los cambios implementados.

---

### Actividades de Gestión de Configuración
<!-- .slide: style="font-size: 0.70em" -->

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
            <td>Informe de estado de la configuración.</td>
            <td>Gestor de configuración.</td>
            <td>Mantener actualizado y publicar el estado de los elementos de configuración.</td>
            <td>Elementos de configuración.</td>
            <td>Informe de estado de elementos de configuración.</td>
        </tr>
        <tr>
            <td>Verificación y auditoría.</td>
            <td>Gestor de configuración.</td>
            <td>Realizar auditorías de la gestión de configuración.</td>
            <td>Registros de la gestión de configuración. Línea base. Registros de cambios.</td>
            <td>Informe de auditoría de gestión de configuración.</td>
        </tr>
    </tbody>
</table>

---

### Identificación de Elementos de Configuración: Tareas
<!-- .slide: style="font-size: 0.46em" -->
- Identificar los productos que se van a mantener bajo gestión de configuración para el proyecto.
- Asignar identificadores únicos para cada elemento de configuración y propiedades como autor, tipo de documento, persona responsable de ese elemento de configuración, etc.
- Definir estructura de almacenamiento.
- Definir un nivel de control de acceso de los miembros del equipo sobre la infraestructura de almacenamiento.
- Seleccionar herramientas específicas para la gestión de configuración.
- Especificar cuándo se va a incluir cada elemento bajo gestión de configuración (en qué momento del ciclo de vida).
- Obtener la autorización para incluir los documentos bajo gestión de configuración (línea base).
- Aplicar los procedimientos definidos para incluir los productos bajo gestión de configuración.
- Documentar los elementos que se han incluido bajo gestión de configuración.
- Desarrollar procedimientos para solicitar e implantar los cambios donde se especifique:
  - Quién solicita los cambios
  - Cómo se notifican los cambios
  - Cómo se evalúa el impacto
  - Quién evalúa el impacto
  - Quién acepta o rechaza el cambio
  - Quién modifica los distintos productos (responsable de cada producto)

---

### Identificación de Elementos de Configuración

<!-- .slide: style="font-size: 0.70em" -->
Dependiendo del proyecto los elementos de configuración pueden variar. 

<div class="grid-container2">
<div class="grid-item">

- Planes
    - Plan de proyecto
    - Plan de calidad
    - Plan de gestión de configuración
    - Plan de gestión de riesgos
- Registros del proyecto
- Material de apoyo al cliente
- Especificación de requisitos
    - Requisitos de negocio
    - Requisitos de usuario
    - Requisitos de sistema
- Matriz de trazabilidad de requisitos
- Documentos de diseño
- Resultados de la resolución y análisis de decisión
- Código fuente
- Plan de integración de software

</div>
<div class="grid-item">

- Informes resultantes de las revisiones realizadas en los puntos de comprobación o al final de las fases
- Plan de pruebas o unitarias o de integración o de sistemas o de aceptación de usuario o de regresión
- Datos de pruebas y casos de pruebas
- Plan de instalación/mantenimiento
- Documentos de manual de usuario
- Plan de entrega de servicios
- Informes de investigación
- Informes de estimación
- Informes de cierre del proyecto
- Prototipos
- Informes de métricas
- Todos los entregables enviados al cliente.
</div></div>

---

### Proceso de control de cambios (2)


Las peticiones de cambio sobre elementos de configuración pueden iniciarse por cualquiera y en cualquier punto del proceso de desarrollo y pueden incluir una sugerencia de solución y prioridad de la petición. Un posible origen de las peticiones de cambio es el inicio de una acción correctiva en respuesta a informes de problemas. El tipo de cambio (.ej.: defecto o mejora) se debe registrar en la petición de cambio (SCR) para así poder recoger métricas sobre los cambios por tipo de cambio.

---

### Proceso de control de cambios (3)
<!-- .slide: style="font-size: 0.90em" -->
Una vez recibida una SCR, se realizará una **evaluación técnica** o **análisis de impacto** para determinar el alcance de las modificaciones que serían necesarias realizar una vez se acepte la petición. En este punto es importante un buen entendimiento de las relaciones entre los elementos de software. Según la línea base afectada, los elementos de configuración implicados, y la naturaleza del cambio, la persona responsable deberá evaluar los aspectos técnicos y de gestión de la petición de cambio, y a continuación aceptar, modificar, rechazar o aplazar el cambio propuesto. En cualquier caso, la decisión tomada deberá quedar documentada de alguna forma.

---

### Proceso de control de cambios (4)


Las SCR aprobadas se implementarán utilizando los procedimientos de software definidos de acuerdo a los requisitos de tiempo que apliquen. Será necesario proporcionar una forma de realizar un seguimiento de qué SCR se incorporan, en qué versiones de software y líneas bases concretas. Como parte del cierre del proceso de cambios, los cambios realizados deben pasar por auditorías de configuración y verificación de la calidad del software. Esto incluye asegurar que sólo se han realizado los cambios aprobados.

---

### Proceso de control de cambios (5)


La implementación del cambio será soportada por una herramienta que permita gestión de versiones y un repositorio de código.

Tras realizar el cambio se comunicará, si así está establecido, a todos aquellos que estén afectados por dicho cambio. De esta forma, se preservar la integridad de los productos haciendo que todo el mundo trabaje con las versiones correctas.

---

### Proceso de control de cambios (6)


La autoridad para aceptar o rechazar los cambios propuestos reside en una entidad conocida como comité de control de configuración (CCB). Puede haber múltiples niveles de autorización de cambios dependiendo de varios criterios como la criticidad de los elementos implicados, la naturaleza del cambio (ej.: impacta en presupuesto o calendario), o el momento actual en el ciclo de vida. Las actividades del CCB están sujetas a revisión y auditoría de calidad de software.

---

### Recuperación de los elementos de configuración
<!-- .slide: style="font-size: 0.90em" -->
La estructura del desarrollo se conformará por dos ramas principales:
- **master:** esta rama contendrá todas las versiones estables del producto, con lo cual cualquier commit que se realice sobre ella, implica que el producto está listo para ser usado por los usuarios. Este paso implica que el producto haya pasado la correspondiente batería de pruebas y que esté debidamente documentado.
- **develop:** en esta rama se aloja el código que conformará la siguiente la versión. Sobre esta rama se trabajará con versiones inestables, que buscan agregar los cambios necesarios para cumplir con los requerimientos.

---

### Recuperación de los elementos de configuración

Además de estas 2 ramas principales se sugiere el uso de **ramas de soporte**:
- **Feature:** Nuevas características del producto.
- **Release:** Últimos cambios antes de pasar a producción.
- **Hotfix:** Cambios en “caliente”, corrección de bugs reportados mediante el uso de tickets en versiones del servicio que se encuentran en la rama master.
- **Cleanup y Optimization:** con estas ramas se busca fomentar las prácticas de limpieza y optimización de todos los productos.

---

### Recuperación de los elementos de configuración

Todas las ramas estarán sujetas a un esquema de nombrado, que permitan identificar cual ha sido la historia de la misma y cuál ha sido el motivo que ha dado origen a la rama. 

Se sugiere que las ramas adopten la siguiente forma: nombrerama/descripcion, en donde el nombrerama identifica alguna de las ramas antes presentadas y descripción es un texto breve que identifica al requerimiento.

---

### Reglas de Branching: Cleanup


Estas ramas son empleadas para la limpieza de todo lo producido, tanto a nivel de código como a nivel de documentación. En lo que respecta a la documentación, permite acomodar formato de la misma eliminación de errores de redacción, etc. A nivel de código permite eliminar piezas de código que no se ajusten a los estándares recomendados, que no cumplan con los requerimientos, etc.

---

### Reglas de Branching: Optimization


Estas ramas son empleadas para la optimización tanto a nivel de documentación como de código. 

En el caso de la documentación implica la reelaboración de aquella documentación que no se corresponda con la realidad. 

En el caso del código, implica la optimización de rutina de código sin impactar sobre la funcionalidad de la misma.

---

### Informe del estado de los elementos de configuración: tipo de información 
<!-- .slide: style="font-size: 0.75em" -->
Incluye la identificación de configuración aprobada así como el estado actual de la implementación de los cambios. Por ejemplo:
- Un registro de documentación de configuración aprobada.
- La designación de un responsable de los elementos de configuración del proyecto.
- El estado de cambios propuestos y desviaciones de la configuración.
- La implementación del estado de los cambios aprobados.
- La configuración de todas las unidades de los elementos de configuración en el inventario.
- Resultados de las auditorías.

Para llevar a cabo estas actividades de obtención de datos y generación de informes se hace necesario el soporte de una herramienta automatizada.

---

### Auditoría

La actividad de auditoría de configuración de software determinará en qué medida un elemento de configuración satisface sus características funcionales y físicas requeridas. Se pueden realizar auditorías de este tipo en puntos clave del proceso de desarrollo. El resultado satisfactorio de una auditoría se puede utilizar como prerrequisito para establecer una línea base del producto.

---

### Auditoría: Objetivos
<!-- .slide: style="font-size: 0.90em" -->
El objetivo de las auditorías de gestión de configuración es asegurarse de que:
- Los elementos de configuración se encuentran en el directorio apropiado.
- El estado actual de los elementos de configuración es consistente.
- La información de línea base se mantiene de forma correcta.
- Se verifica la conformidad con estándares y procedimientos aplicables a la gestión de configuración, por ejemplo, comprobando si se usa la versión correcta del documento de diseño para realizar la codificación.

---

### Auditoría
<!-- .slide: style="font-size: 0.90em" -->
Como resultado de la auditoría se deberá generar un informe donde se registren todas las no conformidades detectadas y así iniciar un plan de mejora para solucionarlas. Después de una auditoría de configuración exitosa se puede establecer una línea base del producto.

La verificación no se realiza sobre los propios productos sino que consiste en comprobar que los productos que conforman una línea base están gestionados correctamente bajo el control de configuración, que todos los cambios realizados sobre estos productos han sido registrados y, por tanto, se puede establecer una trazabilidad entre cambios y productos afectados.

---

### Gestión de la liberación del Software
<!-- .slide: style="font-size: 0.85em" -->
Puesto que los cambios en el producto pueden producirse de forma continua, se deberá plantear cuándo lanzar una nueva versión. Esta decisión se tomará teniendo en cuenta la severidad de los problemas encontrados y la métrica de densidad de defectos registrada en la versión actual. 

En la tarea de **empaquetado** se deben identificar qué elementos del producto se van a entregar y las versiones correctas de esos elementos, según la aplicación deseada del producto. Las **notas de versión** describen las nuevas funcionalidades, problemas conocidos, y requisitos de la plataforma necesarios para la correcta operación del producto. El paquete que se va a liberar deberá contener también instrucciones para la instalación o actualización.


---
## Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
