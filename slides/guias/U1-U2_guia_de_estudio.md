# Ingeniería de Software — Guía de estudio

## Unidades 1 y 2

**Unidad 1:** Introducción a la Ingeniería de Software
**Unidad 2:** Procesos de Software · Herramientas CASE

---

### Cómo usar esta guía

Son 50 preguntas para trabajar por tu cuenta antes del parcial. No están ordenadas por
dificultad: están ordenadas por tema, siguiendo las filminas.

- Las preguntas marcadas con **(C)** son **conceptuales**: se responden con lo visto en clase.
- Las marcadas con **(A)** son de **aplicación**: hay que decidir algo y justificarlo.
- Las marcadas con **(I)** son **integradoras**: cruzan más de un tema o más de una unidad.

Al final hay respuestas orientativas. **Usalas después de intentar cada pregunta**, no antes:
el valor de la guía está en el intento, no en la lectura.

---

## Unidad 1 — Introducción a la Ingeniería de Software

### El software y la disciplina

1. **(C)** ¿Qué es el software? Nombrá las dos características que lo distinguen de un producto
   físico.

2. **(C)** Definí ingeniería de software. ¿Por qué se la considera una **disciplina de
   ingeniería** y no solamente programación?

3. **(C)** ¿Cuál es la diferencia entre ciencias de la computación, ingeniería de software e
   ingeniería de sistemas?

4. **(C)** Enumerá cuatro razones por las que la ingeniería de software es importante.

5. **(A)** *"Para un proyecto chico no hace falta ingeniería de software, alcanza con programar
   bien."* ¿Estás de acuerdo? Justificá con al menos dos argumentos.

### Errores de software

6. **(C)** ¿Por qué a los errores de software se les dice *bugs*? ¿Quién y en qué año dio origen
   al término?

7. **(C)** El Ariane 5 explotó por reutilizar código del Ariane 4. ¿Cuál fue exactamente el
   error técnico?

8. **(I)** El caso Ariane 5 aparece en la Unidad 1 como ejemplo de error, y en la Unidad 2 la
   reutilización se presenta como un **modelo de proceso ventajoso**. ¿Se contradicen? ¿Qué
   lección deja el Ariane 5 sobre los límites de la reutilización?

9. **(C)** ¿Qué falló en el Therac-25 y por qué el problema no se detectaba desde la interfaz?

10. **(C)** El Mars Climate Orbiter se perdió por un error de unidades. ¿En qué etapa del
    proceso debería haberse detectado ese problema?

11. **(A)** Knight Capital perdió 460 millones de dólares en 45 minutos. Identificá **tres**
    fallas distintas en su proceso, no en su código.

12. **(A)** Ordená los cuatro casos vistos según el tipo de daño (humano, económico, científico)
    y explicá cuál te parece más grave y por qué.

### Costos y productos

13. **(C)** ¿Qué cuesta más: desarrollar el software o mantenerlo? Aproximadamente, ¿qué
    porcentaje del ciclo total representa el mantenimiento?

14. **(A)** Si el mantenimiento se lleva la mayor parte del costo, ¿qué decisiones tomarías
    **durante el desarrollo** para reducirlo?

15. **(C)** Diferenciá producto **genérico** de producto **personalizado**, y explicá quién es
    dueño de la especificación en cada caso.

16. **(A)** Clasificá en genérico o personalizado y justificá los dudosos: Excel · una app de
    turnos para una veterinaria de barrio · Moodle · Moodle adaptado para una universidad ·
    Spotify · el sistema de reservas de una aerolínea.

17. **(I)** ¿Por qué la distinción entre producto genérico y personalizado influye en el
    **modelo de proceso** que conviene elegir? (Pensalo con lo visto en la Unidad 2.)

### Diversidad y tipos de sistemas

18. **(C)** *"No existe un conjunto universal de técnicas aplicable a todo el software."*
    Explicá esta afirmación con dos ejemplos de tipos de sistema opuestos.

19. **(C)** Nombrá los ocho tipos de aplicaciones vistos y dá un ejemplo concreto de cada uno.

20. **(A)** Un sistema de semáforos inteligentes de una ciudad, ¿en qué tipo o tipos de
    aplicación encaja? ¿Por qué puede pertenecer a más de uno?

### Actividades y atributos

21. **(C)** Nombrá las cuatro actividades del proceso de desarrollo y describí brevemente cada
    una.

22. **(C)** ¿Cuáles son los cuatro atributos esenciales de un buen software?

23. **(A)** Identificá qué atributo esencial está en juego en cada caso:
    a) Una app de transferencias duplica pagos ocasionalmente.
    b) Un sistema de facturación incorpora nuevas reglas impositivas sin rehacer nada.
    c) Una plataforma educativa no se adapta a celulares y los alumnos la evitan.
    d) Una web de inscripción consume pocos recursos del navegador.

24. **(C)** ¿Cuál es la diferencia entre los **atributos esenciales** del software y los
    **atributos de calidad del diseño**?

25. **(A)** Identificá el atributo de calidad involucrado: confiabilidad, disponibilidad,
    seguridad o protección.
    a) Un sistema de turnos hospitalario queda caído tres horas.
    b) Un comercio electrónico cifra los datos de tarjeta antes de enviarlos.
    c) Los usuarios solo acceden a las secciones que corresponden a su rol.
    d) Una empresa pierde datos por una caída y no tiene respaldo actualizado.

---

## Unidad 2 — Procesos de Software

### Qué es un proceso

26. **(C)** ¿Qué es un proceso de software? ¿Y un modelo de proceso?

27. **(C)** Además de las actividades, ¿qué otros tres elementos puede incluir la descripción de
    un proceso?

28. **(C)** Diferenciá desarrollo **dirigido por plan** de desarrollo **ágil**. ¿Por qué se dice
    que en la práctica la mayoría de los procesos combina los dos?

29. **(I)** Las cuatro actividades fundamentales están presentes en todos los modelos de
    proceso. Entonces, ¿qué es exactamente lo que cambia de un modelo a otro?

### Los modelos

30. **(C)** Nombrá las cinco fases del modelo de cascada y su principal inconveniente.

31. **(A)** ¿En qué situaciones conviene el modelo de cascada, a pesar de que tolera mal el
    cambio? Dá dos razones y un ejemplo de dominio.

32. **(C)** ¿Qué caracteriza al desarrollo incremental? Mencioná dos beneficios y dos problemas.

33. **(C)** Explicá la diferencia entre **desarrollo incremental** y **entrega incremental**,
    con un ejemplo de cada uno.

34. **(C)** Enumerá las cinco etapas de la ingeniería de software orientada a reutilización.
    ¿Cuál de ellas no existe en ningún otro modelo, y por qué es llamativa?

35. **(A)** ¿Cuál es el costo oculto de la reutilización? Relacionalo con un caso donde el
    cliente no pueda obtener exactamente lo que pidió.

36. **(C)** ¿Cuándo conviene el modelo evolutivo? ¿Cuáles son sus cuatro fases?

37. **(C)** ¿En qué se divide cada ciclo del modelo en espiral? ¿Qué lo distingue de los demás
    modelos iterativos?

38. **(I)** Tanto el modelo evolutivo como el espiral son iterativos. ¿Cuál es la diferencia
    entre iterar para **descubrir requisitos** e iterar para **reducir riesgos**? Dá un proyecto
    donde sirva uno y no el otro.

### Actividades del proceso

39. **(C)** ¿Qué comprende la actividad de especificación de requerimientos? Nombrá sus cuatro
    sub-actividades.

40. **(C)** ¿Cuáles son las tres etapas de prueba dentro de la validación, y quién realiza cada
    una?

41. **(A)** Clasificá cada tarea en la actividad que corresponde: especificación, diseño e
    implementación, validación o evolución.
    a) Definir la arquitectura del sistema.
    b) Corregir un bug reportado tras el lanzamiento.
    c) Escribir casos de prueba para un módulo.
    d) Hacer un prototipo para validar una idea con el cliente.

### El cambio y el prototipado

42. **(C)** ¿Cuáles son las dos estrategias para reducir los costos de rehacer? Dá un ejemplo de
    cada una.

43. **(A)** Un equipo invierte tres semanas en un prototipo antes de programar y además trabaja
    en incrementos. ¿Qué estrategia aplica en cada caso? ¿Cuánto cuesta cada una?

44. **(C)** ¿Por qué los prototipos desechables no sirven como base de un sistema de producción?
    Dá tres razones.

45. **(A)** Si el código de un prototipo desechable se tira, ¿qué se lleva el equipo de ese
    trabajo? ¿Cómo se lo justificarías a un cliente que ve que "tiraron todo"?

### Herramientas CASE

46. **(C)** ¿Qué significa CASE y qué es una herramienta CASE? Nombrá tres actividades que
    automatizan.

47. **(C)** Explicá las tres clasificaciones de herramientas CASE. ¿Por qué no son alternativas
    entre sí?

48. **(A)** Ubicá **GitHub** en las tres clasificaciones. ¿Qué dificultad encontraste, y qué te
    dice eso sobre las taxonomías?

49. **(I)** Uno de los objetivos de las herramientas CASE es estandarizar la documentación, y el
    Manifiesto Ágil valora el software funcionando por sobre la documentación extensiva.
    ¿Se contradicen? ¿Puede un equipo ágil usar herramientas CASE?

50. **(I)** ¿Cambia el conjunto de herramientas según el modelo de proceso elegido? Compará el
    *toolchain* de un equipo que trabaja en cascada sobre un sistema regulado con el de un
    equipo que hace entrega incremental de una app de consumo.

---
---

# Respuestas orientativas

> Son **orientativas**: en las preguntas de aplicación e integradoras se evalúa la
> justificación, no la coincidencia literal con este texto.

## Unidad 1

**1.** Conjunto de instrucciones, programas y datos que permiten a un dispositivo realizar
tareas específicas. Lo distinguen que es **intangible** y que está compuesto por **código**
interpretable o ejecutable por una máquina.

**2.** Disciplina que se enfoca en el diseño, desarrollo, prueba, implementación y mantenimiento
de sistemas de software de alta calidad, aplicando de manera sistemática principios, teorías,
métodos y herramientas. Es ingeniería porque usa teorías y métodos adecuados para resolver
problemas **teniendo en cuenta las limitaciones financieras y de organización**, y porque abarca
todos los aspectos de la producción de software, no solo el proceso técnico: también gestión de
proyectos, herramientas y métodos.

**3.** Ciencias de la computación: teoría y fundamentos (algoritmos, estructuras de datos,
complejidad). Ingeniería de software: todos los aspectos de la producción de software, desde la
especificación hasta el mantenimiento posterior al uso. Ingeniería de sistemas: desarrollo
completo de sistemas basados en computadoras, integrando hardware, software y procesos.

**4.** La economía de muchos países depende del software; cada vez más sistemas son controlados
por software; a largo plazo es más barato planificar bien que refactorizar continuamente; el
gasto en software es una fracción significativa del PBI; los errores pueden ser muy caros.

**5.** Argumentos en contra de la afirmación: la mayor parte del costo aparece **después** de la
entrega (corregir lo que ya está en uso), y eso no depende del tamaño inicial; los proyectos
chicos crecen, y lo que se ahorró al principio se paga después; sin proceso no hay forma de
saber si el software cumple lo que se pidió. A favor, con matices: el nivel de formalidad debe
ser proporcional al proyecto — nadie escribe un SRS de 50 páginas para un script. La respuesta
completa distingue **hacer ingeniería** de **hacer burocracia**.

**6.** Por la polilla (*bug*) que Grace Hopper encontró en 1947 entre los relés de la Mark II,
computadora electromecánica de Harvard, cuando investigaba las fallas del equipo.

**7.** Se reutilizó código del Ariane 4 que asignaba el valor de una variable de **64 bits a una
de 16 bits**. En el Ariane 4 los valores nunca superaban el rango de 16 bits (−32.768 a 32.767);
en el Ariane 5, con otra trayectoria, sí lo superaron. Costo: 1.000 millones de dólares.

**8.** No se contradicen. La reutilización sigue siendo válida y es hoy el enfoque estándar; lo
que muestra el Ariane 5 es que **un componente reutilizado hereda los supuestos del contexto
para el que fue escrito**. El código era correcto para el Ariane 4. Reutilizar exige verificar
que los supuestos del componente siguen valiendo en el nuevo entorno, y eso es exactamente lo que
la etapa de "análisis de componentes" del modelo de reutilización debería cubrir.

**9.** Un problema de **control de concurrencia** entre rutinas que se ejecutaban en paralelo —una
*race condition*. La interfaz indicaba que todo estaba bien mientras los pacientes recibían
125 veces más radiación de la indicada. Murieron al menos cinco personas.

**10.** En la **validación**, y antes aún en la **especificación**: los requisitos del sistema
establecían que todo el software debía usar el sistema métrico decimal, y el software de control
en Tierra usaba el anglosajón. Era un incumplimiento de un requisito ya especificado, que las
pruebas de integración debieron detectar.

**11.** Tres fallas de proceso: se desplegó una versión nueva **sin actualizar la configuración**
del algoritmo; el sistema quedó corriendo en **modo test**, con las restricciones de seguridad
desactivadas; y no hubo un mecanismo de detección o corte automático que frenara las operaciones
—cuatro millones en 45 minutos— antes de que el daño fuera irreversible. Ninguna de las tres es
un error de programación: son fallas de gestión de la configuración y del despliegue.

**12.** Therac-25 es el más grave: daño humano irreversible, cinco muertes. Ariane 5 y Knight
Capital son económicos (1.000 y 460 millones). Mars Climate Orbiter combina pérdida económica y
científica. Se acepta cualquier orden bien argumentado, siempre que se sostenga que el daño
humano no es conmensurable con el económico.

**13.** Cuesta más el **mantenimiento**. Ronda el **67%** del costo total del ciclo. Además, el
costo del software suele superar al del hardware, y en sistemas de larga vida el mantenimiento
supera ampliamente al desarrollo.

**14.** Escribir código legible y modular, documentar lo necesario, cubrir con pruebas
automatizadas, mantener la estructura mediante refactorización, elegir tecnologías con soporte a
largo plazo y evitar dependencias que se puedan discontinuar. Todo eso es "pagar por adelantado"
para abaratar el 67% que viene después.

**15.** **Genérico**: se comercializa a cualquier cliente (software de gráficos, CAD,
herramientas de gestión). **Personalizado**: lo encarga un cliente específico para sus propias
necesidades (control de tráfico aéreo, sistemas de monitoreo). La diferencia clave es **de quién
es la especificación**: en el genérico es del desarrollador, que decide los cambios; en el
personalizado es del cliente, que decide.

**16.** Genéricos: Excel, Moodle, Spotify. Personalizados: la app de la veterinaria, el sistema
de reservas de la aerolínea. **Los dudosos son los interesantes**: Moodle adaptado para una
universidad es un producto genérico **personalizado** — se reutiliza la base y se desarrolla la
integración; es exactamente el modelo de reutilización de la Unidad 2. Spotify es genérico, pero
la especificación es del desarrollador y el usuario no puede pedir cambios, lo cual se nota.

**17.** Porque determina **quién controla los requisitos**. En un producto personalizado el
cliente decide y puede cambiar de opinión, lo que favorece enfoques incrementales o evolutivos con
participación del cliente. En un producto genérico la especificación la controla el desarrollador,
que puede planificar versiones y no depende de la disponibilidad de un cliente. Y en el caso de
Moodle adaptado, el modelo natural es el orientado a reutilización.

**18.** Los métodos y herramientas dependen del tipo de aplicación, de los requisitos del cliente
y de la experiencia del equipo. Ejemplo: los **juegos** conviene diseñarlos con una serie de
prototipos, porque lo que se busca —que sea divertido— no se puede especificar por anticipado; los
**sistemas críticos de control de seguridad** requieren una especificación completa y analizable
antes de construir. Ningún método es mejor que otro en abstracto.

**19.** Autónomas (un editor de texto local); basadas en transacciones interactivas (home banking,
cualquier aplicación web); embebidos o de control (el software de un microondas o un ABS); de
procesamiento por lotes (liquidación de sueldos, facturación mensual); de entretenimiento (un
videojuego); de modelado y simulación (simulador de vuelo, modelo climático); de adquisición de
datos (una estación meteorológica con sensores); de sistemas (una plataforma que integra varios
sistemas existentes).

**20.** Encaja en varios a la vez: es **embebido o de control** (gestiona dispositivos de
hardware), de **adquisición de datos** (sensores de tránsito), y visto en conjunto es un
**sistema de sistemas** (integra el control de cada cruce con un centro de monitoreo). Que
pertenezca a más de una categoría no es un error de clasificación: los sistemas reales combinan
tipos, y cada tipo aporta requisitos distintos.

**21.** **Especificación** (clientes e ingenieros definen qué debe hacer el software y sus
restricciones); **desarrollo** (diseño y programación); **validación** (verificar que cumple los
requisitos); **evolución** (adaptación a nuevos requerimientos del cliente o del mercado).

**22.** Mantenimiento, confiabilidad y seguridad, eficiencia, aceptabilidad.

**23.** a) Confiabilidad. b) Mantenimiento. c) Aceptabilidad. d) Eficiencia.

**24.** Los **esenciales** están ligados a la experiencia del usuario y a lo que se espera del
software terminado. Los **de calidad del diseño** se relacionan con la estructura interna del
sistema, y facilitan su evolución, mantenimiento y escalabilidad. Los primeros se juzgan desde
afuera; los segundos, desde adentro.

**25.** a) Disponibilidad. b) Seguridad. c) Protección. d) Confiabilidad.

## Unidad 2

**26.** Un **proceso de software** es un conjunto estructurado de actividades necesarias para
desarrollar un sistema de software. Un **modelo de proceso** es una representación abstracta de
un proceso, presentado desde una perspectiva particular.

**27.** **Productos** (los resultados de cada actividad), **roles** (las responsabilidades de las
personas involucradas) y **pre y post-condiciones** (lo que es verdadero antes y después de que
una actividad se haya realizado o se haya elaborado un producto).

**28.** En el **dirigido por plan**, todas las actividades se planifican con antelación y el
progreso se mide contra ese plan. En el **ágil**, la planificación es gradual y es más fácil
cambiar el proceso para reflejar requisitos cambiantes. Se combinan porque casi ningún proyecto
real es puro: hasta el más ágil planifica arquitectura y presupuesto, y hasta el más planificado
ajusta sobre la marcha. No hay procesos correctos o incorrectos.

**29.** No cambia **qué** se hace: cambia **cuándo y cuántas veces**. En cascada las cuatro
actividades van en secuencia y una sola vez; en incremental se intercalan y se repiten en cada
incremento; en espiral se repiten organizadas alrededor del riesgo. Lo que define a un modelo es
el **ordenamiento** de las actividades.

**30.** Análisis y definición de requerimientos; diseño del sistema y del software;
implementación y prueba de unidades; integración y prueba del sistema; operación y mantenimiento.
Su principal inconveniente es la **dificultad para acomodar cambios** una vez iniciado el
proceso, porque en principio cada fase debe completarse antes de pasar a la siguiente.

**31.** Conviene cuando los **requisitos son estables y bien entendidos**, y cuando existe
**regulación externa** que exige trazabilidad documento por documento. También ayuda a coordinar
proyectos grandes desarrollados en varias sedes. Dominios típicos: aviónica, dispositivos
médicos, señalización ferroviaria, control industrial.

**32.** Especificación, desarrollo y validación se **intercalan**; el sistema se desarrolla en
incrementos sucesivos. Beneficios: se reduce el costo de atender necesidades cambiantes; hay
menos análisis y documentación que rehacer; el cliente da feedback sobre lo implementado; hay
entrega más rápida de software útil. Problemas: el proceso **no es visible** (los gerentes
necesitan entregas regulares para medir progreso) y la **estructura del sistema tiende a
degradarse** a medida que se agregan incrementos, porque se invierte poco en refactorizar.

**33.** El **desarrollo** incremental describe cómo se **construye** el producto: en piezas
manejables, que pueden ser internas y no visibles para el cliente (por ejemplo, primero la base de
datos y la API sin interfaz). La **entrega** incremental describe cómo se **libera** al usuario:
cada incremento ya funciona por sí solo y aporta valor (por ejemplo, se libera el registro de
usuarios, después la gestión de perfiles). Se puede hacer desarrollo incremental sin entregar
nada hasta el final.

**34.** Análisis de requerimientos; análisis de los componentes; **modificación de
requerimientos**; configuración del sistema con la reutilización; desarrollo e integración. La
tercera etapa no existe en ningún otro modelo, y es llamativa porque es el único proceso donde
**los requisitos se ajustan a la solución disponible**, y no al revés.

**35.** El sistema **hereda las limitaciones de cada componente**. Si la plataforma elegida no
permite algo, el requisito se negocia con el cliente o se paga muy caro implementarlo por fuera.
Ejemplo: una tienda online armada sobre una plataforma de e-commerce que no soporta el esquema de
descuentos por volumen que la empresa usa desde hace años.

**36.** Conviene cuando los requerimientos **no están bien definidos desde el principio**. Fases:
desarrollo de un prototipo inicial; retroalimentación del usuario; refinamiento del prototipo; y
repetición del ciclo hasta llegar al producto final.

**37.** Cada ciclo se divide en cuatro sectores: establecimiento de objetivos; **valoración y
reducción del riesgo**; desarrollo y validación; y planeación. Lo distingue que la iteración está
organizada alrededor del **riesgo**: cada vuelta identifica y mitiga un riesgo concreto, en lugar
de simplemente agregar funcionalidad.

**38.** El **evolutivo** itera porque no se sabe **qué** construir; el motor de cada ciclo es el
feedback del usuario sobre un prototipo. El **espiral** itera porque hay **riesgos** que despejar;
el motor es el análisis de riesgo, y puede haber ciclos sin nada visible para el usuario. Sirve el
evolutivo y no el espiral en una app municipal donde nadie sabe qué quiere y el riesgo técnico es
bajo. Sirve el espiral y no el evolutivo al migrar historias clínicas de papel: se sabe
perfectamente qué construir, pero puede fallar la migración de datos, la adopción o la
conectividad.

**39.** Es el proceso de establecer qué servicios son necesarios y cuáles son las restricciones de
funcionamiento y desarrollo del sistema. Sub-actividades: **estudio de factibilidad**
(¿es técnica y financieramente viable?); **obtención y análisis** de requerimientos (¿qué esperan
los distintos actores?); **especificación** (definirlos en detalle); y **validación** (comprobar
su validez).

**40.** **Pruebas de desarrollo o de componente**: los componentes individuales se prueban de
forma independiente, y las hace el equipo de desarrollo. **Pruebas del sistema**: se prueba el
sistema como un todo, con foco en las propiedades emergentes; las hace el equipo. **Pruebas de
aceptación**: las realiza el **cliente**, para verificar que el sistema cumple con sus
necesidades.

**41.** a) Diseño e implementación. b) Evolución. c) Validación. d) Especificación de
requerimientos.

**42.** **Evitar el cambio**: el proceso incluye actividades que anticipan posibles cambios para
no repetir trabajo — por ejemplo, desarrollar un prototipo para mostrarle al cliente las
características clave antes de programar. **Tolerancia al cambio**: el proceso se diseña para que
los cambios cuesten poco — por ejemplo, desarrollo incremental, donde solo hay que alterar un
incremento para incorporar el cambio.

**43.** El prototipo es **evitar** el cambio; trabajar en incrementos es **tolerarlo**. No son
excluyentes y los procesos reales combinan las dos. Costos: evitar cuesta tiempo por adelantado y
falla si el cliente no sabe lo que quiere; tolerar cuesta disciplina técnica sostenida
—refactorización, pruebas automatizadas— que los equipos suelen abandonar justo cuando están
apurados.

**44.** Puede ser imposible ajustarlo para cumplir los requisitos no funcionales; normalmente
está indocumentado; su estructura se degrada por el cambio rápido; y difícilmente cumple con los
estándares de calidad de la organización.

**45.** Se lleva **conocimiento**, no código: requisitos que quedaron claros, decisiones de
interfaz ya validadas, flujos de pantalla, casos de prueba que surgieron al probarlo, y la lista
de cosas que el cliente creía querer y resultó que no. La justificación: el prototipo no es el
producto, es el instrumento para saber qué producto construir. Tirarlo es más barato que
descubrir el error después de haber construido el sistema de producción.

**46.** *Computer-Aided Software Engineering*: ingeniería de software asistida por computadora.
Son aplicaciones que ayudan a desarrollar software automatizando tareas del proceso y brindando
información sobre el sistema. Automatizan, entre otras cosas: el desarrollo de modelos gráficos,
la generación de código a partir de esos modelos, la producción de interfaces de usuario, la
depuración y la traducción entre versiones de un lenguaje.

**47.** Por **cobertura del ciclo de vida** (Upper CASE, Lower CASE, I-CASE); por **grado de
integración** (toolkit, workbench, IPSE); y por **función** (planificación, análisis y diseño,
programación, integración y prueba, prototipos, mantenimiento, gestión de proyectos, soporte). No
son alternativas porque responden a preguntas distintas: qué fases cubre, qué tan acopladas están
entre sí, y qué tarea concreta resuelven. Una misma herramienta se ubica en las tres a la vez.

**48.** Por cobertura se acerca a **I-CASE**, porque va de la gestión del trabajo al despliegue,
aunque no hace análisis ni diseño. Por integración es un **entorno integrado**, heredero del
IPSE. Por función cruza tres: soporte, gestión de proyectos, e integración y prueba. La dificultad
es que **ninguna casilla le queda bien**, y eso muestra que las taxonomías describen el panorama
de su época: no están mal, están fechadas.

**49.** No se contradicen. El Manifiesto no dice "no documentar": dice qué **priorizar cuando hay
que elegir**. Un equipo ágil documenta, pero documenta lo que se usa. Además, la mayoría de las
herramientas que usa un equipo ágil **son** herramientas CASE: el IDE, el control de versiones, la
integración continua, las pruebas automatizadas, el gestor de tareas. Lo que evitan no son las
herramientas, sino la documentación que nadie lee.

**50.** El **núcleo es el mismo**: los dos usan IDE, control de versiones y pruebas. Lo que cambia
es dónde se concentra el esfuerzo. La cascada regulada carga en documentación, trazabilidad de
requisitos, gestión de la configuración y verificación formal, porque un auditor necesita ver el
rastro de cada requisito hasta su prueba. La entrega incremental carga en integración continua,
despliegue automatizado, observabilidad y feedback en producción. Conclusión: el proceso no
determina **qué** herramientas se usan, sino **dónde** se pone el esfuerzo.
