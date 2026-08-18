# Apéndice A. Técnicas de demostración

Este apéndice resume, a modo de referencia rápida, las principales técnicas de demostración usadas a lo largo del libro. No sustituye la lectura de la Sección 1.1, sino que la complementa como recordatorio conciso.

## Demostración directa

Se parte de las hipótesis y, mediante una cadena de implicaciones lógicas válidas, se llega a la conclusión. Es el estilo más común en el libro para las propiedades básicas de divisibilidad (Proposición 1.9) y de congruencias (Proposición 5.1).

## Demostración por contrapositiva

Para demostrar \\(P\Rightarrow Q\\), se demuestra la implicación lógicamente equivalente \\(\neg Q\Rightarrow\neg P\\). Es útil cuando la negación de la conclusión ofrece más información explícita para trabajar que la hipótesis original.

## Demostración por reducción al absurdo (contradicción)

Se supone que la conclusión deseada es falsa (junto con las hipótesis verdaderas) y se deriva una contradicción lógica, lo que fuerza a que la conclusión sea verdadera. Ejemplos centrales en el libro: la infinitud de los primos (Teorema 2.3), la irracionalidad de \\(\sqrt n\\) (Proposición 2.17), y la unicidad de la factorización en primos (Teorema 2.11).

## Inducción matemática

Descrita en detalle en la Sección 1.1 (Teoremas 1.1 y 1.4). Se usa para demostrar afirmaciones \\(P(n)\\) para todo entero \\(n\\) a partir de un caso base y un paso inductivo. La variante **fuerte** (Teorema 1.4) permite usar la validez de \\(P\\) en *todos* los valores anteriores, no solo el inmediatamente previo, y es indispensable en demostraciones como la existencia de factorización en primos (Teorema 2.11).

## El principio del buen orden

Equivalente lógico de la inducción (Teoremas 1.5 y 1.6), se usa típicamente para garantizar la **existencia** de un objeto extremal (mínimo o máximo) con cierta propiedad: el residuo de una división (Teorema 1.12), el máximo común divisor (Teorema 1.16), el menor divisor primo de un número (Proposición 2.1), o el elemento inicial de un argumento de descenso infinito (Ejercicio 33 de la Unidad 1).

## Descenso infinito

Una variante del principio del buen orden, popularizada por Fermat: se supone la existencia de una solución de cierto problema y, a partir de ella, se construye una solución "menor" (en algún sentido preciso, como el valor de una de las variables), contradiciendo la existencia de una solución mínima garantizada por el buen orden. Se ilustra en el Ejercicio 33 de la Unidad 1 (caso \\(n=4\\) del Último Teorema de Fermat).

## Argumentos combinatorios (conteo doble, biyecciones)

Consisten en contar el mismo conjunto de dos maneras distintas, o en establecer una biyección entre dos conjuntos para concluir que tienen la misma cardinalidad. Son el corazón de la Unidad 3 (por ejemplo, las demostraciones combinatorias de los Teoremas de Fermat y Wilson, Sección 3.3) y aparecen también en la Unidad 4 (identidad de Gauss, Teorema 4.17) y en la Unidad 5 (Teorema de Euler, Teorema 5.10).

## El principio del palomar

Un caso particular, pero enormemente útil, de argumento de conteo: si se distribuyen más objetos que cajas disponibles, alguna caja recibe más de un objeto (Proposición 3.3). Se usa, entre otros lugares, para justificar la biyectividad de la función auxiliar en la demostración de la multiplicatividad de φ (Teorema 4.13).

## Recomendaciones generales

Al enfrentar un problema nuevo de teoría de números, suele ser útil preguntarse:

- ¿Puedo reducir el problema a un caso ya conocido, mediante divisibilidad, congruencias, o factorización en primos?
- ¿Existe una cantidad (un entero no negativo) que decrece o se acota en cada paso de un posible argumento inductivo o de descenso?
- ¿El problema tiene una interpretación de conteo (subconjuntos, arreglos, particiones) que permita un argumento combinatorio directo?
- ¿Qué ocurre si clasifico los casos según el residuo de las variables involucradas módulo un entero pequeño (2, 3, 4, ...)?

Estas preguntas orientan a un porcentaje considerable de los ejercicios propuestos en cada unidad.
