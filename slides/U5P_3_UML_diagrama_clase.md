---
title: Diagrama de Clases
theme: solarized
slideNumber: true
---

#### Ingeniería de Software
# UML: Diagrama de Clases
Created by <i class="fab fa-telegram"></i>
[edme88]("https://t.me/edme88")

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

.avanzado {
  border-left: 4px solid #93a1a1;
  padding-left: 14px;
  font-size: 0.86em;
  color: #586e75;
}
</style>

## Recorrido

<div class="grid-item">

1. **Antes de dibujar** — de dónde salen las clases
2. **La clase** — anatomía y visibilidad
3. **Las relaciones** — asociación, agregación, composición, herencia
4. **Herencia y polimorfismo**
5. **Dependencias y paquetes** *(referencia)*
6. **Ejercicio integrador**

</div>

Los bloques 1 a 4 son los que se usan en el trabajo práctico. El 5 es material de consulta.

---

## 1 · Antes de dibujar
### El workflow de análisis

<!-- .slide: style="font-size: 0.80em" -->

Ayuda a definir y especificar el sistema a construir: se **analizan, refinan y estructuran los
requisitos** para llegar a una mayor comprensión de los mismos.

* Crea modelos que capturan el comportamiento deseado del sistema, y por eso **se solapa con los
  requerimientos**: los clarifica y los completa.
* Los detalles se dejan para el diseño. El límite entre análisis y diseño es difuso.
* Genera dos artefactos clave: las **clases de análisis**, que modelan conceptos del dominio, y
  las **realizaciones de casos de uso**, que muestran cómo esas clases interactúan.

**Solo se crean clases del dominio, no de la solución.** `ControladorBD` o `ServicioHTTP` son
decisiones de implementación: van en diseño, no acá.

----

### Reglas para el análisis
<!-- .slide: style="font-size: 0.85em" -->

* Siempre se habla **en términos del negocio**.
* Los modelos deben "contar una historia": si el diagrama no aclara comportamiento, no sirve.
* Concentrarse en la idea general, no en detalles de implementación.
* Distinguir el **dominio del problema** del **dominio de la solución**.
* Minimizar el acoplamiento.
* Explorar la herencia si parece haber una jerarquía natural de abstracciones.
* Preguntarse siempre si el modelo le sirve a alguien más. Costo contra beneficio.

----

### ¿Qué hace buena a una clase de análisis?
<!-- .slide: style="font-size: 0.82em" -->

* Su **nombre refleja su intención** y se mapea con un concepto del dominio (Cliente, Producto, Cuenta).
* Tiene un conjunto de **responsabilidades bien definidas** — el contrato de la clase con quienes la usan.
* **Alta cohesión** y **bajo acoplamiento**.

**Reglas prácticas:** de 3 a 5 responsabilidades por clase · ninguna clase permanece sola, todas
colaboran · cuidado con las clases omnipotentes y con los árboles de herencia muy profundos ·
encontrar el equilibrio entre muchas clases chicas y pocas enormes es difícil, y es parte del oficio.

---

## 1 · Antes de dibujar
### ¿Cómo se encuentran las clases?

<!-- .slide: style="font-size: 0.85em" -->

**No existe un algoritmo.** Hay tres técnicas probadas que llevan a "una buena respuesta", y se
usan combinadas:

1. Análisis **nombre / verbo**
2. Análisis **CRC**
3. **Estereotipos RUP**

----

### Técnica 1: Nombre / Verbo
<!-- .slide: style="font-size: 0.85em" -->

Análisis directo del texto que describe el dominio:

| En el texto | Se convierte en |
|---|---|
| Nombres y frases nominales | **Clases** y **atributos** |
| Verbos y frases verbales | **Responsabilidades** |

**Es peligroso si el dominio está mal definido:** un enunciado ambiguo produce un modelo ambiguo.
No reemplaza a entender el negocio, lo sistematiza.

----

### Técnica 2: Análisis CRC
<!-- .slide: style="font-size: 0.85em" -->

**C**lase · **R**esponsabilidad · **C**olaboradores. Se trabaja con post-its divididos en tres
compartimentos, en dos fases:

1. **Tormenta de ideas:** recopilar información sin filtrar.
2. **Análisis:** depurar, agrupar y descartar.

Complementa al análisis nombre/verbo: este saca los candidatos del texto, el CRC los pone a
trabajar juntos y revela cuáles sobran.

----

### Técnica 3: Estereotipos RUP
<!-- .slide: style="font-size: 0.72em" -->

RUP propone clasificar toda clase de análisis en tres tipos:

| Estereotipo | Qué modela | Ejemplos |
|---|---|---|
| **«boundary»** | El **límite** del sistema: media con los actores externos | Interfaz de usuario, de sistema, de dispositivo |
| **«control»** | El **comportamiento** específico de un caso de uso; coordina | Gestor de reservas, procesador de pago |
| **«entity»** | La **información persistente**: obtiene y establece valores | Cliente, Dirección, Producto |

**Para qué sirve:** si al terminar el modelo no hay ninguna clase de alguno de los tres tipos,
falta algo. Las entity sin boundary no se pueden usar; las boundary sin control terminan con
lógica de negocio en la pantalla.

**Otras fuentes de clases:** objetos físicos (avión, hotel) · el papeleo (recibos, facturas) ·
interfaces con el exterior · entidades conceptuales que justifiquen su existencia (CuentaBancaria).

----

### 💡 Ejercicio: Encontrar las clases
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.75em" -->

> *"El club registra a sus socios con nombre, DNI y categoría. Cada socio puede inscribirse en
> varias actividades, y cada actividad tiene un profesor a cargo, un cupo máximo y un horario.
> La recepcionista registra las inscripciones y cobra la cuota mensual."*

1. Aplicá **nombre/verbo**: subrayá los sustantivos y los verbos, y armá la lista de clases
   candidatas y responsabilidades.
2. Clasificá cada clase candidata según los **estereotipos RUP**.
3. ¿Qué sustantivos del texto **no** deberían ser clases? Justificá.

<!--
1. Clases candidatas: Socio, Actividad, Profesor, Inscripción, Cuota. Responsabilidades:
   registrar, inscribirse, cobrar.
2. Casi todas son entity. "Recepcionista" NO es una clase: es un actor, va en el diagrama de
   casos de uso. Falta una control, por ejemplo GestorDeInscripciones, que coordine verificar
   el cupo y crear la inscripción.
3. Nombre, DNI, categoría, cupo máximo y horario son ATRIBUTOS, no clases: no tienen
   comportamiento ni identidad propia. El error típico es convertir todo sustantivo en clase.
   "Inscripción" sí es clase aunque suene a acción, porque tiene datos propios (fecha) y
   vincula a Socio con Actividad.
-->

---

## 2 · La clase
### Anatomía

<!-- .slide: style="font-size: 0.80em" -->

Una clase define un grupo de objetos que comparten características, condiciones y significado.
Se dibuja con **tres compartimentos**: nombre, atributos y operaciones.

![Clase](images/unidad5/clase_ej.jpg) ![Clase Ejemplo](images/unidad5/clase_ejemplo.jpg)

En análisis los atributos y las operaciones son de **alto nivel**: se capturan las ideas
principales y se evitan los detalles de implementación.

----

### Visibilidad
<!-- .slide: style="font-size: 0.85em" -->

| Símbolo | Nivel | Quién puede acceder |
|---|---|---|
| **+** | Pública | Cualquier parte de la aplicación |
| **−** | Privada | Únicamente la misma clase |
| **#** | Protegida | La misma clase y las que heredan de ella |

Además del nombre, los atributos, las operaciones y la visibilidad, una clase puede llevar
**estereotipos** y **valores etiquetados**, que complementan el lenguaje.

---

## 3 · Las relaciones
### Qué son

<!-- .slide: style="font-size: 0.80em" -->

Una relación es una **conexión significativa** entre elementos del modelo: es la forma en que UML
los vincula. Se dibujan con una línea que une las clases.

![Relaciones](images/unidad5/clases_relaciones.jpg)

**Vínculo vs. asociación:** en ejecución, los *objetos* colaboran mediante **vínculos**, que son
dinámicos y se ven en el diagrama de objetos. La **asociación** es la relación entre las *clases*:
es la que se dibuja acá.

----

### Lo que una relación puede llevar
<!-- .slide: style="font-size: 0.78em" -->

* **Nombre** — frase verbal que indica la acción del origen sobre el destino.
  *Ejemplo: Empresa **emplea** Persona.*
* **Roles** — el papel que desempeña cada extremo. *Ejemplo: empleador — empleado.*
* **Multiplicidad** — cuántos objetos participan. Se escribe como `mínimo..máximo`, con `*` o `n`
  para "cualquier cantidad".
* **Navegabilidad** — se indica con una punta de flecha, y muestra que desde un objeto de la clase
  origen se puede llegar al destino. Permite **minimizar el acoplamiento**; a nivel de código se
  traduce en que el origen tiene una referencia al destino, es decir, un atributo.

**Son complementos: si no suman al entendimiento, no se agregan.**

----

### Los cuatro tipos de relación
<!-- .slide: style="font-size: 0.85em" -->

<div class="grid-item">

**Asociación** — dependencia semántica, la más común
**Agregación** — "tiene un", las partes sobreviven al todo
**Composición** — "está compuesto de", las partes mueren con el todo
**Herencia** — "es un"

</div>

Las tres primeras se distinguen por el **rombo**; la cuarta, por el triángulo.

----

### Asociación
<!-- .slide: style="font-size: 0.85em" -->

La más común. Representa una **dependencia semántica** y se dibuja con una simple línea continua.

*Una mascota pertenece a una persona.*

![Persona-Mascota](images/unidad5/persona_mascota.jpg)

----

### Agregación
<!-- .slide: style="font-size: 0.85em" -->

Relación jerárquica que indica un objeto y **las partes que lo componen**. La parte **tiene
existencia en sí misma**: si el todo desaparece, la parte sigue existiendo.

Se dibuja con un **rombo vacío** del lado de la clase que contiene.

![Agregación](images/unidad5/mesas_tablas.jpg)

----

### Composición
<!-- .slide: style="font-size: 0.85em" -->

La misma idea, pero **más fuerte**: cuando el contenedor desaparece, desaparecen todos los
contenidos. Las partes **no tienen sentido por sí mismas** y comparten el tiempo de vida del todo.

Se dibuja con un **rombo relleno**.

![Composicion](images/unidad5/composicion.jpg)

----

### Agregación vs. composición
<!-- .slide: style="font-size: 0.75em" -->

Es la distinción que más se confunde. **La pregunta que las separa: si borro el todo, ¿la parte
sigue teniendo sentido?**

| | Agregación | Composición |
|---|---|---|
| Rombo | Vacío ◇ | Relleno ◆ |
| Tiempo de vida | Independiente | Compartido |
| Si se borra el todo | La parte sobrevive | La parte se borra |
| Ejemplo | Un equipo **tiene** jugadores: si se disuelve el equipo, los jugadores existen | Una factura **está compuesta de** ítems: sin la factura, el ítem no significa nada |

**En la duda, usá asociación.** Un modelo con una asociación simple bien puesta es mejor que uno
con un rombo mal elegido.

----

### Herencia
<!-- .slide: style="font-size: 0.85em" -->

Permite que una clase (**hija** o subclase) reciba los atributos y métodos de otra (**padre** o
superclase), y que además agregue los suyos propios o anule operaciones.

Se usa en relaciones **"es un"**.

![Herencia](images/unidad5/herencia.jpg)

----

### 💡 Ejercicio: ¿Qué relación es?
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.75em" -->

Para cada par, indicá qué relación corresponde y justificá con la pregunta del tiempo de vida:

1. Pedido — ÍtemDePedido <!--Composición: sin el pedido el ítem no significa nada.-->
2. Universidad — Docente <!--Agregación o asociación: el docente existe fuera de la universidad y puede trabajar en varias.-->
3. Vehículo — Automóvil <!--Herencia: un automóvil ES un vehículo.-->
4. Cliente — Dirección <!--Depende del dominio, y esa es la gracia: si la dirección se guarda solo para ese cliente, composición; si es un catálogo de direcciones reutilizable, asociación.-->
5. Casa — Habitación <!--Composición: demolida la casa, la habitación no existe.-->
6. Playlist — Canción <!--Agregación: borrar la playlist no borra las canciones.-->

<!--
El 4 es el que hay que discutir: no tiene una respuesta única. Sirve para mostrar que el tipo de
relación no sale del par de palabras sino de las reglas del dominio, y que por eso hay que
preguntarle al cliente en lugar de adivinar.
-->

----

### Casos especiales
<!-- .slide: style="font-size: 0.85em" -->

**Clases de asociación** — Acomodan atributos que no pertenecen a ninguna de las dos clases sino a
la relación misma, en asociaciones "muchos a muchos".
*Ejemplo: Empresa — Persona, y el sueldo, que es del vínculo entre ambas.*

**Asociaciones cualificadas** — Reducen una asociación "n a muchos" a una "n a 1" agregando un
**calificador**, e ilustran cómo navegar hasta un objeto específico.

---

## 4 · Herencia y polimorfismo

<!-- .slide: style="font-size: 0.80em" -->

**Generalización** es la relación entre un elemento más general y uno más específico. Obedece al
**principio de sustitución**:

> Se puede usar el elemento más específico en cualquier lugar donde se espere el más general, sin
> romper el sistema.

Hay que cuidar los **niveles de abstracción**: Jaguar y Camión pueden ser ambos vehículos, pero
meterlos en la misma jerarquía rara vez ayuda.

**Herencia** es cómo se implementa: en una jerarquía de generalización, las subclases heredan
implícitamente todas las características de sus superclases.

----

### Clases abstractas y polimorfismo
<!-- .slide: style="font-size: 0.85em" -->

**Clases y operaciones abstractas** — No se pueden instanciar ni invocar. Existen cuando conviene
**diferir la implementación a una subclase**.
*Ejemplo: la operación `dibujarFigura()` en la clase `Figura`.*

**Polimorfismo** — Literalmente, "muchas formas". Una operación es polimórfica cuando tiene varias
implementaciones posibles, y cuál se ejecuta depende del objeto concreto.

Las dos cosas van juntas: `Figura.dibujarFigura()` es abstracta justamente para que cada subclase
—círculo, cuadrado— la implemente a su manera.

---

## 5 · Referencia
### Dependencias

<!-- .slide: style="font-size: 0.72em" -->

Una **dependencia** indica que un cambio en un elemento (el **proveedor**) puede afectar a otro
(el **cliente**). *Ejemplo: pasar un objeto de una clase como parámetro a una operación de otra.*

<div class="avanzado">

Hay tres tipos básicos, cada uno con sus variantes. **Se usan en modelos de especificación
detallada, no en el análisis del trabajo práctico:**

* **De uso** — el cliente usa servicios del proveedor: `use` · `call` · `parameter` · `send`
* **De abstracción** — vinculan elementos con distinto nivel de abstracción: `trace` (son lo mismo
  en modelos distintos) · `substitute` · `refine` · `derive`
* **De permiso** — habilitan el acceso: `access` · `import` · `permit`

</div>

**Lo que hay que retener:** una dependencia es la relación **más débil** de todas. Si dos clases
solo se rozan, es una dependencia; si una guarda una referencia a la otra, ya es una asociación.

----

### Paquetes
<!-- .slide: style="font-size: 0.78em" -->

Un **paquete** es un elemento de agrupación: un contenedor lógico para organizar elementos del
modelo y diagramas, con su propio **espacio de nombres**.

* Los paquetes de análisis contienen **casos de uso**, **clases de análisis** y **realizaciones de
  casos de uso**.
* Todo elemento tiene visibilidad: **(+)** pública o **(−)** privada.
* Se pueden **anidar**, definir **dependencias** entre ellos y **generalizarlos**.

**Regla:** evitar las dependencias cíclicas. Si aparecen, hay dos salidas — fusionar los paquetes
o dividirlos de otra manera.

---

### 💡 Ejercicio integrador
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.74em" -->

> *"Una biblioteca presta ejemplares a socios. De cada título se guarda ISBN, autor y editorial, y
> puede haber varios ejemplares del mismo título. Cada préstamo registra la fecha de retiro, la de
> devolución y el bibliotecario que lo autorizó. Los socios pueden ser estudiantes o docentes;
> los docentes pueden llevarse más ejemplares."*

Dibujá el diagrama de clases completo, con:

1. Las clases y sus atributos principales.
2. Las **multiplicidades** de cada asociación.
3. Al menos una **herencia** y una relación de **composición o agregación**, justificando cuál elegiste.
4. La **navegabilidad**, donde aporte.

<!--
Clases: Título, Ejemplar, Socio (con Estudiante y Docente como subclases), Préstamo, Bibliotecario.
Título 1 — 1..* Ejemplar: composición defendible (sin el título, el ejemplar no significa nada) o
agregación; lo que importa es que justifiquen.
Préstamo asocia un Ejemplar (1) con un Socio (1) y un Bibliotecario (1); un Socio tiene 0..*
Préstamos.
Herencia: Socio → Estudiante / Docente, con el máximo de préstamos como atributo que cambia.
Errores esperables: hacer de "fecha de devolución" una clase; olvidar que Préstamo es una clase y
no solo una asociación; poner al bibliotecario como actor en lugar de clase.
-->

---

### Antes de entregar, revisá
<!-- .slide: style="font-size: 0.78em" -->

* ¿Los **nombres** son del negocio y no de la implementación?
* ¿Cada clase tiene entre **3 y 5 responsabilidades** y ninguna quedó suelta?
* ¿Todas las asociaciones tienen **multiplicidad**?
* ¿Los rombos están bien elegidos? *Si borro el todo, ¿la parte sigue teniendo sentido?*
* ¿Hay al menos una clase de cada **estereotipo RUP**, o falta algo?
* ¿El diagrama **cuenta una historia** o es una lista de cajas?

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
