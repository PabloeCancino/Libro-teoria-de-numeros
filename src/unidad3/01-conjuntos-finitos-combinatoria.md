# 3.1 Conjuntos finitos, combinaciones y permutaciones

La combinatoria elemental —el arte de contar— es una herramienta indispensable en la teoría de números: como veremos en esta unidad, provee demostraciones alternativas, a menudo más transparentes, de resultados centrales como los teoremas de Fermat y de Wilson, y subyace a la teoría de las funciones aritméticas de la Unidad 4.

## Conjuntos finitos y la regla del producto

**Definición.** Un conjunto \\(A\\) es **finito** si existe \\(n\in\mathbb{N}\\) y una biyección \\(f:\\{1,\dots,n\\}\to A\\) (con la convención de que \\(\\{1,\dots,0\\}=\emptyset\\) corresponde a \\(A=\emptyset\\)). El único tal \\(n\\) (su unicidad se sigue del principio del palomar, discutido más abajo) se llama **cardinalidad** de \\(A\\) y se denota \\(|A|\\).

**Proposición 3.1 (regla de la suma).** *Si \\(A\\) y \\(B\\) son conjuntos finitos disjuntos (\\(A\cap B=\emptyset\\)), entonces \\(|A\cup B|=|A|+|B|\\). Más generalmente, si \\(A_1,\dots,A_k\\) son conjuntos finitos, disjuntos dos a dos, \\(|A_1\cup\cdots\cup A_k|=|A_1|+\cdots+|A_k|\\).*

**Proposición 3.2 (regla del producto).** *Si \\(A\\) y \\(B\\) son conjuntos finitos, el producto cartesiano \\(A\times B=\\{(a,b):a\in A,b\in B\\}\\) satisface \\(|A\times B|=|A|\cdot|B|\\). Más generalmente, si un objeto se construye eligiendo sucesivamente un elemento de un conjunto de \\(n_1\\) opciones, luego uno de \\(n_2\\) opciones (posiblemente dependiendo de la primera elección, pero siempre con exactamente \\(n_2\\) opciones disponibles), y así sucesivamente hasta \\(n_k\\) opciones, el número total de objetos distintos que se pueden construir es \\(n_1n_2\cdots n_k\\).*

Estas dos reglas —aparentemente triviales— son la base lógica de **todos** los argumentos de conteo de esta sección; las tomamos como axiomáticas (son, de hecho, consecuencia directa de los axiomas de Peano vía la definición recursiva de suma y producto).

**Proposición 3.3 (principio del palomar / pigeonhole).** *Si \\(n+1\\) objetos se distribuyen en \\(n\\) cajas, alguna caja recibe al menos dos objetos.*

*Demostración.* Por reducción al absurdo: si cada una de las \\(n\\) cajas recibiera a lo más un objeto, el número total de objetos distribuidos sería, por la Proposición 3.1, a lo más \\(n\\), contradiciendo que hay \\(n+1\\) objetos. \\(\blacksquare\\)

El principio del palomar, pese a su simplicidad, es sorprendentemente potente; se usará, por ejemplo, en la demostración del Lema 5.4 de la Unidad 5 (sobre sistemas completos de residuos) y reaparecerá en la Unidad 6 al estudiar fracciones continuas.

## Permutaciones

**Definición.** Una **permutación** de un conjunto de \\(n\\) elementos distintos es un arreglo ordenado de todos ellos.

**Proposición 3.4.** *El número de permutaciones de un conjunto de \\(n\\) elementos es*
\\[ n! = n(n-1)(n-2)\cdots2\cdot1, \\]
*con la convención \\(0!=1\\).*

*Demostración.* Para construir una permutación, elegimos sucesivamente el primer elemento (\\(n\\) opciones), luego el segundo entre los \\(n-1\\) restantes, y así sucesivamente hasta el último (1 opción). Por la regla del producto (Proposición 3.2), el total es \\(n(n-1)\cdots1=n!\\). \\(\blacksquare\\)

**Definición.** Una **permutación parcial** o **arreglo** de \\(k\\) elementos tomados de un conjunto de \\(n\\) (con \\(0\le k\le n\\)) es una selección **ordenada** de \\(k\\) de sus elementos, sin repetición.

**Proposición 3.5.** *El número de permutaciones parciales de \\(k\\) elementos tomados de un conjunto de \\(n\\) es*
\\[ P(n,k) = n(n-1)\cdots(n-k+1) = \frac{n!}{(n-k)!}. \\]

*Demostración.* Análoga a la Proposición 3.4: hay \\(n\\) opciones para el primer elemento, \\(n-1\\) para el segundo, ..., \\(n-k+1\\) para el \\(k\\)-ésimo. Por la regla del producto, \\(P(n,k)=n(n-1)\cdots(n-k+1)\\), que se reescribe como \\(\frac{n!}{(n-k)!}\\) multiplicando y dividiendo por \\((n-k)!=(n-k)(n-k-1)\cdots1\\). \\(\blacksquare\\)

## Combinaciones y coeficientes binomiales

**Definición.** Una **combinación** de \\(k\\) elementos tomados de un conjunto de \\(n\\) es una selección **no ordenada** (es decir, un subconjunto) de tamaño \\(k\\).

**Teorema 3.6.** *El número de subconjuntos de tamaño \\(k\\) de un conjunto de \\(n\\) elementos (\\(0\le k\le n\\)) es*
\\[ \binom{n}{k} = \frac{n!}{k!(n-k)!}. \\]

*Demostración.* Cada subconjunto de tamaño \\(k\\) da lugar a exactamente \\(k!\\) permutaciones parciales distintas (las \\(k!\\) formas de ordenar sus elementos), y toda permutación parcial de tamaño \\(k\\) proviene de exactamente un subconjunto de esta manera. Por la Proposición 3.2 (regla del producto, en su forma de "conteo doble"), \\(P(n,k) = \binom{n}{k}\cdot k!\\), de donde \\(\binom{n}{k}=P(n,k)/k! = \dfrac{n!}{(n-k)!\\,k!}\\). \\(\blacksquare\\)

**Proposición 3.7 (propiedades elementales de \\(\binom{n}{k}\\)).**

1. \\(\displaystyle\binom{n}{k}=\binom{n}{n-k}\\) (simetría).
2. \\(\displaystyle\binom{n}{0}=\binom{n}{n}=1\\).
3. \\(\displaystyle\binom{n}{k}\\) es siempre un entero (a pesar de que su fórmula involucra una división).

*Demostración.* (i) y (ii) son inmediatas de la fórmula del Teorema 3.6, o del argumento combinatorio (elegir los \\(k\\) elementos de un subconjunto es equivalente a elegir los \\(n-k\\) que se excluyen). (iii) es consecuencia directa de que \\(\binom{n}{k}\\) **cuenta** un conjunto de objetos (los subconjuntos de tamaño \\(k\\)), y por tanto es, tautológicamente, un entero no negativo —aunque la fórmula \\(n!/(k!(n-k)!)\\) no lo haga evidente algebraicamente. \\(\blacksquare\\)

La observación (iii) —que un cociente de factoriales sea siempre entero— es, de hecho, un resultado aritmético no trivial si se intenta demostrar directamente por manipulación de exponentes de primos (véase el Ejercicio 15 de esta unidad, que pide precisamente esa demostración alternativa usando la fórmula de Legendre para el exponente de un primo en \\(n!\\)); la demostración combinatoria dada arriba lo evita por completo, y es un buen ejemplo de cómo un argumento de conteo puede sustituir económicamente a un cálculo aritmético.

**Ejemplo 3.8.** El número de manos posibles de póker (5 cartas de una baraja de 52) es \\(\binom{52}{5} = \dfrac{52!}{5!\\,47!} = 2\\,598\\,960\\).

**Proposición 3.9 (Teorema del binomio).** *Para todo \\(n\ge0\\) y cualesquiera \\(x,y\\) (en un anillo conmutativo, en particular en \\(\mathbb{Z}\\)),*
\\[ (x+y)^n = \sum_{k=0}^n \binom{n}{k}x^{n-k}y^k. \\]

*Demostración.* Al expandir \\((x+y)^n=(x+y)(x+y)\cdots(x+y)\\) ( \\(n\\) factores), cada término del desarrollo se obtiene eligiendo, en cada uno de los \\(n\\) factores, o bien \\(x\\) o bien \\(y\\); el término \\(x^{n-k}y^k\\) se obtiene exactamente cuando se elige \\(y\\) en \\(k\\) de los \\(n\\) factores (y \\(x\\) en los \\(n-k\\) restantes), y el número de maneras de elegir **cuáles** \\(k\\) factores aportan \\(y\\) es, por definición, \\(\binom nk\\). Sumando sobre todos los valores de \\(k\\) se obtiene la fórmula. \\(\blacksquare\\)

Este resultado será la herramienta central de la Sección 3.2 (triángulo de Pascal) y de la Sección 3.3 (demostración combinatoria del teorema de Fermat).
