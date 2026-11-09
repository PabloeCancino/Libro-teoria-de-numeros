# 5.3 Los teoremas de Euler y Fermat; pseudoprimos

## El Pequeño Teorema de Fermat como corolario

**Teorema 5.13 (Pequeño Teorema de Fermat).** *Sea \\(p\\) un número primo. Entonces, para todo \\(a\in\mathbb{Z}\\) no divisible por \\(p\\),*
\\[ a^{p-1}\equiv1\pmod p. \\]
*Como consecuencia, \\(a^p\equiv a\pmod p\\) para **cualquier** \\(a\in\mathbb{Z}\\).*

*Demostración.* Como \\(p\\) es primo, \\(\varphi(p)=p-1\\) (Ejemplo 4.11). Si \\(\gcd(a,p)=1\\) (es decir, \\(p\nmid a\\), pues los únicos divisores de \\(p\\) son \\(1\\) y \\(p\\)), el Teorema de Euler (Teorema 5.10) da directamente \\(a^{p-1}\equiv1\pmod p\\).

Para la consecuencia: si \\(p\nmid a\\), multiplicando \\(a^{p-1}\equiv1\pmod p\\) por \\(a\\) (Proposición 5.1(v)) se obtiene \\(a^p\equiv a\pmod p\\). Si en cambio \\(p\mid a\\), entonces \\(a^p\equiv0\equiv a\pmod p\\) trivialmente (ambos son congruentes con \\(0\\)). En cualquier caso, \\(a^p\equiv a\pmod p\\). \\(\blacksquare\\)

Este teorema ya fue demostrado, por un método combinatorio completamente distinto (acción de rotación sobre secuencias), en el Teorema 3.17 de la Unidad 3; se recomienda comparar ambas demostraciones.

## Pseudoprimos y números de Carmichael

El Pequeño Teorema de Fermat da una **condición necesaria** para la primalidad: si \\(p\\) es primo, entonces \\(a^p\equiv a\pmod p\\) para todo \\(a\\). Cabría preguntarse si el recíproco es cierto —si \\(n\\) satisface \\(a^n\equiv a\pmod n\\), ¿es \\(n\\) necesariamente primo? La respuesta, sorprendentemente, es **no**.

**Definición.** Un entero compuesto \\(n\\) se llama **pseudoprimo en base \\(a\\)** si \\(a^n\equiv a\pmod n\\). Se llama simplemente **pseudoprimo** si es pseudoprimo en base \\(2\\), es decir, si \\(2^n\equiv2\pmod n\\). Se llama **pseudoprimo absoluto** o **número de Carmichael** si es pseudoprimo en base \\(a\\) para **todo** entero \\(a\\).

Durante mucho tiempo se atribuyó —erróneamente, según los historiadores— a matemáticos chinos antiguos la conjetura de que \\(2^n\equiv2\pmod n\\) implica que \\(n\\) es primo (la llamada «hipótesis china», que procede de una mala traducción difundida en el siglo XIX); el primer contraejemplo, \\(n=341=11\times31\\), lo dio Sarrus en 1819. Se sabe que existen infinitos pseudoprimos (en cualquier base fija): si \\(n\\) es un pseudoprimo impar, se puede demostrar que \\(2^n-1\\) también lo es, lo que permite generar infinitos a partir de uno solo.

Los números de Carmichael son considerablemente más raros y más difíciles de construir, pero también se sabe (Alford, Granville y Pomerance, 1994, resolviendo una conjetura de más de 80 años) que existen infinitos. El siguiente resultado da un criterio práctico para reconocerlos y construirlos; de hecho, por el **criterio de Korselt** (1899), la condición también es necesaria: todo número de Carmichael es producto de al menos tres primos distintos \\(p_i\\) que cumplen \\((p_i-1)\mid(n-1)\\).

**Proposición 5.14.** *Sea \\(n=p_1p_2\cdots p_r\\) un producto de \\(r>1\\) primos distintos. Si para cada \\(i=1,\dots,r\\) se cumple \\((p_i-1)\mid(n-1)\\), entonces \\(n\\) es un número de Carmichael.*

*Demostración.* Como \\(r>1\\), \\(n\\) es compuesto. Debemos ver que \\(a^n\equiv a\pmod{p_1p_2\cdots p_r}\\) para todo entero \\(a\\); por la Proposición 5.7 (reducción a módulos coprimos), basta ver que \\(a^n\equiv a\pmod{p_i}\\) para cada \\(i\\). Esto es evidente si \\(p_i\mid a\\) (ambos lados son \\(\equiv0\\)). Si \\(p_i\nmid a\\), por el Teorema 5.13 (Fermat), \\(a^{p_i-1}\equiv1\pmod{p_i}\\); como por hipótesis \\((p_i-1)\mid(n-1)\\), digamos \\(n-1=(p_i-1)k\\), se sigue \\(a^{n-1}=(a^{p_i-1})^k\equiv1^k=1\pmod{p_i}\\), y multiplicando por \\(a\\), \\(a^n\equiv a\pmod{p_i}\\). \\(\blacksquare\\)

**Ejemplo 5.15.** Con la Proposición 5.14 se verifica que \\(561=3\times11\times17\\) es un número de Carmichael (de hecho, el más pequeño de todos, descubierto por Carmichael en 1910): \\(560=(3-1)\cdot280=(11-1)\cdot56=(17-1)\cdot35\\), así que \\(2\mid560\\), \\(10\mid560\\) y \\(16\mid560\\) se verifican directamente. Otros ejemplos que satisfacen el criterio de la proposición son \\(1729=7\times13\times19\\), \\(6601=7\times23\times41\\) y \\(10585=5\times29\times73\\). También satisfacen el criterio \\(1105=5\times13\times17\\), \\(2821=7\times13\times31\\) y \\(15841=7\times31\times73\\); y algunos con más de tres factores primos, como \\(16\\,046\\,641=13\times37\times73\times457\\) (descubierto por el propio Carmichael, uno de los pocos conocidos originalmente con cuatro factores). Se sabe que hay únicamente 43 números de Carmichael menores que un millón —una rareza notable frente a la infinitud de primos.

## El Teorema de Wilson

**Ejemplo 5.16 (motivación).** En el conjunto de residuos no nulos módulo \\(11\\), \\(\\{1,2,\dots,10\\}\\), se observan los pares disjuntos \\(\\{2,6\\}\\), \\(\\{3,4\\}\\), \\(\\{5,9\\}\\), \\(\\{7,8\\}\\), cada uno con producto \\(\equiv1\pmod{11}\\) (además de \\(1\\) y \\(10\equiv-1\\), que son sus propios inversos). Multiplicando:
\\[ 2\cdot3\cdot4\cdot5\cdot6\cdot7\cdot8\cdot9 = (2\cdot6)(3\cdot4)(5\cdot9)(7\cdot8) \equiv 1\cdot1\cdot1\cdot1 = 1\pmod{11}. \\]
Esto no es casualidad, y el mismo fenómeno ocurre para cualquier módulo primo, dando lugar al siguiente teorema (ya demostrado combinatoriamente en el Teorema 3.19 de la Unidad 3; aquí damos la demostración aritmética clásica, vía congruencias).

**Teorema 5.17 (Wilson).** *Si \\(p\\) es primo, entonces \\((p-1)!\equiv-1\pmod p\\).*

*Demostración.* Los casos \\(p=2,3\\) se comprueban directamente. Supongamos \\(p>3\\). Para cada \\(a\in\\{1,2,\dots,p-1\\}\\), la congruencia lineal \\(ax\equiv1\pmod p\\) tiene, como veremos en el Corolario 5.25 de la Sección 5.4 (o directamente, porque \\(\gcd(a,p)=1\\)), exactamente una solución módulo \\(p\\), representada por un único \\(a'\in\\{1,\dots,p-1\\}\\). Esto define una función \\(\\{1,\dots,p-1\\}\to\\{1,\dots,p-1\\}\\), \\(a\mapsto a'\\), que es una involución (aplicarla dos veces regresa a \\(a\\)) y por tanto biyectiva.

Si \\(a'=a\\), entonces \\(a^2\equiv1\pmod p\\), es decir, \\(p\mid(a-1)(a+1)\\); por el Lema de Euclides para primos (Proposición 2.2), \\(p\mid(a-1)\\) o \\(p\mid(a+1)\\), es decir (como \\(a\in\\{1,\dots,p-1\\}\\)), \\(a=1\\) o \\(a=p-1\\). Por tanto, el conjunto \\(\\{2,3,\dots,p-2\\}\\) se descompone en parejas disjuntas \\(\\{a,a'\\}\\) con \\(a\ne a'\\) y \\(aa'\equiv1\pmod p\\), exactamente como en el Ejemplo 5.16. Multiplicando los elementos de \\(\\{2,\dots,p-2\\}\\) agrupados por parejas, \\(2\cdot3\cdots(p-2)\equiv1\pmod p\\), y por tanto
\\[ (p-1)! = 1\cdot\big(2\cdot3\cdots(p-2)\big)\cdot(p-1) \equiv 1\cdot1\cdot(p-1)\equiv-1\pmod p. \qquad\blacksquare \\]

**Observación 5.18.** A diferencia del Pequeño Teorema de Fermat, la congruencia de Wilson sí **caracteriza** a los primos entre los enteros \\(n>4\\): si \\(n\\) es compuesto y \\(d\ne1,n\\) es un divisor suyo, entonces \\(d\\) es uno de los factores de \\((n-1)!\\), así que \\(d\mid(n-1)!\\), y de hecho (con más trabajo, como en la Proposición 3.21 de la Unidad 3) se puede ver que \\((n-1)!\equiv0\pmod n\\) si \\(n>4\\) es compuesto —nunca \\(\equiv-1\\).

## Una aplicación: existencia de raíces de \\(-1\\) módulo \\(p\\)

**Teorema 5.19.** *Sea \\(p\\) primo. La congruencia \\(x^2\equiv-1\pmod p\\) tiene solución si y solo si \\(p=2\\) o \\(p\equiv1\pmod4\\).*

*Demostración.* (\\(\Rightarrow\\)) Supongamos que \\(a\\) es solución de \\(x^2\equiv-1\pmod p\\), con \\(p\\) impar (el caso \\(p=2\\) es trivial: \\(x=1\\) sirve). Como \\(a^2\equiv-1\pmod p\\), \\(p\nmid a\\) (si no, \\(0\equiv-1\\), absurdo). Veamos que \\(p\not\equiv3\pmod4\\): si lo fuera, \\(\frac{p-1}2\\) sería impar, y entonces
\\[ a^{p-1}=(a^2)^{(p-1)/2}\equiv(-1)^{(p-1)/2}=-1\pmod p \\]
(pues el exponente es impar), contradiciendo el Pequeño Teorema de Fermat (Teorema 5.13), que exige \\(a^{p-1}\equiv1\pmod p\\) (ya que \\(p\nmid a\\)). Luego \\(p\equiv1\pmod4\\).

(\\(\Leftarrow\\)) Si \\(p=2\\), \\(x=1\\) satisface \\(1\equiv-1\pmod2\\). Supongamos \\(p\equiv1\pmod4\\), de modo que \\(\frac{p-1}2\\) es par. Consideremos las \\(\frac{p-1}2\\) congruencias (triviales, por definición de resta módulo \\(p\\)):
\\[ 1\equiv-(p-1),\quad2\equiv-(p-2),\quad\dots,\quad\frac{p-1}2\equiv-\left(\frac{p+1}2\right) \pmod p. \\]
Multiplicando todas estas congruencias entre sí, y usando que hay un número **par** de ellas (por lo que los signos \\((-1)\\) se cancelan en pares):
\\[ \left(\frac{p-1}2\right)! \equiv (-1)^{(p-1)/2}\cdot(p-1)(p-2)\cdots\frac{p+1}2 = (p-1)(p-2)\cdots\frac{p+1}2 \pmod p, \\]
donde se usó que \\((-1)^{(p-1)/2}=1\\) por ser \\(\frac{p-1}2\\) par. Multiplicando ambos lados por \\(\left(\frac{p-1}2\right)!\\) de nuevo:
\\[ \left(\left(\frac{p-1}2\right)!\right)^2 \equiv (p-1)(p-2)\cdots\frac{p+1}2\cdot\left(\frac{p-1}2\right)! = (p-1)! \equiv -1\pmod p, \\]
usando el Teorema de Wilson (Teorema 5.17) en el último paso. Por tanto, \\(x=\left(\frac{p-1}2\right)!\\) es una solución de \\(x^2\equiv-1\pmod p\\). \\(\blacksquare\\)

**Corolario 5.20.** *Existen infinitos números primos de la forma \\(4k+1\\).*

*Demostración.* Supongamos, por reducción al absurdo, que \\(p_1,\dots,p_r\\) fueran **todos** los primos de la forma \\(4k+1\\). Consideremos \\(a=(2p_1p_2\cdots p_r)^2+1\\), y sea \\(p\\) un divisor primo de \\(a\\) (existe por la Proposición 2.1, ya que \\(a>1\\)). Como \\(2p_1\cdots p_r\\) es solución de \\(x^2\equiv-1\pmod p\\) (pues \\(p\mid a\\) significa \\((2p_1\cdots p_r)^2\equiv-1\pmod p\\)), el Teorema 5.19 da \\(p=2\\) o \\(p\equiv1\pmod4\\), es decir, \\(p=2\\) o \\(p=p_i\\) para algún \\(i\\). Pero \\(a\\) es impar (es \\((\text{par})^2+1\\)), así que \\(p\ne2\\); y ningún \\(p_i\\) divide a \\(a=(2p_1\cdots p_r)^2+1\\) (pues \\(p_i\\) divide al primer sumando, así que dividiría también a \\(1\\), absurdo). Esta contradicción muestra que la lista \\(p_1,\dots,p_r\\) no puede ser completa. \\(\blacksquare\\)

**Corolario 5.21.** *Existen infinitos números primos de la forma \\(8k+5\\).*

*Demostración.* Como en la demostración del Corolario 5.20, supongamos que \\(p_1,\dots,p_r\\) fueran todos los primos de esa forma, y consideremos de nuevo \\(a=(2p_1\cdots p_r)^2+1\\). Por el argumento anterior, todo divisor primo de \\(a\\) es de la forma \\(4k+1\\), es decir, de la forma \\(8k+1\\) u \\(8k+5\\). Como \\(p_1\cdots p_r\\) es impar (producto de primos impares, ya que ninguno de ellos es \\(2\\)), escribamos \\(p_1\cdots p_r=2m+1\\); entonces \\((p_1\cdots p_r)^2=4m(m+1)+1\\) es impar, de la forma \\(8j+1\\) (pues \\(m(m+1)\\) es par), así que \\(a=4(p_1\cdots p_r)^2+1=4(8j+1)+1=32j+5\\), que es de la forma \\(8k+5\\). Por tanto, \\(a\\) no puede tener **todos** sus divisores primos de la forma \\(8k+1\\) (el producto de números \\(\equiv1\pmod8\\) es \\(\equiv1\pmod8\\), no \\(\equiv5\\)); debe tener algún divisor primo de la forma \\(8k+5\\), es decir, algún \\(p_i\\). Pero, como antes, ningún \\(p_i\\) divide a \\(a\\), contradicción. \\(\blacksquare\\)

Estos dos corolarios son casos particulares del **Teorema de Dirichlet sobre primos en progresiones aritméticas** (mencionado en la Unidad 2), que en su generalidad requiere herramientas analíticas; los casos aquí presentados son notables porque admiten demostraciones completamente elementales, en el espíritu de la demostración original de Euclides.
