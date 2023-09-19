<div align="center"><a href="https://www.escuelaing.edu.co/es/investigacion-e-innovacion/centro-de-estudios-de-sistemas-de-gestion/" target="_blank"><img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Centro%20de%20Estudios%20en%20Sistemas%20de%20Gestio%CC%81n.jpg" alt="R.LTWB" width="100%" border="0" /></a></div>

  <div align="center">
  
  <h1>ESTRUCTURA DE CÁLCULO MATEMÁTICO PARA MODELAR EL INVENTARIO Y EL IMPACTO AMBIENTAL DEL CICLO DE VIDA DE UN PRODUCTO </h1>
  <h1>Ejercicios propuestos</h1>

 
</p>

</div>

<div align="justify">

### 1.1 Propósito de la sección
Vamos a proponerte unos ejercicios tomados de Heijungs (s.f). Esperamos puedan serte útiles para prácticar los conceptos y metodologías vistas en este curso.

### 1.2 Ejercicios

### Ejercicio 1

Con base en el diagrama que se muestra a continuación y la tabla sobre los datos de cada uno de los procesos, indique lo siguiente:</p>
-Matriz A</p>
-Matriz B</p>
-Vector de demanda f</p>
-Vector de inventario g</p>

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen5.png" alt="Ecuación de balance" width=50%>
</div>



![Diagrama de ciclo de vida para la producción de una probeta de aluminio](https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/DIAGRAMA%20CV_Imagen%201.png)

![Datos de los procesos untarios](https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/IMAGEN2_DATOS.png)

### 1.3 Modelo básico de inventario: La solución matemática con escalamiento secuencial

Para poder entender más adelante la lógica de la estructura cálculo del inventario basada en el uso del álgebra lineal y que al respecto el referente más importante sigue siendo el libro de  Heijungs & Suh (2002), vamos a comenzar calculando el inventario, cnn el método denominado **secuencial** y en que en este curso algunas veces tambén denominamos como el **método manual** . Lo primero que observamos es que la cantidad de probeta que produce el proceso unitario denominado "producción de la parte de aluminio" no coincide con la cantidad de probetas que le vamos a demandar que es de 100 unidades que están determinadas en la unidad funcional. Por lo tanto, debemos escalar este proceso para que produzca 100 probetas, por lo que debemos multiplicar por 100 la salida de ese proceo para que nos dé las 100 unidades que le estamos demandando al sistema. 

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

Se observa que para el cálculo del inventario de ciclo de vida que se obtuvo anteriormente, lo que se hizo fue ir encontrando los factores de escalonamiento de cada proceso, al ir pasar de un proceso a otro (por eso se denomina método secuencial). De manera que lo que era desconocido eran precisamente los factores de escalamiento, los demás datos de los procesos unitarios se conocían de antemano. Podemos entonces introducir un tratamiento más formal, partiendo que se tienen nueve (9) factores de escalamiento desconocidos. También asumimos la siguiente numeración para cada uno de los procesos unitarios del sistema:


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



  
Los factores de escalamiento los denotaremos como s₁ que significa factor de escalamiento del proceso 1, s₂ factor de escalamiento del proceso 2 y de manera similar, se entenderán los demás factores de escalamiento. Por otro lado, los flujos económicos se numeran de la siguiente manera:

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




Con la representación del conjunto de ecuaciones que aparece más abajo, a₁₁s₁ significa el flujo económico 1 del proceso 1 multiplicado por el factor de escalamiento del proceso 1; a₁₂s₂ significa el flujo económico 1 en el proceso 2 multiplicado por el factor de escalamiento del proceso 2, los demás elementos del lado izquierdo de la ecuación se interpretarían de manera similar a como se ha hecho aquí. f₁ sería el total del flujo económico 1 y así para sería su interpretación para el total de los demás flujos económicos.

Abajo también aparece un ejemplo concreto teniendo en cuenta que por convención se utilizará el signo menos si es una entrada y el signo + si es una salida, esto para garantizar que no debe sobrar de un flujo económico cuando se está haciendo el escalamiento, es decir, que lo que produce un proceso es la cantidad exacta de lo que necesita otro proceso, no debe sobrar ni faltar flujo.




Cuando hacemos f₁ igual a cero, significa que toneladas de bauxita no deben sobrar, por que cuando escalamos, la cantidad de bauxita que debe producir el proceso de la minería de la bauxita (proceso 1) debe ser exactamente igual a la cantidad de bauxita que necesita el proceso de producción de alúmina (proceso 2). Así que el uso de signos ("–" para las entradas y el "+" para las salidas, nos va a permitir balancear la ecuación para  hacer f₁ igual a cero (no sobre ni falte el flujo económico 1). Ahora bien, la ecuación 2 por sí sola no nos permite despejar o solucionarla para s1 y s2 por lo que vamos a necesitar completar el conjunto de ecuaciones para hallar las incógnitas que son los factores de escalamiento, así que para una mejor comprensión indiquemos cuáles serían las ecuaciones en su totalidad:


<p align="center">
<img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen4.png" alt="Sistema de ecuaciones" width="700" height="350" />
</p>

Como se puede observar en el conjunto de ecuaciones simultáneas, lo que allí se está expresando es que el sistema producto está balanceado escalando cada proceso unitario con factores de escalamiento, que son las variables desconocidas. No olvidar que solo se está empleando los flujos económicos para hallar los factores de escalamiento desconocidos. Vemos entonces que tenemmos un conjunto de ecuaciones determinado, por que el número de ecuaciones (nueve ecuaciones) es igual al número de variables desconocidas (nueve variables desconocidas). Más abajo ilustramos con los datos del ejercicio hipótético cuál es el conjunto de ecuaciones. Óbsérvese que el lado de derecho de las ecuaciones todos los valores son iguales a cero, excepto para el total del flujo económico 7 que corresponde a un valor de 100 que es el flujo de referencia derivado de la unidad funcional (en este caso la unidad funcional y el flujo de referncia tienen los mismos valores, pero no siempre es así). Esto significa que de todos los otros flujos no deben sobrar ni faltar (esto matemáticamente se expresa con el valor cero) y para el caso del flujo económico 7, el total debe dar 100 que es la cantidad total que le estamos demandando producir al sistema producto, que de acuerdo con los datos del ejercicio es cien (100) probetas de aluminio. Así que una vez hallados los 9 factores de escalamiento (los mismos que aparecen anteriormente en la tabla sobre los datos de los procesos escalonados), podemos saber cuáles son las cantidades de entradas y salidas de cada proceso en términos de flujos económicos (en este caso denominados flujos de referencia) que satisfacen la unidad funcional especificada para el estudio de análisis de ciclo de vida. 

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen7png.png" alt="Ecuación de balance" width=60%>
</div>

Seguidamente vamos a ver los factores de escalamiento a partir de la solución del conjunto de ecuaciones simultáneas que como se puede observar son los mismos que se hallaron cuando se hizo el escalamiento "manual".

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen8.png" alt="Ecuación de balance" width=15%>
</div>

Una vez hallados los factores de escalamiento podemos construir un conjunto de ecuaciones para determinar el inventario de ciclo de vida, las cuales no es necesario resolver porque dado que utilizan los factores de escalamiento que previamente se han encontrado al resolver el conjunto anterior de ecuaciones simultáneas. Para ellos partimos de las siguientes convenciones:

b<sub>1  = Flujo ambiental 1 (Kg de dióxido de carbono, CO<sub>2)

b<sub>2  = Flujo ambiental 2 (Kg de metano, CH<sub>4)

b<sub>3  = Flujo ambiental 3 (dióxido de azufrem SO<sub>2)

b<sub>4  = Flujo ambiental 4 (Óxido nitroso, N<sub>2</sub>O)

b<sub>5  = Flujo ambiental 5 (mineral de bauxita)

b<sub>6  = Flujo ambiental 6 (petróleo) crudo

b<sub>11 = Flujo ambiental 1 en el proceso 1

b<sub>12 = Flujo ambiental 1 en el proceso 2

... b<sub>19 = Flujo ambiental 1 en el proces 9, 

g<sub>1 = el total del flujo 1 que satisface la unidad funcional

g<sub>2 = el total del flujo 2 que satisface la unidad funcional

...g<sub>6 el total del flujo 6 que satisface la unidad funcional

A continuación veamos cuál es el conjunto de ecuaciones:

He aquí el conjunto ecuaciones que con los factores de escalamiento ofrece la clave directa para la solución final del inventario. No olvidar que el escalonamiento de un proceso unitario afecta tanto a los flujos económicos como a los flujos ambientales.

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen9.png" alt="Ecuación de balance" width=60%>
</div>

Ahora bien, veamos cómo sería el conjunto de ecuaciones anterior pero con las cantidades de cada uno de los tipos de flujo ambiental.


 <div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen10.png" alt="Ecuación de balance" width=100%>
</div>

 
### 1.5 Modelo básico de inventario basado en álgebra matricial

El uso de álgebra lineal y matrices para resolver ecuaciones simultáneas (como las referidas anteriormente) es una elección sólida debido a su eficiencia, precisión, escalabilidad y aplicabilidad general, así como a las herramientas disponibles que facilitan su implementación (ejemplo excel, Matlab, entre otros). Esta metodología es esencial en una amplia gama de campos y garantiza resultados más confiables y rápidos en comparación con los métodos manuales o tradicionales. Así que vamos a aprender cómo cálcular el inventario de ciclo de vida utilizando algebra matricial. A continuación la solución para hallar los factores de escalamiento empleando una solución matricial para el conjunto de ecuaciones simultáneas:

 <div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen11.png" alt="Ecuación de balance" width=50%>
</div>

Ahora bien, la matriz que contiene los flujos tecnológicos la denominaremos con la letra **A**, el vector donde aparecen los factores de escalamiento con la letra **s** y el vector donde aparece la demanda final con la letra **f**.
De manera que empleando las anteriores convenciones, podemos establecer de manera generalizada un tratamiento en términos de una solución matricial empleando la relación que se muestra a continuación, done **A* siempre deberá ser cuadrada y ser invertible (tener inversa), si no  se cumplen estas dos condiciones, la estructura básica para calcular el inventario con procesos monofuncionales no se puede llevar a cabo. Una manera práctica para determinar si la matriz **A** es no singular (es decir tiene inversa) es averiguar su determinante y si este valor es distinto de cero, estamos ante una matriz invertible.

<p align="center"><strong>A</strong><strong>s</strong> = <strong>f</strong></p>

De la expresión algebraica anterior (matricialmente hablando),  la matriz **A** se conoce, lo mismo que el vector de demand **f** , por lo que para encontrar los factores de escalamiento, debemos despejar **s**, quedaría como resultado el siguiente:

<p align="center"><strong>s</strong> = <strong>A<sup>-1</sup></strong><strong>f</strong></p>

Donde **A<sup>-1</sup>** es la matriz inversa de la matriz de tecnología **A**, para el ejemplo que estamos tratando sería lo siguiente (solo lo que aparece entre corchetes corresponde a las matrices, lo demás se ofrece a modo de ilustración para comprender mejor la construcción de las matrices):

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen12.png" width=70%>
</div>

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen13.png" width=70%>
</div>

<br>
<p>
Haciendo la multiplicación correspondiente se tendría el siguiente resultado para <strong>s</strong> = <strong>A<sup>-1</sup></strong><strong>f</strong>:</p>


<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen14.png" width=90%><p>
</div>

Habiendo hallado los factores de escalamiento pasamos a resolver el problema del inventario de ciclo de vida. No olvidar como lo referíamos anteriormente, que el factor de escalamiento afecta a todas las entradas y salidas de cada proceso unitario, Así que veamos cómo se vería el resulado desde el punto de vista matricial, teniendo en cuenta que la letra **B** denota la matriz de intervención ambiental, **g** es el vector de inventario y que el inventario se obtendría mediante la ecuación matricial que aparece más abajo. En el cuadro que aparece más abajo, se ha indicado el nombre de los flujos ambientales y el nombre de los procesos unitarios para ayudar en la comprensión de la construcción de la relación matricial respectiva.

<div align="center"><strong>B</strong>s</div><p>

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen15.png" width=150%><p>
</div>

Teniendo en cuenta las relaciones matriciales anteriormenrte y sabiendo que la multiplicación de matrices también es una operación asociativa, podemos entonces determinar la fórmula para calcular el vector de inventario **g**:

<p align="center"><strong>g = (BA<sup>-1</sup>)f</strong></p>


</div>

<div align="center">
   
   <a href="https://enlace-academico.escuelaing.edu.co/psc/FORMULARIO/EMPLOYEE/SA/c/EC_LOCALIZACION_RE.LC_FRM_ADMEDCO_FL.GBL" target="_blank"><img src="https://github.com/MaterialsCompTools/DRX-MaterialesCristalinos/blob/main/.graph/Logo%20Obtener%20certificado%20PNG.png" alt="R.LTWB" width="260" border="0" /></a>

</div>

