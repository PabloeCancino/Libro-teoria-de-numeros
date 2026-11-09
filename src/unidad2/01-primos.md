# 2.1 Números primos, números relativos y la criba de Eratóstenes

## Definición y primeras propiedades

**Definición.** Un entero \\(p > 1\\) se llama **primo** si sus únicos divisores positivos son \\(1\\) y \\(p\\). Un entero \\(n>1\\) que no es primo se llama **compuesto**: existe entonces un divisor \\(d\\) de \\(n\\) con \\(1<d<n\\).

Por convención, el entero \\(1\\) no se considera ni primo ni compuesto (es la **unidad** del anillo \\(\mathbb{Z}\\)); esta convención, aparentemente arbitraria, resulta indispensable para que el Teorema Fundamental de la Aritmética (Sección 2.2) sea válido tal como se enuncia, evitando que \\(6=2\cdot3=1\cdot2\cdot3=1\cdot1\cdot2\cdot3=\cdots\\) tenga infinitas factorizaciones "distintas".

**Proposición 2.1.** *Todo entero \\(n>1\\) tiene al menos un divisor primo.*

*Demostración.* Sea \\(S\\) el conjunto de divisores de \\(n\\) que son mayores que \\(1\\). Como \\(n \in S\\), \\(S \neq \emptyset\\), y por el Principio del Buen Orden, \\(S\\) tiene un elemento mínimo \\(p\\). Afirmamos que \\(p\\) es primo: si no lo fuera, tendría un divisor \\(d\\) con \\(1<d<p\\); pero entonces \\(d \mid p \mid n\\) (Proposición 1.9(i)) da \\(d \mid n\\) con \\(d \in S\\) y \\(d<p\\), contradiciendo la minimalidad de \\(p\\). Luego \\(p\\) es primo y \\(p \mid n\\). \\(\blacksquare\\)

**Proposición 2.2 (Lema de Euclides, versión para primos).** *Sea \\(p\\) primo. Si \\(p \mid ab\\), entonces \\(p \mid a\\) o \\(p \mid b\\). Más generalmente, si \\(p \mid a_1a_2\cdots a_k\\), entonces \\(p \mid a_i\\) para algún \\(i\\).*

*Demostración.* Si \\(p \mid a\\), no hay nada que probar. Si \\(p \nmid a\\), como los únicos divisores positivos de \\(p\\) son \\(1\\) y \\(p\\), y \\(p\\) no divide a \\(a\\), se sigue \\(\gcd(p,a)=1\\). Por la Proposición 1.19(vi) (Lema de Euclides general), de \\(p \mid ab\\) y \\(\gcd(p,a)=1\\) se obtiene \\(p \mid b\\).

La versión general se sigue por inducción sobre \\(k\\): el caso \\(k=1\\) es trivial y el caso \\(k=2\\) es lo que acabamos de probar. Si vale para \\(k-1\\) factores, y \\(p \mid a_1\cdots a_{k-1}\cdot a_k\\), aplicando el caso \\(k=2\\) con \\(a=a_1\cdots a_{k-1}\\) y \\(b=a_k\\): \\(p \mid a_1\cdots a_{k-1}\\) o \\(p \mid a_k\\); en el primer caso, la hipótesis de inducción da \\(p \mid a_i\\) para algún \\(i \le k-1\\). \\(\blacksquare\\)

Esta propiedad es, de hecho, **característica** de los números primos entre los enteros mayores que 1: se puede demostrar (Ejercicio 8 de esta sección) que si \\(n>1\\) tiene la propiedad de que \\(n\mid ab \Rightarrow n\mid a\ \text{o}\ n\mid b\\) para todos \\(a,b\\), entonces \\(n\\) es primo.

## Infinitud de los números primos

**Teorema 2.3 (Euclides).** *Existen infinitos números primos.*

*Demostración (la demostración original de Euclides, por reducción al absurdo).* Supongamos que solo hay finitos primos, digamos \\(p_1,p_2,\dots,p_r\\) (la lista completa). Consideremos el entero
\\[ N = p_1p_2\cdots p_r + 1. \\]
Como \\(N>1\\), por la Proposición 2.1, \\(N\\) tiene un divisor primo \\(p\\). Como \\(p_1,\dots,p_r\\) son *todos* los primos, \\(p=p_i\\) para algún \\(i\\). Pero entonces \\(p_i \mid N\\) y \\(p_i \mid p_1\cdots p_r\\), luego \\(p_i \mid \big(N-p_1\cdots p_r\big)=1\\) (Proposición 1.9(ii)), lo cual es absurdo pues \\(p_i \ge 2\\). Esta contradicción muestra que no puede haber solo finitos primos. \\(\blacksquare\\)

**Observación 2.4.** El número \\(N=p_1\cdots p_r+1\\) no es necesariamente primo; lo único que garantiza la demostración es que *algún* divisor primo de \\(N\\) no está en la lista original. Por ejemplo, \\(2\cdot3\cdot5\cdot7\cdot11\cdot13+1=30031=59\cdot509\\) es compuesto, y en efecto ni 59 ni 509 estaban en la lista de los primeros seis primos.

La demostración de Euclides admite numerosas variantes que producen infinitud de primos en *progresiones aritméticas* particulares; dos casos (primos de la forma \\(4k+1\\) y \\(8k+5\\)) se demostrarán en los Corolarios 5.20 y 5.21 de la Unidad 5. El resultado general —el **Teorema de Dirichlet**, que afirma que toda progresión aritmética \\(a, a+n, a+2n,\dots\\) con \\(\gcd(a,n)=1\\) contiene infinitos primos— requiere herramientas de teoría analítica de números y queda fuera del alcance de este curso.

**Proposición 2.5 (una cota elemental sobre la distribución de primos).** *Si \\(p_n\\) denota el \\(n\\)-ésimo primo (en orden creciente, \\(p_1=2,p_2=3,\dots\\)), entonces \\(p_n \le 2^{2^{n-1}}\\).*

*Demostración.* Por inducción. Para \\(n=1\\), \\(p_1=2=2^{2^0}\\). Supongamos \\(p_k \le 2^{2^{k-1}}\\) para todo \\(k\le n\\). El entero \\(p_1p_2\cdots p_n+1\\) tiene, por la Proposición 2.1, un divisor primo, que necesariamente es distinto de \\(p_1,\dots,p_n\\) (por el mismo argumento del Teorema 2.3), luego es \\(\ge p_{n+1}\\). Por tanto,
\\[ p_{n+1} \le p_1p_2\cdots p_n + 1 \le 2^{2^0}2^{2^1}\cdots2^{2^{n-1}}+1 = 2^{2^0+2^1+\cdots+2^{n-1}}+1=2^{2^n-1}+1 \le 2^{2^n}, \\]
usando la hipótesis de inducción y que \\(2^{2^n-1}+1\le 2^{2^n}\\) para \\(n\ge1\\). \\(\blacksquare\\)

Esta cota es muy débil comparada con el comportamiento real (el **Teorema de los Números Primos** da la estimación asintótica mucho más precisa \\(p_n \sim n\ln n\\)), pero tiene la virtud de ser completamente elemental.

## Números primos entre sí

**Definición (recordatorio de la Sección 1.3).** Dos enteros \\(a,b\\) son **primos relativos** o **coprimos** si \\(\gcd(a,b)=1\\). Más generalmente, los enteros \\(a_1,\dots,a_k\\) se dicen **primos relativos dos a dos** si \\(\gcd(a_i,a_j)=1\\) para todo \\(i\neq j\\) (una condición estrictamente más fuerte que \\(\gcd(a_1,\dots,a_k)=1\\); por ejemplo, \\(\gcd(6,10,15)=1\\) pero no son primos relativos dos a dos).

**Proposición 2.6.** *Sean \\(a,b\in\mathbb{Z}^+\\). Entonces \\(\gcd(a,b)=1\\) si y solo si \\(a\\) y \\(b\\) no comparten ningún divisor primo.*

*Demostración.* Si \\(\gcd(a,b)=1\\) y \\(p\\) fuera un primo que divide a ambos, entonces \\(p\\) sería un divisor común mayor que \\(1\\), contradiciendo que el máximo común divisor es \\(1\\). Recíprocamente, si \\(a\\) y \\(b\\) no comparten divisores primos, sea \\(d=\gcd(a,b)\\); si \\(d>1\\), por la Proposición 2.1, \\(d\\) tendría un divisor primo \\(p\\), y como \\(p\mid d \mid a\\) y \\(p \mid d \mid b\\), \\(p\\) sería un divisor primo común, contradicción. Luego \\(d=1\\). \\(\blacksquare\\)

## La criba de Eratóstenes

El siguiente resultado, atribuido a Eratóstenes de Cirene (c. 200 a.C.), es la base de un método efectivo —la **criba**— para listar todos los primos hasta un límite dado, y también proporciona un criterio práctico para decidir si un número dado es primo.

**Proposición 2.7.** *Si \\(n>1\\) es compuesto, entonces \\(n\\) tiene un divisor primo \\(p \le \sqrt{n}\\).*

*Demostración.* Como \\(n\\) es compuesto, \\(n=ab\\) con \\(1<a\le b<n\\). Si \\(a>\sqrt{n}\\) y \\(b>\sqrt n\\), entonces \\(ab>n\\), contradicción; luego \\(a \le \sqrt n\\). Por la Proposición 2.1, \\(a\\) tiene un divisor primo \\(p\\), y \\(p \le a \le \sqrt n\\) (Proposición 1.9(iii)); además \\(p \mid a \mid n\\). \\(\blacksquare\\)

**Corolario 2.8 (criterio de primalidad por ensayo de divisiones).** *Un entero \\(n>1\\) es primo si y solo si no es divisible por ningún primo \\(p \le \sqrt n\\).*

Este corolario es la base del **algoritmo de la criba de Eratóstenes** para listar todos los primos \\(\le N\\):

1. Escríbanse todos los enteros de \\(2\\) a \\(N\\) en una lista.
2. Sea \\(p=2\\) el primer número no tachado de la lista.
3. Táchense todos los múltiplos propios de \\(p\\) (es decir, \\(2p,3p,4p,\dots\\), pero no \\(p\\) mismo).
4. Sea \\(p\\) el siguiente número no tachado mayor que el anterior; si \\(p>\sqrt N\\), deténgase: los números no tachados son exactamente los primos \\(\le N\\). En caso contrario, regrese al paso 3.

La validez del algoritmo es consecuencia inmediata del Corolario 2.8: un número compuesto \\(n \le N\\) necesariamente es tachado al procesar alguno de sus divisores primos \\(p\le\sqrt n \le \sqrt N\\).

**Ejemplo 2.9.** Para hallar los primos \\(\le 50\\): como \\(\sqrt{50}<8\\), basta tachar los múltiplos propios de \\(2,3,5,7\\). Al terminar, los números no tachados son:
\\[ 2,3,5,7,11,13,17,19,23,29,31,37,41,43,47. \\]

**Ejemplo 2.10.** Para verificar que \\(541\\) es primo (usando el Corolario 2.8), basta comprobar que no es divisible por ningún primo \\(\le\sqrt{541}\approx23.3\\), es decir, por \\(2,3,5,7,11,13,17,19,23\\). Verificando cada caso (los detalles se dejan al lector), ninguno divide a \\(541\\), luego \\(541\\) es primo.

Aunque la criba de Eratóstenes y el ensayo de divisiones son completamente correctos y elementales, son muy ineficientes para números grandes (de cientos de dígitos, como los usados en criptografía); los tests de primalidad modernos, mucho más rápidos, se apoyan en el Pequeño Teorema de Fermat y sus refinamientos, que estudiaremos en la Unidad 5.
