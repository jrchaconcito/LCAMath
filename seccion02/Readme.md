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

Una vez hemos escalonado el proceso de producción de electrólisis, pasamos a escalar el proceso de producción de la alúmina. Para que este proceso produzca 0.09595 toneladas de alúmina, se debe multiplicar sus entradas y salidas por el factor de escalamiento de 0.047975. Por lo que este proceso va a necesitar 9.0193 kwh de electricidad, 0.2731696 toneladas de bauxita y 6.829241 tkm de transporte. Luego pasamos a escalar el proceso de la minería de la bauxita. Para que este proceso produzca 0.273168 toneladas del mineral de la bauxita que requiere el proceso de producciómn de la alúmina, debemos multiplicar sus entradas y salidas por el factor de escalamiento de 0.049667. El proceso requiere además 0.4097543 kwh de electricidad.

Una vez ha sido escalonado el proceso de producción de electrólisis se sabe que se requiere en este proceso 0.023 toneladas de ánodo, por lo que debemos pasar a escalonar el proceso de producción dd ánodo. Para que este proceso produzca 0.023 toneladas de ánodo, debemos multiplicar las entradas y salidas del proceso por el factor de escalamiento de 0.0231156. Lo que daría además un consumo de energía eléxtrica de 4.3456 kwh.

Ahora bien habiendo hecho el escalamiento anterior para los procesos allí referidos, encontramos que el total del consumo de energía para estos procesos es de: 0.409754 kwh + 4.3456 kwh + 2.65 kwh +9.0193 kwh + 703.3 kwh +300 kwh, lo que daría un total de 1019.7136 Kwh. Para qu el proceso de producción de electricidad produzca esta cantidad total de energía eléctrica,se debe multiplicar por el factor de escalamiento de 101.972478. Lo quedaría además un consumo de combustible de 203.944956 litros.

Por otro lado, El total de servicios de transporte recibidos por los anteriores procesos habiendo sido escalados corresponde a 6.82924 tkm + 1 tkm, para un total de 7.82924 tkm. Sin haber hecho escalamiento todavía, sabemos que el proceso que presta el servicio de transporte por camión tiene una salida de 1 tkm, de manera que para que este proceso preste un servicio de 7.82924 tkm a los procesos que requieren este servcio, debemos multiplicar el proceso por el factor de escalamiento de 7.829241, lo que daría además la necesidad de combustibe para este proceso de 47.8117 litros.

El total de combustible requerido habiendo hecho los escalonamientos anteriores es de 0.0548 litros + 203.944956 litros, para un total de 203.99976 litros. El proceso de producción de combustible requiere escalonarse con el factor de 2.039997 para satisfacer la demanda de combustible anterior.

Nos hemos dado cuenta que cuando se escalona un proceso unitario, no solo los flujos tecnológicos se ven afectados sino que también se afectan todas las demás entradas de forma proporcional, incluyendo las intervenciones ambientales. Así por ejemplo, para el caso del procceso de la minería de la bauxita y teniendo en cuenta el factor de escalamiento de 0.049667, la cantidad de dióxido de carbono que se liberaría sería de 49667.209 x 38.5, que daría como resultado 1912187.547 kg. La siguiente tabla ilustra la cantidad de cada uno de los tipos de flujos ambientales y económicos de cada proceso unitario, habiendo aplicado los factores de escalanamiento respectivos.


![Procesos unitarios escalonados con respecto a la unidad funcional](https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen3.png)

### 1.4 Cálculo del modelo básico del inventario como una solución de un sistema de ecuaciones lineales

Se observa que para el cálculo del inventario de ciclo de vida que se obtuvo anteriormente, lo que se hizo fue ir encontrando los factores de escalonamiento de cada proceso, al ir pasar de un proceso a otro. De manera que lo que era desconocido eran precisamente los factores de escalamiento, los demás datos de los procesos unitarios se conocían de antemano. Podemos entonces introducir un tratamiento más formal, partiendo que se tienen nueve (9) factores de escalamiento desconocidos. También asumimos la siguiente numeración para cada uno de los procesos unitarios del sistema:


Se observa que para el cálculo del inventario de ciclo de vida que se obtuvo anteriormente, lo que se hizo fue ir encontrando los factores de escalonamiento de cada proceso, al ir pasar 
de un proceso a otro. De manera que lo que era desconocido eran precisamente los factores de escalamiento, los demás datos de los procesos unitarios se conocían de antemano. 

<p align="center">




Podemos entonces introducir un tratamiento más formal, partiendo que se tienen nueve (9) factores de escalamiento desconocidos. También asumimos la siguiente numeración para cada uno de los procesos unitarios del sistema:

  - Proceso 1: Minería de la bauxita
  - Proceso 2: Producción de alúmina
  - Proceso 3: Transporte (Si bien aparece en el diagrama dos veces, se asume que es un mismo proceso el que está prestando el servicio de transporte por camión)
  - Proceso 4: Electrólisis
  - Proceso 5: Fundición de lingotes de aluminio
  - Proceso 6: Producción del ánodo
  - Proceso 7: Producción de parte de aluminio
  - Proceso 8: Producción de combustible
  - Proceso 9: Producción de energía eléctrica
</p>

<p align="center">



  
Los factores de escalamiento los denotaremos como s₁ que significa factor de escalamiento del proceso 1, s₂ factor de escalamiento del proceso 2 y de manera similar, se entenderán los demás factores de escalamiento. Por otro lado, los flujos económicos se numneran de la siguiente manera:

  -  Flujo económico 1: toneladas de bauxita que produce el Proceso 1
  -  Flujo económico 2: toneladas de alúmina que produce el Proceso 2
  -  Flujo económico 3: tkm de servicio de transporte por camión prestado por el Proceso 3
  -  Flujo económico 4: toneladas de aluminio líquido producidas por el proceso 4
  -  Flujo económico 5: toneladas de lingotes producidas por el proceso 5
  -  Flujo económico 6: toneladas de ánodo producidas por el proceso 6
  -  Flujo económico 7: unidades de probetas de aluminio producidas por el proceso 7
  -  Flujo económico 8: litros de combustible producidos por el proceso 8
  -  Flujo económico 9: kwh de energía eléctrica producida por el proceso 9
  </p>

Para el primer flujo económico, toneladas de bauxita, se puede establecer la siguiente ecuación de balance:

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen5.png" alt="Ecuación de balance" width=50%>
</div>




Donde a₁₁s₁ significa el flujo económico 1 del proceso 1 multiplicado por el factor de escalamiento del proceso 1; a₁₂s₂ significa el flujo económico 1 en el proceso 2 multiplicado por el factor de escalamiento del proceso 2, los demás elementos del lado izquierdo de la ecuación se interpretarían de manera similar a como se ha hecho aquí. f₁ sería el total del flujo económico 1 y así para sería su interpretación para el total de los demás flujos económicos.

Veámolo con un ejemplo concreto teniendo en cuenta que por convención se utilizará el signo menos si es una entrada y el signo + si es una salida, esto para garantizar que no debe sobrar de un flujo económico cuando se está haciendo el escalamiento, es decir, que lo que produce un proceso es la cantidad exacta de lo que necesita otro proceso, no debe sobrar ni faltar flujo.

"<div align="center">
5.5s₁ - 5.694s₂ + 0s₃ + 0s₄ + 0s₅ + 0s₆ + 0s₇ + 0s₈ + 0s₉ = 0
</div

Cuando hacemos f₁ igual a cero, significa que toneladas de bauxita no debe sobrar, por que cuando escalamos, la cantidad de bauxita que debe producir el proceso de la minería de la bauxita (proceso 1) debe ser exactamente igual a la cantidad de bauxita que necesita el proceso de producción de alúmina (proceso 2). Así que el uso de signos ("–" para las entradas y el "+" para las salidas, nos va a permitir balancear la ecuación para  hacer f₁ igual a cero (no sobre ni falte el flujo económico 1). Ahora bien, la ecuación 2 por sí sola no nos permite despejar o solucionarla para s1 y s2 por lo que vamos a necesitar completar el conjunto de ecuaciones para hallar las incógnitas que son los factores de escalamiento, así que para una mejor comprensión indiquemos cuáles serían las ecuaciones en su totalidad:


<p align="center">
<img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen4.png" alt="Sistema de ecuaciones" width="700" height="350" />
</p>

Como se puede observar en el conjunto de ecuaciones simultáneas, lo que allí se está expresando es que el sistema producto está balanceado escalando cada proceso unitario con factores de escalamiento, que son las variables desconocidas. No olvidar que solo se está empleando los flujos económicos para hallar los factores de escalamiento desconocidos. Vemos entonces que tenemmos un conjunto de ecuaciones determinado, por que el número de ecuaciones (nueve ecuaciones) es igual al número de variables desconocidas (nueve variables desconocidas). A continuación ilustramos con los datos del ejercicio hipótético cuál es el conjunto de ecuaciones.

 
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
