<div align="center"><a href="https://www.escuelaing.edu.co/es/investigacion-e-innovacion/centro-de-estudios-de-sistemas-de-gestion/" target="_blank"><img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Centro%20de%20Estudios%20en%20Sistemas%20de%20Gestio%CC%81n.jpg" alt="R.LTWB" width="100%" border="0" /></a></div>

  <div align="center">
  
  <h1>ESTRUCTURA DE CÁLCULO MATEMÁTICO DEL ANÁLISIS AMBIENTAL DEL CICLO DE VIDA DE UN PRODUCTO </h1>
  <h1>Sección 3</h1>

  <h2>Modelo ampliado del modelo de inventario</h2>
</p>

</div>

<div align="justify">

### 1.1 Propósito de la sección
Aprenderás cómo es la estructura de cálculo matemático para determinar el inventario de ciclo de vida cuando la matriz no es cuadrada.

### 1.2 Modelo de inventario: Sistemas incompletos


Cuando se están llevando a cabo estudios de análisis de ciclo de vida, es común que existan dificultades en la obtención de los datos para el inventario (s vuelve costoso recolectar la información, no se tiene el tiempo o simplemente se hace muy difícil tener el dato apropiado), por ejemplo, sabemos que en un determinado proceso unitario entra una determinada cantidad de flujo económico pero pero no tenemos información sobre el proceso que produjo dicha entrada tecnológica.Este caso se denomina sistemas incompletos y corresponde a aquellos  casos donde no se ha incluido los procesos unitarios para la producción de un determinado flujo económico que hemos incluido en la matriz de procesos y/o no se ha incluido tampoco los procesos unitarios encargados de recibir o tratar un flujo económico que se ha incluido en la matriz de procesos. Por lo anterior, es obvio que la ecuación fundamental **As = f** no se puede solucionar para **s**, por cuanto no podemos tener la inversa de una matriz que es rectangular, es decir que no es cuadrada. Así que para lograr la una solución, se han propuesto algunos "trucos matemáticos":

* Incorporación de procesos ficticios
* Eliminar de la matriz de tecnología **A** los flujos económicos de demás y que no tiene asociado un proceso unitario que los haya producido o que posteriormente los trate o los reciba.

Veamos cómo sería la inclusión de procesos ficticio Asumamos la siguiente matriz tecnológica teniendo en cuenta que asumimos que la producción que la electrólisis  y la producción de ánodo requiere 5 Kg de acero y 2 Kg de acero, respectivamente y que además la producción de la probeta de aluminio necesita 0,0001 Kg de solvente. Así que en principio la matriz de tecnología sería la siguiente:


![Diagrama de ciclo de vida para la producción de una probeta de aluminio](https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen16.png)<p>

Ahora vamos a "cuadrar" la matriz de tecnología **A**, adicionando procesos ficticios. Como existe el flujo económico "Kg de acero", incorporamos en la matriz **A**, un proceso ficticio que se asume fue el que produjo los kg de acero que requiere los procesos de electrólisis y de producción de ánodo y otro que se asume fue el que produjo los Kg de solvente que se utilizan en el proceso de producción de la probeta de aluminio.  Como se puede ver a continuación, el proceso ficticio solo tiene el número 1 y las demás dimensiones son cero, tanto en la matriz **A** como en la matriz de intervención ambiental **B**. Obsérvese que los "unos" son con signo "+", por cuanto se asume que si un proceso está necesitando (necesitando significa una entrada y por lo tanto se indica con signo "menos") acero o solvente, entonces otro proceso (ficticio para nuestro caso) debió producir cada uno de estos flujos (producir significa una salida, y por lo tanto se indica con signo "+". Una vez hemos incorporado los procesos ficticios, vemos que ahora la matriz **A** es cuadrada e invertible, veamos como luciría:

![Diagrama de ciclo de vida para la producción de una probeta de aluminio](https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen20.png)<p>

El vector de demanda sería el siguiente:



<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen19.png" alt="Ecuación de balance" width=30%><p>
</div>

La inversa de la anterior matriz sería la siguiente:

![Diagrama de ciclo de vida para la producción de una probeta de aluminio](https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen17.png)<p>

El vector **s** de factores de escalamiento sería el siguiente:

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen21.png" alt="Ecuación de balance" width=30%><p>
</div>

La matriz de intervención ambiental sería la siguiente:

![Diagrama de ciclo de vida para la producción de una probeta de aluminio](https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen18.png)<p>

Y finalmente el resultado final del modelo de inventario que era a donde queríamos llegar aplicando las relaciones matriciales vistas anteriormente.

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen22.png" alt="Ecuación de balance" width=30%><p>
</div>

Ahora bien, otra forma de tratar los sistemas incompletos es remover los flujos económicos para los cuales en la matriz de procesos no se tienen los procesos unitarios que los haya producido o absorbido. La matriz **A* sería la siguiente resaltando los flujos que habría que remover:


<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen23.png" alt="Ecuación de balance" width=80%><p>
</div>

Una vez se han removido estos flujos económicos, encontramos que la matriz **A** es cuadrada e invertible y por lo tanto podemos aplicar la estructura de cálculo matricial vista anteriormenre para hallar el inventario de ciclo de vida.


### 1.3 Modelo de inventario: Procesos multifuncionales

Es común que los sistemas industriales produzcan más de un flujo económico. Pot ejemplo, una refinería produce diferentes tipos de combustibles o una empresa de lácteos produce diferentes tipos de productos (quesos, leche, etc.) o un matadero genere carne, cuero, vísceras, etc. que se venden en el mercado. Así que un proceso que tiene más de una función o presta más de un servicio se denomina proceso multifuncional. Las siguientes son categorías de procesos multifuncionales:

   - Un proceso unitario que produce más de una salida valiosa, es decir coproductos, se generan inevitablemente por la misma naturaleza del proceso productivo. por ejemplo, en la       producción de combustibles, invevitablemente se producen en ese proceso petroquímico diferentes tipos de combustibles a la vez.
   - Procesos unitarios que tratan dos o más residuos, por ejemplo, un incinerador  para el tratamiento de residuos, le entra residuos de cartón , plástico, papel, etc.
   - Procesos unitarios que tratan un tipo de residuo y producen una salida valiosa. Por ejemplo, una planta le entra residuos de papel (recicla este tipo de residuo) y los convierte en 
    cartón corrugado
   - Procesos unitarios que deliberadamenrte se les asigna más de una función o servicio. Por ejemplo, el transporte de pasajeros en un avión pero que al mismo tiempo en el mismo avión se 
    transporta carga o mercancías
    </p>

Otro asunto que amerita resaltarse es que con los procesos multifuncionales se tiene un problema denominado el problema de la asignación. Cuando un proceso unitario, por ejemplo, produce un bien en madera, se genera un coproducto que es el aserrín, este último material es un coproducto que se puede vender por ejemplo a las empresas que producen alimentos cárnicos para que allí lo utilicen por ejemplo para la preparación del jamón ahumado o con destino a otras empresas que producen muebles a base de compuestos aglomerados. Ahora bien, si estamos haciendo un estudio de análisis de ciclo de vida, por ejemplo, de un sistema producto hecho a base de madera, en principio no sabemos cuál es la carga ambiental que debemos asignarle al producto o bien en madera y cuál es la carga ambiental que debemos asignarle al coproducto. Por lo tanto debemos solucionar este problema y para ello existen diferentes enfoques metodológicos que son los que vamos a explicar a continuación.

  -**Método de substitución**

Para hacer mejor la explicación, partamos del siguiente ejemplo: asumamos que el proceso de producción del ánodo genera residuos de acero y que estos residuos de acero los recoge una empresa  que los utiliza para hacer envases. Veamos cómo sería el diagrama de flujo del ciclo de vida con la incorporación del coproducto que corresponde a la generaciónd de residuos de acero en una cantidad de 4.7 kilogramos y donde se observa que la matriz no es cuadrada y que de las cargas ambientales (ver matriz intervención ambiental que se mostró anteriormente) del proceso de producción del ánodo, no sabemos cuántas de ellas se las asignamos al flujo en toneldas de ánodo y cuántas al flujo en kilogramos de acero residual. A continuación se muestra el nuevo diagrama de ciclo de vida. Es importante anotar que este residuo de acero como coproducto, indica que es valioso para otra empresa, por ejemplo, para utlizarlo como materia prima. Cuando hablamos "para otra empresa" significa que el residuo puede ir a otro sistema producto diferente al sistema producto donde se está generando este tipo de residuo, esto se conoce como **reciclaje de bucle abierto**. A continuación se ilustra cómo sería el diagrama de ciclo de vida incorporando el coproducto y la **matriz A** que como se ve no es cuadrada:

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen28.png" alt="Ecuación de balance" width=80%><p>
</div>

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen54.png" alt="Ecuación de balance" width=100%><p>
</div>





El **método de substitución** consiste en encontrar  un proceso unitario (ya sea en la literatura técnica o especializada o en la realidad o bases de datos especializadas) que tenga como función o servicio principal la producción del coproducto (acero) o un material que sea equivalente o cumpla funciones similares al material de acero. Lo que sucede es que cuando se encuentra este proceso, lo que está pasando es que al incorporar este nuevo proceso a la **matriz A**, la información de entradas y salidas que tiene este proceso se restan de las entradas y salidas del proceso donde se está produciendo el coproducto (desde luego esta "resta" se hace con base en la aplicación de factores de escalonamiento, operación que se realiza cuando aplicamos el modelo básico del cálculo de inventario visto anteriormente). Veamos entonces cómo sería la  aplicación de esta técnica o truco "matemático" para solucionar el problema de la asignación y al mismo tiempo convertir la  **matriz A** en una matriz cuadrada e invertible. 

Asumamos que hemos encontrado un proceso unitario cuya función principal es producir acero. Veamos entonces cómo sería la **matriz A** con la incorporación de este nuevo proceso:

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen55.png" alt="Ecuación de balanc" width=130%><p>
</div>

La anterior matriz podemos volverla "cuadrada" buscando una equivalencia o inequivalencia entre los dos tipos de acero, si asumimos que los dos tipos de flujos en cuanto a su calidad es la misma (por ejemplo, porque tanto los residuos de acero (coproducto) como el acero virgen producido por el nuevo proceso unitario que se incorporó al sistema, sus propiedades inherentes no cambian, entonces los dos flujos es una misma cosa (indistinguibles por así decirlo) y por lo tanto las dos nuevas filas se pueden fusionar en una sola fila:

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen56.png" alt="Ecuación de balanc" width=130%><p>
</div>

Por otro lado, este proceso unitario de producción de acero emite 28.28 Kg de CO<sub>2</sub>, 0.00575 Kg de SO<sub>2</sub> y 0.00384 Kg de N<sub>2</sub>O y produced 947 kilogramos de acero virgen. Veamos entonces cómo quedarían, el **vector de demanda f**, **la matriz inversa de A**, el **vector de factores de escalamiento s**, la **matriz de intervención ambiental B**y el **vector de inventario g**, al incorporar este nuevo proceso al sistema (por eso también se le conoce como la técnica de expansión del sistema, porque se está incorporando un nuevo proceso al sistema industrial):

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen58.png" alt="Ecuación de balance" width=15%><p>
</div>



<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen57.png" alt="Ecuación de balance" width=120%><p>
</div>

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen60.png" alt="Ecuación de balance" width=120%><p>
</div>

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen61.png" alt="Ecuación de balance" width=30%><p>
</div>

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen62.png" alt="Ecuación de balance" width=30%><p>
</div>



 -**Algunas consideraciones adicionales sobre el método de substitución**

 Teniendo en cuenta las indicaciones dadas por Heijungs % Suh (2002), a continuación las siguientes consideraciones sobre el método de sustitución:

- El factor de escalamiento para el proceso unitario que produce como servicio principal el acero tiene signo negativo. Esto se interpreta que ese proceso unitario se resta del sistema, por esos este factor de escalamiento es negativo. Generalmente el proceso de producción de acero o cualquier otro proceso unitario que se haya incorporado para aplicar la técnica de sustitución, tendrá un factor de escalamiento más pequeño que el que podría tener en el sistema original con el producto respectivo.  Por otro lado, en general cuando se incorpora el nuevo proceso unitario al sistema, todas las intervenciones ambientales pueden permanecer inalteradas, porque el nuevo proceso unitario realmente no tiene un rol o participación en el sistema o si la tiene, su participación en el ciclo de vida es marginal o menor y eso hace que su involucramiento se de un alcance restringido.
- Otro problema con la técnica de sustitución, es que puede haber dificultades en encontrar el nuevo proceso unitario o concluir que no existe tal proceso.
- Suele pasar que la incorporación del nuevo proceso unitario, su flujo económico puede sustituir el coproducto del sistema, aún cuando los dos flujos no sean exactamente de la misma naturaleza. Por ejemplo, el acero producido como producto tiene una calidad X (por ejemplo,por razones de que es más fácil de conseguir en determinada instalación o por el contrario difícil de conseguir o porque tiene impurezas), mientras que el nuevo proceso unitario produce un acero de calidad Y (por ejemplo, sus propiedades son relativamente diferentes al coprooducto).
 

 -**Método de partición**

 Otra técnica o "truco matemático" para hacer que la matriz A tenga inversa (sea invertible) es el denominado método de partición. Este método consiste primero en dividir el proceso unitario multifuncional en procesos monofuncionales independientes, por esto a esta ténica se le denomina el método de la partición. El objetivo principal es distribuir equitativamente las cargas ambientales (recursos y emisiones), entre el producto principal (servicio principal del proceso unitario) y los coproductos. Paara este proopósito es práctica generalizada que esta asignación se haga sobre la base de la asignación basada en unidades físicas (masa, volumen, energía) y asignación económica.  Veamos entonces cómo se aplicaría este método empleando 
como base unidades físicas de masa para hallar los respectivos **factores de asignación**:

  -  **Dibujar el proceso multifuncional mediante una caja con todas sus entradas y salidas**
 La mejor manera de ver esto es con los siguientes diagramas donde aparece primero el proceso unitario multifuncional y luego los procesos monofuncionales y donde see indica el cálculo de los factores de asignación hechos a partir de unidades físicas. Es importante que cuando se hace la partición en procesos monofuncionales, se tiene una caja con la salida del producto principal (Kg de ánodo) y otra caja con la salida del coproducto (Kg residuos de acero). Los valores para estas salidas no deben sufrir ninguna alteración o cambio, las demás entradas (recursos) y salidas ambientales de cada uno de estos procesos monofuncionales van a tener que ser modificados cuando se les aplique los factores de asignación. La asignaación basada en masa es la siguiente: En el proceso monofuncional para la salida de los Kg de ánodo,  sale un total de una tonelada de ánodo y para el proceso monofuncional donde se produce el coproducto, sale un total de 5 kilogramos de acero residual. Sumamos estas dos cantidades, lo que daría un total de 1005 kilogramos. Luego se halla para el proceso que produce el ánodo, la proporción en que participa el total en Kg de ánodo con respecto a este total, es decir 1000 Kg/1005 Kg = 0.9950. Este sería el factor de asignación para el proceso de producción de ánodo. De igual forma, calculo la proporción de producción de  acero residual con respecto al mismo total anterior , lo cual daría 5/1005 = 0.005, que sería el factor de asignación para la producción de acero residual. Importante señalar que la suma de los factores de asignación siempre deber ser igual a 1. Luego multiplico en cada uno de los procesos monofuncionales, sus otras entradas y salidas por el respectivo factor de asignación como se observa en la figura que aparece más abajo.



  -  **Partir el proceso multifuncional en procesos monofuncionales**

 <div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen63.png" width=90%><p>
</div></p>





Una vez se ha hecho la partición anterior que se muestra en la imagen, se procede a ingresar esta información a la **matriz A** (eliminando el proceso multifuncional e ingresando la información de entradas y salidas de los dos procesos monofuncionales), veamos entonces cómo quedaría la **matriz A**, **la matriz B**, **el vector de demanda f**, **el vector de escalamiento s** y **el vector de inventario g**:




 <div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen65.png" width=30%><p>
</div></p>


 <div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen66.png" width=100%><p>
</div></p>




A continuación vamos explicar cómo sería la determinación de los factores de asignación con base en valor económico. La aplicación de este criterio tiene en cuenta el precio en el mercado tanto del ánodo como del acero residual que son las dos salidas del proceso multifuncional. Para comenzar asumamos que tenemos la siguiente información:

| Material              | Cantidad | Unidad  | Precio venta por Unidad | Total ingreso por venta del material/producto |
|-----------------------|----------|---------|-------------------|----------------------------------------------|
| Ánodo                 | 1000     | Kg      | US$ 2/Kg          | U$ 2000.00                                      |
| Residuos de acero     | 5.17     | KG      | U$ 0.30/Kg        | U$ 1.551                                      |
| Total venta           |          |         |                   |  U$ 2000.551

Teniendo en cuenta la información de la tabla anterior, se procede de forma similar a como se hallaron los factores de asignación con base en unidades físicas, así que hallamos la proporción en que participa el ingreso por ventas del ánodo con respecto a la venta total tanto del ánodo como del acero residual, es decir, U$ 2000/U$ 2000.551 = 0.9997, que sería el factor de asignación para la producción del ánodo; de igual forma, el factor de asignación para la producción de los residuos de acero sería U$ 1.551/2000.551 = 0.0003. Vericamos que 0.9997+0.0003 = 1.00 A continuación veamos cómo sería la  información de entradas y salidas para los procesos particionados:

 <div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen40.png" width=80%><p>
</div></p>

Una vez se ha hecho la partición anterior que se muestra en la imagen, se procede a ingresar esta información a la matriz A (eliminando el proceso multifuncional e ingresando la información de entradas y salidas de los dos procesos monofuncionales), veamos entonces cómo quedaría **la matriz A**, **la matriz B**, **el vector de demanda f**, **el vector de escalamiento s** y **el vector de inventario g**:

 <div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen41.png" width=80%><p>
</div></p>

Por otro lado, si se utliza el contenido energético o unidades de energía (ejemplo MJ) de los materiales como criterio para obtener los factores de asignación, se procede de forma similar a lo explicado anteriormente. En este caso, es importante que en el proceso multifuncional se tengan materiales/productos/coproductos que salen del proceso multifuncional con información sobre su poder calorífico inferior (como es el caso de los combustibles, madera, caucho, etc.), de manera que teniendo esta información y sabiendo la cantidad en Kg de estas salidas se puede obtener el contenido energético total (por ejemplo en MJ o BTU) y luego se haya la proporción con respecto a este total del producto/material principal y del coproducto y se procede a determinar el inventario conforme las explicaciones anteriores.

-**Método del excedente**

El último enfoque para solucionar los problemas que presentan los procesos multifuncionales consiste en el denominado **método del excedente** que tiene su sustento para aplicarlo en que un proceso unitario tiene como función principal prestar un solo servicio o en otras palabras, opera para el flujo principal mientras que para los otros flujos "secundarios", opera en un grado de menor importancia. Así que cuando se tiene un proceso multifuncional, uno podría tratarlo como si hubiera sido diseñado para producir el flujo principal y eliminar (quitar) los flujos secundarios (coproductos). Veamos cómo quedaría el proceso multifuncional:

 <div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen42.png" width=80%><p>
</div></p>

Así que las matrices y vectores referidos con anterioridad que forman parte de la estructura básica para el cálculo del inventario serían los siguientes:


<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen43.png" width=80%><p>
</div></p>

Como se puede observar en la imagen anterior, nuevamente se han obtenido los mismos flujos ambientales con que iniciamos nuestra explicación sobre la estructura básica de cálculo para el inventario de ciclo de vida y eso era obvio de esperar por cuanto este método ignora el hecho de que se están produciendo coproductos.

### 1.4 Reciclaje de bucle cerrado

Nos referimos al reciclaje de bucle cerrado cuando un residuo que produce un proceso unitario, en su totalidad es usado por otro proceso que forma parte del mismo sistema producto. Por ahora supongamos el siguiente diagrama de ciclo de vida donde se ilustra cómo los residuos de aluminio que se generan para la producción de la parte de aluminio (probeta) se utlizan en la producción de lingotes de aluminio:

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen44.png" width=80%><p>
</div></p>

Con datos hipotéticos y manteniendo la misma unidad funcional (una demanda de 100 unidades o probetas) veamos cómo se vería la **matriz de tecnología A** que como se observa no es cuadrada y por lo tanto no puede ser invertible, por lo tanto, la estructura básica de cálculo del inventario que se explicó al principio no se podría aplicar cuando se tieme un proceso de reciclaje de bucle cerrado. Cuando existe reciclaje de bucle cerrado, se presenta que una ecuación  es redundante, al ser combinación lineal de otras del conjunto de ecuaciones simultáneas, por lo que se configura un sistema  sobre determinado, porque existen más ecuaciones que variables desconocidas, generalmente un sistema sobre determinado es inconsistente (not tiene solución). Cuando se presenta la anterior situación se procede a hacer uso de la seudoinversa.

La seudoinversa es un método matemático para tener una solución aproximada lo más cercana al valor de las variables desconocidas. Lo que se está haciendo con la aplicación de este método no es más que un análisis de regresión de mínimos cuadrados para minimizar el vector de discrepancia **d** En este caso emerge el concepto de vector de discrepancia indicado como **d**, el cual se intepreta como la variable que se requiere minimizar. El valor que se obtenga para **d** es una medida de la calidad del ajuste. Así entonces, **As** no será exactamente igual al vector de demanda a menos que  todo el material se emplee en el proces unitario que lo recicla.  Más adelante explicaremos cómo aplicar en un ejemplo el vector de discrepancia **d**. 

La expresión para la seudoinversa  que permite solucionar sistemas redundantes de ecuaciones para el caso del reciclaje de bucle cerrado es la siguiente:

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen46.png" width=30%><p>
</div></p>

La letra T significa que corresponde a la transpuesta de la matriz **A**

**El caso cuando el reciclaje de bucle cerrado no funciona**

A continuación vamos a iniciar aplicando la fórmula de la seudoinversa, para ello se recomienda inciar calculando la matriz transpuesta de A:


<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen47.png" width=80%><p>
</div></p>

Luego procedamos a hallar el resultado de multiplicar la matriz transpuesta de A por la matriz A:


<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen48.png" width=80%><p>
</div></p>

Continuamos ahora hallando la inversa de la multiplicación enre la transpuesta de A por A:

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen49.png" width=80%><p>
</div></p>

Continuamos multiplicando la anterior matriz por la transpuesta de A:

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen50.png" width=80%><p>
</div></p>

Finalmente multiplico la anterior matriz por el vector de demanda f, sabiendo que el vector de demanda f es el siguiente, con el fin de obtener el vector de escalamiento s:



<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen51.png" width=30%><p>
</div></p>

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen52.png" width=40%><p>
</div></p>

Si repasamos las fórmulas de la estructura básica para el cálculo del inventarios, el vector **f**, es el resultado de multiplicar la matriz **A** por el vector de escalamiento **s**, así que revisemos si hay un ajuste al multiplicar la matriz **A** por el vector de escalamiento que se obtuvo utilizando la seudoinversa, para ver si nos da el vector **f**:

<div align="center">
  <img src="https://github.com/jrchaconcito/REPOTEST/blob/main/.graph/Imagen53.png" width=70%><p>
</div></p>

Como se observa en los resultados anteriores no se tuvo un ajuste perfecto, veamos entonces cuál es el resultado para el vector de dicrepancia **d**, que se obtiene restando del valor anterior **f** que se obtuvo con la seudoinversa, el vector de demanda **f** original y vemos que de algunos materiales o productos sobra mientras que de otros falta, si hubiera habido un ajuste perfecto, el vector de discrepancia en todas sus dimensiones debió aparecer cero (0), eso lo que significa es que de algunos productos está sobrando algo y para otros está faltando, cosa que no debió presentarse si hubiera habido un ajuste perfecto, pero es natural que se presenten estos resultados que se está aplicando un análisis de regresión y lo que se busca con este análisis de regresión es que la diferencia  **As - f** sea lo más cercana a = (cero) pero nunca desde luego va a ser igual a cero (0). Heijungs & Suh (2002) recomiendan asignar exactamente el material o producto suficiente al proceso de reciclaje y enviar el resto ya sea a un proceso de reciclaje de bucle cerrado o aun proceso de tratamiento de residuos.




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

El uso de álgebra lineal y matrices para resolver ecuaciones simultáneas (como las referidas anteriormente) es una elección sólida debido a su eficiencia, precisión, escalabilidad y aplicabilidad general, así como a las herramientas disponibles que facilitan su implementación. Esta metodología es esencial en una amplia gama de campos y garantiza resultados más confiables y rápidos en comparación con los métodos manuales o tradicionales. Así que vamos a aprender cómo cálcular el inventario de ciclo de vida utilizando algebra matricial. A continuación la solución para hallar los factores de escalamiento empleando una solución matricial para el conjunto de ecuaciones simultáneas:

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

