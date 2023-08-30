<div align="center">
  
  <h1>Sección 2</h1>

  <h2>Modelo básico del  inventario de ciclo de vida</h2>
</p>

</div>

<div align="justify">

### 1.1 Propósito de la sección
Aprenderás cómo es la estructura de cálculo matemático para determinar el inventario de ciclo de vida con procesos monofuncionales.

### 1.2 Modelo básico de inventario: Representando los procesos unitarios y los flujos


Recordemos que en el paso del inventario de ciclo de vida, el resultado final es la cuantificación de todos las intervenciones ambientales que el sisteme producto a lo largo de su ciclo de vida ha tenido. Denominamos como modelo de inventario básico a la estructura fundamental  de naturaleza matemática que siempre nos va a permitir calcular el inventario de ciclo de vida. Lo primero que hay que hacer para determinar el inventario, es haber definido previamente la unidad funcional y los flujos de referencia. Luego hay que determinar cuál es el sistema producto que se va a tener en cuenta. Recordemos que el sistema producto es el conjunto de procesos unitarios que describen el ciclo de vida del producto. En principio una manera práctica de empezar a modelar el ciclo de vida del producto es elaborar un diagrama que visualiza el conjunto de procesos unitarios del sistema. Así que para empezar imaginemos que tenemos el diagrama de flujno de los procesos unitarios que se muestra más abajo. Importante señalar que cada uno de los procesos solo presta un servicio o función, si observas bien, verás que cada proceso entrega/produce solamente un solo flujo tecnológico o intermedio (por eso hablamos de procesos monofuncionales). Luego es útil preparar una tabla de entradas y salidas (tanto con flujos tecnológicos como ambientales). Más abajo aparece la tabla respectiva para nuestro ejemplo hipotético.

![Diagrama de ciclo de vida para la producción de una probeta de aluminio](https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/DIAGRAMA%20CV_Imagen%201.png)

![Datos de los procesos untarios](https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/IMAGEN2_DATOS.png)

### 1.3 Modelo básico de inventario: La solución matemática con escalamiento manual

Para poder entender más adelante la lógica de la estructura cálculo del inventario basada en el uso del álgebra lineal, vamos a comenzar calculando el inventario, digamolo de manera "manual". Lo primero que observamos es que la cantidad de probeta que produce el proceso unitario denominado "producción de la parte de aluminio" no coincide con la cantidad de probetas que le vamos a demandar el servicio que es de 100 unidades que están contempladas en la unidad funciona. Por lo tanto, debemos escalar este proceso para que produzca 100 probetas, por lo que debemos multiplicar por 100 la salida de ese proceo para que nos de las 100 unidades que le estamos demandando al sistema. Ahora bien, asumimnos que existe una relación de proporcionalidad entre la cantida de probetas producidas y la cantidad de las otras entradas y salidas del proceso, por lo tanto, la cantidad de energía eléctrica y de lingotes que requiere ese proceso debemos también multiplicarla por 100. Este valor de "100" (que es adimensional) se le conoce como factor de escalamiento y habrá tantos factores de escalamiento como procesos unitarios existen en el sistema producto. Lo que quiere decir que para satisfacer la producción de 100 probetas, ahora vamos a necesitar 0.05 toneladas de lingotes y 300 kwh de electricidad. Esto nos lleva a escalar el proceso de producción de lingotes. Para que este proceso satisfaga la necesidad de lingotes de 0.05 toneladas que se requieren para la producción de las probetas, debemos multiplicar las entradas y salidas del proceso de producción de lingotes por el valor de 0.05 que corresponde al segundo factor de escalamiento. De esta manera ya tenemos exactamente las cantidades de lingotes que requiere la producción de probetas, por lo tanto ni sobra ni falta material, es decir por ahora el flujo de material de lingotes es cero, es decir, que exactamente la cantidad que se requiere de lingotes para producir las 100 probetas que demanda la unidad funcional, es igual, a la cantidad de lingotes que produce el proceso de producción de lingotes.



También existe los flujos económicos o tecnológicos (otras veces denominados flujos intermedios o flujos de la tecnosfera), los cuales son flujos de materia y energía que son creados por intervención del hombre. Se denominan tecnológicos porque para su creación fue necesario la aplicación de tecnología desarrollada por el ser humano. También se denominan económicos porque esos flujos se tranzan en el mercado. Un ejemplo de flujos económicos son la energía eléctrica, el poliestireno o el diésel.

Otro concepto fundamental es proceso unitario, que corresponde a una función que es capaz de transformar unas entradas en unas salidas y se constituye como el elemento más pequeño para recolectar información cuantitativa sobre los flujos de entradas y salidas para el análisis de inventario del ciclo de vida del producto. Un ejemplo podría ser la producción de energía eléctrica o la extrusión de una pieza plástica. 

Un concepto de especial relevancia es *unidad funcional" que refiere al desempeño cuantificado de la cantidad de servicio o función que se le demanda a un determinado sistema de producto. Un ejemplo sería *la cantidad de acero, en libras, necesarias para producir una parte automotriz que cumpla con todos los requisitos estructurales y de seguridad relevantes para una vida útil del vehículo de 200.000 kilómetros recorridos. Finalmente el concepto de flujo de referencia va a tener una estrecha conexión con la unidad funcional, en el sentido que el flujo de referencia es la manifestación física de las salidas que va a tener cada proceso unitario en el ciclo de vida del producto que van a satisfacer la función o servicio que se expresa a través de la unidad funcional. Retomando el ejemplo anterior de unidad funcional, aquél proceso que produce acero tendría como flujo de referencia, la cantidad de acero producido necesaria para fabricar la parte de acero del vehículo y que cumpla los requisitos de calidad y de vida útil expresados en la unidad funcional.



### 1.4 Principios del ACV y sus limitaciones
La norma internacional ISO 14040:2006 ofrece uno principios orientadores para llevar a cabo estudios de ACV:
- Perspectiva de ciclo de vida: El ACV tiene en cuenta las etapas del ciclo de vida de un producto que fueron referidas anteriormente. Esta mirada holística ayudar a identificar, reducir o evitar el cambio o traslado de algún impacto ambiental entre las etapas del ciclo de vida.
- Énfasis en lo ambiental: Se refiere que el ACV solo tiene en cuenta las consideraciones ambientales, dejando de lado aspectos como los sociales y económicos.
- Enfoque basado en la función o servicio del sistema: El ACV se realiza teniendo como base la unidad funcional, de manera que todo el estudio de ACV tiene como fundamento en la cantidad de servicio o función que se haya determinado para el sistema producto.
- Enfoque iterativo: Refiere a la interacción que existe entre una paso y otro para llevar a cabo el estudio de ACV y que permite una consistencia del estudio.
- Transparencia: Los resultados de un estudio de ACV tiene el suficiente respaldo documental y explicaciones que facilitan una adecuada interpretación de los mismos
- Basado en información científica: Las decisiones en un estudio de ACV tiene principalmente su fundamento en la ciencia y en ausencia de este principio es válido tener en cuenta juicios de valor.
- Flexibilidad: No existe un único método para realizar un estudio de ACV y por lo tanto las organizaciones tienen la flexibilidad de escoger el método que consideren de acuerdo con los objetivos y alcance del estudio.


### 1.5 Pasos para llevar a cabo un ACV
De acuerdo con la norma internacional ISO 14040:2006 existen cuatro fases de un estudio de ACV:
1. Definición del objetivo y del alcance
2. Análisis del inventario
3. Evaluación del impacto
4. Interpretación

En la definición del objetivo y del alcance se deja claro cuáles son las motivaciones para llevar a cabo el estudio y los parámetros a tener en cuenta. Dentro de los parámetros clave están, la determinación de la unidad funcional, los límites del sistema, reglas de asignación, método de evaluación del impacto potencial ambiental, requisitos de calidad de los datos, entre otros.

El análisis del inventario identifica y cuantifica las entradas y salidas de cada uno de los procesos unitarios del sistema industrial  que satisfacen la unidad funcional escogida
para luego finalizar cuantificando el  total  de cada tipo de flujo ambiental a lo largo de todo el sistema producto.

Con la evaluación del impacto se convierte el total de cada tipo de flujo ambiental determinado anteriormente en términos de cuál sería su impacto ambiental potencial en una determinada categoría de impacto.

Finalmente en la etapa de interpretación se hace un análisis de la información recolectada y procesada en los pasos anteriores, entre algunos de los asuntos que se estudian está la identificación de los asuntos significativos, una evaluación de la completitud, análisis de sensibilidad y consistencia, conclusiones y limitaciones y recomendaciones.

</div>
