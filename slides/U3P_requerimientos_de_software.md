---
title: Requerimientos de Software
theme: solarized
slideNumber: true
---

# Ingeniería de Software
## Requerimientos de Software
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

.exercise-slide {
  border: 2px dashed #b58900;
  border-radius: 12px;
  padding: 20px;
}
</style>
## Temario
<div class="grid-container2">
<div class="grid-item">

### El documento SRS
* El estándar
* Historial de Cambios
* **Introducción**
* Propósito
* Alcance
* Personal Involucrado
* Definiciones, Acrónimos y Abreviaturas
* Referencias y Resumen
</div>
<div class="grid-item">

* **Descripción General**
* Perspectiva del Producto
* Funciones del Producto
* Características de los Usuarios
* Restricciones
* Supuestos y Dependencias
* **Requerimientos Específicos**
* Interfaces Externas
* Requerimientos Funcionales
* Requerimientos No Funcionales
* **Ejercicios**

*Cada sección se acompaña con el ejemplo
de un mismo caso: SIGETUR, el sistema de
turnos de un centro médico.*
</div>
</div>

---

### ¿De dónde sale esta estructura?
<!-- .slide: style="font-size: 0.85em" -->

La plantilla que vamos a recorrer es la del estándar **IEEE 830 — *Recommended Practice for
Software Requirements Specifications***, publicado en 1998. Es la estructura de SRS más difundida
y la que se sigue usando en la mayoría de las cátedras y de las consultoras.

**Está formalmente reemplazado por ISO/IEC/IEEE 29148**, que integra los requerimientos de sistema
y de software en un marco único y contempla desarrollos iterativos. En la práctica, la estructura
de secciones sigue siendo casi la misma.

**Lo importante:** la plantilla es un *checklist para no olvidarse de nada*, no un formulario a
completar por obligación. Un SRS de tres páginas bien escrito vale más que uno de cincuenta con
todas las secciones rellenadas.

---
## Historial de Cambios
<!-- .slide: style="font-size: 0.85em" -->

Registra las modificaciones que sufre el documento a lo largo del tiempo. Sirve para cuatro cosas:

* **Control de versiones** — quién cambió qué y cuándo.
* **Colaboración** — evita que dos personas trabajen sobre versiones distintas.
* **Recuperación** — permite volver a una versión anterior.
* **Auditoría** — deja traza para cumplimiento legal o regulatorio.

Es especialmente importante en un SRS porque el documento **suele formar parte del contrato**:
hay que poder demostrar qué se acordó y en qué momento.

----

### Historial de Cambios: cómo se ve

| Versión | Fecha | Autor | Descripción del cambio |
|---|---|---|---|
| 1.0 | 12/03/2026 | F. Ameri | Versión inicial aprobada por el cliente |
| 1.1 | 27/03/2026 | F. Ameri | Se agrega RF-12 (recordatorio por WhatsApp) a pedido de recepción |
| 1.2 | 05/04/2026 | M. Suárez | Se corrige RNF-03: la disponibilidad pasa de 99% a 99,5% |
| 2.0 | 20/04/2026 | F. Ameri | Se excluye del alcance la facturación electrónica |

Una tabla de cuatro columnas. Nada más que eso.

---
## Sección 1: Introducción
* Propósito
* Alcance
* Personal Involucrado
* Definiciones, Acrónimos y Abreviaturas
* Referencias
* Resumen

---
### Propósito
<!-- .slide: style="font-size: 0.85em" -->

Responde tres preguntas, en pocos párrafos:

1. **¿Qué documenta este SRS?** Qué producto o qué parte del producto especifica.
2. **¿Para quién está escrito?** Clientes y usuarios, el equipo de desarrollo, los testers, el
   área legal. Cada uno lee secciones distintas.
3. **¿Qué se espera que hagan con él?** Aprobarlo, diseñar a partir de él, derivar casos de prueba.

**Ejemplo:**

> Este documento especifica los requerimientos del Sistema de Gestión de Turnos (SIGETUR) para el
> Centro Médico Norte. Está dirigido al equipo de desarrollo, que lo usará como base de diseño;
> al personal de recepción y a la dirección del centro, que deben validarlo; y al equipo de
> pruebas, que derivará de él los casos de prueba de aceptación.

---
### Alcance
<!-- .slide: style="font-size: 0.80em" -->

Define **los límites del producto**: qué se va a construir y qué no.

* **Nombre del producto** — identificación clara, para que todos se refieran a lo mismo.
* **Funcionalidades incluidas** — qué hará el software.
* **Funcionalidades excluidas** — qué **no** hará. Tan importante como lo anterior: es lo que
  evita las expectativas incumplidas.
* **Beneficios y objetivos** — qué mejora aporta, con metas medibles cuando sea posible.
* **Restricciones conocidas** — presupuesto, plazo, recursos.

----

### Alcance: cómo se ve
<!-- .slide: style="font-size: 0.78em" -->

> **Producto:** SIGETUR — Sistema de Gestión de Turnos.
>
> **Incluye:** solicitud y cancelación de turnos por parte del paciente vía web; gestión de la
> agenda de cada profesional; recordatorio automático por correo 24 horas antes; reportes de
> ausentismo para la dirección.
>
> **No incluye:** historia clínica, facturación, obras sociales, ni aplicación móvil nativa.
> Estas funciones quedan fuera de esta versión y podrán abordarse en etapas posteriores.
>
> **Objetivo:** reducir el ausentismo a turnos del 22% actual a menos del 12% en los primeros
> seis meses de operación.

**Notar el objetivo:** tiene un número de partida, uno de llegada y un plazo. Un alcance que dice
"mejorar la atención al paciente" no se puede verificar ni aprobar.

---
### Personal Involucrado
<!-- .slide: style="font-size: 0.85em" -->

Deja registrado **quién es quién** en el proyecto: para saber a quién preguntarle, y sobre todo
**quién tiene autoridad para aprobar un requerimiento**.

Campos habituales: nombre, rol, responsabilidades y datos de contacto. Si el equipo es distribuido,
conviene sumar disponibilidad horaria.

| Nombre | Rol | Responsabilidad | Contacto |
|---|---|---|---|
| Dra. L. Pereyra | Directora médica | Aprueba el alcance y los requerimientos | lpereyra@... |
| M. Gómez | Jefa de recepción | Referente funcional del proceso de turnos | mgomez@... |
| F. Ameri | Analista funcional | Releva, redacta y mantiene el SRS | fameri@... |
| Equipo de desarrollo | Desarrollo | Diseña e implementa | dev@... |

---
### Definiciones, Acrónimos y Abreviaturas
<!-- .slide: style="font-size: 0.82em" -->

Un SRS lo leen personas de dos mundos: el del **negocio** y el **técnico**. Esta sección evita que
cada uno entienda algo distinto por la misma palabra.

Se ordena alfabéticamente, y cada acrónimo se expande la primera vez que aparece en el texto.

| Término | Definición |
|---|---|
| Ausentismo | Turno confirmado al que el paciente no se presenta ni cancela |
| Profesional | Médico o especialista con agenda propia dentro del sistema |
| SIGETUR | Sistema de Gestión de Turnos, objeto de este documento |
| Sobreturno | Turno asignado por fuera de los horarios regulares de la agenda |
| SRS | *Software Requirements Specification* |

**El caso típico:** "turno" no significa lo mismo para recepción que para el desarrollador. Esta
tabla es donde se resuelve esa diferencia, y no en una reunión seis semanas después.

---
### Referencias y Resumen
<!-- .slide: style="font-size: 0.90em" -->

**Referencias** — Lista los documentos complementarios mencionados en el cuerpo del SRS: normativa
aplicable, manuales de sistemas con los que hay que integrarse, actas de reunión, contratos.

**Resumen** — Una descripción breve de cómo está organizado el resto del documento. Le dice al
lector qué va a encontrar en cada sección y cuál le interesa a él.

---
## Sección 2: Descripción General
* Perspectiva del Producto
* Funciones del Producto
* Características de los Usuarios
* Restricciones
* Supuestos y Dependencias

---
### Descripción General
Esta sección describe cuáles son los factores que afectan al producto de software a desarrollar y
a sus requerimientos.

Es el **contexto**: todavía no se enumeran requerimientos, se explica el escenario donde el
sistema va a vivir.

---
### Perspectiva del Producto
<!-- .slide: style="font-size: 0.85em" -->

Detalla la relación del producto con **otros sistemas**. Si forma parte de un sistema mayor,
describe cómo se relacionan sus requerimientos con los del conjunto. En cualquier caso, se
detallan las interfaces necesarias para la comunicación.

> **Ejemplo:** SIGETUR es un sistema nuevo e independiente, pero debe integrarse con el padrón de
> profesionales del sistema administrativo existente (SISADM), del que toma las agendas y las
> especialidades. No reemplaza a SISADM ni escribe sobre él: solo lo consulta.

---
### Funciones del Producto
<!-- .slide: style="font-size: 0.85em" -->

Resumen de las funcionalidades más importantes. Es una vista de alto nivel, no la lista detallada
de requerimientos (esa va en la Sección 3). Suele acompañarse con un diagrama de casos de uso.

> **Ejemplo:** el sistema permitirá que un paciente solicite y cancele turnos, que un profesional
> consulte y bloquee su agenda, que recepción gestione turnos presenciales y sobreturnos, y que la
> dirección obtenga reportes de ocupación y ausentismo.

---
### Características de los Usuarios
<!-- .slide: style="font-size: 0.72em" -->

Establece las cualidades que deben poseer los usuarios para utilizar el producto. Sirve para
dimensionar cuánta capacitación hace falta y qué tan simple tiene que ser la interfaz.

| Tipo de Usuario | Formación | Habilidades | Actividades |
|---|---|---|---|
| Paciente | Ninguna | Uso básico de web o celular; puede ser adulto mayor con poca experiencia digital | Solicita y cancela turnos |
| Recepcionista | Secundario completo | Uso fluido de sistemas de gestión; capacitación de 4 h | Gestiona turnos, sobreturnos y reprogramaciones |
| Profesional | Universitario | Uso básico; poco tiempo disponible para capacitarse | Consulta y bloquea su agenda |
| Dirección | Universitario | Lectura de reportes | Consulta indicadores de ocupación y ausentismo |

**Por qué importa:** la fila del paciente es la que justifica el requerimiento de accesibilidad.
Sin esta tabla, ese requerimiento parece un capricho.

---
### Restricciones
<!-- .slide: style="font-size: 0.85em" -->

Limitaciones a las que está sujeto el desarrollo: políticas gubernamentales, limitaciones de
hardware, protocolos de comunicación, consideraciones de seguridad, plazos, tecnologías impuestas.

> **Ejemplo:** el sistema debe alojarse en el servidor propio del centro médico, que corre Linux
> con PostgreSQL. Debe cumplir con la Ley 25.326 de Protección de Datos Personales. El desarrollo
> no puede superar los cuatro meses porque debe estar operativo antes de la temporada de invierno.

---
### Supuestos y Dependencias
<!-- .slide: style="font-size: 0.85em" -->

Los **supuestos** son cosas que damos por ciertas y que, si resultan falsas, invalidan parte de los
requerimientos. Las **dependencias** son factores externos fuera del control del equipo.

> **Supuestos:** se asume que todos los pacientes registrados tienen una dirección de correo
> válida, y que la validación de identidad la resuelve el sistema administrativo existente y no
> SIGETUR.
>
> **Dependencias:** el envío de correos depende del servicio contratado por el centro médico. El
> acceso al padrón de profesionales depende de que el proveedor de SISADM habilite su API.

**Escribirlos sirve para dos cosas:** dejar por escrito de qué no se hace cargo el equipo, y tener
una lista de riesgos lista para revisar.

---
## Sección 3: Requerimientos Específicos
* Interfaces Externas
* Requerimientos Funcionales
* Requerimientos No Funcionales

---
### Requerimientos Específicos
<!-- .slide: style="font-size: 0.85em" -->

Es la sección **más extensa e importante** del documento. Describe todos los requerimientos con
suficiente nivel de detalle como para que sirvan a la vez para dos cosas:

* que el equipo **diseñe** el sistema a partir de ellos, y
* que los testers deriven de ellos los **casos de prueba**.

Ese doble uso es el criterio para saber si un requerimiento está lo bastante detallado:
**si no se puede escribir una prueba que lo verifique, todavía no está terminado.**

---
### Interfaces Externas
<!-- .slide: style="font-size: 0.78em" -->

Se definen todas las entradas y salidas que el producto debe soportar:

* **Interfaces de usuario** — por ejemplo, el cliente puede haber solicitado cierta plantilla o
  combinación de colores institucionales.
* **Interfaces de hardware** — características lógicas entre el software y el hardware. Por
  ejemplo, el uso de un lector de código de barras o de un puerto serie.
* **Interfaces de software** — si hay que comunicarse con otros sistemas: contenido, formato y
  protocolo.

**Una aclaración necesaria:** en la unidad anterior vimos que el SRS dice *qué* y no *cómo*.
¿No es contradictorio fijar acá los colores o el puerto serie? No: esas decisiones **no las está
tomando el equipo de desarrollo, las impone el cliente o el entorno**. Cuando una decisión técnica
viene dada desde afuera, deja de ser diseño y pasa a ser un requerimiento.

---
### Requerimientos Funcionales
<!-- .slide: style="font-size: 0.80em" -->

Describen las acciones que el sistema debe realizar. Se redactan empezando por
**"El sistema deberá..."**.

Al describirlos hay que cubrir:

* Comprobación de validez de las entradas
* Secuencia exacta de operaciones
* Respuesta a situaciones anormales (desbordamientos, fallos de comunicación, recuperación de errores)
* Parámetros
* Generación de salidas
* Relaciones entre entradas y salidas (secuencias, fórmulas de conversión)
* Requisitos lógicos de la información que se almacenará en la base de datos

----

### Cómo se escribe uno, en concreto
<!-- .slide: style="font-size: 0.62em" -->

> **RF-07 — Cancelación de turno por el paciente**
>
> **Descripción:** El sistema deberá permitir que un paciente cancele un turno propio a través de
> la web.
>
> **Entradas:** identificador del turno, identificador del paciente autenticado.
>
> **Precondición:** el turno existe, está en estado *Confirmado* y faltan más de 24 horas para su
> inicio.
>
> **Proceso:** el sistema verifica la precondición, cambia el estado del turno a *Cancelado*,
> libera la franja horaria en la agenda del profesional y registra la operación en la bitácora.
>
> **Salidas:** confirmación en pantalla y correo de aviso al paciente.
>
> **Postcondición:** la franja queda disponible para otro paciente.
>
> **Excepción:** si faltan menos de 24 horas, el sistema rechaza la cancelación y muestra el
> mensaje indicando que debe comunicarse telefónicamente con recepción.
>
> **Prioridad:** Alta · **Origen:** entrevista con la jefa de recepción, 12/03/2026

**Fijate qué permite esto:** de la precondición y la excepción salen dos casos de prueba, casi sin
pensar. Ese es el estándar al que hay que llegar.

----

![Tabla efectos](images/unidad3/tabla_efecto.jpg)

---
### Requerimientos No Funcionales
<!-- .slide: style="font-size: 0.90em" -->

También llamados **atributos de calidad** o **criterios de calidad**. Definen **cómo** debe
comportarse el sistema, en lugar de **qué** debe hacer.

No son secundarios: si no se cumplen, el sistema puede resultar inutilizable aunque todas sus
funciones estén implementadas.

----

### Los más habituales
<!-- .slide: style="font-size: 0.72em" -->

* **Performance** — Capacidad de responder con eficiencia: tiempo de carga, velocidad de
  procesamiento, uso de memoria y CPU.
* **Seguridad** — Autenticación, control de acceso, encriptación, prevención de ataques.
* **Disponibilidad** — Que el sistema esté operativo cuando se lo necesita; minimizar el tiempo de
  inactividad no planificado.
* **Mantenibilidad** — Facilidad para modificar y mejorar el software: legibilidad, documentación,
  modularidad.
* **Portabilidad** — Capacidad de ejecutarse en distintas plataformas sin cambios significativos.
* **Escalabilidad** — Absorber un aumento de carga sin degradarse.
* **Usabilidad** — Facilidad de uso, navegación intuitiva, eficiencia del usuario.
* **Cumplimiento normativo** — Regulaciones aplicables al dominio.
* **Eficiencia de recursos** — Consumo de energía, ancho de banda, almacenamiento.

----

### El error más común: no medirlos
<!-- .slide: style="font-size: 0.75em" -->

| Mal escrito | Bien escrito |
|---|---|
| El sistema debe ser rápido | El 95% de las búsquedas de turno deberá responder en menos de 2 segundos con 200 usuarios concurrentes |
| El sistema debe ser fácil de usar | Un recepcionista sin experiencia previa deberá completar la carga de un turno en menos de 90 segundos tras 4 horas de capacitación |
| El sistema debe ser seguro | Las contraseñas deberán almacenarse con hash bcrypt; la sesión deberá expirar tras 15 minutos de inactividad |
| El sistema debe estar siempre disponible | La disponibilidad mensual no deberá ser inferior al 99,5% en el horario de 07:00 a 21:00 |

**La columna izquierda no son requerimientos, son *objetivos*.** Sirven para comunicar la
intención, pero no se pueden verificar. Todo requerimiento no funcional necesita una métrica, un
valor y una condición de medición.

---

### 💡 Ejercicio: Convertir objetivos en requerimientos
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.78em" -->

Reescriban cada objetivo como un requerimiento no funcional **verificable**. Necesitan una
métrica, un valor y una condición de medición.

1. "El sistema tiene que ser confiable." <!--Ej: la tasa de fallos no deberá superar 1 cada 1000 operaciones; el tiempo medio de recuperación tras un fallo no deberá superar los 15 minutos.-->
2. "Los reportes tienen que salir rápido." <!--Ej: el reporte mensual de ausentismo deberá generarse en menos de 10 s para un volumen de hasta 20.000 turnos.-->
3. "La app debe andar bien en el celular." <!--Ej: la interfaz deberá ser usable en pantallas desde 320 px de ancho, y la carga inicial no deberá superar los 3 s en una conexión 4G.-->
4. "El sistema debe ser accesible para adultos mayores." <!--Ej: deberá cumplir WCAG 2.1 nivel AA; el tamaño mínimo de fuente será 16 px y el contraste mínimo 4.5:1.-->

<!--
Cierre: notar que para escribir la versión verificable hace falta información que el objetivo no
tiene (¿cuántos turnos? ¿qué conexión? ¿qué norma?). Por eso este ejercicio, en la vida real,
termina en otra reunión con el cliente. Ese es el aprendizaje.
-->

---

### 💡 Ejercicio: Detectar la sección
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.72em" -->

¿En qué sección del SRS va cada una de estas frases?

1. "El centro médico ya tiene contratado el servicio de correo con un proveedor externo." <!--Supuestos y Dependencias-->
2. "El sistema deberá enviar un recordatorio 24 horas antes del turno." <!--Requerimientos Funcionales-->
3. "No se incluirá la gestión de obras sociales." <!--Alcance (funcionalidades excluidas)-->
4. "Sobreturno: turno asignado fuera de los horarios regulares de la agenda." <!--Definiciones, Acrónimos y Abreviaturas-->
5. "La base de datos debe ser PostgreSQL porque es la que ya usa el centro." <!--Restricciones-->
6. "Los recepcionistas tienen secundario completo y usan sistemas de gestión a diario." <!--Características de los Usuarios-->
7. "El sistema consulta el padrón de profesionales de SISADM mediante su API REST." <!--Perspectiva del Producto, y el detalle del formato y protocolo en Interfaces Externas-->
8. "La disponibilidad no deberá ser inferior al 99,5% mensual." <!--Requerimientos No Funcionales-->

<!--
La 7 es la interesante: puede ir en dos lados y está bien que así sea. En Perspectiva del Producto
se explica la relación entre sistemas; en Interfaces Externas se detalla el contrato técnico.
-->

---

### 💡 Ejercicio: Escribir un requerimiento completo
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.78em" -->

Tomen esta frase suelta de una reunión con el cliente:

> *"Necesitamos que recepción pueda meter un sobreturno cuando llega alguien urgente."*

Escríbanla como un requerimiento funcional completo, con el formato de RF-07: descripción,
entradas, precondición, proceso, salidas, postcondición, excepciones, prioridad y origen.

Después respondan: **¿cuántas preguntas nuevas al cliente les generó el ejercicio?**

<!--
Preguntas que deberían aparecer: ¿quién puede autorizar un sobreturno? ¿hay un máximo por día o
por profesional? ¿qué pasa si el profesional ya se fue? ¿se le avisa? ¿cuenta para las
estadísticas de ocupación? ¿el paciente recibe confirmación?
El punto del ejercicio: una frase de diez palabras esconde seis decisiones sin tomar. Redactar el
requerimiento con formato completo es lo que las hace visibles.
-->

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
