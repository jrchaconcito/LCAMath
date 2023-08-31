<div align="center">
  
  <h1>Sección 2</h1>

  <h2>Modelo básico del  inventario de ciclo de vida</h2>
</p>

</div>

<div align="justify">

### 1.1 Propósito de la sección
Aprenderás cómo es la estructura de cálculo matemático para determinar el inventario de ciclo de vida con procesos monofuncionales.

### 1.2 Modelo básico de inventario: Representando los procesos unitarios y los flujos


Recordemos que en el paso del inventario de ciclo de vida, el resultado final es la cuantificación de todos las intervenciones ambientales que el sisteme producto a lo largo de su ciclo de vida ha tenido como consecuencia de habérsele demandado o pedido una cantidad de servicio o función que se determina en la unidad funcional. Denominamos como modelo de inventario básico a la estructura fundamental  de naturaleza matemática que siempre nos va a permitir calcular el inventario de ciclo de vida. Lo primero que hay que hacer para determinar el inventario, es haber definido previamente la unidad funcional y los flujos de referencia. Luego hay que determinar cuál es el sistema producto que se va a tener en cuenta. Recordemos que el sistema producto es el conjunto de procesos unitarios que describen el ciclo de vida del producto. En principio una manera práctica de empezar a modelar el ciclo de vida del producto es elaborar un diagrama que visualiza el conjunto de procesos unitarios del sistema. Así que para empezar imaginemos que tenemos el diagrama de flujno de los procesos unitarios que se muestra más abajo. Importante señalar que cada uno de los procesos solo presta un servicio o función, si observas bien, verás que cada proceso entrega/produce solamente un solo flujo tecnológico o intermedio (por eso hablamos de procesos monofuncionales). Luego es útil preparar una tabla de entradas y salidas (tanto con flujos tecnológicos como ambientales). Más abajo aparece la tabla respectiva para nuestro ejemplo hipotético.

![Diagrama de ciclo de vida para la producción de una probeta de aluminio](https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/DIAGRAMA%20CV_Imagen%201.png)

![Datos de los procesos untarios](https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/IMAGEN2_DATOS.png)

### 1.3 Modelo básico de inventario: La solución matemática con escalamiento manual

Para poder entender más adelante la lógica de la estructura cálculo del inventario basada en el uso del álgebra lineal y que fue desarrollada por Heijungs & Suh (2002), vamos a comenzar calculando el inventario, digamolo de manera "manual". Lo primero que observamos es que la cantidad de probeta que produce el proceso unitario denominado "producción de la parte de aluminio" no coincide con la cantidad de probetas que le vamos a demandar que es de 100 unidades que están determinadas en la unidad funcional. Por lo tanto, debemos escalar este proceso para que produzca 100 probetas, por lo que debemos multiplicar por 100 la salida de ese proceo para que nos dé las 100 unidades que le estamos demandando al sistema. 

Ahora bien, asumimos que existe una relación de proporcionalidad entre la cantidad de probetas producidas y la cantidad de las otras entradas y salidas de este proceso, por lo tanto, la cantidad de energía eléctrica y de lingotes que requiere este proceso debemos también multiplicarlas por 100. Este valor de "100" (que es adimensional) se le conoce como factor de escalamiento (habrá tantos factores de escalamiento como procesos unitarios distintos existan en el sistema producto). Lo que quiere decir que para satisfacer la producción de 100 probetas, ahora vamos a necesitar 0.05 toneladas de lingotes y 300 kwh de electricidad. Esto nos lleva a escalar el proceso de producción de lingotes. Para que este proceso satisfaga la necesidad de lingotes de 0.05 toneladas que se requieren para la producción de las probetas, debemos multiplicar las entradas y salidas del proceso de producción de lingotes por el valor de 0.05 que es otro factor de escalamiento. De esta manera ya tenemos exactamente las cantidades de lingotes que requiere la producción de probetas (0.05 toneladas de lingotes) y la cantidad de energía eléctrica que es de 2.5 kwh. Por lo tanto ni sobra ni falta lingotes, es decir por ahora el flujo neto de material de lingotes es cero, es decir, que exactamente la cantidad que se requiere de lingotes para producir (0.05 toneladas) las 100 probetas que determina la unidad funcional, es igual, a la cantidad de lingotes que produce el proceso de producción de lingotes (0.05 toneladas). 

Teniendo en cuenta el escalamiento anterior del proceso de producción de lingotes, pasamos a escalar el proceso de electrólisis que produce el aluminio líquido para la fundición de los lingotes. El proceso de electrólisis produce en principio una tonelada de aluminio líquido pero con el esacalamiento que se hizo anteriormente, sabemos que el proceso de fundición de lingotes requiere 0.05 toneladas de aluminio, por lo que hay que multiplicar las salidas y entradas del proceso de electrólisis por un factor de escalamiento de 0.05, lo que da que ahora este proceso debe producir 0.05 toneladas de aluminio y necesita 0.09595 toneladas de alúmina, 0.023 toneladas de ánodo, 703.3 kwh de electricidad y 1 tkm de transporte por camión

Una vez hemos escalonado el proceso de producción de electrólisis, pasamos a escalar el proceso de producción de la alúmina. Para que este proceso produzca 0.09595 toneladas de alúmina, se debe multiplicar sus entradas y salidas por el factor de escalamiento de 0.047975. Por lo que este proceso va a necesitar 9.0193 kwh de electricidad, 0.2731696 toneladas de bauxita y 6.829241 tkm de transporte. Luego pasamos a escalar el proceso de la minería de la bauxita. Para que este proceso produzca 0.273168 toneladas del mineral de la bauxita que requiere el proceso de producciómn de la alúmina, debemos multiplicar sus entradas y salidas por el factor de escalamiento de 0.049667. El proceso requiere además 0.4097543 kwh de electricidad

Una vez ha sido escalonado el proceso de producción de electrólisis se sabe que se requiere en este proceso 0.23 toneladas de ánodo, por lo que debemos pasar a escalonar el proceso de producción dd ánodo. Para que este proceso produzca 0.23 toneladas de ánodo, debemos multiplicar las entradas y salidas del proceso por el factor de escalamiento de 0.0231156. Lo que daría además un consumo de energía eléxtrica de 4345.7286 kwh.

Ahora bien habiendo hecho el escalamiento anterior para los procesos allí referidos, encontramos que el total del consumo de energía para estos procesos es de: 409754.4743 kwh + 4345.7286 kwh + 0.15 Kwh +9019.3 kwh + 703 kwh +300 kwh, lo que daría un total de 424122.6529 Kwh. Para qu el proceso de producción de electricidad produzca esta cantidad total de energía eléctrica,se debe multiplicar por el factor de escalamiento de 42412.26529. Lo quedaría además un consumo de combustible de 84824.53058 litros.

Por otro lado, El total de servicios de transporte recibidos por los anteriores procesos habiendo sido escalados corresponde a 6829.24125 tkm + 1 tkm, para un total de 6830.24125 tkm. Sin Sin haber hecho escalamiento todavía, sabemos que el proceso que presta el servicio de transporte por camión tiene una salida de 1 tkm, de manera que para que este proceso preste un servicio de 6830.24125 tkm a los procesos que requieren este servcio, debemos multiplicar el proceso por el factor de escalamiento de 6830.2413, lo que daría además la necesidad de combustibe para este proceso de 47.8117 litros.

El total de combustible requerido habiendo hecho los escalonamientos anteriores es de 47.8117 litros + 84824.53058 litros, para un total de 84872.34227 litros. El proceso de producción de combustible requiere escalonarse con el factor de 848.7234227 para satisfacer la demanda de combustible anterior.

Nos hemos dado cuenta que cuando se escalona un proceso unitario, nos solo los flujos tecnológicos se ven afectados sino que también se afectan todas las demás entradas de forma proporcional, incluyendo las intervenciones ambientales. Así por ejemplo, para el caso del procceso de la minería de la bauxita y teniendo en cuenta el factor de escalamiento de 49667.209, la cantidad de dióxido de carbono que se liberaría sería de 49667.209 x 38.5, que daría como resultado 1912187.547 kg. La siguiente tabla ilustra la cantidad de cada uno de los tipos de flujos ambientales y económicos de cada proceso unitario, habiendo aplicado los factores de escalanamiento respectivos.


![Procesos unitarios escalonados con respecto a la unidad funcional](https://github.com/jrchaconcito/REPOTEST/blob/main/Imagen3.png)



### 1.4 Cálculo del modelo básico del inventario  como una solución de un sistema de ecuaciones lineales

Se observa que para el cálculo del inventario de ciclo de vida que se obtuvo anteriormente, lo que se hizo fue ir encontrando los factores de escalonamiento de cada proceso, al ir pasar de un proceso a otro. De manera que lo que era desconocido eran precisamente los factores de escalamiento, los demás datos de los procesos unitarios se conocían de antemano. Podemos entonces introducir un tratamiento más formal, partiendo que se tienen nueve (9) factores de escalamiento desconocidos. También asumimos la siguiente numeración para cada uno de los procesos unitarios del sistema:
-Proceso 1: Minería de la bauxita
-Proceso 2: Producción de alúmina
-Proceso 3: Transporte (Si bien apareece en el diagrama dos veces, se asume que es un mismo proceso el que está prestando el servicio de transporte por camión)
-Proceso 4: Electrólisis
-Proceso 5: Fundición de lingotes de aluminio
-Proceso 6: Producción del ánodo
-Proceso 7: Producción de parte de aluminio
-Proceso 8: Producción de combustible
-Proceso 9: Producción de la probeta de alumninio

Los factores de escalamiento los denotaremos como s1 que sifnifica factor de escalamiento del proceso 1, s2 factor de escalamiento del proceso 2 y de manera similar, se entenderán los demás factores s3, s4, s5, s6, s7, s8 y s9. Los flujos económicos se numneran de la siguiente manera:
-Flujo 1: Las toneladas de bauxita que produce el Proceso 1
-Flujo 2: Las toneladas de alúmina que produce el Proceso 2
-Flujo 3: tkm de servicio de transporte por camión prewstado por el Proceso 3
-Flujo 4: Las toneladas de aluminio líquido producidas por el proceso 4
-Flujo 5: Las toneladas de lingotes producidas por el proceso 5
-Flujo 6: Las 


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
