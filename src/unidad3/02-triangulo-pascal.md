# 3.2 El triángulo de Pascal y sus aplicaciones aritméticas

## La relación de recurrencia de Pascal

**Teorema 3.10 (identidad de Pascal).** *Para \\(1\le k\le n-1\\),*
\\[ \binom{n}{k} = \binom{n-1}{k-1}+\binom{n-1}{k}. \\]

*Demostración (combinatoria).* Sea \\(A\\) un conjunto de \\(n\\) elementos y fijemos un elemento particular \\(a\in A\\). Todo subconjunto \\(B\subseteq A\\) de tamaño \\(k\\) o bien contiene a \\(a\\), o bien no lo contiene. Los subconjuntos de tamaño \\(k\\) que contienen a \\(a\\) están en correspondencia biunívoca con los subconjuntos de tamaño \\(k-1\\) de \\(A\setminus\{a\}\\) (que tiene \\(n-1\\) elementos), y hay \\(\binom{n-1}{k-1}\\) de ellos. Los que no contienen a \\(a\\) son subconjuntos de tamaño \\(k\\) de \\(A\setminus\{a\}\\), y hay \\(\binom{n-1}{k}\\) de ellos. Por la regla de la suma (Proposición 3.1), \\(\binom nk = \binom{n-1}{k-1}+\binom{n-1}k\\). \\(\blacksquare\\)

Esta identidad, junto con \\(\binom n0=\binom nn=1\\), permite calcular todos los coeficientes binomiales recursivamente, disponiéndolos en el **triángulo de Pascal**:

```
n=0:            1
n=1:           1 1
n=2:          1 2 1
n=3:         1 3 3 1
n=4:        1 4 6 4 1
n=5:       1 5 10 10 5 1
n=6:      1 6 15 20 15 6 1
```

donde la entrada en la fila \\(n\\), posición \\(k\\) (contando desde \\(0\\)), es \\(\binom nk\\), y cada entrada interior es la suma de las dos que están inmediatamente arriba de ella, conforme al Teorema 3.10. Este triángulo era conocido en distintas culturas mucho antes de Pascal —en China se le atribuye a Yang Hui (s. XIII), y en Persia a Al-Karají (s. X-XI)— pero el nombre "triángulo de Pascal" honra el tratado sistemático que Blaise Pascal escribió sobre él en 1654, incluyendo su relación con la probabilidad y con el teorema del binomio.

## Divisibilidad en el triángulo de Pascal

Los coeficientes binomiales esconden patrones aritméticos notables, algunos de los cuales anticipan resultados centrales de las unidades siguientes.

**Proposición 3.11.** *Si \\(p\\) es primo y \\(1\le k\le p-1\\), entonces \\(p \mid \binom pk\\).*

*Demostración.* De la fórmula \\(\binom pk = \dfrac{p!}{k!(p-k)!}\\), obtenemos \\(k!(p-k)!\binom pk = p!\\), es decir,
\\[ k!(p-k)!\binom pk = p\cdot(p-1)!. \\]
El lado derecho es claramente divisible por \\(p\\). Como \\(1\le k\le p-1\\), ni \\(k!\\) ni \\((p-k)!\\) contienen al factor primo \\(p\\) (todos sus factores son \\(<p\\)), así que por el Corolario 2.13 (o directamente por la Proposición 2.2, el Lema de Euclides para primos, aplicado repetidamente), \\(p \nmid k!(p-k)!\\). Como \\(p\\) divide al producto \\(k!(p-k)!\binom pk\\) pero no a \\(k!(p-k)!\\), el Lema de Euclides (Proposición 1.19(vi), con \\(\gcd(p,k!(p-k)!)=1\\) pues \\(p\\) es primo y no divide a ese factor) da \\(p\mid \binom pk\\). \\(\blacksquare\\)

**Ejemplo 3.12.** La fila \\(n=7\\) del triángulo de Pascal es \\(1,7,21,35,35,21,7,1\\); en efecto, \\(7\\) divide a \\(7,21,35\\) (todas las entradas interiores), consistente con la Proposición 3.11.

**Corolario 3.13 (congruencia de Frobenius / "sueño del estudiante de primer año").** *Si \\(p\\) es primo, entonces para cualesquiera enteros \\(x,y\\),*
\\[ (x+y)^p \equiv x^p+y^p \pmod p. \\]

*Demostración.* Por el Teorema del binomio (Proposición 3.9),
\\[ (x+y)^p = \sum_{k=0}^p \binom pk x^{p-k}y^k = x^p+y^p+\sum_{k=1}^{p-1}\binom pk x^{p-k}y^k. \\]
Por la Proposición 3.11, cada coeficiente \\(\binom pk\\) con \\(1\le k\le p-1\\) es divisible por \\(p\\), así que toda la suma intermedia es divisible por \\(p\\). Anticipando el lenguaje de congruencias que se formaliza en la Unidad 5 (donde \\(a\equiv b\pmod n\\) significa \\(n\mid(a-b)\\)), esto da \\((x+y)^p \equiv x^p+y^p \pmod p\\). \\(\blacksquare\\)

Este corolario es el punto de partida de una de las demostraciones más elegantes del Pequeño Teorema de Fermat, que desarrollamos en la Sección 3.3.

## Identidades adicionales

**Proposición 3.14 (suma de una fila).** *Para todo \\(n\ge0\\), \\(\displaystyle\sum_{k=0}^n \binom nk = 2^n\\).*

*Demostración.* Tomando \\(x=y=1\\) en el Teorema del binomio (Proposición 3.9): \\((1+1)^n=\sum_{k=0}^n\binom nk\\). \\(\blacksquare\\)

Combinatoriamente, esto refleja que un conjunto de \\(n\\) elementos tiene exactamente \\(2^n\\) subconjuntos en total (cada elemento se incluye o no, de forma independiente), y estos se distribuyen entre los \\(n+1\\) tamaños posibles \\(k=0,1,\dots,n\\) según la fila correspondiente del triángulo de Pascal.

**Proposición 3.15 (suma alternada).** *Para \\(n\ge1\\), \\(\displaystyle\sum_{k=0}^n(-1)^k\binom nk=0\\).*

*Demostración.* Tomando \\(x=1,y=-1\\) en el Teorema del binomio: \\((1-1)^n=0=\sum_{k=0}^n\binom nk(-1)^k\\). \\(\blacksquare\\)

Esta identidad se usará en la Unidad 4 al estudiar la función de Möbius y el principio de inclusión-exclusión, del cual es, de hecho, un caso particular.

**Proposición 3.16 (identidad de Vandermonde, opcional).** *Para \\(m,n,k\ge0\\),*
\\[ \binom{m+n}{k} = \sum_{i=0}^k \binom mi\binom n{k-i}. \\]

*Demostración.* Si se tienen dos conjuntos disjuntos \\(A,B\\) con \\(|A|=m\\), \\(|B|=n\\), un subconjunto de tamaño \\(k\\) de \\(A\cup B\\) se determina eligiendo \\(i\\) elementos de \\(A\\) (para algún \\(0\le i\le k\\)) y \\(k-i\\) elementos de \\(B\\); sumando sobre todos los valores posibles de \\(i\\) (regla de la suma) y usando la regla del producto para cada término, se obtiene la identidad. \\(\blacksquare\\)
