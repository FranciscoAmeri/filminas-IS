---
title: Modelado de Sistemas
theme: solarized
slideNumber: true
---

#### Ingeniería de Software
# Modelado de Sistemas
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

.fuente {
  border-top: 2px solid rgba(121, 177, 217, 0.6);
  padding-top: 8px;
  margin-top: 14px;
  font-size: 0.78em;
}
</style>
## Temario
<div class="grid-container2">
<div class="grid-item">

### Modelado de Sistemas
* Modelos de Sistemas
* Perspectivas del Sistema
* Tipos de Diagramas UML
* Qué diagrama usar para qué
* Uso de modelos gráficos
* Modelos de Contexto
* Límites del sistema
* Perspectiva del proceso
* Modelos de Interacción
* Modelado de Casos de Uso
</div>
<div class="grid-item">

* Diagramas de Secuencia
* Modelos Estructurales
* Diagramas de Clases
* Generalización
* Agregación
* Modelos de Comportamiento
* Modelado Impulsado por Datos
* Modelado Impulsado por Eventos
* Modelos de Máquina de Estado
* Ingeniería Dirigida por Modelos
</div>
</div>

---

## Libro:
![Book](images/book.png)
“Ingeniería del Software: Un enfoque práctico 7ma ed.” de Roger Pressman
Apéndice 1: Introducción a UML

---

### Modelado de Sistemas

<!--https://diagramasuml.com/-->

Un **modelo es una abstracción** de un sistema o entidad del mundo real. 

Una **abstracción es una simplificación**, que incluye sólo aquellos detalles relevantes para algún determinado propósito.

El modelado permite abordar la complejidad de los sistemas.

---

### El modelado de sistemas
* El modelado de sistemas es el proceso de elaboración de modelos abstractos de un sistema, con cada modelo que presenta 
una vista o perspectiva diferente de ese sistema.
* El modelado de sistemas se representa mediante algún tipo de notación gráfica, casi siempre basada en anotaciones en 
el Lenguaje Unificado de Modelado (UML).
* El modelado de sistemas ayuda al analista a entender la funcionalidad del sistema y se pueden utilizar modelos para 
comunicarse con los clientes.

----

### Modelos de sistemas
* Los modelos del sistema se utilizan durante la ingeniería de requisitos para ayudar a explicar los requisitos 
propuestos a otros actores del sistema. Los ingenieros utilizan estos modelos para discutir las propuestas de diseño y 
documentar el sistema de aplicación.
* En un proceso de ingeniería basado en modelos, es posible generar una implementación completa o parcial del sistema 
desde el modelo del sistema.

---

### Perspectivas del sistema
* Una **perspectiva externa**, donde se modela el contexto o el entorno del sistema.
* Una **perspectiva de interacción**, donde se modelan las interacciones entre un sistema y su entorno, o entre los 
componentes de un sistema.
* Una **perspectiva estructural**, donde se modela la organización de un sistema o de la estructura de los datos que son 
procesados por el sistema.
* Una **perspectiva conductual**, en la que se modela el comportamiento dinámico del sistema y la forma en que responde 
a los eventos.

----

### Ejemplo:
````java
package codemodel;

public class Guitarist extends Person implements MusicPlayer {

    Guitar favoriteGuitar;

    public Guitarist(String name) { super(name); }

    public void setInstrument(Instrument instrument) {
        if (instrument instanceof Guitar) {
            this.favoriteGuitar = (Guitar) instrument;
        } else {
            System.out.println("I'm not playing that thing!");
        }
    }

    public Instrument getInstrument() { return this.favoriteGuitar; }

    public void play() { /* implementa MusicPlayer */ }

    public static void main(String[] args) { }
}
````
* Representa sólo la lógica e ignora el resto
* El ser humano lo interpreta muy lentamente
* No facilita la reutilización ni la comunicación

---
````text
Guitarist es una clase que contiene seis miembros: 1 estático y 5
no estáticos. Guitarist usa, y por lo tanto necesita, una instancia 
de Guitar; Sin embargo, dado que esto podría compartirse con otras 
clases en su paquete, la variable de instancia Guitar, llamada 
favoritoGuitar, se declara como predeterminada.
Cinco de los miembros dentro de Guitarist son métodos. Cuatro no son 
estáticos. Uno de estos métodos es un constructor que toma un argumento, 
y las instancias de String se llaman nombre, lo que elimina el constructor 
predeterminado.
Luego se proporcionan tres métodos regulares. El primero se llama setInstrument, 
y toma un parámetro, una instancia de Instrument llamada instrument, y 
no tiene tipo de retorno. El segundo se llama getInstrument y no tiene 
parámetros, pero su tipo de retorno es Instrument. El método final se 
llama play. El método de reproducción en realidad lo aplica la interfaz 
MusicPlayer que implementa la clase Guitarrista. El método play no toma 
parámetros y su tipo de retorno es nulo.
````
* Es ambigua y confusa
* Es lenta de interpretar
* Difícil de procesar

---
![UML: Guitarrista](images/unidad5/ejemplo_guitarrista.jpg)

<!-- .slide: style="font-size: 0.60em" -->
* No es ambigua ni confusa (una vez conocemos la semántica de cada elemento de modelado)
* Es fácil y rápida de interpretar
* Es fácil de procesar por herramientas

---
### UML
* Siglas de "Unified Modeling Language".
* Lenguaje de modelado estándar para modelado orientado a objetos.
* Define 14 tipos de diagramas, pero en la gran mayoría de sistemas se usan solo **5**.
* UML puede usarse para visualizar, especificar, construir y documentar los artefactos de un sistema de software

![Logo UML](images/unidad5/logo-UML.png)

----

### ¿Por qué UML?
* Es **sencillo**
* Es capaz de modelar todo tipo de sistemas.
* Es un lenguaje universal
* Es fácilmente extensible.
* Es visual y, por lo tanto, intuitivo.
* Es independiente del desarrollo, del lenguaje y de la plataforma.
* Bien ejecutado aporta un conjunto considerable de buenas prácticas.

----

### Consideraciones sobre UML
Los diagramas UML NO son completos. Utilizando los distintos diagramas no podemos estar seguros de comprender con 
totalidad el sistema que va a desarrollarse. Los diagramas, para facilitar la comprensión pueden (y suelen) omitir 
información, pueden tener partes que se entienden de distintas maneras o, incluso, pueden tener conceptos que no 
pueden ser representados por ningún diagrama.

----

### ¿Con qué se dibujan?
<!-- .slide: style="font-size: 0.85em" -->

* **StarUML** — específica de UML, valida el modelo y genera código. Es la que usamos en la materia.
* **Draw.io / Lucidchart** — de propósito general: dibujan rápido, pero no entienden UML ni avisan si el modelo es inconsistente.
* **PlantUML** — el diagrama se escribe como texto y se versiona junto al código, así que no queda desactualizado.

**La diferencia que importa:** una herramienta que *entiende* UML detecta errores de consistencia;
una que solo *dibuja*, no. Con la segunda el diagrama puede estar mal y verse bien.

---

![Clasificación de los diagramas UML](images/unidad5/clasificacion-diagramas.png)

---

### Diagramas UML
<!--http://www.softwero.com/2017/08/los-13-diagramas-uml-y-sus-componentes-1.html-->

<div class="grid-container2">
<div class="grid-item">

### Diagramas de Estructura

1. Diagrama de Clases
2. Diagrama de Objetos
3. Diagrama de Componentes
4. Diagrama de Estructura Compuesta
5. Diagrama de Despliegue
6. Diagrama de Paquetes
7. Diagrama de Perfiles

</div>
<div class="grid-item">

### Diagramas de Comportamiento

8. Diagrama de Actividad
9. Diagrama de Casos de Uso
10. Diagrama de Máquinas de Estado
11. Diagrama de Secuencia
12. Diagrama de Comunicaciones
13. Diagrama de Tiempo
14. Diagrama de Descripción de Interacción

</div></div>

**UML 2.5 define 14 diagramas: 7 de estructura y 7 de comportamiento.**
Los cuatro últimos de comportamiento son, en rigor, **diagramas de interacción**.

----

### Tipos de diagramas UML

<!-- .slide: style="font-size: 0.90em" -->
* **Diagramas de actividades:** Muestran las actividades involucradas en un proceso o en el procesamiento de datos.
* **Diagramas de casos de uso:** Muestran las interacciones entre un sistema y su entorno.
* **Diagramas de secuencia:** Muestran las interacciones entre los actores y el sistema y entre los componentes del sistema.
* **Diagramas de clases:** Muestran las clases de objetos en el sistema y las asociaciones entre estas clases.
* **Diagramas de estado:** Muestran cómo el sistema reacciona a los acontecimientos internos y externos.

----

### Cada perspectiva tiene su diagrama
<!-- .slide: style="font-size: 0.70em" -->

Al principio vimos cuatro perspectivas del sistema. **Así se conectan con los cinco diagramas:**

| Perspectiva | ¿Qué modela? | Diagrama |
|---|---|---|
| **Externa** | El contexto: qué queda dentro y fuera del sistema | Modelo de contexto |
| **De interacción** | Cómo se comunican el sistema y su entorno, o sus componentes entre sí | Casos de uso · Secuencia |
| **Estructural** | Cómo se organiza el sistema y los datos que procesa | Clases |
| **Conductual** | Cómo responde el sistema a estímulos: datos o eventos | Actividad (datos) · Estado (eventos) |

**No se elige un diagrama porque sí:** se elige la perspectiva desde la que hace falta mirar el
sistema, y esa perspectiva determina el diagrama.

----

### ¿Qué diagrama responde qué pregunta?
<!-- .slide: style="font-size: 0.70em" -->

| Si necesitás saber… | Usá |
|---|---|
| ¿Dónde termina mi sistema y empieza otro? | **Modelo de contexto** |
| ¿Quién usa el sistema y para qué? | **Casos de uso** |
| ¿En qué orden se llaman los objetos para resolver una tarea? | **Secuencia** |
| ¿Qué entidades existen y cómo se relacionan? | **Clases** |
| ¿Cuál es el flujo de trabajo, con sus decisiones y ramas? | **Actividad** |
| ¿En qué estados puede estar esto y qué lo hace cambiar? | **Máquina de estado** |

**Un mismo sistema necesita varios.** Ninguno lo describe entero: cada uno responde una
pregunta distinta, y por eso el modelado es siempre un conjunto de vistas.

----

### 💡 Ejercicio: ¿Qué diagrama usarías?
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.68em" -->

Para cada necesidad, elegí **un** diagrama y justificá en una línea:

1. Hay que decidir si la facturación la resuelve nuestro sistema o el sistema contable que ya existe. <!--Modelo de contexto: define los límites del sistema.-->
2. El cliente quiere ver de un vistazo todo lo que podrá hacer cada tipo de usuario. <!--Casos de uso.-->
3. Un pedido puede estar pendiente, pagado, en preparación, enviado o cancelado, y no todas las transiciones son válidas. <!--Máquina de estado.-->
4. Hay que documentar qué objetos intervienen, en qué orden, cuando alguien saca un turno. <!--Diagrama de secuencia.-->
5. Necesitamos saber qué datos guarda el sistema y cómo se vinculan entre sí. <!--Diagrama de clases.-->
6. El equipo discute si la aprobación de un pedido va antes o después del control de stock. <!--Diagrama de actividad: modela el flujo del proceso de negocio.-->

<!--
Cierre: en el 1 y el 6 la respuesta se confunde seguido. El de contexto responde "¿esto es
parte de mi sistema?"; el de actividad responde "¿en qué orden ocurren las cosas?".
-->

---
### El uso de modelos gráficos
* Como una forma de facilitar el debate sobre un sistema
* Como una manera de **documentar** el sistema: el modelo debe ser una representación exacta, pero no tiene que ser completa.
* Como una **descripción detallada** del sistema: en ese caso sí debe ser correcta y completa.

---
### Modelos de contexto
* Se utilizan modelos de contexto para ilustrar el contexto operativo de un sistema, muestran lo que se
encuentra fuera de los límites del sistema.
* Las cuestiones organizacionales pueden influir en la decisión sobre dónde situar los límites del sistema.
* Los modelos de contexto muestran el sistema y su relación con otros sistemas.

----

### Límites del sistema
* Los límites del sistema se establecen para definir lo que está dentro y lo que está fuera del sistema, muestran otros
sistemas que se utilizan o dependen del sistema que está siendo desarrollado.
* La posición de los límites del sistema tiene un efecto profundo en los requisitos del sistema.
* La definición del límite del sistema es fundamental: si los límites aumentan o disminuyen, cambia la
carga de trabajo de las diferentes partes de una organización.

----

#### El contexto del MHC-PMS
<!-- .slide: style="font-size: 0.85em" -->

> **MHC-PMS** (*Mental Health Care Patient Management System*): sistema de gestión de pacientes
> de salud mental. Es el caso de estudio que se usa en todos los ejemplos de esta unidad.

![Ejemplo de Diagrama de Contexto](images/unidad5/diagrama_contexto_mhc-pms.jpg)

---

### Perspectiva del proceso
* Los modelos de contexto simplemente muestran los otros sistemas del ambiente, no cómo se utiliza en ese
entorno el sistema que está siendo desarrollado.
* Los modelos de proceso revelan cómo se utiliza el sistema en desarrollo en los procesos de negocio
* Diagramas de actividades de UML se pueden utilizar para definir los modelos de procesos de negocio.

----

### Diagrama de Actividad
![Modelo de proceso de la detención involuntaria](images/unidad5/modelo_proceso_detencion.jpg)

---
### Modelos de interacción
<!-- .slide: style="font-size: 0.90em" -->
* El modelado de la interacción de usuario es importante ya que ayuda a identificar las necesidades de los usuarios.
* El modelado de interacción de sistema a sistema resalta los problemas de comunicación que puedan surgir.
* El modelo de interacción de componentes ayuda a comprender si la estructura del sistema propuesto es
adecuada para ofrecer el rendimiento y la fiabilidad del sistema necesario.
* Los **diagramas de casos de uso** y los **diagramas de secuencia** se pueden utilizar para el modelado de la interacción.

---
### Modelado de casos de uso
* Los casos de uso se desarrollaron originalmente para apoyar la obtención de **requisitos** y están incorporados en el UML.
* Especifica un comportamiento deseado del sistema.
* Representa los requisitos funcionales del sistema.
* Describe qué hace el sistema, no cómo lo hace.
* Cada caso de uso es una **tarea discreta** que implica interacción externa con el sistema, y sus **actores** pueden ser personas u otros sistemas.
* Se documenta en dos niveles: una **representación esquemática** para la visión general, y una **textual** para el detalle.

<div class="fuente">

📎 **La notación completa está en [Práctico: Casos de Uso](U5P_2_UML_casos_de_uso.html)** — acá solo vemos para qué sirve.

</div>

----

### Los casos de uso en el MHC-PMS que implica el papel 'Médico Recepcionista'
![Casos de uso Médico Recepcionista](images/unidad5/ejemplo_caso_de_uso.jpg)

---
### Diagramas de secuencia
<!-- .slide: style="font-size: 0.90em" -->
* Los diagramas de secuencia son parte de UML y se utilizan para modelar las interacciones entre los actores y
los objetos dentro de un sistema.
* Un diagrama de secuencia muestra la secuencia de interacciones que tienen lugar durante un caso de uso en particular.
* Los objetos y los actores involucrados están listados en la parte superior del diagrama, con una línea de puntos
trazada verticalmente a partir de estos.
* Las interacciones entre los objetos se indican mediante flechas anotadas.

----

### Diagrama de secuencia para Ver la información del paciente
![Diagrama de secuencia: Ver información del paciente](images/unidad5/diagrama_secuencia.jpg)

<div class="fuente">

📎 **La notación completa está en [Práctico: Diagrama de Secuencia](U5P_4_UML_diagramas_secuencia.html)** — acá solo vemos para qué sirve.

</div>

---
### Modelos estructurales
* Los modelos estructurales muestran la organización de un sistema en función de los componentes que conforman
este sistema y sus relaciones.
* Los modelos estructurales son modelos estáticos, que muestran la estructura del sistema.

---
### Diagramas de clases
* Los diagramas de clases se utilizan en el desarrollo de un modelo de sistema orientado a objetos para mostrar las
clases de un sistema y las asociaciones entre estas clases.
* Una clase de objeto es una definición general de un tipo de objeto del sistema.
* Una asociación es una relación entre clases.
* Los objetos representan algo en el mundo real, tal como un paciente, una prescripción, médico, etc.

----

### Las clases y asociaciones en el MHC-PMS
![Clases y asociaciones en el MHC-PMS](images/unidad5/clases_asociaciones_MHC-PMS.jpg)

<div class="fuente">

📎 **La notación completa está en [Práctico: Diagrama de Clases](U5P_3_UML_diagrama_clase.html)** — acá solo vemos para qué sirve.

</div>

----

### 💡 Ejercicio: Del enunciado al modelo
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.70em" -->

> *"La biblioteca de la facultad presta libros a estudiantes y docentes. Cada préstamo lo
> registra un bibliotecario, tiene una fecha de retiro y una de devolución, y alcanza a un
> único ejemplar. Un mismo título puede tener varios ejemplares. Los docentes pueden llevarse
> hasta cinco libros; los estudiantes, dos."*

1. Identificá los **actores** y al menos tres **casos de uso**.
2. Identificá las **clases candidatas** y sus **asociaciones**, con las multiplicidades.
3. ¿Dónde ubicarías la regla de los cinco libros y los dos libros? ¿Es una clase, un atributo
   o algo que no se representa en el diagrama de clases?

<!--
1. Actores: Estudiante, Docente, Bibliotecario. Casos de uso: registrar préstamo, devolver
   ejemplar, consultar disponibilidad, registrar socio.
2. Clases: Socio (con Estudiante y Docente como especializaciones), Préstamo, Ejemplar, Título.
   Un Título tiene muchos Ejemplares (1..*); un Préstamo alcanza un único Ejemplar (1); un
   Socio puede tener varios Préstamos (0..*).
3. Es el punto interesante. El límite distinto por tipo de socio se resuelve con
   generalización: un atributo "máximo de préstamos" en Socio, con valor distinto en cada
   subclase. La REGLA de que no se puede exceder ese máximo es una restricción de
   comportamiento: no se ve en el diagrama de clases. Ahí es donde el modelo estructural
   muestra su límite y hace falta otra vista.
-->

---
### Generalización
* La generalización es una técnica que utilizamos para gestionar la complejidad.
* En lugar de definir las características detalladas de cada entidad, ponemos estas características en las clases
más generales (animales, coches, casas, etc).
* Esto nos permite inferir que los diferentes miembros de estas clases tienen algunas características comunes.
* En lenguajes orientados a objetos se implementa con **herencia**: las subclases heredan los atributos y
  operaciones de sus superclases, y pueden agregar los suyos propios.

----

### Una jerarquía de generalización
![Una jerarquía de generalización](images/unidad5/jerarquia_de_generalizacion.jpg)

<div class="fuente">

📎 **La notación completa está en [Práctico: Diagrama de Clases](U5P_3_UML_diagrama_clase.html)** — acá solo vemos para qué sirve.

</div>

---
### Agregación
<!-- .slide: style="font-size: 0.85em" -->
Un modelo de agregación muestra cómo unas clases **se componen** de otras. Es la relación
"parte de": equivale a la relación de parte en los modelos de datos semánticos.

![Agregacion](images/unidad5/agregacion.jpg)

<div class="fuente">

📎 **La notación completa está en [Práctico: Diagrama de Clases — agregación vs. composición](U5P_3_UML_diagrama_clase.html#/5/6)** — acá solo vemos para qué sirve.

</div>

---

### Modelos de comportamiento
* Modelos de comportamiento son los modelos del comportamiento dinámico de un sistema, cuando se está ejecutando.
* Muestran lo que ocurre cuando un sistema responde a un estímulo de su entorno.
* Los estímulos pueden ser de dos tipos: **Datos** o **Eventos**

---

### Modelado impulsado por datos
* Muchos sistemas empresariales son sistemas de procesamiento de datos. Son controlados por la entrada de
datos al sistema, con relativamente poco procesamiento de eventos externos.
* Estos modelos muestran la secuencia de las acciones involucradas en el procesamiento de datos de entrada y la
salida asociada.
* Son particularmente útiles durante el análisis de los requisitos, ya que pueden ser utilizados para mostrar el
procesamiento de extremo a extremo en un sistema.

----

### Un modelo de actividad de la operación de la bomba de insulina

![Modelo de actividad de Bomba de insulina](images/unidad5/modelo_actividad_bomba_insulina.jpg)

----

#### Procesamiento de pedidos

![Procesamiento de pedidos](images/unidad5/procesamiento_de_pedidos.jpg)

----

### Modelado impulsado por eventos

* Sistemas de tiempo real son a menudo gestionados por eventos, con un procesamiento de datos mínimo.
* Modelado por eventos muestra cómo un sistema responde a acontecimientos externos e internos.
* Se basa en la suposición de que un sistema tiene un número finito de estados y que los acontecimientos
(estímulos) puede causar una transición de un estado a otro.

---
### Modelos de máquina de Estado
* Estos modelan el comportamiento del sistema en respuesta a eventos externos e internos.
* Muestran las respuestas del sistema a los estímulos, por lo que se utilizan a menudo para modelar sistemas de tiempo real.
* Modelos de máquinas de estado muestran los estados del sistema como nodos y eventos como arcos entre estos
nodos. Cuando ocurre un evento, el sistema pasa de un estado a otro.

----

### Diagrama de estado de un horno de microondas
![Diagrama de estado: Microondas](images/unidad5/diagrama_estado_microondas.jpg)

----

### Los Estados y los estímulos para el horno de microondas
<!-- .slide: style="font-size: 0.50em" -->
<!--
| Estado            | Descripción                                                                                                                                                                                                                                                                    |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Esperando         | El horno está a la espera para la entrada. La pantalla muestra la hora actual.                                                                                                                                                                                                 |
| Potencia Media    | La potencia del horno es de 300 vatios. La pantalla muestra 'Potencia Media'.                                                                                                                                                                                                  |
| Potencia Completa | La fuente de horno se establece en 600 vatios. La pantalla muestra 'Potencia Máxima'.                                                                                                                                                                                          |
| Establecer tiempo | El tiempo de cocción se ajusta al valor de entrada del usuario. La pantalla muestra el tiempo de cocción seleccionado y se actualiza a medida que el tiempo se ajusta.                                                                                                         |
| Deshabilitar      | El funcionamiento del horno está deshabilitado por seguridad. Luz interior del horno está encendido. La pantalla muestra "No está listo'.                                                                                                                                      |              
| Habilitado        | Se habilita el funcionamiento del horno. Luz interior del horno está apagado. La pantalla muestra "Listo para cocinar'.                                                                                                                                                        |   
| Operacion         | Horno en funcionamiento. Luz interior del horno está encendido. La pantalla muestra la cuenta atrás del temporizador. Al término de la cocción, el zumbador suena durante cinco segundos. La luz del horno está encendido. La pantalla muestra 'Cocinando completa ", mientras |                                                                                                                                                                                                                                                       
-->
<table>
<thead>
<tr>
<th style="text-align:left">Estado</th>
<th style="text-align:left">Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Esperando</td>
<td style="text-align:left">El horno está a la espera para la entrada. La pantalla muestra la hora actual.</td>
</tr>
<tr>
<td style="text-align:left">Potencia Media</td>
<td style="text-align:left">La potencia del horno es de 300 vatios. La pantalla muestra &#39;Potencia Media&#39;.</td>
</tr>
<tr>
<td style="text-align:left">Potencia Completa</td>
<td style="text-align:left">La fuente de horno se establece en 600 vatios. La pantalla muestra &#39;Potencia Máxima&#39;.</td>
</tr>
<tr>
<td style="text-align:left">Establecer tiempo</td>
<td style="text-align:left">El tiempo de cocción se ajusta al valor de entrada del usuario. La pantalla muestra el tiempo de cocción seleccionado y se actualiza a medida que el tiempo se ajusta.</td>
</tr>
<tr>
<td style="text-align:left">Deshabilitar</td>
<td style="text-align:left">El funcionamiento del horno está deshabilitado por seguridad. Luz interior del horno está encendido. La pantalla muestra &#39;No está listo&#39;.</td>
</tr>
<tr>
<td style="text-align:left">Habilitado</td>
<td style="text-align:left">Se habilita el funcionamiento del horno. Luz interior del horno está apagado. La pantalla muestra &#39;Listo para cocinar&#39;.</td>
</tr>
<tr>
<td style="text-align:left">Operación</td>
<td style="text-align:left">Horno en funcionamiento. La luz interior está encendida. La pantalla muestra la cuenta atrás del temporizador. Al término de la cocción, el zumbador suena durante cinco segundos y la pantalla muestra &#39;Cocción completa&#39; mientras la puerta siga cerrada.</td>
</tr>
</tbody>
</table>

----

### Los Estados y los estímulos para el horno de microondas
<!-- .slide: style="font-size: 0.60em" -->
<!--
| Estimulo | Descripción                                                   |
|:---------|:--------------------------------------------------------------|
| Potencia Media | El usuario ha pulsado el botón de media potencia.       |
| Potencia Máxima | El usuario ha pulsado el botón de alta potencia.       |
| Temporizador | El usuario ha pulsado el botón del temporizador.          |
| Nú mero | El usuario ha pulsado una tecla numérica.                     |
| Puerta Abierta | El interruptor de la puerta del horno no está cerrada.  |
| Puerta Cerrada | El interruptor de la puerta del horno está cerrada.     |
| Iniciar | El usuario ha pulsado el botón de Inicio.                     |
| Cancelar | El usuario oprime el botón Cancelar                           |
-->
<table>
<thead>
<tr>
<th style="text-align:left">Estimulo</th>
<th style="text-align:left">Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Potencia Media</td>
<td style="text-align:left">El usuario ha pulsado el botón de media potencia.</td>
</tr>
<tr>
<td style="text-align:left">Potencia Máxima</td>
<td style="text-align:left">El usuario ha pulsado el botón de alta potencia.</td>
</tr>
<tr>
<td style="text-align:left">Temporizador</td>
<td style="text-align:left">El usuario ha pulsado el botón del temporizador.</td>
</tr>
<tr>
<td style="text-align:left">Número</td>
<td style="text-align:left">El usuario ha pulsado una tecla numérica.</td>
</tr>
<tr>
<td style="text-align:left">Puerta Abierta</td>
<td style="text-align:left">El interruptor de la puerta del horno no está cerrada.</td>
</tr>
<tr>
<td style="text-align:left">Puerta Cerrada</td>
<td style="text-align:left">El interruptor de la puerta del horno está cerrada.</td>
</tr>
<tr>
<td style="text-align:left">Iniciar</td>
<td style="text-align:left">El usuario ha pulsado el botón de Inicio.</td>
</tr>
<tr>
<td style="text-align:left">Cancelar</td>
<td style="text-align:left">El usuario oprime el botón Cancelar</td>
</tr>
</tbody>
</table>

----

### El funcionamiento del horno de microondas
![Funcionamiento Microondas](images/unidad5/funcionamiento_microondas.jpg)

----

### 💡 Ejercicio: Modelar una máquina de estados
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.72em" -->

Modelá el ciclo de vida de un **pedido en una tienda online**.

1. Listá los **estados** posibles del pedido.
2. Listá los **eventos** que provocan cada transición.
3. Dibujá el diagrama de máquina de estados.
4. Respondé: ¿hay algún estado del que no se pueda salir? ¿Y alguno al que se pueda llegar por
   más de un camino?

<!--
Estados típicos: Pendiente de pago · Pagado · En preparación · Enviado · Entregado ·
Cancelado · Devuelto.
Eventos: confirmar pago, rechazar pago, preparar, despachar, confirmar entrega, cancelar,
solicitar devolución.
4. "Entregado" y "Cancelado" son estados finales: no se sale de ellos (salvo que se modele
la devolución, y ahí Entregado deja de ser final). A "Cancelado" se llega desde varios
estados distintos, y esa es la pregunta que hace pensar: ¿se puede cancelar un pedido ya
enviado? La respuesta es una decisión de negocio, no de modelado — y el diagrama la hace
visible, que es justamente para lo que sirve.
-->

---
### Ingeniería dirigida por modelos
<!-- .slide: style="font-size: 0.90em" -->
* Ingeniería dirigida por modelos (MDE) es un enfoque para el desarrollo de software donde los modelos en lugar
de los programas son los principales resultados del proceso de desarrollo.
* Los programas que se ejecutan en una plataforma de hardware / software se generan automáticamente a partir
de los modelos.
* Los defensores de la MDE sostienen que esto eleva el nivel de abstracción en la ingeniería de software para que
los ingenieros ya no tienen que preocuparse por los detalles del lenguaje de programación o las características
específicas de plataformas de ejecución.

----

### MDA: Model-Driven Architecture

* MDE tiene sus orígenes en MDA. 
* MDA se enfoca en las etapas de diseño e implementación del desarrollo de software
* MDE se interesa por todos los aspectos del proceso de ingeniería de software

----

### Ingeniería dirigida por modelos
El método de MDA recomienda la producción de tres tipos de modelo de sistema 
abstracto:
- **Modelo Independiente de Computación (CIM):** Modela las importantes abstracciones de dominio usadas en el sistema.
- **Modelo Independiente de Plataforma (PIM):** Modela la operación del sistema sin referencia a su implementación.
- **Modelo Específico de Plataforma (PSM):** Traduce el PIM a una plataforma concreta. De un mismo PIM pueden derivarse varios PSM, uno por cada tecnología de destino.

----

![Proceso MDA](images/unidad5/proceso_mda.png)

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
