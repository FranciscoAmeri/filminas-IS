---
title: Usabilidad
theme: solarized
slideNumber: true
---

# Usabilidad
### Ingeniería de Software.

Created by <i class="fab fa-telegram"></i>
[edme88]("https://t.me/edme88")

---
<!-- .slide: style="font-size: 0.60em" -->
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
## Temario
<div class="grid-item">

### Usabilidad
* Definición y medición
* Principios de usabilidad
* Diseño centrado en el usuario (DCU)
  * Objetivos, fases y beneficios
  * Principios básicos
* Metodologías y técnicas del DCU
  * Identificación de los usuarios
  * Prototipado
  * Proceso de evaluación
* Pruebas de usabilidad
* SUS: System Usability Scale

</div>

---
### Usabilidad: Definición

Facilidad con que las personas pueden utilizar una herramienta particular u otro objeto
fabricado por humanos con el fin de alcanzar un objetivo concreto.

---
La norma **ISO 9241-11** la define como la cualidad que tiene un sistema por la cual permite a sus
usuarios alcanzar objetivos específicos con **efectividad, eficiencia y satisfacción** en un
contexto de uso determinado.

El concepto en torno al cual gravita la usabilidad es la **calidad de uso**.

Notar los tres componentes: que se pueda **lograr** el objetivo (efectividad), con **cuánto
esfuerzo** (eficiencia) y **cómo se siente** el usuario al hacerlo (satisfacción). Un sistema puede
ser efectivo y eficiente, y aun así resultar desagradable de usar.

---

### Principios de Usabilidad
* Robustez
* Facilidad de Aprendizaje
* Facilidad de Uso
* Flexibilidad

----

### Robustez
Es el nivel de apoyo al usuario que facilita el cumplimiento de sus objetivos.

Está relacionado con la capacidad de observación del usuario, de recuperación de información y de
ajuste de la tarea al usuario.

----

### Facilidad de Aprendizaje
Facilidad con la que nuevos usuarios desarrollan una interacción efectiva con el sistema o producto.

Está relacionada con:
* La predicibilidad
* La sintetización
* La familiaridad
* La generalización de los conocimientos previos
* La consistencia

----

### Facilidad de Uso
Facilidad con la que el usuario hace uso de la herramienta, con menos pasos o más naturales a su formación específica.

Está relacionada con:
* La eficacia
* La eficiencia

----

### Flexibilidad
Relativa a la variedad de posibilidades con las que el usuario y el sistema pueden intercambiar información.

Abarca la posibilidad de diálogo, la multiplicidad de vías para realizar la tarea, similitud con tareas anteriores
y la optimización entre el usuario y el sistema.

----

### Principios y criterios: cómo se conectan
<!-- .slide: style="font-size: 0.75em" -->

Los cuatro principios describen **qué buscar** en un diseño. Más adelante vamos a ver los criterios
**medibles** que se usan para evaluarlo. No son dos listas rivales: una se mide con la otra.

| Principio (qué buscar) | Se mide con (criterio) |
|---|---|
| Facilidad de aprendizaje | *Learnability*: cuánto tarda un usuario nuevo en su primera tarea |
| Facilidad de uso | Eficacia y eficiencia: cuántos terminan la tarea, y en cuánto tiempo |
| Robustez | Tasa de errores, y qué tan rápido el usuario se recupera de ellos |
| Flexibilidad | Cantidad de caminos alternativos para completar la misma tarea |
| *(transversal)* | Memorabilidad y satisfacción subjetiva |

**El principio sin el criterio es una intención; el criterio sin el principio es un número
sin sentido.**

---
### USABILIDAD

El grado de usabilidad de un sistema es una medida empírica y relativa de su usabilidad.

Se mide a partir de pruebas empíricas y relativas:
* **Empírica:** porque no se basa en opiniones o sensaciones, sino en pruebas de usabilidad
realizadas en laboratorio u observadas mediante trabajo de campo.
* **Relativa:** porque el resultado no es ni bueno ni malo, sino que depende de las metas planteadas

---
### LA USABILIDAD
Es un atributo de calidad que, dependiendo de los usuarios, las tareas y el contexto, mide:
* la facilidad de aprendizaje
* La eficiencia motriz y cognitiva
* la capacidad de recordar lo aprendido
* el manejo de errores
* la satisfacción subjetiva

---
### Diseño centrado en el usuario
El concepto nace de la publicación **User-Centered System Design: New Perspectives on Human-Computer
Interaction (Norman and Draper, 1986).**

Reconocen las necesidades y los intereses de los usuarios, y ponen foco en el diseño basado en las capacidades y 
limitaciones naturales de las personas a fin de lograr una mayor facilidad de uso.

---
![Diseño Centrado en el Usuario](images/unidad4/disenio_centrado_usuario.jpg)

En el ámbito de las interacciones humano-computadora, el DCU pone al usuario como eje central de todos los procesos 
relacionados a la ingeniería de software

---
### DCU: OBJETIVOS
* Satisfacer las necesidades de todos sus usuarios potenciales
* Adaptar la tecnología utilizada a las expectativas de los usuarios
* Crear interfaces que faciliten la consecución de los objetivos de los usuarios

---
### DCU: FASES
<!-- .slide: style="font-size: 0.80em" -->

* **Entender y especificar el contexto de uso:** identificar a las personas a las que se dirige el
producto, para qué lo usarán y en qué condiciones.
* **Especificar requisitos:** identificar los objetivos del usuario y del proveedor del producto a satisfacer.
* **Producir soluciones de diseño:** esta fase se puede subdividir en diferentes etapas secuenciales,
desde las primeras soluciones conceptuales hasta la solución final de diseño; generalmente utilizando
técnicas de prototipado.
* **Evaluar:** es la fase más importante del proceso, en la que se validan las soluciones de diseño (el
sistema satisface los requisitos), o por el contrario se detectan problemas de usabilidad, normalmente
a través de pruebas con usuarios.

---
### DCU: FASES
![Fases del Diseño Centrado en el Usuario](images/unidad4/dcu_proceso.jpg)

---
### DCU - BENEFICIOS
<!-- .slide: style="font-size: 0.90em" -->
* **Aumento de la productividad:** un sistema diseñado siguiendo los principios de usabilidad, y adaptado a la
forma de trabajar del usuario, permitirá más efectividad en lugar de perder el tiempo luchando con un complejo
conjunto de funciones. Un sistema usable permitirá al usuario concentrarse en la tarea en lugar de la herramienta.
* **Reducción de errores:** una significativa proporción de error humano a menudo se le puede atribuir a una
interfaz de usuario mal diseñada. Evitar incoherencias, ambigüedades u otras faltas del diseño de la interfaz
generan menor cantidad de errores del usuario.

----

### DCU - BENEFICIOS
* **Menor capacitación y entrenamiento:** un sistema bien diseñado y usable puede reforzar el aprendizaje,
reduciendo así el tiempo de formación y la necesidad de apoyo humano.
* **Aceptación:** mejorar la aceptación del usuario es a menudo una medida de resultado indirecta del diseño de
un sistema utilizable. La mayoría de los usuarios prefiere utilizar un sistema bien diseñado que proporcione 
información que pueda ser fácilmente accedida y que se presenta en un formato que sea fácil de asimilar y utilizar.

---

### DCU - PRINCIPIOS BÁSICOS
<!-- .slide: style="font-size: 0.80em" -->
* **Participación activa de los usuarios:** entendimiento de estos y de las tareas que requieren. Al incorporar a los
usuarios finales al proceso desde el inicio, se mejora además la aceptación y el compromiso con el sistema, al
sentir que ha sido diseñado teniendo en cuenta sus necesidades y no ha sido impuesto.
* **Iteración en el diseño:** esto implica recibir realimentación por parte de los usuarios finales después de su uso en
varias etapas, las cuales pueden ir desde simples maquetas con papel hasta prototipos de software con mayor grado de 
fidelidad. La respuesta de cada ciclo de iteración se utiliza para desarrollar el siguiente diseño. Se intenta además 
lograr las condiciones más similares al mundo real en el cual se desenvolverán los usuarios con el sistema.

----

### DCU - PRINCIPIOS BÁSICOS
* **Utilizar un equipo multidisciplinario:** el DCU es un proceso de colaboración que se beneficia de la participación 
activa de diversas partes cada una de las cuales tiene conocimiento y experiencia específicos para compartir con el 
resto. El equipo podría incluir gerentes, especialistas en usabilidad, usuarios finales, ingenieros de software, 
diseñadores gráficos, diseñadores de interacción y personal de capacitación y apoyo.

---
### METODOLOGÍAS Y TÉCNICAS DEL DCU
* Identificación de los usuarios
* Prototipado 
* Proceso de evaluación 
* Pruebas de usabilidad

---
### IDENTIFICACIÓN DE LOS USUARIOS
* **Usuarios primarios:** las personas que usarán el producto final para realizar una tarea.
* **Usuarios secundarios:** los que ocasionalmente pueden usar el producto, o aquellos que lo consumen a través de
un intermediario.
* **Usuarios terciarios:** los que se verán afectados por el uso del producto, o pueden tomar decisiones sobre el
mismo 

**Para que el diseño de un producto sea exitoso se deben tener en cuenta los tres niveles de usuarios**

----

## IDENTIFICACIÓN DE LOS USUARIOS: Ejemplo
<!-- .slide: style="font-size: 0.60em" -->
- **Usuarios primarios**
  - **Pacientes:** son quienes usan directamente el sistema para agendar, modificar o cancelar sus citas médicas.
  - **Médicos:** usan el sistema para revisar su agenda y ver a sus pacientes.

- **Usuarios secundarios**
  - **Recepcionistas:** usan el sistema de manera ocasional para ayudar a los pacientes a programar citas o para actualizar información.
  - **Personal de soporte técnico:** accede al sistema para resolver problemas.

- **Usuarios terciarios**
  - **Gerentes del hospital:** no usan el sistema directamente, pero se benefician de los reportes y estadísticas que genera.
  - **Compañías de seguros:** pueden verse afectadas por cómo se gestionan las citas o los datos de pacientes.
  - **Familiares de pacientes:** aunque no usan el sistema, se ven impactados por la calidad del servicio que ofrece.

----

### 💡 Ejercicio: ¿Quiénes son los usuarios?
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.78em" -->

Tomen el **sistema de gestión de la biblioteca de la facultad**. Identifiquen usuarios
**primarios, secundarios y terciarios**, con al menos dos de cada tipo.

Después respondan:

1. ¿Qué requerimiento de usabilidad surge de un usuario **primario** que no surgiría de los demás?
2. ¿Qué pasa si se diseña pensando **solo** en los primarios?

<!--
Primarios: estudiantes que buscan y reservan material; bibliotecarios que registran préstamos.
Secundarios: docentes que consultan bibliografía ocasionalmente; personal de sistemas.
Terciarios: la dirección de la biblioteca (decide el presupuesto según los reportes);
las editoriales o proveedores; los estudiantes de otras sedes afectados por la disponibilidad.

1. Del bibliotecario, que usa el sistema ocho horas por día, surge la necesidad de atajos de
   teclado y de eficiencia por sobre la simplicidad. Del estudiante, que entra dos veces por
   cuatrimestre, surge lo contrario: que se entienda sin aprender nada.
   Ese es el conflicto clásico de usabilidad: usuario frecuente vs. usuario ocasional.
2. Se pierden requerimientos que solo ven los terciarios: qué datos necesita la dirección para
   decidir compras, o qué exige la normativa de accesibilidad. Suelen aparecer tarde y caros.
-->

---
### PROTOTIPADO
<!-- .slide: style="font-size: 0.90em" -->
Una vez que las partes interesadas han sido identificadas y se ha hecho una investigación completa de sus necesidades, 
los diseñadores pueden desarrollar soluciones con diseños alternativos, los cuales pueden ser evaluados por los usuarios.

Estas alternativas pueden ser simples dibujos en lápiz y papel en la fase inicial del proceso. También es posible 
escuchar a los usuarios discutir sobre los diseños alternativos presentados, lo cual posibilita amplificar la 
comprensión de los diseñadores y pueden proporcionar información que no se obtuvo en las entrevistas iniciales, en otras 
palabras las observaciones y el análisis de necesidades ya realizado.

---
### PROCESO DE EVALUACIÓN
<!-- .slide: style="font-size: 0.80em" -->
A medida que avanza el ciclo del diseño, los prototipos (versiones iniciales y limitadas del producto) pueden ser 
producidos y luego probados por los usuarios.

Las evaluaciones ayudarán a identificar criterios medibles de usabilidad:
* **Eficacia:** ¿Cuántas veces los usuarios logran terminar las tareas? ¿Lograron terminar las tareas sin dificultad?
* **Facilidad de Aprendizaje (Learnability):** ¿Cuán fácil resulta para los usuarios llevar a cabo tareas básicas la
primera vez que se enfrentan al diseño?
* **Eficiencia:** Una vez que los usuarios han aprendido el funcionamiento básico del diseño, ¿cuánto tardan en la
realización de tareas?

----

### PROCESO DE EVALUACIÓN
<!-- .slide: style="font-size: 0.80em" -->
* **Cualidad de ser recordado (Memorability):** Cuando los usuarios vuelven a usar el diseño después de un periodo sin 
hacerlo, ¿cuánto tardan en volver a adquirir el conocimiento necesario para usarlo eficientemente?
* **Tasa de errores de usuario:** Durante la realización de una tarea, ¿cuántos errores comete el usuario?, ¿Qué
tan graves son las consecuencias de esos errores?, ¿Qué tan rápido puede el usuario deshacer las consecuencias de sus 
propios errores?
* **Satisfacción subjetiva:** ¿Cuán agradable y sencillo le ha parecido al usuario la realización de las tareas?
Las evaluaciones también revelarán la satisfacción de los usuarios con el producto. Esto se logra solamente
a través de comentarios recogidos en un proceso interactivo e iterativo con la participación de los usuarios

---
### PRUEBAS DE USABILIDAD
<!-- .slide: style="font-size: 0.90em" -->
Se utilizan metodologías que requieren la participación de usuarios reales o de personas que
concuerdan con el perfil de los futuros usuarios.
* Investigación Etnográfica
* Diseño Participativo
* Grupos Focales
* Entrevistas
* Encuestas
* Card sorting
* Usability Testing
* Estudios de Seguimiento
* Evaluación Heurística

----

### PRUEBAS DE USABILIDAD
**La Investigación Etnográfica:** se observa a los usuarios en el lugar donde normalmente se utiliza el sistema (por 
ejemplo, trabajo, hogar, etc.) para recopilar datos sobre quiénes son sus usuarios, cuáles son las tareas y metas que 
se han relacionado con el sistema, y el contexto en el que trabajan para lograr sus objetivos. A partir de esta 
investigación cualitativa, se pueden desarrollar perfiles de usuario, personajes arquetípicos (los usuarios), los 
escenarios y descripciones de tareas.

----

### PRUEBAS DE USABILIDAD
**El Diseño Participativo:** si bien no se considera una técnica en sí misma, es más bien una forma de realización del 
DCU, el diseño participativo emplea a uno o más usuarios representativos durante todo el proceso de desarrollo. Este
enfoque posiciona al usuario final en el corazón del proceso de diseño, desde el inicio mismo del proyecto, aprovechando 
el conocimiento del usuario, habilidades, e incluso las reacciones emocionales, en el diseño.

----

### PRUEBAS DE USABILIDAD
<!-- .slide: style="font-size: 0.90em" -->
**Los Grupos Focales (Focus Group):** son utilizados en las primeras etapas de un proyecto para evaluar conceptos 
preliminares con usuarios representativos. El objetivo es identificar si los conceptos principales, son satisfactorios 
o no, y cómo podrían ser más aceptables y útiles. Se explora cómo los usuarios finales piensan y sienten. Un grupo 
focal es bueno para la información general, cualitativa, pero no para aprender sobre los problemas de rendimiento y los
comportamientos reales del sistema. Las pruebas de usabilidad se consideran mejores para la observación de los 
comportamientos y la medición de los problemas de rendimiento.

----

### PRUEBAS DE USABILIDAD
**Las entrevistas:** con usuarios son una poderosa herramienta cualitativa, pero no para evaluar la usabilidad de un 
diseño, sino para descubrir deseos, motivaciones, valores y experiencias de nuestros usuarios. Durante estas 
entrevistas, el entrevistador debe mostrarse neutral y no dirigir o condicionar las respuestas del entrevistado. Lo
que se pretende es descubrir información que oriente en el diseño, no confirmar creencias sobre cómo son los usuarios.

----

### PRUEBAS DE USABILIDAD
**Las encuestas:** también son una herramienta útil y se pueden utilizar en cualquier momento del ciclo de vida, pero 
se utiliza con mayor frecuencia en las primeras etapas para comprender mejor el potencial usuario. Son una herramienta 
de investigación cuantitativa que complementan a las entrevistas, y permiten medir con validez estadística los conceptos 
hallados con técnicas cualitativas.

----

### PRUEBAS DE USABILIDAD
<!-- .slide: style="font-size: 0.90em" -->
**Card sorting:** consiste en solicitar a un grupo de participantes (los cuales deben tener un perfil acorde con la 
audiencia a la que se dirige el producto) que agrupen los conceptos representados en tarjetas por su similitud semántica. 

Con el objetivo de identificar qué conceptos, de los representados en cada tarjeta, tienen relación semántica entre sí, 
e incluso cuál es el grado de esa relación.

El card sorting es una prueba destinada a comprender la forma en que los usuarios estructuran la información para 
asegurar que será comprendida fácilmente, por tanto tiene lugar en etapas tempranas del proyecto.

----

### PRUEBAS DE USABILIDAD
<!-- .slide: style="font-size: 0.85em" -->
**Usability Testing:** Emplea técnicas para recoger datos empíricos mediante la observación de usuarios finales que
utilizan el sistema para realizar tareas en tiempo real.

Las pruebas se dividen en dos enfoques principales
1. **Primero:** pruebas formales realizadas como verdaderos experimentos, con el fin de confirmar o refutar hipótesis
específicas. 
2. **Segundo:** menos formal, pero riguroso, emplea a un ciclo repetitivo de pruebas destinadas a exponer las
deficiencias de usabilidad y moldear el producto. Una técnica habitual es el **"think-aloud"** (pensamiento en voz alta), que
consiste en pedirle al participante que verbalice lo que piensa mientras usa el sistema.

----

### PRUEBAS DE USABILIDAD
Los **Estudios de Seguimiento** se realizan después de la liberación formal del sistema. La idea es recoger datos que 
se utilizarán para la próxima versión, a través de encuestas, entrevistas y observaciones. Una vez estructurados,
los estudios de seguimiento son, probablemente, las apreciaciones más adecuadas y más precisas de la
facilidad de uso de un sistema.

----

### PRUEBAS DE USABILIDAD
La **Evaluación Heurística** se realiza por inspección: varios expertos analizan el diseño en busca
de potenciales problemas de usabilidad, comprobando el cumplimiento de principios de diseño usable
(principios heurísticos) previamente establecidos.

**¿Cuáles son esos principios?** Los dos conjuntos más usados son las **8 Reglas de Oro de
Shneiderman** y los **10 Principios Heurísticos de Nielsen**. Los vemos completos, con ejemplos,
en la filmina siguiente.

---
### 💡 Ejercicio: ¿Qué técnica usarías?
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.70em" -->

Para cada situación, elegí **una** de las nueve técnicas vistas y justificá en una línea:

1. Todavía no hay ni un boceto. Hay que entender cómo trabaja hoy el personal de recepción. <!--Investigación etnográfica: observar en el lugar real, antes de tener nada que mostrar.-->
2. Hay que decidir cómo agrupar las 40 secciones del menú del sistema. <!--Card sorting: sirve exactamente para descubrir cómo estructura la información el usuario.-->
3. El prototipo está listo y hay que ver si la gente puede sacar un turno sin ayuda. <!--Usability testing con think-aloud: observación de comportamiento real sobre una tarea concreta.-->
4. Hace falta saber qué porcentaje de los 3.000 pacientes usaría la app en el celular. <!--Encuesta: se necesita validez estadística sobre una población grande.-->
5. El sistema salió hace seis meses y hay que planificar la próxima versión. <!--Estudio de seguimiento: datos de uso real posteriores a la liberación.-->
6. Hay dos conceptos de diseño muy distintos y hay que saber cuál genera mejor reacción. <!--Grupo focal: bueno para evaluar conceptos preliminares y explorar percepciones.-->
7. No hay presupuesto ni tiempo para convocar usuarios, pero hay que detectar problemas evidentes. <!--Evaluación heurística: la hacen expertos por inspección, sin usuarios.-->

<!--
Cierre: las técnicas no son intercambiables. Las cualitativas (etnografía, entrevistas, focus)
sirven para descubrir; las cuantitativas (encuestas, testing) para medir y decidir. Usar una
encuesta para descubrir necesidades, o un focus group para medir rendimiento, es el error típico.
-->

---
### SUS: System Usability Scale
<!--https://www.uxables.com/investigacion-ux/medir-con-el-sistema-de-escala-de-usabilidad-sus/-->
Es un cuestionario estandarizado que permite evaluar la percepción de la usabilidad de un sistema digital.

 Fue creado por **John Brooke en 1986** y publicado en 1996 en *Usability Evaluation in Industry*.
Se convirtió en una herramienta ampliamente utilizada por diseñadores, investigadores y
profesionales de la experiencia de usuario (UX).

----

### SUS: Preguntas
<!-- .slide: style="font-size: 0.70em" -->
Las respuestas se califican del 1 al 5:
1. Creo que me gustaría utilizar este (sistema/función/producto) con frecuencia.
2. Encontré el (sistema/función/producto) innecesariamente complejo.
3. Pensé que (sistema/función/producto) era fácil de usar.
4. Creo que necesitaría el apoyo de un técnico para poder utilizar este (sistema/función/producto).
5. Descubrí que las diversas funciones de este (sistema/característica/producto) estaban bien integradas.
6. Pensé que había demasiada inconsistencia en este (sistema/característica/producto).
7. Me imagino que la mayoría de la gente aprendería a utilizar este (sistema/función/producto) muy rápidamente.
8. Encontré el (sistema/función/producto) muy complicado de usar.
9. Me sentí muy seguro al utilizar (sistema/función/producto).
10. Necesitaba aprender muchas cosas antes de poder empezar con este (sistema/función/producto).

----

### SUS: cálculo del puntaje
<!-- .slide: style="font-size: 0.85em" -->
Las preguntas impares están redactadas en positivo y las pares en negativo, por eso se puntúan
distinto:

1. **Impares (1, 3, 5, 7, 9):** sumar las respuestas y **restarle 5** al total.
2. **Pares (2, 4, 6, 8, 10):** sumar las respuestas y **restar ese total a 25**.
3. **Sumar los dos resultados anteriores.**
4. Multiplicar esa suma por **2,5**.

El resultado va de **0 a 100**. No es un porcentaje: es un puntaje en una escala propia.

**Referencia:** el promedio de la industria es **68**. Por debajo de ese valor la usabilidad está
por debajo de la media; por encima de 80 se considera buena.

<!--
Error frecuente: multiplicar por 2,5 solamente el resultado de los pares. Así el puntaje máximo
posible sería 62,5 y no 100, y se estarían descartando las cinco preguntas positivas.
-->

----

### SUS: Escala

![Escala](images/unidad4/sus.webp)

----

### 💡 Ejercicio: Calcular un SUS
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.75em" -->

Un usuario completó el cuestionario con estas respuestas:

| P1 | P2 | P3 | P4 | P5 | P6 | P7 | P8 | P9 | P10 |
|---|---|---|---|---|---|---|---|---|---|
| 4 | 2 | 5 | 1 | 4 | 2 | 5 | 2 | 4 | 2 |

1. Calculen el puntaje SUS.
2. ¿Cómo se interpreta ese resultado?
3. ¿Qué pasaría si se multiplicara por 2,5 **solo** el resultado de las preguntas pares?

<!--
1. Impares (1,3,5,7,9): 4+5+4+5+4 = 22 -> 22-5 = 17
   Pares (2,4,6,8,10): 2+1+2+2+2 = 9 -> 25-9 = 16
   Suma: 17+16 = 33 -> 33 x 2,5 = 82,5
2. 82,5 está bastante por encima del promedio de la industria (68): buena usabilidad percibida.
   Recordar que es percepción, no rendimiento: no reemplaza a un usability testing.
3. Daría 16 x 2,5 = 40, es decir "por debajo de la media". El mismo sistema pasaría de bueno a
   malo por un error de cálculo. Es el error más común al aplicar SUS.
-->

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
