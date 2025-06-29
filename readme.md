# Redes Neuronales
**Grupo N° 1**  
**Jessica Tejero**  
**Melina Vazquez**  
**Fabiola Suárez**  
**Lautaro Martinez**  
**Angie Denise Oldano**  
**Cesar Emiliano Gerace**



## **¿Qué son las redes neuronales?**

Las redes neuronales son un componente crucial de los modelos de inteligencia artificial que imitan la estructura del cerebro humano, permitiendo a los sistemas aprender y mejorar a partir de grandes conjuntos de datos.

Una red neuronal es un modelo computacional compuesto por capas de nodos, también llamados neuronas, que están interconectadas entre sí. Estas capas incluyen una capa de entrada, una o más capas ocultas y una capa de salida.

Cada neurona recibe una entrada, la procesa y transmite una salida a las neuronas de la siguiente capa, repitiendo este proceso hasta que se genera el resultado final.

Las redes neuronales artificiales y las biológicas comparten la idea básica de estar compuestas por neuronas que procesan información y están interconectadas.

Además, estas redes son un tipo de algoritmo de aprendizaje automático inspirado en el cerebro humano, utilizado para resolver problemas complejos como el reconocimiento de imágenes y el procesamiento de lenguaje natural.

## **Arquitectura de una red neuronal simple**

Una red neuronal básica tiene neuronas artificiales interconectadas en tres capas:

Capa de entrada

La información del mundo exterior entra en la red neuronal artificial desde la capa de entrada. Los nodos de entrada procesan los datos, los analizan o los clasifican y los pasan a la siguiente capa.

Capa oculta

Las capas ocultas toman su entrada de la capa de entrada o de otras capas ocultas. Las redes neuronales artificiales pueden tener una gran cantidad de capas ocultas. Cada capa oculta analiza la salida de la capa anterior, la procesa aún más y la pasa a la siguiente capa.

Capa de salida

La capa de salida proporciona el resultado final de todo el procesamiento de datos que realiza la red neuronal artificial. Puede tener uno o varios nodos. Por ejemplo, si tenemos un problema de clasificación binaria (sí/no), la capa de salida tendrá un nodo de salida que dará como resultado 1 o 0. Sin embargo, si tenemos un problema de clasificación multiclase, la capa de salida puede estar formada por más de un nodo de salida.

## **¿Cuáles son los tipos de redes neuronales?**

Las redes neuronales artificiales pueden clasificarse en función de cómo fluyen los datos desde el nodo de entrada hasta el nodo de salida. A continuación, se indican varios ejemplos:

Redes neuronales pre alimentadas

Las redes neuronales pre alimentadas procesan los datos en una dirección, desde el nodo de entrada hasta el nodo de salida. Todos los nodos de una capa están conectados a todos los nodos de la siguiente capa. Una red prealimentada utiliza un proceso de retroalimentación para mejorar las predicciones a lo largo del tiempo.

Algoritmo de retropropagación

Las redes neuronales artificiales aprenden de forma continua mediante el uso de bucles de retroalimentación correctivos para mejorar su análisis predictivo. En pocas palabras, puede pensar en los datos que fluyen desde el nodo de entrada hasta el nodo de salida a través de muchos caminos diferentes en la red neuronal. Solo un camino es el correcto: el que asigna el nodo de entrada al nodo de salida correcto. Para encontrar este camino, la red neuronal utiliza un bucle de retroalimentación que funciona de la siguiente manera:

Cada nodo intenta adivinar el siguiente nodo de la ruta.

Se comprueba si la suposición es correcta. Los nodos asignan valores de peso más altos a las rutas que conducen a más suposiciones correctas y valores de peso más bajos a las rutas de los nodos que conducen a suposiciones incorrectas.

Para el siguiente punto de datos, los nodos realizan una predicción nueva con las trayectorias de mayor peso y luego repiten el paso 1.

Redes neuronales convolucionales (CNN)

Las capas ocultas de las redes neuronales convolucionales realizan funciones matemáticas específicas, como la síntesis o el filtrado, denominadas convoluciones. Son muy útiles para la clasificación de imágenes porque pueden extraer características relevantes de las imágenes que son útiles para el reconocimiento y la clasificación de imágenes. La forma nueva es más fácil de procesar sin perder características que son fundamentales para hacer una buena predicción. Cada capa oculta extrae y procesa diferentes características de la imagen, como los bordes, el color y la profundidad.

## **¿Cómo funcionan las redes neuronales?**

Una neurona es la unidad básica de procesamiento, similar a una neurona biológica, estas neuronas tienen conexiones de entrada a través de los que reciben estímulos externos, los valores de entrada. Con estos valores, la neurona realizará un cálculo interno y generará un valor de salida.

Internamente, la neurona utiliza todos los valores de entrada para realizar una suma ponderada de ellos. La ponderación de cada una de las entradas viene dada por el peso que se le asigna a cada una de las conexiones de entrada. Es decir, cada conexión que llega a nuestra neurona tendrá asociado un valor que servirá para definir con qué intensidad cada variable de entrada afecta a la neurona.

### **1. Suma ponderada de entradas**

Es un paso fundamental en el funcionamiento de una neurona artificial. Es la operación en la que se multiplican los valores de entrada por sus respectivos pesos, y luego se suman los productos. Esta operación calcula el potencial o activación previa de una neurona.

La neurona toma todas las entradas x1, x2, …. xn y las multiplica por sus respectivos pesos w1, w2, …. wn. Luego, realiza una suma:

```prolog
z = w1x1 + w2 x2 + … + wn xn + b
```

donde b es un valor adicional llamado sesgo (bias), que permite desplazar la función de activación y mejorar la capacidad de ajuste del modelo.

Pasos de su funcionamiento:

Entradas: La neurona recibe varios valores (por ejemplo, características de una imagen: color, brillo, bordes...).

Pesos: Cada entrada tiene un peso asociado que indica su importancia relativa.

Suma ponderada: Se multiplica cada entrada por su peso y se suman los resultados. A veces se le suma un bias (un valor adicional que ajusta la salida).

Función de activación: El resultado de la suma ponderada se pasa a través de una función no lineal (como ReLU, sigmoid, tanh) para decidir si la neurona "se activa" o no

Esta suma es importante para el aprendizaje durante el entrenamiento, los pesos (wiw_iwi​) se ajustan para que la salida de la red sea más precisa y  su capacidad de representación es decir que las combinaciones ponderadas permiten a la red "aprender" patrones complejos en los datos.

Se usa para: clasificación de imágenes, traducciones automáticas, reconocimiento de voz y predicción de valores.

### **2. Función de activación**

Esta función es un componente fundamental en las redes neuronales artificiales. Su objetivo principal es introducir no linealidad en el modelo, permitiendo que la red aprenda relaciones complejas entre los datos de entrada y salida. Sin una función de activación, una red neuronal sería simplemente una combinación lineal de sus entradas, lo que limitaría mucho su capacidad para resolver problemas reales.

Pasos de su funcionamiento:

Recibe una entrada numérica (el resultado de la suma ponderada de una neurona).

Transforma esa entrada aplicando una fórmula matemática.

Devuelve una salida que se pasa a la siguiente capa de la red.

Son importantes porque permiten aprender relaciones no lineales (como "si la entrada A es alta y B es baja, la salida es 1"). Hacen posible resolver problemas complejos como reconocimiento de imágenes, lenguaje natural, etc. Sin ellas, incluso una red profunda se comportaría como una simple regresión lineal.

El resultado z se pasa por la función, como la sigmoide, ReLU o tanh. Por ejemplo:´

```prolog
ReLU(z) = max⁡(0,z)
```

Esto da como salida un valor que luego se transmite a las neuronas de la siguiente capa.

## **¿Cómo aprenden las redes neuronales?**

El proceso de aprendizaje se realiza mediante un algoritmo llamado retropropagación (backpropagation) combinado con descenso del gradiente:

Propagación hacia adelante: Se pasan los datos de entrada por toda la red hasta obtener una predicción.

Cálculo del error: Se compara la salida obtenida con la salida esperada utilizando una función de error o pérdida.

Retropropagación: Se calcula cuánto contribuyó cada peso al error y se ajustan los pesos en consecuencia.

Actualización de pesos: Se modifican los pesos para minimizar el error, repitiendo este proceso muchas veces (épocas) hasta que la red aprende.

## **Lógica vs Redes neuronales**

La programación lógica se basa en reglas y hechos definidos de manera explícita, utilizando lógica formal para inferir conclusiones a partir de estos.

Por otro lado, las redes neuronales imitan el funcionamiento del cerebro humano, aprendiendo patrones a partir de datos y ajustando sus parámetros internos durante el proceso de entrenamiento.

Aunque las redes neuronales no se basan en reglas lógicas explícitas, pueden modelar relaciones complejas y no lineales entre entradas y salidas, lo que las hace útiles para tareas como el reconocimiento de patrones, el procesamiento del lenguaje natural y la visión por computador. En contraste, la programación lógica es más adecuada para problemas donde las reglas son claras y bien definidas.

## **Aplicación en Prolog para una red neuronal**

```prolog

% Red neuronal: clasifica si puede donar sangre

red_neuronal(X1, X2, Y) :-

w1(W1),

w2(W2),

b(B),

suma_ponderada(X1, X2, W1, W2, B, Z),

activacion(Z, Y).


% Pesos sinápticos y sesgo

w1(0.6).

w2(0.6).

b(-0.8).



% Cálculo de la suma ponderada

suma_ponderada(X1, X2, W1, W2, B, Z) :-

Z is X1 * W1 + X2 * W2 + B.



% Función de activación tipo umbral

activacion(Z, 1) :- Z >= 0. %puede donar sangre

activacion(Z, 0) :- Z < 0. %no puede donar sangre



% Base de conocimiento: personas

% persona(Nombre, MayorDeEdad, Saludable)

persona(ana, 1, 1).        % mayor y saludable

persona(juan, 1, 0).       % mayor pero no saludable

persona(lucia, 0, 1).      % menor pero saludable

persona(marcos, 0, 0).     % menor y no saludable



% Clasificación

clasificar_persona(Nombre) :-

persona(Nombre, X1, X2),

red_neuronal(X1, X2, Y),


Y = 1,

format('~w puede donar sangre.~n', [Nombre]).


clasificar_persona(Nombre) :-

persona(Nombre, X1, X2),

red_neuronal(X1, X2, Y),


Y = 0,

format('~w NO puede donar sangre.~n', [Nombre])
```

```prolog

?- clasificar_persona(ana).


ana puede donar sangre.
```

```prolog

?- clasificar_persona(marcos).


marcos NO puede donar sangre.
```