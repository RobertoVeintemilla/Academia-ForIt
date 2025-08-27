"Test Driven Development by Example" es un libro fundamental esrito por Kent Beck, uno de los pioneros de las metodologías ágiles y creador de Extreme Programming (XP), que transformó radicualmente cómo los desarrolladores abordan la creación de software.

Este libro se ha establecido como un recurso indispensable para programadores que buscar mejorar la calidad y confiabilidad de su código. La premisa central es revolucionaria pero pragmática: escribir pruebas antes que el código de proucción conuce a mejor diseño y mayor calidad.

Beck presenta el Test Driven Development (TDD) no sólo como una técnica de pruebas, sino como una metodoloía completa de desarrollo que impulsa un diseño emergente y una codificación más enfocada. A través de ejemplos concretos, ejercicios prácticos y explicaciones clara, el libro muestro cómo implementar TDD en situaciones reales.

Concepto principal de TDD:
El libro se centra en un ciclo muy simple:
1- Red(Rojo): Escribir una prueba unitaria que falle. Lo haces antes de escribir el código de producción. La prueba falla porque la funcionalidad aún no existe.
2-Green(Verde):escribir la mínima cantidad de código de producción para que la prueba pase. No te preocupes por la perección, solo haz que la prueba funcione.
3-Refactor(Refactorizar): Una vez que la pureba pasa, revisa tu código(tanto la prueba como el código de producción) para mejorar su estructura, eliminar duplicaciones y hacerlo más limpio, sin cambiar su comportamiento.

Kent Beck se refiere a esto como un diseño emergente", donde el diseño del software evoluciona de forma incremental a partir de las pruebas.

"By example"(con ejemplos):
El libro no es teórico, si no que te lleva a través de una serie de ejemplos de código para que vea cómo se aplica TDD en la práctica, desde tan simple como un sistema de dinero hasta un framework de pruebas.

#Ejercicios

1. El objetivo principal del TDD es eliminar el miedo en el desarrollo de software. Beck argumenta que la programación puede ser una actividad llena de incertidumbres y temor, especialmente al enfrentarse a problemas complejos o al modificar código existente.
El ciclo de TDD actúa como un mecanismo de seguridad que permite a los programadores trabajar en pasos pequeños y verificables. A lescribir una prueba que falla antes de implementar cualquier funcionalidad, el programador sabe exactamente lo que debe hacer para que el código funcione. Una vez que la prueba pasa, tienen la confianza de que la funcionalidad está resuelta y pueden refactorizar (mejorar el diseño del código) con la seguridad de que las pruebas existentes les avisarán si rompen algo. Este proceso iterativo y continuo de feedback reduce la ansiedad y fomenta un diseño de software simple y emergente.

2. La secuencia del ciclo de TDD (Red-Green-Refaactor) es:
EScribir test que falla - Hacer que el test pase - Refactorizar

3. En el paso "Red" del ciclo TDD, se busca idealmente un fallo especifico y significativo que indique que la funcionalidad aún no existe.
No se busca un error de compilación (Syntax error) o un fallo genérico. La idea es escribir una prueba que demuestre de manera inequivoca la ausencia de la funcionalidad que se va a implementar. Por ejemplo, si se quiere crear un método sum() que sume dos números, la prueba debería fallar por que el método sum() aún no existe o, si existe, devuelva un resultado incorrecto. Este fallo, causado por una "expectactiva no cumplida", actúa como una guía clara de lo que se debe hacer a continuación.

4. "Fake It" es una de las estrategias que KEnt Beck describe en el libro para pasar un test rápidamente en la fase "Green". Consiste en escribir el código más simple posible que haga que le test pase, incluso si la solución no es la implementación correcta o completa del problema
El objetivo es pasar al siguiente paso del ciclo TDD lo más rápido posiblem para obtener una prueba verde y luego refactorizar el código para que sea una solución correcta y general


5. Cuand Kent Beck se refiere a la Triangulación en el contexto de TDD, está hablano de una tecnica para refinar y generalizar el código. La triangulación implica escribir una segunda prueba que ejerza el mismo código de producción, pero con un valor diferente.
La idea es que una vez que la primera prueba pasa (paso Verde), la segunda prueba hará que el código de producción sea más general y flexible. Esto se logra refactorizando el código de producción para que pueda manejar ambos casos de prueba de manera correcta.

6. La velocidad de ejecución de los tests unitarios es crucial en TDD por varias razones fundamentales que están directamente relacionadas con el objetivo de proporcionar un feedback inmediatio y reducir el miedo a cambiar el código. KEnt Beck enfatiza este punto porque: 
  a. Iteraciones rápidas y feedback constante: El cuclo TDD de "Roo-Verde-Refactor" se basa en ciclos muy cortos. Un programador puede ejecutar los tests decenas o includo cientos de veces al día. Si los tests tardan en ejecutarse, el ciclo se ralentiza, la retroalimentación se vuelve lenta y la disciplina de TDD se debilita. La velocidad permite que el programador ejecute los test después de cada pequeño cambio, lo que le da una confirmación instantánea de que no ha roto nada.
  b. Confianza y seguridad: Los test unitarios ráidos confiables actúan como una red de seguridad. Si el desarrollador sabe que puede ejecutar todas las pruebas en segundoos y obtener una respuesta clara de si todo funciona, puede refactorizar el código con confianza. El miedo a introducir regresiones o bugs desaparece, lo que fomenta la mejora continua del diseño de software.
  c. Fomento de un buen diseño. La necesidad de tests unitarios rápidos y aislados fomenta un diseño de software que sea modular y de baja acomplamiento. Un código muy acoplado con dependencias externas (como bases de datos, APIs o archivos) haría que las pruebas fueran lentas y dificiles de aislar. La velocidad del test unitario fuerza al desarrollador a pensar en cómo puede hacer que su código sea más "testeable", lo que a menudo se traduce en un código mejor diseñado.
  d. Hábito y disciplina: La rapidez de los test fomenta el habito de ejecutarlos con frecuencia. si un conjunto de test tarda 10 minutos, un desarrollador probablemente los ejecutará sol al final del día. Si tardan 10 segundos, los ejecutará varias veces por minuto. Esta frecuencia es lo que hace que TDD sea una práctica de desarrollo diaria y efectiva, en lugar de una tarea ocasional.

7. Las caracteristicas de un buent test unitario según TDD:
  a. Rápido: debe ejecutarse en milisegundos para permitir un feedback contastante y frecuente.
  b. Aislado: debe probar un sola cosa a la vez y no depender de otros tests o de factores externos como una base de datos o una API.
  c. Automático: debe poder ejecutarse con un solo comando o click
  d. Confiable: no debe fallar de manera intermitente. El test debe pasar cuando el código es correcto y fallar cuando no lo es.
  d. Fácil de leer: el test debe ser claro y comprensible para cualquier programador. Debe ser fácil de entender qué es lo que se está probando

8. La forma de manejar el miedo en el desarrollo de software es aprender concretamente lo más rápido posible, a través de tests.
El miedo es un tema central en la filosofía de Beck. Él argumenta que los programadores a menudo tienen miedo de:
Introducir errores al cambiar el código existente.
Afectar otras partes del sistema sin saberlo.
Enfrentarse a un problema que no saben cómo resolver.
La práctica de TDD, al basarse en ciclos muy cortos de retroalimentación, permite a los desarrolladores obtener la seguridad de que su código funcione antes de continuar. Al escribir un pequeño test que fall y luego escribir la minima cantidad de código para que pase, el desarrollador aprende de manera incremental y concreta que ha resuelto una parte del problema. Este proceso repetido, a través de test rápido y automatizados, elimina la incertidumbre y contruye confianza, reduciendo así el miedo inherente al proceso de programación. 

9. #Pregunta. Considerando el siguiente test en TypeScript, ¿qué se espera en el paso 'Red' si add aún no está implementado?
##Respuesta. El paso "Rojo" del ciclo TDD tiene comp objetivo crear un test que demuestre que la funcionalidad desada AÚN NO EXISTE. Este fallo debe ser predecible y significativo. El test debe ser capaz de compilar y ejecutarse; el fallo se produce cuando el valor real devuelto por la funcion(undefined, null o un valor incorrecto) no coincide con el valor esperado (3). Este tipo de fallo es una guía clara y precisa de lo que se necesita construir a continuación

10. Según Kent Beck, el propósito de la fase de 'Refactor' en TDD es mejorar el diseño del código, no su comportamiento. Esta es la tercera y última etapa del ciclo de TDD, que sigue las fases de "Rojo" (escribir un test que falle) y "Verde" (escribir el código mínimo para que el test pase)
El refactor permite:
 *Eliminar la duplicación: A menudo, para que una prueba pase, se escribe código duplicado. La fase de refactor es el momento de eliminarlo y consolidar la lógica
 *Mejorar la legibildad: Se pueden cambiar nombres de variables o métodos, extraer métodos complejos o reorganizar el código para que sea más fácil de entender para otros desarrolladores (y para ti mismo en el futuro)
 *Simplificar el diseño: El diseño del software emerge de la serie de pequeños pasos de refactorización. En lugar de diseñar un sistema completo desde el principio, el diseño se forma gradualmente a medida que el código se limpia y se simplifica

11. Tener una "lista de tests" es crucial por varias razones que abordan la gestión de desarrollo y la mentalidad del programador.
 a. Guía y enfoque: La lista de tests actúa como una guía de navegación. En lugar de tener una idea vaga de lo que se va a construir, la lista te obliga a desglosar una gran tarea en pasos pequeños y concretos. Cada ítem de la lista se convierte en el proximo test que debes escribir, lo que te ayuda a mantenerte enfocado y a no perder de vista el objetivo final.
 b. Manejo de la complejidad: La programación puede ser abrumadora cuando te enfrentas a un problema complejo. La lista de tests te permite gestionar esa complejidad dividiendo el problema en partes manejables. Al completar cada test. te da cuenta de que has resuelto una pequeña porción de problema, lo que genera una sensación de progreso y reduce el sentimiento de agobio.
 c. Registro de progreso: La lista de tests es un registro tangible del progreso. A medida que completas un test y lo eliminas de la lista, tienes una prueba visible de que has avanzado. Esta retroalimentación positiva ayuda a mantener la motivación y a evitar que te sientas "atascado" en el proceso.
 d. Descubrimiento de casos de borde: A medida que creas la lista, te ves obligado a pensar en diferentes escenarios, incluyendo casos de borde o situaciones que podrías haber olvidad si hubieras abordado el problema de una manera más holística. ESto ayuda a garantizar una cobertura más completa de la funcionalidad

12. Si un test unitario es "frágil", suguiere que una parte de la aplicación está afectano sorprendentemente a otra, lo que indica un acomplamiento inesperado
  Explicación:
   Un test frágil es aquel que falla por una razón no relacionada con la funcionalidad que está probando. Este tipo de fallo a menudo ocurre cuando el test depende de un estado global o de la configuración de otra parte del sistema. Por ejemplo, si un test de una clase de usuario falla porque un test anterior modificó el estado de la base de datos de manera ineperada, el test es frágil.
   Becl argumenta que esta fragilidad en los tests es un síntoma de un problema de diseño más profundo: el alto acoplamiento. Un código acomplado significa que los módulos o componentes no son independientes. Los cambios en un módulo pueden tener efectos secundarios no deseados en otro. En el contexto de TDD, los tests actúan como un sistema de alerta temprana para este tipo de problemas de diseño. Un test frágil te avisa que las partes de tu aplicación no están lo suficientemente aisladas, l que hace que el ódigo sea difícil de mantener y de cambiar sin romper algo. La soluciíon no es arreglar el test, sino refactorizar el código de producción para reducir el acomplamiento.

13. El principio de 'Clean Code That Works' (Código Limpio que Funciona) en el contexto de TDD significa que el objetivo del desarrollo no es solo crear software que pase las pruebas, sino también asegurar que ese código sea legible, fácil de mantener y de entender. Es el resultado directo de la combinación de las tres fases del ciclo de TDD: Rojo, Verde y Refactor
Este principio abarca dos ideas fundamentales:
  "That Works"(que funciona): Esta parte del principio se aborda durante las fases Rojo y Verde. Al describir un test antes de escribir el código de producción, se garantiza que el código que se va a implementar va a cumplir con la funcionalidad esperada. Los tests unitarios actúan como una prueba de que el código está haciendo lo que se supone que debe hacer. Si un test pasa, tienes la seguridad de que esa porción de código funciona.
  "Clean Code"(código limpio): Esta parte se logra en la fase Refactor. Una vez que el código funciona y las pruebas lo confirman, la fase de refactorización permite mejorar el diseño interno del código sin cambiar su comportamiento. Esto incluye eliminar duplicación, mejorar la legibilidad y simplificar la estructura. La red de seguridad de los tests te da la confianza para hacer estos cambios sin miedo a romper la funcionalidad ya existente.

14. La primera parte de un test que se debe escribir es la aserción(assertion)
Escribir la aserción al principio, incluso antes de escribiri el código que la llamará, te obliga a pensar en el comportamiento deseado de tu código. La aserción define lo qu consideras un resultado exitos para el test. Este enfoque tiene varias ventajas:
  Define el "hecho": Te obliga a clarificar qué es lo que estás probando y qué valor esperas. Por ejemplo, en un test para una función de suma, la aserción expect(resultado).toBe(3) establece que un resultado de 3 es el "correcto" y el único que te permitirá avanzar.
  Simplifica el test: El saber exactamente lo que se espera, puedes escribir el resto del test (la llamada a la función, la configuración inicial) con el único proposito de llegar a esa aserción.
  Enfoque de "outside-in": Este método fomenta una mentalidad de diseño de afuera hacia adentro. En el lugar de pensar en cómo se va a construir la funcionalidad, piensas en cómo se va a usar y qué se espera que devuelva. Esto a menudo conduce a interfaces de código más intuitivas y a un mejor diseño.

15. Un beneficio clave de TDD es que ayuda a los desarrolladores a enfocarse en los requisitos y la interfaz de la funcionalidad antes de escribir el código de producción.
La práctica de escribir un test que falle (el paso "Rojo") antes de cualquier implementacion fuerza al desarrollador a pensar en cómo se va a usar la nueva funcionalidad. Esto implica: 
* Clarificar los requisitos: Para escribir un test, debes saber exactamente qué se espera que haga el código, Este proceso te obliga a entender los requisitos de manera precisa, eliminando ambiguedades. 
* Diseñar la interfaz: La aserciín del test (e.g., expect(miFuncion(param)).toBe(resultado) ) actúa como un contrato o una especificación para la interfaz pública de tu código. Estás definiendo la forma de la funciin (su nombre, sus parametros y su valor de retorno) antes e preocuparte por la implementación interna.

16. La situación que indica un 'code smell' en el contexto de TDD, relacionado con los tests, es: Tests con código de setup muy largo y repetitivo
Explicación: un 'code smell' es una señal de que algo podría estar mal en el diseño del código. En el contexto de los test unitarios, el código de setup largo y repetitivo ( a menudo llamado "boilerplate") es un claro indicio de un problema. Este 'smell' sugiere que el código bajo pruebas peude tener un alto acoplamiento o que las clases son difíciles de instanciar y probar de forma aislada
Consecuencias del 'Code Smell'
 * Aumenta el acoplamiento: El 'setup' repetitivo a menudo oculta dependencias entre los objetos, haciendo que el código sea difícil de mantener y refactorizar.
 * Dificulta la lectura: los tests se vuelven menos legibles. En lugar de centrarse en lo que se está probando, el lector tiene que descifrar una gran cantidad de código de configuración.
 * Desincentiva la refactorización: A nadie le gusta refactorizar un test que es dificil de leer y está lleno de repetición. Esto va en contra de la disciplina de TDD.

17. Es totalmente aceptable la introducción de códio duplicado para hacer pasar el test. esté es una práctica comun en la fase 'Green' de TDD.
La meta principal de la fase 'Green' es hacer pasar el test de la manera más simple y rápida posibl, sin preocuparse por la limpieza o optimización del código. A menudo, esto significa que el código que escribes puede ser redundante o ineficiente.
En REFACTOR es donde se resuelve la duplicación. Una vez que el test está en verde, se tiene una red de seguridad que permite reorganizar y limpiar el código sin miedo a romper algo.

18. TDD influye en el diseño de software de manera sinificativa, promoviendo un diseño más simple, modular y flexible. No es solo una técnica de pruebas, sino una disciplina de diseño que se basa en la retroalimentación constante del ciclo Rojo-Verde-Refactor.

19. Según el libro, si el tiempo se acaba mientras haces programación en pareja, debes dejar el código con todos los tests pasando, incluso si eso significa deshacer el íultimo cambio que hiciste para llegar a ese estado. Esto se conoce como "Leave the camp clean" (Dejar el campamento limpio).
El objetivo principal de esta regla es mantener la integridad del sistema y la disciplina edlequipo. Si te alejas de tu computadora y dejas un test fallando, la siguiente persona que trabaje en el código podría no entender el contexto de ese fallo, lo que genera confusión, pérdida de tiempo y, en el peor de los casos, la introduccion de errores.
Si estás en medio de un ciclo TDD (en la fase "Rojo" o "Verde") cuando el tiempo se acaba, la recomendación es revertir tus cambios para volver a un estado de tests todos en "Verde". Esto puede parecer un retroceso, pero en realidad mantiene la estabilidad del proyecto y permite que el siguiente desarrollador (o tú mismo más tarde) comience a trabajar con una base sólida y confiable.

20. Un 'Test Double' como un Mock Object es útil en TDD cuando se necesita simular el comportamiento de dependencias externas (base de datos, servicios, etc.) para aislar la unidad bajo prueba.
La esencia de un test unitario es probar una sola "unidad" de código de forma aislada. Sin embargo, el código a menudo tiene dependencias de otros componentes, como:
 * Base de datos: Acceder a una base de datos real es lento e introduce complejidad.
 * SErvicios web externos: Llamar a una API externa es lento y depende de la disponibilidad del servicio.
 * Archivos del sistema: La lectura o esritura de archivos puede hacer que os tests sean frágiles y lentos