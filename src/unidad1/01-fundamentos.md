# 1.1 Los axiomas de Peano y el principio del buen orden

## Los axiomas de Peano

Toda la teoría de números se construye, en última instancia, sobre el conjunto de los números naturales. En 1889 Giuseppe Peano propuso una axiomatización de \\(\mathbb{N}\\) que captura de manera precisa nuestra intuición de "contar". La presentamos aquí en una versión moderna, con la función sucesor como noción primitiva.

**Axiomas de Peano.** Un conjunto \\(\mathbb{N}\\), junto con un elemento distinguido \\(0 \in \mathbb{N}\\) y una función \\(S : \mathbb{N} \to \mathbb{N}\\) (el *sucesor*), satisface los axiomas de Peano si:

1. \\(0 \in \mathbb{N}\\).
2. Para todo \\(n \in \mathbb{N}\\), \\(S(n) \in \mathbb{N}\\) (cerradura del sucesor).
3. No existe \\(n \in \mathbb{N}\\) tal que \\(S(n) = 0\\) (el cero no es sucesor de nadie).
4. Si \\(S(m) = S(n)\\), entonces \\(m = n\\) (el sucesor es inyectivo).
5. **(Axioma de inducción.)** Si \\(A \subseteq \mathbb{N}\\) satisface (i) \\(0 \in A\\) y (ii) \\(n \in A \Rightarrow S(n) \in A\\), entonces \\(A = \mathbb{N}\\).

Intuitivamente, \\(S(n) = n+1\\); los axiomas 1-4 garantizan que \\(\mathbb{N} = \\{0, S(0), S(S(0)), \dots\\} = \\{0,1,2,3,\dots\\}\\) es una sucesión sin repeticiones que comienza en \\(0\\) y no tiene "vueltas". El quinto axioma, el de inducción, es el que dota a \\(\mathbb{N}\\) de su fuerza demostrativa y es, junto con el principio del buen orden que veremos a continuación, la herramienta central de todo el curso.

A partir de estos axiomas se definen recursivamente la suma (\\(a + 0 = a\\), \\(a + S(b) = S(a+b)\\)) y el producto (\\(a \cdot 0 = 0\\), \\(a \cdot S(b) = a\cdot b + a\\)), y se demuestran —aunque no lo haremos aquí, por ser objeto de un curso de fundamentos— las propiedades algebraicas usuales: asociatividad, conmutatividad, distributividad, cancelación, y la existencia de un orden total \\(\le\\) compatible con ellas. En este texto damos por conocidas estas propiedades y las usaremos libremente, junto con la extensión de \\(\mathbb{N}\\) al anillo \\(\mathbb{Z}\\) de los enteros mediante la adjunción de los inversos aditivos.

## El principio de inducción matemática

El axioma de inducción se traduce, en la práctica demostrativa, en el siguiente esquema.

**Teorema 1.1 (Principio de inducción matemática, primera forma).** *Sea \\(P(n)\\) una proposición que depende de \\(n \in \mathbb{Z}^+\\) (o de \\(n \in \mathbb{N}\\)). Supóngase que:*

1. *(Base) \\(P(1)\\) es verdadera (respectivamente, \\(P(0)\\)).*
2. *(Paso inductivo) Para todo \\(k \ge 1\\), si \\(P(k)\\) es verdadera entonces \\(P(k+1)\\) es verdadera.*

*Entonces \\(P(n)\\) es verdadera para todo \\(n \ge 1\\) (respectivamente, para todo \\(n \ge 0\\)).*

*Demostración.* Sea \\(A = \\{n \in \mathbb{Z}^+ : P(n) \text{ es verdadera}\\}\\). Por la hipótesis (1), \\(1 \in A\\). Por la hipótesis (2), si \\(k \in A\\) entonces \\(k+1 \in A\\). Por el axioma de inducción (aplicado a \\(\mathbb{Z}^+\\), que es una copia de \\(\mathbb{N}\\) desplazada en 1), se concluye \\(A = \mathbb{Z}^+\\), es decir, \\(P(n)\\) es verdadera para todo \\(n \ge 1\\). \\(\blacksquare\\)

A la hipótesis "\\(P(k)\\) es verdadera" en el paso inductivo se le llama **hipótesis de inducción**.

**Ejemplo 1.2.** Demostremos que para todo \\(n \ge 1\\),
\\[ 1 + 2 + \dots + n = \frac{n(n+1)}{2}. \\]

*Base.* Para \\(n=1\\): el lado izquierdo es \\(1\\) y el derecho es \\(\frac{1 \cdot 2}{2} = 1\\). Se cumple.

*Paso inductivo.* Supongamos que \\(1 + 2 + \dots + k = \frac{k(k+1)}{2}\\) para algún \\(k \ge 1\\) (hipótesis de inducción). Entonces
\\[ 1 + 2 + \dots + k + (k+1) = \frac{k(k+1)}{2} + (k+1) = (k+1)\left(\frac{k}{2} + 1\right) = \frac{(k+1)(k+2)}{2}, \\]
que es precisamente la fórmula para \\(n = k+1\\). Por el Teorema 1.1, la fórmula vale para todo \\(n \ge 1\\). \\(\blacksquare\\)

**Ejemplo 1.3.** Demostremos que \\(3 \mid (4^n - 1)\\) para todo \\(n \ge 0\\) (anticipando la definición formal de divisibilidad de la siguiente sección: esto significa que \\(4^n - 1\\) es múltiplo de 3).

*Base.* \\(n = 0\\): \\(4^0 - 1 = 0 = 3 \cdot 0\\).

*Paso inductivo.* Supongamos \\(4^k - 1 = 3m\\) para algún entero \\(m\\). Entonces
\\[ 4^{k+1} - 1 = 4 \cdot 4^k - 1 = 4(4^k - 1) + 4 - 1 = 4(3m) + 3 = 3(4m+1), \\]
que es múltiplo de 3. \\(\blacksquare\\)

A veces la hipótesis de inducción "\\(P(k)\\) verdadera" es insuficiente y se necesita suponer la validez de \\(P\\) para *todos* los valores anteriores a \\(k+1\\). Esto da lugar a una variante lógicamente equivalente pero muy útil en la práctica.

**Teorema 1.4 (Principio de inducción fuerte).** *Sea \\(P(n)\\) una proposición para \\(n \in \mathbb{Z}^+\\). Supóngase que:*

1. *\\(P(1)\\) es verdadera.*
2. *Para todo \\(k \ge 1\\), si \\(P(1), P(2), \dots, P(k)\\) son todas verdaderas, entonces \\(P(k+1)\\) es verdadera.*

*Entonces \\(P(n)\\) es verdadera para todo \\(n \ge 1\\).*

*Demostración.* Sea \\(Q(n)\\) la proposición "\\(P(1) \wedge P(2) \wedge \dots \wedge P(n)\\)". Por hipótesis, \\(Q(1) = P(1)\\) es verdadera. Si \\(Q(k)\\) es verdadera, la hipótesis (2) da que \\(P(k+1)\\) es verdadera, y por tanto \\(Q(k+1) = Q(k) \wedge P(k+1)\\) también lo es. Por el Teorema 1.1, \\(Q(n)\\) es verdadera para todo \\(n\\), y en particular \\(P(n)\\) lo es para todo \\(n \ge 1\\). \\(\blacksquare\\)

La inducción fuerte será indispensable, por ejemplo, en la demostración de la existencia de la factorización en primos (Unidad 2).

## El principio del buen orden

**Definición.** Un conjunto ordenado \\((X, \le)\\) está **bien ordenado** si todo subconjunto no vacío de \\(X\\) tiene un elemento mínimo.

**Axioma (Principio del Buen Orden, PBO).** *Todo subconjunto no vacío de \\(\mathbb{N}\\) tiene un elemento mínimo.*

Nótese que el orden usual de \\(\mathbb{Z}\\) **no** es un buen orden (por ejemplo, \\(\mathbb{Z}\\) mismo no tiene mínimo), pero sí lo es el de cualquier subconjunto de \\(\mathbb{Z}\\) acotado inferiormente, en particular el de \\(\mathbb{N}\\) y el de cualquier conjunto de enteros positivos.

El resultado más importante de esta sección es que, sobre la base de los demás axiomas de \\(\mathbb{N}\\) (orden, suma compatible, etc.), el **principio del buen orden es equivalente al principio de inducción**. Esto significa que se puede tomar cualquiera de los dos como axioma y demostrar el otro como teorema; en la práctica, usaremos el que resulte más conveniente en cada demostración.

**Teorema 1.5.** *El principio de inducción matemática (Teorema 1.1) implica el principio del buen orden.*

*Demostración.* Sea \\(S \subseteq \mathbb{N}\\) no vacío y supongamos, por reducción al absurdo, que \\(S\\) no tiene elemento mínimo. Sea \\(P(n)\\) la proposición "\\(n \notin S\\)". Vamos a demostrar por inducción fuerte que \\(P(n)\\) es verdadera para todo \\(n\\), lo que dará \\(S = \emptyset\\), una contradicción.

*Base.* Si \\(0 \in S\\), entonces \\(0\\) sería el mínimo de \\(S\\) (pues \\(0 \le n\\) para todo \\(n \in \mathbb{N}\\)), contradiciendo la suposición. Luego \\(0 \notin S\\), es decir, \\(P(0)\\) es verdadera.

*Paso inductivo.* Supongamos que \\(P(0), P(1), \dots, P(k)\\) son todas verdaderas, es decir, ninguno de \\(0, 1, \dots, k\\) pertenece a \\(S\\). Si \\(k+1 \in S\\), entonces \\(k+1\\) sería el elemento mínimo de \\(S\\) (ya que todo elemento menor, es decir, todo elemento de \\(\\{0,\dots,k\\}\\), no está en \\(S\\)), lo cual contradice la suposición. Luego \\(k+1 \notin S\\), es decir, \\(P(k+1)\\) es verdadera.

Por el Teorema 1.4, \\(P(n)\\) es verdadera para todo \\(n\\), es decir, \\(S \cap \mathbb{N} = \emptyset\\), luego \\(S = \emptyset\\). Esto contradice que \\(S\\) es no vacío. La contradicción muestra que \\(S\\) sí tiene un mínimo. \\(\blacksquare\\)

**Teorema 1.6.** *El principio del buen orden implica el principio de inducción matemática.*

*Demostración.* Sea \\(P(n)\\) una proposición sobre \\(\mathbb{N}\\) que satisface la base \\(P(0)\\) y el paso inductivo \\(P(k) \Rightarrow P(k+1)\\). Sea
\\[ S = \\{n \in \mathbb{N} : P(n) \text{ es falsa}\\}. \\]
Queremos ver \\(S = \emptyset\\). Supongamos, por reducción al absurdo, que \\(S \neq \emptyset\\). Por el PBO, \\(S\\) tiene un elemento mínimo \\(m\\). Como \\(P(0)\\) es verdadera, \\(0 \notin S\\), luego \\(m \ge 1\\), y por tanto \\(m - 1 \in \mathbb{N}\\). Como \\(m\\) es el mínimo de \\(S\\), \\(m - 1 \notin S\\), es decir, \\(P(m-1)\\) es verdadera. Por el paso inductivo (aplicado a \\(k = m-1\\)), \\(P(m)\\) es verdadera, es decir, \\(m \notin S\\). Esto contradice que \\(m \in S\\). Luego \\(S = \emptyset\\) y \\(P(n)\\) es verdadera para todo \\(n \in \mathbb{N}\\). \\(\blacksquare\\)

En conjunto, los Teoremas 1.5 y 1.6 muestran la equivalencia buscada:
\\[ \text{Inducción} \iff \text{Buen Orden}. \\]

Ambos principios reaparecerán constantemente: la inducción como técnica demostrativa directa, y el buen orden como herramienta para garantizar la **existencia** de objetos mínimos (el cociente y residuo en el algoritmo de la división, el máximo común divisor, el menor divisor primo, etc.), típicamente por reducción al absurdo tomando el elemento mínimo de un conjunto de "contraejemplos" o de "candidatos".

**Ejemplo 1.7 (uso del buen orden).** No existe ningún entero \\(n\\) con \\(0 < n < 1\\). En efecto, si el conjunto \\(S = \\{n \in \mathbb{Z}^+ : n < 1\\}\\) fuera no vacío, por el PBO tendría un mínimo \\(m\\), con \\(0 < m < 1\\). Pero entonces \\(0 < m^2 < m < 1\\) (pues \\(0<m<1\\)), y \\(m^2 \in \mathbb{Z}^+\\) sería un elemento de \\(S\\) menor que \\(m\\), contradiciendo la minimalidad de \\(m\\). Luego \\(S = \emptyset\\).

Este hecho, aparentemente trivial, es la base de numerosos argumentos de "descenso infinito" que usaremos más adelante (por ejemplo, en la demostración de la irracionalidad de \\(\sqrt{2}\\) o en ciertos argumentos sobre ecuaciones diofánticas).
