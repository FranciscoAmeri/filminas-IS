---
title: Planeación de Proyectos - Material de examen final
theme: solarized
slideNumber: true
---

#### Ingenieria de Software
# Planeación de Proyectos
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

---

### Que es este mazo
<!-- .slide: style="font-size: 0.80em" -->

<div class="grid-item">

Estas filminas **no se dictan en clase** por razones de tiempo, pero
**entran en el examen final**.

Son la profundizacion de los temas que si se vieron en
**[Planeación de Proyectos](U10b_planeacion_de_proyectos.html)**. Conviene estudiarlas despues de ese mazo,
no antes.

</div>

Son **65 filminas**.

---

### Etapa 1 – Especulación

- Descripción a alto nivel del proyecto
- Revisión del plan si se obtiene el contrato
- Cálculo preliminar del precio según esfuerzo estimado
- Considerar factores externos que influyen en la fijación de precios

---

### Una vez asignado el contrato...

- Refinar el plan recabando más requerimientos y refinándolos.
- Asignar recursos o decidir contratación de nuevo personal.
- Definir mecanismos de monitoreo del proyecto (avances y costos)
- Se re-analizan el calendario, estimación de costos y riesgos.

---

### Fijación de precio: Realidad

En la práctica influyen:  

- Consideraciones **organizacionales**
- Factores **económicos y políticos**
- Estrategia **empresarial**
- Riesgos y tipo de **contrato firmado**

---

<!-- .slide: style="font-size: 0.85em" -->
- **Oportunidad de mercado:** Cotizar bajo para ganar un cliente o adquirir experiencia en nuevos productos.  
- **Incertidumbre en la estimación:** Incrementar el precio para cubrir contingencias derivadas de falta de conocimiento o experiencia.  
- **Términos contractuales:** Si el cliente conserva la propiedad del código y puede reutilizarlo, la ganancia a largo plazo será menor.  
- **Volatilidad de requerimientos:** Reducir el precio inicial para obtener el contrato, compensando luego con cargos por cambios de alcance.  
- **Salud financiera:** Ajustar precios para obtener liquidez, incluso con márgenes bajos o nulos.  

---

### De la propuesta al acuerdo

Un costo de proyecto se negocia a partir de un borrador de propuesta.  

Luego cliente y proveedor acuerdan la **especificación detallada** antes de la ejecución.

---

### Desarrollo dirigido por un plan


5. **División del trabajo:** Listado de actividades con sus plazos y entregas asociadas.
6. **Calendario del proyecto:** Indica las dependencias entre las actividades, el tiempo 
estimado requerido para alcanzar cada plazo y la asignación de personal.
7. **Mecanismos de monitorización y reporte:** Lista los informes que deben producirse, cuándo tienen que elaborarse y los mecanismos de monitorización que se usarán.

---

### Complementos del plan
<!-- .slide: style="font-size: 0.95em" -->
8. **Plan de calidad:** Describe los procedimientos de calidad y estándares que se usarán.
9. **Plan de validación:**  Describe el enfoque, los recursos y el calendario utilizados para la 
validación del sistema.
10. **Configuración del plan de gestión:** Describe la configuración de los procedimientos y las estructuras para la gestión.
11. **Plan de mantenimiento:** Predice los requerimientos, los costos y el esfuerzo de mantenimiento.
12. **Plan de desarrollo de personal:** Describe cómo se desarrollarán las habilidades y la experiencia de los miembros del equipo de proyecto.

---

### Revisión y ajustes del plan

Los cambios son inevitables: deben revisarse regularmente ante variaciones en requerimientos, calendario o riesgos.  

Factores a considerar: **fecha de entrega, personal disponible, presupuesto y herramientas**.  

---

### Realismo en la planificación

Se debe ser realista a la hora de preparar un plan. Por eso, las suposiciones deben ser **prudentes y conservadoras**.

Tiene que incluir suficiente **contingencia** para evitar renegociaciones frecuentes.

---

### Mitigación de problemas graves


- Tomar acciones de **mitigación de riesgos**.  
- Renegociar calendario y realizar **revisión técnica formal** para validar alineación con los objetivos del cliente.  
- Decidir si se debe **continuar o cancelar** el proyecto. 

---

### Reutilización de estimaciones

- Si el proyecto es similar a uno anterior, pueden **reutilizarse estimaciones previas**.  
- Si cambian los **métodos de diseño o lenguajes de implementación**, las estimaciones anteriores pueden no ser aplicables.  

---

### Regla empírica para estimar

1. **Estimar en condiciones ideales** (asumiendo que nada saldrá mal).  
2. **Ampliar la estimación** para cubrir problemas anticipados.  
3. Añadir un **factor de contingencia** (30% a 50%) para imprevistos no anticipados. 

---

### Elementos de cada actividad

Cada actividad debe incluir:  
1. **Duración** en días o meses calendario.  
2. **Esfuerzo** requerido en días-hombre.  
3. **Plazo límite** para su finalización.  
4. **Resultado esperado** al completarla.  

---

### Definición de hitos

- Los **hitos** marcan puntos clave en el calendario.  
- Cada hito debe documentarse con un **reporte breve** que resuma el avance y el trabajo realizado.  

---

### Gráfica de barras de actividad


![Grafico de Secuencia](images/unidad10/grafico-secuencia.jpg)

---

### Tareas independientes

- Las tareas **independientes** pueden realizarse en paralelo.  

---

### Gráfica de asignación de personal


![Grafico de asignacion de personal](images/unidad10/asignacion-de-personal.png)

---

### Reglas de asignación de personal

- Una persona puede trabajar en **más de una tarea** al mismo tiempo.  
- Puede haber períodos sin asignación (vacaciones, otro proyecto, capacitación, etc.).  
- Las **asignaciones parciales** se indican con una línea diagonal sobre la barra.  

---

###  Planeación ágil

1. Planeación de la entrega (release), que prevé con muchos meses de antelación y 
decide sobre las características que deben incluirse en una entrega de un sistema.
2. Planeación de la iteración, tiene un panorama a corto plazo y se enfoca en 
la planeación del siguiente incremento de un sistema. En general representa de 2 a 4 semanas de trabajo.

---

### Planeación en XP

1. **Identificar** un conjunto de **historias** que comprendan toda la funcionalidad que se incluirá en el sistema final.
2. Para poder **estimar**, el equipo lee y discute las historias y las clasifica de acuerdo con la cantidad de tiempo que consideran que se tardará en implementarla. Se asigna puntos de esfuerzo hipotéticos.
3. Seleccionar y afinar las historias que reflejarán las características a aplicar en una **entrega** de un sistema y el orden en el que deben implementar. El cliente participa de este proceso.

---

### Planeación en XP

4. Se eligen las historias a implementar en dicha **iteración**; el número de historias depende del tiempo del sprint y la velocidad del equipo. Se suman los puntos de las historias terminadas
y se calcula nuevamente la velocidad.
5. Planeación más detallada en donde las historias se dividen en **tareas**.

---

### Beneficios del enfoque de planeación ágil

1. Todo el equipo conoce las tareas a completar en una iteración.
2. Los desarrolladores eligen las tareas a implementar, por lo que tienen 
un sentido de propiedad y eso motiva más a completar la tarea.

---

### Modelado algorítmico de costos


![Formula-estimacion](images/unidad10/modelado-algoritmico.png)

- **A:** factor constante (depende de prácticas de la organización y tipo de software).  
- **Tamaño:** líneas de código o puntos de función.  
- **B:** exponente entre 1 y 1.5 (según complejidad).  
- **M:** multiplicador de atributos (procesos, confiabilidad, experiencia del equipo, etc.).  

---

![Cocomo](images/unidad10/cocomo.png) 


---

### 1. Modelo de composición de aplicación


- Permite estimar el costo y el esfuerzo en la etapa 1 del  Modelo COCOMO II 
- El tamaño se estima mediante Puntos de Objeto
- Los **Puntos de Objeto** definen pantallas, informes y módulos de tercera generación (3GL)

---

### 1. Modelo de composición de aplicación


Para estimar el esfuerzo para desarrollar un proyecto se siguen los siguientes pasos:
1. Acceso a recuentos de objetos
2. Clasifique los niveles de complejidad de cada objeto
3. Asignar pesos de complejidad a cada objeto
4. Determinar los puntos del objeto
5. Calcular nuevos puntos de objeto (NOP)
6. Calcular la tasa de productividad (PROD)
7. Calcular el esfuerzo estimado

---

### 1. Modelo de composición de aplicación

#### 1. Acceso a recuentos de objetos

Calcule el número de pantallas, informes y componentes 3GL que conformarán esta aplicación.

---

### 1. Modelo de composición de aplicación

#### 2. Clasifique los niveles de complejidad de cada objeto

Se clasifica cada instancia de objeto en niveles de complejidad simple, media y difícil.

![Calculo de Pantallas](images/unidad10/calculo-pantallas.jpg)

---

### 1. Modelo de composición de aplicación

#### 2. Clasifique los niveles de complejidad de cada objeto

![Calculo de Reportes](images/unidad10/calculo-reportes.jpg)

---

### 1. Modelo de composición de aplicación

#### 3. Asignar pesos de complejidad a cada objeto

Los pesos se utilizan para tres tipos de objetos: pantallas, informes y componentes 3GL.

![Calculo de Complejidad](images/unidad10/calculo-complejidad.jpg)

---

### 1. Modelo de composición de aplicación

#### 4. Determinar los puntos del objeto

Sumar todas las instancias de objetos ponderados para obtener un número; esto se conoce como recuento de puntos de objeto.

**Punto de objeto = Sigma (número de instancias de objeto) * (peso de complejidad de cada instancia de objeto)**

---

### 1. Modelo de composición de aplicación

#### 5. Calcular nuevos puntos de objeto (NOP)
Estimar el porcentaje de reutilización que se debe lograr en un proyecto.

**NOP = [(puntos de objeto) * (100 - % reutilización)] / 100**

Los NOP son los puntos de objeto que se deben desarrollar y se diferencian del recuento de puntos de objeto porque puede haber reutilización de alguna instancia de objeto en el proyecto.

---

### 1. Modelo de composición de aplicación
#### 6. Calcular la tasa de productividad (PROD)
<!-- .slide: style="font-size: 0.90em" -->
La tasa de productividad se calcula a partir de la información sobre la experiencia y la capacidad del desarrollador.

![Porcentaje de Productividad](images/unidad10/Productivity-Rate.webp)

---

### 1. Modelo de composición de aplicación

#### 7. Calcule el esfuerzo estimado
El esfuerzo para desarrollar un proyecto se puede calcular como:

```
Esfuerzo = NOP / PROD
```

El esfuerzo se mide en personas-mes.

---

### EJEMPLO


Considere un proyecto de aplicación de base de datos con
1. La aplicación tiene 4 pantallas con 4 vistas cada una y 7 tablas de datos para 3 servidores y 4 clientes.
2. La aplicación puede generar 2 informes de 6 secciones cada uno a partir de 7 tablas de datos para 2 servidores y 3 clientes.
3. 10% de reutilización de puntos de objeto.
4. La experiencia y capacidad del desarrollador en entornos similares es baja.

---

#### Paso 1: 


Número de pantallas = 4

Número de informes = 2

---

#### Paso 2: Para las pantallas,

Número de vistas = 4

Número de tablas de datos = 7

Número de servidores = 3

Número de clientes = 4

De la tabla obtenemos que el **nivel de complejidad** para cada pantalla es **medio**.

---

#### Paso 2: Para informes


Número de secciones = 6

Número de tablas de datos = 7

Número de servidores = 2

Número de clientes = 3

De la tabla obtenemos que el **nivel de complejidad** para cada informe es **difícil**.

---

#### Paso 3: Peso de Complejidad


De la tabla de peso de complejidad obtenemos:

Peso de complejidad para cada pantalla = 2

Peso de complejidad para cada informe = 8

---

#### Paso 4: Puntos Objeto


Recuento de puntos del objeto = sigma (número de instancias del objeto) * (su peso de complejidad)

Puntos Objeto = 4 * 2 + 2 * 8 = 24

---

#### Paso 5: % de reutilización 


El porcentaje de reutilización de puntos de objeto = 10% (dado)

**NOP = [puntos de objeto * (100 - %reutilización)] / 100**

NOP = [24 * (100 -10)]/100 = 21,6


---

#### Paso 6:


La experiencia y capacidad del desarrollador son **bajas**.
Utilizando la tabla de tasa de productividad:

Tasa de productividad (PROD) del proyecto dado = 7


---

#### Paso 7:


**Esfuerzo = NOP / PROD**

Esfuerzo = 21,6/7

Esfuerzo ≈ 3,09 personas-mes

<!--
### 1. Modelo de composición de aplicación
Modela el esfuerzo en proyectos con **componentes reutilizados**, código generado o programación de bases de datos.  

- Tamaño medido en **puntos de aplicación**.  
- Esfuerzo = **Tamaño / Productividad**.  
- Se pondera: nº de pantallas, informes, módulos y líneas de código. 

### 1. Modelo de composición de aplicación
Enfocado en **prototipos y proyectos con reutilización**.  
- La **productividad** depende de la experiencia, habilidades y herramientas.  

![Productividad](images/unidad10/productividad.png)


### Fórmula de estimación en composición
![Estimación de Esfuerzo](images/unidad10/estimacion-esfuerzo.png)

- **PM:** esfuerzo en meses-hombre.  
- **NAP:** número de puntos de aplicación.  
- **%Reutilización:** proporción de código reutilizado.  
- **PROD:** productividad del equipo.  
-->

---

### 2. Modelo de diseño temprano
Simplifica la fórmula general:  

**Esfuerzo = A × Tamaño^B × M**  

- Tamaño expresado en **puntos de función**, convertidos a **KSLOC** (miles de líneas de código).  
- Factores: entradas/salidas externas, interacciones, interfaces y tablas.

---

### Parámetros del diseño temprano
<!-- .slide: style="font-size: 0.70em" -->
![Fórmula](images/unidad10/diseno-temprano.png)

- **A = 2.94** (propuesto por Boehm)
- **B = 1.1 a 1.24**, según innovación, riesgos, cohesión y madurez.  
- **M:** multiplicador basado en 7 atributos:  
  - PERS (habilidad personal)  
  - RCPX (fiabilidad y complejidad)  
  - RUSE (reutilización)  
  - PDIF (dificultad de plataforma)  
  - PREX (experiencia personal)  
  - FCIL (facilidades de soporte)  
  - SCED (ajuste de calendario)  

---
<!-- .slide: style="font-size: 0.42em" -->

Los valores de **M** se pueden tomar de la siguiente tabla:

<table>
  <thead>
    <tr>
      <th>Factor</th>
      <th>Muy Bajo</th>
      <th>Bajo</th>
      <th>Nominal</th>
      <th>Alto</th>
      <th>Muy Alto</th>
      <th>Extra Alto</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>PERS (Habilidad personal)</th>
      <td>1.62</td>
      <td>1.26</td>
      <td>1.00</td>
      <td>0.83</td>
      <td>0.63</td>
      <td>–</td>
    </tr>
    <tr>
      <th>RCPX (Fiabilidad y complejidad)</th>
      <td>0.49</td>
      <td>0.60</td>
      <td>1.00</td>
      <td>1.33</td>
      <td>1.91</td>
      <td>–</td>
    </tr>
    <tr>
      <th>RUSE (Reutilización requerida)</th>
      <td>–</td>
      <td>–</td>
      <td>1.00</td>
      <td>1.07</td>
      <td>1.15</td>
      <td>1.24</td>
    </tr>
    <tr>
      <th>PDIF (Dificultad de la plataforma)</th>
      <td>–</td>
      <td>–</td>
      <td>1.00</td>
      <td>1.29</td>
      <td>1.81</td>
      <td>–</td>
    </tr>
    <tr>
      <th>PREX (Experiencia personal)</th>
      <td>1.59</td>
      <td>1.33</td>
      <td>1.00</td>
      <td>0.87</td>
      <td>0.71</td>
      <td>–</td>
    </tr>
    <tr>
      <th>FCIL (Facilidades de soporte)</th>
      <td>1.43</td>
      <td>1.14</td>
      <td>1.00</td>
      <td>0.87</td>
      <td>0.73</td>
      <td>–</td>
    </tr>
    <tr>
      <th>SCED (Compresión del calendario)</th>
      <td>1.43 (75%)</td>
      <td>1.14 (85%)</td>
      <td>1.00 (100%)</td>
      <td>1.00 (130%)</td>
      <td>–</td>
      <td>–</td>
    </tr>
  </tbody>
</table>

---

### Ejercicio:

Supongamos:
<!-- .slide: style="font-size: 0.80em" -->
- Tamaño = 100 Puntos de Aplicación (AP).
- Exponente B = 1.12 (un caso intermedio, ni muy riesgoso ni muy maduro).
- Atributos: 
  - PERS: Alto
  - RCPX: Nominal
  - RUSE: Alta
  - PDIF: Nominal
  - PREX: Baja
  - FCIL: Alta
  - SCED: Nominal
- ¿Cuánto demoraría un equipo de 10 dev o 25 devs?

---

#### Paso 1: Calcular M

𝑀 = 0.83 × 1.00 × 1.07 × 1.00 × 1.33 × 0.87 × 1.00 = **1.03**
  
#### Paso 2: Calcular esfuerzo (PM)
PM = 2.94 × (100) 1.12 × 1.03 = **526 meses-persona**

#### Paso 3: Equipos
526/10 = 52.6 meses ≈ **4.4 años**

526/25 = 21 meses ≈ **1.7 años**

---

###  3. Modelo de reutilización

Calcula esfuerzo al integrar **código existente o generado automáticamente**.  

Tipos:  
- **Caja negra:** código reutilizado sin cambios (esfuerzo 0).  
- **Caja blanca:** requiere adaptación e integración.  

---

### Fórmula de reutilización

<!-- .slide: style="font-size: 0.90em" -->
**ASLOC** son las siglas de "Adapted Source Lines of Code".

Representa el número de líneas de código existentes que se van a adaptar/reutilizar en el nuevo proyecto.

No todo ese código cuenta como “nuevo”, porque adaptarlo no cuesta lo mismo que desarrollarlo desde cero.

![Reutilización](images/unidad10/reutilizacion.png)

- **ASLOC:** líneas de código reutilizado.  
- **AT:** % de código generado automáticamente.  
- **ATPROD:** productividad al integrarlo. 

---

### Conversión a ESLOC

**ESLOC** son las siglas de "Equivalent Source Lines of Code".

Es una medida ajustada que convierte el esfuerzo de reutilización/adaptación en un equivalente a "líneas nuevas".

**ESLOC = ASLOC × AAM**  

- **ESLOC:** líneas equivalentes de nuevo código.  
- **AAM:** multiplicador de ajuste de adaptación.  

---

#### AAM: Adaptation Adjustment Multiplier
<!-- .slide: style="font-size: 0.60em" -->

![AAM](images/unidad10/AAM.png)

Son **cuatro** parámetros, y conviene no confundirlos:

| Parámetro | Qué mide | Rango |
|---|---|---|
| **AAF** | Factor de ajuste de adaptación: cuánto hay que cambiar | 0 a 100 (calculado) |
| **AA** | Evaluación y asimilación: el esfuerzo de evaluar, elegir e integrar el componente | **0 a 8** |
| **SU** | Comprensión del software: cuánto cuesta **entenderlo** antes de tocarlo | **10** (muy simple) a **50** (muy complejo) |
| **UNFM** | Desconocimiento del programador: qué tan poco familiarizado está con ese código | **0** (lo conoce) a **1** (nunca lo vio) |

La fórmula es **por tramos**:

* Si **AAF ≤ 50** → `AAM = [ AA + AAF × (1 + 0,02 × SU × UNFM) ] / 100`
* Si **AAF > 50** → `AAM = [ AA + AAF + (SU × UNFM) ] / 100`

<div class="alerta">

**Ojo con dos confusiones habituales:** *AA* y *UNFM* son parámetros distintos —uno es el costo de
asimilar, el otro el desconocimiento del programador— y **UNFM va de 0 a 1**, no de 0 a 8. Y la
fórmula **no es** una suma de los tres factores divididos por 100.

</div>

---

### AAF: Factor de Ajuste de Adaptación


Se calcula como:
**AAF = 0.4 × DM + 0.3 × CM + 0.3 × IM**

- **DM** = % de diseño modificado.
- **CM** = % de código modificado.
- **IM** = % de integración modificada.

---

### Ejercicio:


Supongamos:
- ASLOC = 8.000
- DM = 25%, CM = 10%, IM = 20%
- **AA = 4** (esfuerzo intermedio de evaluación y asimilación)
- **SU = 30** (dificultad media para entender el software)
- **UNFM = 0,4** (el equipo conoce parcialmente ese código)

---

#### 1. Calcular AAF


`AAF = (0,4 × 25) + (0,3 × 10) + (0,3 × 20) = 10 + 3 + 6 = `**`19`**

#### 2. Calcular AAM

Como **AAF = 19 ≤ 50**, se usa el primer tramo:

`AAM = [ 4 + 19 × (1 + 0,02 × 30 × 0,4) ] / 100`

`AAM = [ 4 + 19 × 1,24 ] / 100 = [ 4 + 23,56 ] / 100 = `**`0,2756`**

#### 3. Calcular ESLOC

`ESLOC = 8.000 × 0,2756 ≈ `**`2.205`**

Reutilizar 8.000 líneas en esas condiciones cuesta como escribir **2.205 líneas nuevas**: un
ahorro de alrededor del **72 %**.

---

### ¿Por qué importa el resultado?
<!-- .slide: style="font-size: 0.80em" -->

El número que sale de ahí responde una pregunta de decisión concreta: **¿conviene reutilizar o
escribir de nuevo?**

| AAM | Interpretación | Decisión |
|---|---|---|
| Cercano a **0** | Reutilización casi gratis: caja negra | Reutilizar sin dudar |
| **0,2 a 0,5** | Adaptación con ahorro real | Reutilizar |
| Cercano a **1** | Adaptarlo cuesta casi lo mismo que escribirlo | Evaluar los dos caminos |
| **Mayor a 1** | Adaptarlo cuesta **más** que escribirlo de cero | Escribirlo de nuevo |

**Y sí, AAM puede pasar de 1.** Con `AAF = 60`, `AA = 8`, `SU = 50` y `UNFM = 1`:
`AAM = [8 + 60 + 50] / 100 = 1,18`. Es el caso del código heredado que nadie entiende: lo barato
sale caro.

---

### 4. Modelo posarquitectónico

Se aplica cuando ya existe un diseño arquitectónico inicial.  

- Permite estimaciones más precisas del **tamaño**.  
- Incluye multiplicadores adicionales sobre **personas, producto y proyecto**.  

---

### Fórmula posaquitectonica


![Postarquitetconica](images/unidad10/posarquitectonico.png)

- A = 2.94 (constante calibrada).
- Tamaño = LOC, Puntos de Función o ESLOC (si hay reutilización).
- B = Exponente que refleja la escala
- EMi = Multiplicadores de esfuerzo (17 en total en este modelo).

---

### Factores posarquitectónicos

1. **Precedencia:** experiencia previa en proyectos similares.  
2. **Flexibilidad de desarrollo:** libertad para definir procesos. 
3. **Resolución de riesgos:** nivel de análisis de riesgos realizado.  
4. **Cohesión de equipo:** calidad de la comunicación y trabajo conjunto.  
5. **Madurez del proceso:** nivel **CMMI** (Modelo de Madurez de Capacidades Integrado) de la organización. Desde 2023 rige **CMMI v3.0**, que reemplazó al viejo CMM.  

---

### Multiplicadores de Esfuerzo

- Producto
- Plataforma
- Personal

---

### Multiplicadores de Esfuerzo: Producto
<!-- .slide: style="font-size: 0.90em" -->
1. **RELY:** Reliability / Fiabilidad requerida. Qué tan crítico es que el software funcione sin fallas.
2. **DATA:** Database Size / Tamaño de base de datos. Relación entre la base de datos y el código fuente.
3. **CPLX:** Complexity / Complejidad del producto. Número de operaciones, interfaces, algoritmos, interacción con usuarios, etc
4. **RUSE:** Required Reusability / Reutilización requerida. Nivel de calidad y documentación exigida para que el software pueda ser reutilizado en otros proyectos
5. **DOCU:** Documentation. Cantidad y calidad de documentación requerida (manuales, guías, especificaciones).

---

### Multiplicadores de Esfuerzo: Plataforma

6. **TIME:** Execution Time Constraint / Restricciones de tiempo de ejecución. Qué porcentaje del tiempo de CPU puede usar la aplicación.
7. **STOR:** Main Storage Constraint / Restricciones de memoria. Aplicaciones que deben correr con muy poca RAM son más difíciles de desarrollar.
8. **PVOL:** Platform Volatility / Volatilidad de la plataforma. Qué tan seguido cambia el hardware, el SO o el middleware en el que corre el sistema.


---

### Multiplicadores de Esfuerzo: Personal
<!-- .slide: style="font-size: 0.80em" -->
9. **ACAP:** Analyst Capability. Habilidad de analistas en requerimientos y diseño.
10. **PCAP:** Programmer Capability. Habilidad técnica del equipo de codificación.
11. **PCON:** Personnel Continuity. Mide la rotación del equipo (turnover). Mucha rotación = más esfuerzo.
12. **APEX:** Applications Experience. Familiaridad del equipo con el dominio específico del sistema (ej. banca, salud, telecom).
13. **PLEX:** Platform Experience. Experiencia en el hardware/SO/middleware donde se implementará el sistema.
14. **LTEX:** Language and Tool Experience. Qué tanto conoce el equipo los lenguajes de programación, librerías y herramientas de desarrollo que usará.

---

### Multiplicadores de Esfuerzo: Proyecto

15. **TOOL:** Use of Software Tools. Nivel de soporte de CASE, entornos integrados, repositorios de versiones, herramientas de prueba, etc.
16. **SITE:** Multisite Development. Equipos distribuidos en varios husos horarios → más esfuerzo.
17. **SCED:** Schedule Compression. Ajuste del calendario respecto al nominal (ej. terminar en 75% del tiempo normal implica más esfuerzo).

---

![Estimacion COCOMO](images/unidad10/estimacion-cocomo.png)


---

### Ejemplo de COCOMO

¿Qué ocurre al variar los controladores de costo?  
- Valores **altos** → esfuerzo estimado puede triplicarse.  
- Valores **bajos** → esfuerzo se reduce a 1/3 del original.  


---
## Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
