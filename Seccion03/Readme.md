<div align="center"><a href="https://www.escuelaing.edu.co/es/investigacion-e-innovacion/centro-de-estudios-de-sistemas-de-gestion/" target="_blank"><img src="../.graph/Centro%20de%20Estudios%20en%20Sistemas%20de%20Gestio%CC%81n.jpg" alt="R.LTWB" width="100%" border="0" /></a></div>

  <div align="center">
  
  <h1>ESTRUCTURA DE CÁLCULO MATEMÁTICO PARA MODELAR EL INVENTARIO Y EL IMPACTO AMBIENTAL DEL CICLO DE VIDA DE UN PRODUCTO </h1>
  <h1>SECCIÓN 3</h1>

  <h2>ESTRUCTURA AMPLIADA DEL CÁLCULO MATEMÁTICO PARA EL MODELO DE INVENTARIO</h2>
</p>

</div>

<div align="justify">

### 1.1 Propósito de la sección
Aprenderás cómo es la estructura de cálculo matemático para determinar el inventario de ciclo de vida cuando la matriz no es cuadrada.

### 1.2 Modelo de inventario: Sistemas incompletos


Cuando se están llevando a cabo estudios de análisis de ciclo de vida, es común que existan dificultades en la obtención de los datos para el inventario (se vuelve costoso recolectar la información, no se tiene el tiempo o simplemente se hace muy difícil tener el dato apropiado), por ejemplo, sabemos que en un determinado proceso unitario entra una determinada cantidad de flujo económico pero pero no tenemos información sobre el proceso que produjo dicha entrada tecnológica. Este caso se denomina **sistemas incompletos** (otras veces se denomina corte de flujos económicos) y corresponde a aquellos casos donde no se ha incluido los procesos unitarios para la producción de un determinado flujo económico que hemos incluido en la matriz de procesos y/o no se ha incluido tampoco los procesos unitarios encargados de recibir o tratar un flujo económico que se ha incluido en la matriz de procesos. Por lo anterior, es obvio que la ecuación fundamental **As = f** no se puede solucionar para **s**, por cuanto no podemos tener la inversa de una matriz que es rectangular, es decir que no es cuadrada. Así que para lograr una solución, se han propuesto algunos "trucos matemáticos" que explicaremos a continuación.

* Incorporación de procesos ficticios
* Eliminar de la matriz de tecnología **A** los flujos económicos de demás y que no tiene asociado un proceso unitario que los haya producido o que posteriormente los trate o los reciba o absorba.

Veamos cómo sería la inclusión de procesos ficticios. Asumamos la siguiente matriz tecnológica teniendo en cuenta que asumimos que la electrólisis  y la producción de ánodo requiere 5 Kg de acero y 2 Kg de acero, respectivamente y que además la producción de la probeta de aluminio necesita 0,0001 Kg de solvente. Así que en principio la matriz de tecnología sería la siguiente:


![Diagrama de ciclo de vida para la producción de una probeta de aluminio](../.graph/Imagen16.png)<p>

Ahora vamos a "cuadrar" la matriz de tecnología **A**, adicionando procesos ficticios. Como existe el flujo económico "Kg de acero", incorporamos en la matriz **A**, un proceso ficticio que se asume fue el que produjo los kg de acero que requiere los procesos de electrólisis y de producción de ánodo y otro que se asume fue el que produjo los Kg de solvente que se utilizan en el proceso de producción de la probeta de aluminio.  Como se puede ver a continuación, el proceso ficticio solo tiene el número 1 y las demás dimensiones son cero, tanto en la matriz **A** como en la matriz de intervención ambiental **B**. Obsérvese que los "unos" son con signo "+", por cuanto se asume que si un proceso está necesitando (necesitando significa una entrada y por lo tanto se indica con signo "menos") acero o solvente, entonces otro proceso (ficticio para nuestro caso) debió producir cada uno de estos flujos (producir significa una salida, y por lo tanto se indica con signo "+". Una vez hemos incorporado los procesos ficticios, vemos que ahora la matriz **A** es cuadrada e invertible, veamos como luciría:

![Diagrama de ciclo de vida para la producción de una probeta de aluminio](../.graph/Imagen20.png)<p>

El vector de demanda sería el siguiente:


<div align="center">
  <img src="../.graph/Imagen19.png" alt="Ecuación de balance" width=30%><p>
</div>

La inversa de la anterior matriz sería la siguiente:

![Diagrama de ciclo de vida para la producción de una probeta de aluminio](../.graph/Imagen17.png)<p>

El vector **s** de factores de escalamiento sería el siguiente:

<div align="center">
  <img src="../.graph/Imagen21.png" alt="Ecuación de balance" width=30%><p>
</div>

La matriz de intervención ambiental sería la siguiente:

![Diagrama de ciclo de vida para la producción de una probeta de aluminio](../.graph/Imagen18.png)<p>

Y finalmente el resultado del modelo de inventario que era a donde queríamos llegar aplicando las relaciones matriciales vistas anteriormente:

<div align="center">
  <img src="../.graph/Imagen22.png" alt="Ecuación de balance" width=30%><p>
</div>

Ahora bien, otra forma de tratar los sistemas incompletos es remover los flujos económicos para los cuales en la matriz de procesos no se tienen los procesos unitarios que los haya producido o absorbido. La matriz **A* sería la siguiente resaltando los flujos que habría que remover:


<div align="center">
  <img src="../.graph/Imagen23.png" alt="Ecuación de balance" width=80%><p>
</div>

Una vez se han removido estos flujos económicos, encontramos que la matriz **A** es cuadrada e invertible y por lo tanto podemos aplicar la estructura de cálculo matricial vista anteriormenre para hallar el inventario de ciclo de vida.


### 1.3 Modelo de inventario: Procesos multifuncionales

Es común que los sistemas industriales produzcan más de un flujo económico. Pot ejemplo, una refinería produce diferentes tipos de combustibles o una empresa de lácteos produce diferentes tipos de productos (quesos, leche, etc.) o un matadero genere carne, cuero, vísceras, etc. que se venden en el mercado. Así que un proceso que tiene más de una función o presta más de un servicio se denomina **proceso multifuncional**. Las siguientes son categorías de procesos multifuncionales:

   - Un proceso unitario que produce más de una salida valiosa, es decir **coproductos**, se generan inevitablemente por la misma naturaleza del proceso productivo. por ejemplo, en la       producción de combustibles, invevitablemente se producen en ese proceso petroquímico diferentes tipos de combustibles a la vez.
   - Procesos unitarios que tratan dos o más residuos, por ejemplo, un incinerador para el tratamiento de residuos, le entra y trata residuos de cartón, plástico, papel, etc.
   - Procesos unitarios que tratan un tipo de residuo y producen una salida valiosa. Por ejemplo, una planta le entra residuos de papel (recicla este tipo de residuo) y los convierte en 
    cartón corrugado
   - Procesos unitarios que deliberadamenrte se les asigna más de una función o servicio. Por ejemplo, el transporte de pasajeros en un avión pero que al mismo tiempo en el mismo avión se 
    transporta carga o mercancías
    </p>

Otro asunto que amerita resaltarse es que con los procesos multifuncionales se tiene un problema denominado el problema de la asignación. Cuando un proceso unitario, por ejemplo, produce un bien en madera, se genera un coproducto que es el aserrín, este último material es un coproducto que se puede vender por ejemplo a las empresas que producen alimentos cárnicos para que allí lo utilicen por ejemplo para la preparación del jamón ahumado o con destino a otras empresas que producen muebles a base de compuestos aglomerados. Ahora bien, si estamos haciendo un estudio de análisis de ciclo de vida, por ejemplo, de un sistema producto hecho a base de madera, en principio no sabemos cuál es la carga ambiental que debemos asignarle al producto o bien en madera y cuál es la carga ambiental que debemos asignarle al coproducto. Por lo tanto debemos solucionar este problema y para ello existen diferentes enfoques metodológicos que son los que vamos a explicar a continuación.

  -**Método de substitución**

Para hacer mejor la explicación, partamos del siguiente ejemplo: asumamos que el proceso de producción del ánodo genera residuos de acero y que estos residuos de acero los recoge una empresa  que los utiliza para hacer envases. Veamos cómo sería el diagrama de flujo del ciclo de vida con la incorporación del coproducto que corresponde a la generaciónd de residuos de acero en una cantidad de 4.7 kilogramos y donde se observa que la matriz no es cuadrada y que de las cargas ambientales (ver matriz intervención ambiental que se mostró anteriormente) del proceso de producción del ánodo, no sabemos cuántas de ellas se las asignamos al flujo en toneladas de ánodo y cuántas al flujo en kilogramos de acero residual. A continuación se muestra el nuevo diagrama de ciclo de vida. Es importante anotar que este residuo de acero como coproducto, indica que es valioso para otra empresa, por ejemplo, para utlizarlo como materia prima. Cuando hablamos "para otra empresa" significa que el residuo puede ir a otro sistema producto diferente al sistema producto donde se está generando este tipo de residuo, esto se conoce como **reciclaje de bucle abierto**. A continuación se ilustra cómo sería el diagrama de ciclo de vida incorporando el coproducto y la **matriz A** que como se ve no es cuadrada:

<div align="center">
  <img src="../.graph/Imagen28.png" alt="Ecuación de balance" width=80%><p>
</div>

<div align="center">
  <img src="../.graph/Imagen54.png" alt="Ecuación de balance" width=100%><p>
</div>


El **método de substitución** consiste en encontrar  un proceso unitario (ya sea en la literatura técnica o especializada o en la realidad o bases de datos especializadas) que tenga como función o servicio principal la producción del coproducto (acero) o un material que sea equivalente o cumpla funciones similares al material de acero. Lo que sucede es que cuando se encuentra este proceso, lo que está pasando es que al incorporar este nuevo proceso a la **matriz A**, la información de entradas y salidas que tiene este proceso se restan de las entradas y salidas del proceso donde se está produciendo el coproducto (desde luego esta "resta" se hace con base en la aplicación de factores de escalonamiento, operación que se realiza cuando aplicamos el modelo básico del cálculo de inventario visto anteriormente). Veamos entonces cómo sería la  aplicación de esta técnica o truco "matemático" para solucionar el problema de la asignación y al mismo tiempo convertir la  **matriz A** en una matriz cuadrada e invertible. 

Asumamos que hemos encontrado un proceso unitario cuya función principal es producir acero. Veamos entonces cómo sería la **matriz A** con la incorporación de este nuevo proceso:

<div align="center">
  <img src="../.graph/Imagen55.png" alt="Ecuación de balanc" width=130%><p>
</div>

La anterior matriz podemos volverla "cuadrada" buscando una equivalencia o inequivalencia entre los dos tipos de acero, si asumimos que los dos tipos de flujos en cuanto a su calidad es la misma (por ejemplo, porque tanto los residuos de acero (coproducto) como el acero virgen producido por el nuevo proceso unitario que se incorporó al sistema, sus propiedades inherentes no cambian, entonces los dos flujos es una misma cosa (indistinguibles por así decirlo) y por lo tanto las dos nuevas filas se pueden fusionar en una sola fila:

<div align="center">
  <img src="../.graph/Imagen56.png" alt="Ecuación de balanc" width=130%><p>
</div>

Por otro lado, este proceso unitario de producción de acero emite 28.28 Kg de CO<sub>2</sub>, 0.00575 Kg de SO<sub>2</sub> y 0.00384 Kg de N<sub>2</sub>O y produced 947 kilogramos de acero virgen. Veamos entonces cómo quedarían el **vector de demanda f**, **la matriz inversa de A**, el **vector de factores de escalamiento s**, la **matriz de intervención ambiental B**y el **vector de inventario g**, al incorporar este nuevo proceso al sistema (por eso también se le conoce como la técnica de expansión del sistema, porque se está incorporando un nuevo proceso al sistema industrial):

<div align="center">
  <img src="../.graph/Imagen58.png" alt="Ecuación de balance" width=15%><p>
</div>


<div align="center">
  <img src="../.graph/Imagen57.png" alt="Ecuación de balance" width=120%><p>
</div>

<div align="center">
  <img src="../.graph/Imagen60.png" alt="Ecuación de balance" width=120%><p>
</div>

<div align="center">
  <img src="../.graph/Imagen61.png" alt="Ecuación de balance" width=30%><p>
</div>

<div align="center">
  <img src="../.graph/Imagen62.png" alt="Ecuación de balance" width=30%><p>
</div>



 -**Algunas consideraciones adicionales sobre el método de substitución**

 Teniendo en cuenta las indicaciones dadas por Heijungs % Suh (2002), a continuación las siguientes consideraciones sobre el método de sustitución:

- El factor de escalamiento para el proceso unitario que produce como servicio principal el acero tiene signo negativo. Esto se interpreta que ese proceso unitario se resta del sistema, por esos este factor de escalamiento es negativo. Generalmente el proceso de producción de acero o cualquier otro proceso unitario que se haya incorporado para aplicar la técnica de sustitución, tendrá un factor de escalamiento más pequeño que el que podría tener en el sistema original con el producto respectivo.  Por otro lado, en general cuando se incorpora el nuevo proceso unitario al sistema, todas las intervenciones ambientales pueden permanecer inalteradas, porque el nuevo proceso unitario realmente no tiene un rol o participación en el sistema o si la tiene, su participación en el ciclo de vida es marginal o menor y eso hace que su involucramiento se de un alcance restringido.
- Otro problema con la técnica de sustitución, es que puede haber dificultades en encontrar el nuevo proceso unitario o concluir que no existe tal proceso.
- Suele pasar que la incorporación del nuevo proceso unitario, su flujo económico puede sustituir el coproducto del sistema, aún cuando los dos flujos no sean exactamente de la misma naturaleza. Por ejemplo, el acero producido como producto tiene una calidad X (por ejemplo,por razones de que es más fácil de conseguir en determinada instalación o por el contrario difícil de conseguir o porque tiene impurezas), mientras que el nuevo proceso unitario produce un acero de calidad Y (por ejemplo, sus propiedades son relativamente diferentes al coprooducto).
- También puede suceder que el nuevo proceso unitario (llamemolo PN) también tenga coproductos, en este caso sería necesario incorporar otro proceso unitario al sistema para contabilizar el coproducto del proceso unitario PN.
 

 -**Método de partición**

 Otra técnica o "truco matemático" para hacer que la matriz A tenga inversa (sea invertible) es el denominado **método de partición**. Este método consiste primero en dividir el proceso unitario multifuncional en procesos monofuncionales independientes, por eso a esta técnica se le denomina el método de la partición. El objetivo principal es distribuir equitativamente las cargas ambientales (recursos y emisiones), entre el producto principal (servicio principal del proceso unitario) y los coproductos. Para este proopósito es práctica generalizada que esta asignación se haga sobre la base de la **asignación basada en unidades físicas (masa, volumen, energía)** y **asignación económica**.  Veamos entonces cómo se aplicaría este método empleando como base unidades físicas de masa para hallar los respectivos **factores de asignación**:

  -  **Dibujar el proceso multifuncional mediante una caja con todas sus entradas y salidas**
 La mejor manera de ver esto es con los siguientes diagramas donde aparece primero el proceso unitario multifuncional y luego los procesos monofuncionales y donde see indica el cálculo de los factores de asignación determinados a partir de unidades físicas. Es importante que cuando se hace la partición en procesos monofuncionales, se tiene una caja con la salida del producto principal (Kg de ánodo) y otra caja con la salida del coproducto (Kg residuos de acero). Los valores para estas salidas no deben sufrir ninguna alteración o cambio, las demás entradas (recursos) y salidas ambientales de cada uno de estos procesos monofuncionales van a tener que ser modificados cuando se les aplique los factores de asignación. La asignaación basada en masa es la siguiente: En el proceso monofuncional para la salida de los Kg de ánodo, sale un total de una tonelada de ánodo y para el proceso monofuncional donde se produce el coproducto, sale un total de 5 kilogramos de acero residual. Sumamos estas dos cantidades, lo que daría un total de 1005 kilogramos. Luego se halla para el proceso que produce el ánodo, la proporción en que participa el total en Kg de ánodo con respecto a este total, es decir 1000 Kg/1005 Kg = 0.9950. Este sería el factor de asignación para el proceso de producción de ánodo. De igual forma, calculo la proporción de producción de acero residual con respecto al mismo total anterior, lo cual daría 5/1005 = 0.005, que sería el factor de asignación para la producción de acero residual. Importante señalar que la suma de los factores de asignación siempre deber ser igual a 1. Luego multiplico en cada uno de los procesos monofuncionales, sus otras entradas y salidas por el respectivo factor de asignación como se observa en la figura que aparece más abajo.



  -  **Partir el proceso multifuncional en procesos monofuncionales**

 <div align="center">
  <img src="../.graph/Imagen63.png" width=90%><p>
</div></p>


Una vez se ha hecho la partición anterior que se muestra en la imagen, se procede a ingresar esta información a la **matriz A** (eliminando el proceso multifuncional e ingresando la información de entradas y salidas de los dos procesos monofuncionales), veamos entonces cómo quedaría la **matriz A**, **la matriz B**, **el vector de demanda f**, **el vector de escalamiento s** y **el vector de inventario g**:



 <div align="center">
  <img src="../.graph/Imagen65.png" width=30%><p>
</div></p>

 <div align="center">
  <img src="../.graph/Imagen67.png" width=100%><p>
</div></p>




 <div align="center">
  <img src="../.graph/Imagen66.png" width=100%><p>
</div></p>

 <div align="center">
  <img src="../.graph/Imagen68.png" width=100%><p>
</div></p>

 <div align="center">
  <img src="../.graph/Imagen69.png" width=20%><p>
</div></p>

 <div align="center">
  <img src="../.graph/Imagen70.png" width=20%><p>
</div></p>



A continuación vamos explicar cómo sería la determinación de los factores de asignación con base en valor económico. La aplicación de este criterio tiene en cuenta el precio en el mercado tanto del ánodo como del acero residual que son las dos salidas del proceso multifuncional. Para comenzar asumamos que tenemos la siguiente información:

| Material              | Cantidad | Unidad  | Precio venta por Unidad | Total ingreso por venta del material/producto |
|-----------------------|----------|---------|-------------------|----------------------------------------------|
| Ánodo                 | 1000     | Kg      | US$ 2/Kg          | U$ 2000.00                                      |
| Residuos de acero     | 5.17     | Kg      | US$ 0.30/Kg       | US$ 1.551                                      |
| Total venta           |          |         |                   | US$ 2000.551

Teniendo en cuenta la información de la tabla anterior, se procede de forma similar a como se hallaron los factores de asignación con base en unidades físicas, así que hallamos la proporción en que participa el ingreso por ventas del ánodo con respecto a la venta total tanto del ánodo como del acero residual, es decir, U$ 2000/U$ 2000.551 = 0.9997, que sería el factor de asignación para la producción del ánodo; de igual forma, el factor de asignación para la producción de los residuos de acero sería U$ 1.551/2000.551 = 0.0003. Vericamos que 0.9997+0.0003 = De forma análoga que cuando se hizo la determinación de los factores de asignación con base en unidades físicas, se procede a determinar cuáles serías las cargas ambientales y recursos en cada proceso monofuncional.

 
Por otro lado, si se utliza el contenido energético o unidades de energía (ejemplo MJ o BTU) de los materiales como criterio para obtener los factores de asignación, se procede de forma similar a lo explicado anteriormente. En este caso, es importante que en el proceso multifuncional se tengan materiales/productos/coproductos que salen del proceso multifuncional con información sobre su poder calorífico inferior (BTU/Kg o MJ/Kg) (como es el caso de los combustibles, madera, caucho, cartón, papel, carbón, etc.), de manera que teniendo esta información y sabiendo la cantidad en Kg de estas salidas se puede obtener el contenido energético total (por ejemplo en MJ o BTU) y luego se haya la proporción con respecto a este total del producto/material principal y del coproducto y se procede a determinar el inventario conforme las explicaciones anteriores.

-**Método del excedente**

El último enfoque para solucionar los problemas que presentan los procesos multifuncionales consiste en el denominado **método del excedente** que tiene su sustento para aplicarlo en que un proceso unitario tiene como función principal prestar un solo servicio o en otras palabras, opera para el flujo principal mientras que para los otros flujos "secundarios", opera en un grado de menor importancia. Así que cuando se tiene un proceso multifuncional, uno podría tratarlo como si hubiera sido diseñado para producir el flujo principal y eliminar (quitar) los flujos secundarios (coproductos). Veamos cómo quedaría el proceso multifuncional:

 <div align="center">
  <img src="../.graph/Imagen42.png" width=80%><p>
</div></p>

Así que las matrices y vectores referidos con anterioridad que forman parte de la estructura básica para el cálculo del inventario serían los siguientes:


<div align="center">
  <img src="../.graph/Imagen43.png" width=80%><p>
</div></p>

Como se puede observar en la imagen anterior, nuevamente se han obtenido los mismos flujos ambientales con que iniciamos nuestra explicación sobre la estructura básica de cálculo para el inventario de ciclo de vida y eso era obvio de esperar por cuanto este método ignora el hecho de que se están produciendo coproductos.

### 1.4 Reciclaje de bucle cerrado



Nos referimos al reciclaje de bucle cerrado cuando un residuo que produce un proceso unitario, **en su totalidad es usado** por otro proceso que forma parte del mismo sistema producto. Por ahora supongamos el siguiente diagrama de ciclo de vida donde se ilustra cómo los residuos de aluminio que se generan para la producción de la parte de aluminio (probeta) se utlizan en la producción de lingotes de aluminio: 

<div align="center">
  <img src="../.graph/Imagen44.png" width=80%><p>
</div></p>

Con datos hipotéticos y manteniendo la misma unidad funcional (una demanda de 100 unidades o probetas), más abajo se muestra cómo se vería la **matriz de tecnología A** que como se observa no es cuadrada y por lo tanto no puede ser invertible, por lo tanto, la estructura básica de cálculo del inventario que se explicó al principio no se podría aplicar cuando se tieme un proceso de reciclaje de bucle cerrado. En esta imagen que muestra la matriz A, tener en cuenta que para el proceso que produce la probeta de Al, se necesitan 0.0005 toneladas de lingotes de Al, dato que no aparece en la matriz A pero que por un error se dejó de indicar en la imagen. Cuando existe reciclaje de bucle cerrado, se presentan ecuaciones redundantes, al ser combinación lineal de otras del conjunto de ecuaciones simultáneas, por lo que se configura un sistema sobre determinado, porque existen más ecuaciones que variables desconocidas, generalmente un sistema sobre determinado es inconsistente (no tiene solución). Cuando se presenta la anterior situación se procede a hacer uso de la seudoinversa (Heijungs & Frischknecht, 1998). 

<div align="center">
  <img src="../.graph/Imagen71.png" width=80%><p>
</div></p>

La seudoinversa es un método matemático para tener una solución matricial aproximada lo más cercana al valor de las variables desconocidas. Lo que se está haciendo con la aplicación de este método no es más que un análisis de regresión de mínimos cuadrados para minimizar el vector de discrepancia.  En este caso emerge el concepto de vector de discrepancia indicado como **d**, el cual se intepreta como la variable que se requiere minimizar. El vector **d**, es la diferencia entre el suministro final y la demanda final. Entendiendo el suministro final como aquél vector obtenido a partir de la técnica de la seudoinversa y la demanda final como el vector de demanda **f**. El vector de suministro final se obtiene como **As**, donde el vector de escalamiento **s** se obtiene con la técnica de la seudoinversa. Este vector de suministro final lo indicaremos como **f'**. Con la técnica de la seudoinversa lo que se busca es minimizar la diferencia **d = f'- f= O**, donde f' denota el vector de suministro. El vector **f'** se obtiene multiplicando la matriz A por el vector de escalamiento obtenido con la seudoinversa.

El valor que se obtenga para **d** es una medida de la calidad del ajuste. Así entonces, **As** (que es lo mismo que f') no será exactamente igual al vector de demanda **f**, a menos que todo el material se emplee en el proceso unitario que lo recicla.  Más adelante explicaremos cómo aplicar con un ejemplo el vector de discrepancia **d**. 

Es importante llamar la atención que con la aplicación de la técnica de la seudoinversa, generalmente se tiene una solución aproximada y no siempre el vector de suministro final **f'**  (que se obtiene con la seudoinversa, no siempre es igual al vector de demanda final **f** (donde está representada la unidad funcional).

En estudios reales de análisis de ciclo de vida el vector de discrepancia **d** puede desviarse de cero (0) debido al redondeo computacional y en este caso lo que daría son valores muy pequeños cercanos a **0**, por lo que con seguridad podemos ignorarlos y asumirlos como si fueran **0**. También es importante indicar, que también existen otras situaciones en que se pueden introducir errores que pueden ser importantes por cuanto se pierde precisión en los resultados. Para este último problema algunos autores han sugerido técnicas de reescalonado las cuales no serán objeto del presente curso, sin embargo, sigue este tema siendo un asunto de estudio y por lo tanto el problema del reescalonado óptimo todavía sigue sin tener una solución definitiva (Golub & Van Loan, 1996; Forsyth & Moler, 1967; Heijungs & Suh, 2002) cuando se utiliza la técnica con la seudoinversa para hallar el inventario de ciclo de vida en una situación de reciclaje de bucle cerrado. 

En el mejor de los casos, es posible que el vector de discrepancia **d** siempre tenga valores muy cercanos a cero y al valor de la demanda o unidad funcional. En el peor de los casos, es posible, que el vector de discrepancia **d**, presente números de condición grande que desde luego hace que se pierda precisión lo cual por supuesto importa y habría que dejarlo claro en el informe del estudio de análisis de ciclo de vida, pero que en ciertas circuntancias al no tener otras opciones o el conocimiento sobre teoría de la perturbación (donde se estudia la influencia de las perturbaciones de los coeficientes de las ecuaciones en las soluciones de dichas ecuaciones) y sus técnicas para mejorar la precisisón de los datos, los resultados que se obtienen podrían considerarse no como la solución óptima sino como una solución satisfactoria y que para los efectos prácticos en ciertos contextos donde se realiza el estudio de análisis de ciclo de vida, podría ser útil para los que encargan el estudio.

Ahora bien, la expresión para calcular el vector de escalamiento **s** usando la seudoinversa (que permite solucionar sistemas redundantes de ecuaciones para el caso del reciclaje de bucle cerrado) es la siguiente:

<p align="center">
  <span style="font-size:larger"><b>A<sup>+</sup></b> = (A<sup>T</sup>A)<sup>-1</sup>A<sup>T</sup></span>
</p>


Donde la seudoinversa la indicaremos con la letra <b>A<sup>+</sup></b> y corresponde a la siguiente expresión: 


<p align="center">
  <span style="font-size:larger"><b>A<sup>+</sup></b> = (A<sup>T</sup>A)<sup>-1</sup>A<sup>T</<//span>
</p>

Y el vector de escalonamiento se obtiene mediante la siguiente expresión:

<p align="center">
  <span style="font-size:larger"><b>s</b> = (A<sup>T</sup>A)<sup>-1</sup>A<sup>T</sup>f<//span>
</p>
    
La letra T significa que corresponde a la transpuesta de la matriz **A**.

A continuación vamos a ver cómo funciona esta estructura de cálculo.

 - **El caso cuando el reciclaje de bucle cerrado no funciona**

A continuación vamos a iniciar aplicando la fórmula de la seudoinversa, para ello se recomienda inciar calculando la matriz transpuesta de A:


<div align="center">
  <img src="../.graph/Imagen47.png" width=80%><p>
</div></p>

Luego procedamos a hallar el resultado de multiplicar la matriz transpuesta de A por la matriz A:


<div align="center">
  <img src="../.graph/Imagen48.png" width=80%><p>
</div></p>

Continuamos ahora hallando la inversa de la multiplicación entre la transpuesta de A por A:

<div align="center">
  <img src="../.graph/Imagen49.png" width=80%><p>
</div></p>

Continuamos multiplicando la anterior matriz por la transpuesta de A:

<div align="center">
  <img src="../.graph/Imagen50.png" width=80%><p>
</div></p>

Finalmente multiplico la anterior matriz por el vector de demanda f, sabiendo que el vector de demanda f es el siguiente, con el fin de obtener el vector de escalamiento s:



<div align="center">
  <img src="../.graph/Imagen51.png" width=30%><p>
</div></p>

<div align="center">
  <img src="../.graph/Imagen52.png" width=40%><p>
</div></p>

Si repasamos las fórmulas de la estructura básica para el cálculo del inventarios, el vector **f**, es el resultado de multiplicar la matriz **A** por el vector de escalamiento **s**, así que revisemos si hay un ajuste al multiplicar la matriz **A** por el vector de escalamiento que se obtuvo utilizando la seudoinversa, para ver si nos da el vector **f**:

<div align="center">
  <img src="../.graph/Imagen85.png" width=100%><p>
</div></p>


Como se observa en los resultados anteriores no se tuvo un ajuste perfecto, vemos entonces el resultado para el vector de dicrepancia **d**, que se obtiene restando del valor anterior **f'** que se obtuvo con la seudoinversa, el vector de demanda **f** original, vemos que de algunos materiales o productos sobra mientras que de otros falta, si hubiera habido un ajuste perfecto, el vector de discrepancia **d** en todas sus dimensiones debió tener valores de cero (0). Lo que muestran los resultados es que de algunos productos/materiales está sobrando algo y para otros está faltando, cosa que no debió presentarse si hubiera habido un ajuste perfecto, pero es natural que se presenten estos resultados porque se está aplicando un análisis de regresión y lo que se busca con este análisis de regresión es que la diferencia  **As - f** sea lo más cercana a (cero), o lo que es lo mismo que la diferencia **d = f' – f = 0** pero no siempre desde luego va a ser igual a cero (0), reiteramos va estar muy cerca de cero, por razones del redondeo que se presenta con la herramienta de cálculo y por la naturaleza misma al usar cálculo matricial. Heijungs & Suh (2002) recomiendan asignar exactamente el material o producto suficiente para el proceso de reciclaje y enviar el resto ya sea a un proceso de reciclaje de bucle cerrado o a un proceso de tratamiento de residuos. A continuación explicaremos con el uso de excel cómo sería el cálculo a realizar.

 - **El caso cuando el reciclaje de bucle cerrado empieza a funcionar**

Lo que vamos a llevar a cabo a continuación es buscar que la cantidad de residuos de aluminio que genera el proceso unitario de producción de la probeta de alumninio sea exactamente igual a la cantidad de estos residuos que requiere el proceso unitario de producción de lingotes de aluminio. Para ello, hacemos un escalamiento secuencial para lo cual procedemos de la siguiente manera: Como la unidad funcional le pide al sistema producto que produzca 100 probetas, entonces las entradas y salidas del proceso unitario de producción de probetas se deben multiplicar por 100 (factor de escalamiento) dado que originalmente este proceso tiene como salida una unidad de probeta. Como este factor afecta a todo el proceso, entonces también debo multiplicar los 0,030 Kg de residuos de aluminio por 100, lo que arroja un valor de 3 Kg de residuos de aluminio. También debo multiplicar la entrada al proceso de los lingotes de aluminio, es decir las 0.0005 toneladas las multiplico por 100 con lo cual se tiene como resultado 0.05 toneladas de lingotes. Luego paso al proceso unitario que produce los lingotes de aluminio y donde se emplean los residuos de aluminio que genera la producción de las probetas. Como la producción de probetas requiere 0.05 toneladas de lingotes, entonces la salida de una tonelada de lingotes que sale del proceso unitario de producción de lingotes debo multiplicarla por 0.05 (factor de escalamiento). También la entrada de residuos de aluminio que requiere este proceso debo multiplicarla por este mismo factor de escalamiento, es decir 0.20 Kg de residuos de aluminio multiplicado por 0.05 que da un valor de 0.01 Kg de residuos de aluminio.

Teniendo en cuenta las anteriores consideraciones, observe lo siguiente, una vez hecho este escalamiento secuencial: El proceso unitario de producción de probetas genera 3 Kg de residuos de aluminio, sin embargo, el proceso unitario que produce los lingotes de aluminio, solo necesita 0.01 Kg de residuos de aluminio, es decir, el proceso unitario de la producción de las probetas está produciendo más residuo del que se necesita en la producción de los lingotes de alumninio (hay excedentes del material a reciclar). 

En  el ejemplo que nos ocupa, la producción de probetas produce más residuo de aluminio del que se requiere en la producción de lingotes de aluminio (pero puede suceder lo contrario, que la producción de probetas genere menos residuo del que se requiere en la producción de lingotesm, para este caso se debe suministrar el faltante agregando un proceso que produzca el material faltante o requerido).

Ahiora bien, retomando nuestro ejemplo y con base en las consideraciones anteriores, lo que se hace es que la producción de probetas sólo debería generar 0.01 Kg de residuos de aluminio pero como ese proceso tiene como factor de escalamiento 100, entonces debo colocar una cantidad X de residuos de aluminio que al multiplicarla me de como resultado 0.01 kg de residuos de aluminio. Entonces esablezco la siguiente expresión:

<p align="center">
  100X = 0.01
</p>

Despejando X, encuentro que este valor debe ser igual a 0.0001 Kg de residuos de aluminio. Pero no hay que olvidar de acuerdo con las explicaciones que se dieron anteriormente, el proceso de producción de probetas debe producir 3 Kg de residuos de alumninio, de manera que si ya se generaron 0.0001 Kg de residuos de aluminio, para completar los 3 Kg, se deberían generar por aparte 2.9999 Kg de residuos de aluminio, así que se debe buscar una cantidad Y que al multiplicarla por el factor de escalamiento 100 de como resultado 2.9999 Kg de residuos de aluminio:

<p align="center">
  100Y = 2.9999
</p>

Despejando Y encontramos que su valor corresponde a 0.029999 Kg de residuos. Estos residuos de más de aluminio (excedente) que no requiere el proceso de producción de lingotes de aluminio, se envían a un proceso de reciclaje de bucle abierto (utilizando la técnica de procesos ficticios). Veamos entonces cómo sería la matriz **A** incorporando la información anterior:

<div align="center">
  <img src="../.graph/Imagen74.png" width=110%><p>
</div></p>

A continuación vamos a indicar todas las demás matrices y vectores que se requiere con el fin de calcular el vector de escalamiento **s** con la técnica de la seudoinversa y se finaliza mostrando los resultados del inventario de ciclo de vida (vector g).

<div align="center">
  <img src="../.graph/Imagen75.png" width=60%><p>
</div></p>


<div align="center">
  <img src="../.graph/Imagen77.png" width=80%><p>
</div></p>

<div align="center">
  <img src="../.graph/Imagen79.png" width=80%><p>
</div></p>


<div align="center">
  <img src="../.graph/Imagen80.png" width=80%><p>
</div></p>


<div align="center">
  <img src="../.graph/Imagen81.png" width=45%><p>
</div></p>
 
<div align="center">
  <img src="../.graph/Imagen82.png" width=100%><p>
</div></p>


<div align="center">
  <img src="../.graph/Imagen83.png" width=100%><p>
</div></p>

<div align="center">
  <img src="../.graph/Imagen84.png" width=50%><p>
</div></p>

  </p>

En el ejemplo anterior, observamos que fue necesario enviar el sobrante de residuos de aluminio a un proceso de reciclaje de bucle abierto. Pero expliquemos cómo sería el cálculo del inventario con la seudoinversa para cuando se presenta el caso contrario, es decir, que se tiene un faltante o déficit de residuos de aluminio en el proceso de reciclaje del material en la producción de lingotes de aluminio. Para comenzar, hemos cambiado los datos de la **matriz A** para ilustrar con un nuevo ejemplo, el cálculo con la seudoiversa del inventario de ciclo de vida en el caso de reciclaje de bucle cerrado. A continuación presentamos la **matriz A**.



<div align="center">
  <img src="../.graph/Imagen88.png" width=100%><p>
</div></p>

Tal como se procedió anteriormente para explicar el caso de reciclaje de bucle cerrado donde existía un excedente de residuos de aluminio, comencemos haciendo un escalamiento secuencial. Como la unidad funcional corresponde a 100 unidades de probetas, se debe multiplicar las entradas del proceso de producción de probetas por el factor de escalonamiento 100. Al escalar los flujos tecnológicos encontramos que se generan **0.001 x 100 = 0.1** Kg de residuos de aluminio y se requiere **0.0005 x 100 = 0.05 toneladas de aluminio**. Luego paso al proceso que produce lingotes de aluminio y como el proceso de producción de probetas requiere 0.05 toneladas de aluminio, debo multiplicar las entradas y salidas del proceso de producción de lingotes de aluminio por el factor de escalamiento 0.05. Ahora, este proceso requiere **30 x 0.05 = 1.5** Kg de residuos de aluminio. Al observar la cantidad de residuos de aluminio que se producen en la producción de la probeta, vemos que es una cantidad inferior a la que se necesita en la producción de los lingotes de aluminio (0.1 < 1.5). Por lo tanto, se requiere incorporar un proceso que suministre el faltante para el proceso de producción de lingotes de aluminio. Ahora bien, el faltante o déficit de residuos de aluminio es **1.5 – 0.1 = 1.4** Kg de residuos de alumnio. Como ese nuevo proceso hay que escalonarlo también por el valor de 100, requerimos que ese proceso produzca una salida de residuos de aluminio tal que al multplicarla por 100 de como resultado el faltante que es de 1.4, así que con una ecuación como Zx100 = 1.4, podemos despejar Z = 0.014 Kg de residuos de aluminio. Veamos entonces cómo entonces incorporamos este nuevo proceso en la **matriz A**:

<div align="center">
  <img src="../.graph/Imagen89.png" width=100%><p>
</div></p>

Como se hizo con anterioridad, se procede a través por ejemplo de una hoja excel con los cálculos de rutina aplicando la técnica de la seudoinversa. A continuación los resultados respectivos.

<div align="center">
  <img src="../.graph/Imagen90.png" width=10%><p>
</div></p>

<div align="center">
  <img src="../.graph/Imagen91.png" width=70%><p>
</div></p>

<div align="center">
  <img src="../.graph/Imagen92.png" width=50%><p>
</div></p>

<div align="center">
  <img src="../.graph/Imagen93.png" width=80%><p>
</div></p>

<div align="center">
  <img src="../.graph/Imagen94.png" width=80%><p>
</div></p>

<div align="center">
  <img src="../.graph/Imagen95.png" width=30%><p>
</div></p>



Para finalizar una breve observación, la **técnica de la seudoinversa**, es un enfoque útil que la mayoría de las veces se puede emplear con matrices que no son cuadradas y que no son invertibles como es el caso cuando se tiene reciclaje de bucle cerrado, pero también es cierto que esta técnica matemática también se puede emplear incluso con matrices invertibles cuadradas. 

</div>

<div align="center">
   
   <a href="https://enlace-academico.escuelaing.edu.co/psc/FORMULARIO/EMPLOYEE/SA/c/EC_LOCALIZACION_RE.LC_FRM_ADMEDCO_FL.GBL" target="_blank"><img src="https://github.com/MaterialsCompTools/DRX-MaterialesCristalinos/blob/main/.graph/Logo%20Obtener%20certificado%20PNG.png" alt="R.LTWB" width="260" border="0" /></a>

</div>

<div align="center">
  <img src="../.graph/escuela%20laura.png" width=40%><p>
</div>
