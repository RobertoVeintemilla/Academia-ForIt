"Clean Code: A Handbook of Agile Software Craftsmanship" es una obra fundamental escrita por Robert C. Martin que revolucionó la forma en que los desarrolladores piensan sobre a calidad del código.

El libro se ha convertido en una referencia esencial para programadores de todos los niveles que buscan mejorar sus habilidades de programación. La premisa central es simple pero poderosa: el código limpio no es solo una cuestipn de estética, sino de profesionalismo y eficiencia. Martin argumenta que escribir código limpio es una disciplina y un arte que marca la diferencia entre un buen programador y un gran programador. A través de ejemplos práctivos, casos de estudio y principios concretos, el libro enseña cómo transformar código confuso y deordenado en código elegante y mantenible.

Los temas principales incluyen:
 * Nombres significativos para variables, funciones y clases.
 * Diseño de funciones efectivas y concisas.
 * Comentarios apropiados (y cuándo evitarlos)
 * Formato de código para mejorar la legibilidad
 * Manejo de errores profesional
 * Estructuras de datos y objetos bien diseñados
 * Pruebas unitarias y desarrollo guiado por pruebas (TDD)
 * Refactorización sistemática

# Preguntas

1. El principal beneficio de usar nombres significativos y pronunciables es que hace que el  código sea más legible y fácil de entender.
El auto argumentar que la mayor parte del tiempo de un programador se dedica a leet y entender código, no a escribirlo. Si una variable se llama 'd' en lugar de 'diasTranscurridos', o una función se llama 'a' en luar de 'calcularArea, el lector tiene que descifrar su propósito, lo que consume tiempo y energía mental.
Los nombres biene elegidos actúan como una forma de documentación intrinseca. Le dicen al lector lo que la variable, función o clase hace o representa, sin necesidad de recurrir a comentarios. Esto permite al programador comprender la lógica del código de un vistazo.

2. La recomendación principal de "Clean Code" sobre la longitud de las funciones es que deben ser pequeñas y hacer una sola cosa. El autor suguiere que las funciones no deberian tener mas de 20 líneas, y en lo posible, incluso menos.
¿Por qué funciones cortas? El principio de "una sola cosa" es fundamental para el libro. Una función que hace solo una cosa es más fácil de nombrar, entender y probar. Si una función es larga, es probable que esté haciendo múltiples tareas, lo que la hace difícil de leet y mantener. Al dividir una función larga en varias funciones más cortas, cada una con un nombre descriptivo, el código se vuelve mucho más legible, ya que la lógica se puede leer como una historia.

3. Un comentario '// Incrementar el contador' es un mal comentario y un 'codigo oloroso' (code smell). El libro argumenta que este tipo de comentario es redundatne y que el código ya debería ser lo suficientemente claro como para explicar su propósito por sí mismo.
Por que es un 'código oloroso'
* Redundancia: El comentario simplemente repite lo que el código ya esta diciendo. Si la línea de código es 'contador++', no hay necesidad de un comentario que lo explique.
* Mantenimiento: Los comentarios redundantes son difíciles de mantener. A menudo, el código cambia, pero el comentario no se actualiza, lo que lleva a la desinformación y la confusión.
* Falta de valor: un comentario debe explicar el "por qué" detrás del código, no el "qué" o el "cómo". Si el código es tan complejo que necesita una explicación de lo que hace, la solución es simplificar el código, no agregar un comentario.

4. La práctica que se alinea mejor con los principios de "Clean Code" es utilizar herramientas automáticas como Prettier y ESLint con una configuración compartida commiteada en el repositorio GIT.
El libro enfatiza que el formato es crucial para la legibilidad. Si cada desarrollador usa su propio estilo, el código se vuelve inconsistente, lo que dificulta su lectura y mantenimiento. La solución no es confiar en que cada uno lo haga bien manualmente, sino automatizar la consistencia.

5. La clase 'userProcessor' en el ejercicio viola principalemnte el Principio de Responsabilidad Única(SRP).
El SRP establecé que una clase debe tener una, y solo una, razón para cambiar. En otras palabras, una clase debe ser responsable de una sola tarea o de un solo aspecto de la funcionalidad de la aplicación.

6. La diferencia fundamental entre Objetos y Estructura de datos radica en la relación entre datos y el comportamiento. Esta diferencia es la base de dos filosofías de programación opuestas: la Programación Orientada a Objetos (POO) y la Programación Procedimental.
La Estructura de Datos (o Data Transfer Objects - DTOs) son un conjunto de datos públicos sin comportamiento significativo. Tienen miembros públicos que pueden ser accedidos directamente por cualquier parte del código. La lógica de negocio no está en la estructura de datos en sí, sino en funciones o clases externas que operan sobre esa estructura. Este es el enfoque de la Programación Procedimental.

7. En el manejo de errores, "Clean Code prefiere generalmente lanzar excepciones en lugar de devolver códigos de error como 'null' o '-1'.
La principal razón para esta preferencia es que el manejo de errores no debe entorpecer el flujo normal del código. Usar códigos de error como valores de retrno tiene varios incovenientes:
* Obscurece la lógica: Cuando una funcion devuelve un valor especial para indicar un error (por ejemplo, null), el código que llama a esa función debe verificar ese valor en cada invocación. Esto crea una lógica de negocio entremezclado con el manejo de errores, haciendo que la función sea más difícil de leer y entender.
* Fácil de ignorar: Un desarrollador puede olvidarse de verificar el código de error devuelto. Si se omite la verificación, el programa puede continuar ejecutándose con datos incorrectos, lo que puede llevar a errores inesperados y didíciles de depurar.
Falta de contexto: un código de error como '-1' no proporciona mucha información sobre lo que salió mal. Por otro lado, una excepción ('FileNotFoundException', 'InvalidArgumentException', etc) tiene un nombre claro y puede contener un mensaje detallado, lo que facilita la depuración y la resolución del problema.

8. La mejor estrategia para interactuar con una libreria externa de pagos es crear una capa de "Adaptador" (Adapter pattern) que envuelva la librería, exponiendo una interfaz que controle la aplicación y oculte los detalles de la librería.
Robert C. Martin argumenta que las librerias de terceros (third-party libraries) son intrínsecamente volátiles. El desarrollador no tiene control sobre ellas; pueden cambiar, ser discontinuadas o tener un comportamiento inesperado. Por lo  tanto, no se debe permitir que "contaminen" directamente la lógica de negocio de la aplicación.
El patrón Adaptador (o Wrapper) ofrece una capa de protección. Funciona de la siguiente manera:
* Define una Interfaz Propia: Creas una interfaz dentro de tu aplicación (por ejemplo, 'PaymentGateway').
* Crea una Clase Adaptadora: Escribes una clase que implementa esa interfaz (por ejemplo, 'StripeAdapter'). Esta clase es la única parte de tu código que interactua directamente con la librería de terceros (en este caso, Stripe).
* Llama desde tu Lógica: Tu lógica de negocio solo sabe sobre la interfaz 'PaymentGateway'. No tiene idea de que existe Stripe o de sus detalles de implementación.

9. La 'F' en el acrónimo FIRST significa Fast (Rápido)

10. La función en TypeScript señala un problema potencial conocido como la 'Bandera Booleana' (Boolean Flag).
La recomendación para evitar la bandera booleana es dividir la función en dos funciones separadas, cada una con una responsabilidad única y un nombre descriptivo:
* processOrder (order: Order, user: User): Esta función solo se encargaría de procesar la orden.
* processOrderAndSendNotification(order: Order, user: User): Esta función llamaría a 'processOrder' y luego se encargará de enviar la notificación.
Esta refactorización mejora la legibilidad, ya que el nombre de cada función ahora comunica claramente su propósito. También simplifica la lógica, haciendo que cada función sea más fácil de probar y de mantener de forma aislada.

11. La "Ley de Demeter" (Law of Demeter) o Principio de Menor Conocimiento es una guía de diseño de software que establece que un objeto debe saber lo menos posible sobre la estructura de otros objetos. Esta Ley prohibe la "cadenas de llamadas" o "trenes de mensajes"

12. Un "Code Smell" (Olor a Código) es un síntoma o una característica en el código fuente de un programa que, por sí mismo, no es necesariamente un error o un fallo, pero que sugiere la existencia de un problema más profundo en el diseño o en la estructura del software.
El objetivo de identificar y eliminar "Code Smells" es mejorar la calidad del código, haciéndolo más legible, más fácil de mantener y menos propenso a errores en el futuro.

13. La "Regla del Boy Scout" aplicada al desarrollo de software postula que siempre se debe dejar el código un poco más limpio de lo que se encontró. 
Esta práctica garantiza que la calidad del código no se deteriore con el tiempo sino que mejore constantemente. Al igual que los Boy Scouts dejan un campamento más limio de lo que lo ecnontraron, los desarrolladores deben dejar el código base en un mejor estado. Esto reduce la "deuda técnica" y hace que el sistema se mas sostenible y fácil de mantener a largo plazo.

14. Si se tiene dos funciones en TypeScript que hacen casi lo mismo, "Clean Code" promovería la refactorización para eliminar la duplicación de código. La estrategia principal para lograr esto es extraer el código común en una nueva función o método y luego hacer que las funciones originales llamen a esta nueva función.

15. "Clean Code" aboga a clases pequeñas y con alta cohesión para hacer que el software sea más fácil de entender, mantener y cambiar. Esta recomendación se basa en el Principio de Responsabilidad Única (SRP).

16. Según Kent Beck, la primera y más importante regla del "Diseño Simple" es que el software debe pasar todas las pruebas (All test pass).

17. El principio de diseño que ayudaría a desacoplar la lógica de negocio de los detalles de la base de datos es el Principio de Inversión de Dependencias (Dependency Inversion Principle - DIP).
El DIP postula dos ideas claves:
* Los módulos de alto nivel no deben depender de modulos de bajo nivel. Ambos deben depender de abtracciones (interfaces).
* Las abstracciones no deben depender de los detalles. Los detalles deben depender de las abstracciones.

18. Una de las principales críticas a la aplicación estricta de TDD es que puede ser percibida como una práctica lenta en las etapas iniciales de un proyecto, especialmente cuando se está explorando un nuevo dominio o una API desconocida.
La crítica se basa en la percepción de que el ciclo de TDD y la necesidad de escribir pruebas para cada fragmento de funcionalidad pueden ralentizar la "velocidad de implementación". En un entorno de startups o con plazos de entrega muy ajustados, la presión por enrtegar funcionalidad rápidamente puede chocar con la disciplina de TDD, que prioriza la calidad y el diseño por encima de la velocidad inicial.

19. "Clean Code" prefiere devolver un objeto específico y bien nombrado que encapsule todos los datos relacionados.
La principal razón es la claridad y la legibilidad. Usar parámetros de salida o devolver un objeto genérico 'Object' (o un 'Array') tiene varios incovenientes.
* Parámetros de salida (out parameters): Este enfoque obliga al lector del código a examinar la firma de la función para entender qué datos se están modificando. El nombre del parámetro de salida puede ser engañoso y no está claro si es una entrada o una salida. Además, puede hacer que la función sea menos intuitiva de usar, ya que su comportamiento no se refleja completamente en su valor de retorno.
* Objetos genéricos (Object o Array): Devolver un objeto o un array genérico es aún peor. No hay un contrato claro sobre qué propiedades o valor contiene el objeto. El desarrollador que usa la función debe saber por conveción (o por la documentación) qué índices o claves debe usar para acceder a los datos. Esto es frágil y propenso a errores. Por ejemplo, si una funciín devuelve '['Juan', 25]', no hay forma de saber si el primer elemento es un nombre o un apellido sin leer la documentación.

20. La práctica más importante para segurar que no se introduzcan regresiones al refactorizar es tener un conjunto completo y robusto de tests automatizados que cubran el comportamiento existente del código.