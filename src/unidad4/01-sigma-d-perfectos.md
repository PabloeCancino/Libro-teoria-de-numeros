# 4.1 Las funciones σ(n) y d(n): números perfectos y de Mersenne

## Funciones aritméticas y multiplicatividad

**Definición.** Una **función aritmética** es cualquier función \\(f:\mathbb{Z}^+\to\mathbb{C}\\) (para nuestros propósitos, casi siempre con valores en \\(\mathbb{Z}\\) o \\(\mathbb{Q}\\)). Se dice que \\(f\\) es **multiplicativa** si \\(f(1)=1\\) y
\\[ f(mn)=f(m)f(n) \quad \text{siempre que } \gcd(m,n)=1. \\]
Se dice **completamente multiplicativa** si la igualdad \\(f(mn)=f(m)f(n)\\) vale para *todos* los \\(m,n\\), sin requerir coprimalidad.

La multiplicatividad es la propiedad estructural más importante de esta unidad: **reduce el cálculo de \\(f(n)\\) para cualquier \\(n\\) al cálculo de \\(f(p^e)\\) en cada potencia prima de la factorización de \\(n\\)** (Teorema Fundamental de la Aritmética, Teorema 2.11), como se precisa a continuación.

**Proposición 4.1.** *Si \\(f\\) es multiplicativa y \\(n=p_1^{e_1}\cdots p_r^{e_r}\\) es la factorización en primos de \\(n>1\\), entonces*
\\[ f(n) = f(p_1^{e_1})f(p_2^{e_2})\cdots f(p_r^{e_r}). \\]

*Demostración.* Por inducción sobre \\(r\\). Para \\(r=1\\) es trivial. Si vale para \\(r-1\\) factores, como \\(\gcd(p_1^{e_1}\cdots p_{r-1}^{e_{r-1}},\, p_r^{e_r})=1\\) (primos distintos, Proposición 2.6), la multiplicatividad da
\\[ f(n) = f(p_1^{e_1}\cdots p_{r-1}^{e_{r-1}})\cdot f(p_r^{e_r}) = f(p_1^{e_1})\cdots f(p_{r-1}^{e_{r-1}})\cdot f(p_r^{e_r}), \\]
usando la hipótesis de inducción en el segundo paso. \\(\blacksquare\\)

## El número de divisores \\(d(n)\\)

**Definición.** Para \\(n\ge1\\), \\(d(n)\\) (también denotada \\(\tau(n)\\)) denota el número de divisores positivos de \\(n\\).

Ya obtuvimos una fórmula explícita en la Proposición 2.18; la revisamos aquí desde la perspectiva de la multiplicatividad.

**Proposición 4.2.** *\\(d\\) es multiplicativa, y \\(d(p^e)=e+1\\) para todo primo \\(p\\) y \\(e\ge0\\).*

*Demostración.* Los divisores de \\(p^e\\) son exactamente \\(1,p,p^2,\dots,p^e\\), es decir, \\(e+1\\) de ellos. Para la multiplicatividad: si \\(\gcd(m,n)=1\\), todo divisor \\(c\\) de \\(mn\\) se escribe de manera única como \\(c=c_1c_2\\) con \\(c_1\mid m\\), \\(c_2\mid n\\) (esto se sigue directamente comparando exponentes de primos, Corolario 2.13, ya que \\(m\\) y \\(n\\) no comparten factores primos). Por la regla del producto, el número de tales pares \\((c_1,c_2)\\) es \\(d(m)d(n)\\), luego \\(d(mn)=d(m)d(n)\\). \\(\blacksquare\\)

Combinando la Proposición 4.1 con la Proposición 4.2 recuperamos \\(d(n)=\prod_i(e_i+1)\\) (Proposición 2.18) para \\(n=\prod_i p_i^{e_i}\\).

## La suma de divisores \\(\sigma(n)\\)

**Definición.** Para \\(n\ge1\\), \\(\sigma(n)\\) denota la suma de todos los divisores positivos de \\(n\\): \\(\sigma(n)=\sum_{d\mid n} d\\).

**Proposición 4.3.** *\\(\sigma\\) es multiplicativa, y para todo primo \\(p\\) y \\(e\ge0\\),*
\\[ \sigma(p^e) = 1+p+p^2+\cdots+p^e = \frac{p^{e+1}-1}{p-1}. \\]

*Demostración.* La fórmula para \\(\sigma(p^e)\\) es la suma de los divisores de \\(p^e\\) (que son \\(1,p,\dots,p^e\\)), una serie geométrica finita. La multiplicatividad se demuestra igual que en la Proposición 4.2: si \\(\gcd(m,n)=1\\), cada divisor de \\(mn\\) se escribe únicamente como \\(c_1c_2\\) con \\(c_1\mid m,c_2\mid n\\), así que
\\[ \sigma(mn) = \sum_{c_1\mid m}\sum_{c_2\mid n} c_1c_2 = \Big(\sum_{c_1\mid m}c_1\Big)\Big(\sum_{c_2\mid n}c_2\Big) = \sigma(m)\sigma(n). \qquad\blacksquare \\]

**Ejemplo 4.4.** Para \\(n=360=2^3\cdot3^2\cdot5\\):
\\[ \sigma(360)=\sigma(2^3)\sigma(3^2)\sigma(5) = 15\cdot13\cdot6=1170, \qquad d(360)=4\cdot3\cdot2=24 \\]
(coincidiendo con el Ejemplo 2.19 para \\(d(360)\\)).

## Números perfectos

**Definición.** Un entero positivo \\(n\\) es **perfecto** si es igual a la suma de sus divisores propios (es decir, sus divisores positivos distintos de sí mismo), equivalentemente si \\(\sigma(n)=2n\\).

**Ejemplo 4.5.** \\(6=1+2+3\\) es perfecto (\\(\sigma(6)=1+2+3+6=12=2\cdot6\\)). También lo es \\(28=1+2+4+7+14\\) (\\(\sigma(28)=56=2\cdot28\\)). Los siguientes dos números perfectos son \\(496\\) y \\(8128\\), ya conocidos desde la antigüedad (Euclides, *Elementos*, Libro IX).

## Números de Mersenne y el teorema de Euclides–Euler

**Definición.** Un **número de Mersenne** es un entero de la forma \\(M_k=2^k-1\\). Se llama **primo de Mersenne** si además \\(M_k\\) es primo.

**Proposición 4.6.** *Si \\(M_k=2^k-1\\) es primo, entonces \\(k\\) es primo.*

*Demostración.* Esta es exactamente la afirmación del Ejercicio 1 de la Unidad 2: si \\(k=ab\\) con \\(1<a,b<k\\), entonces, usando la identidad \\(x^a-1=(x-1)(x^{a-1}+\cdots+x+1)\\) con \\(x=2^b\\), se obtiene que \\(2^b-1\\) divide propiamente a \\(2^k-1=2^{ab}-1\\) (y \\(1<2^b-1<2^k-1\\)), así que \\(2^k-1\\) sería compuesto. Por contrapositiva, si \\(2^k-1\\) es primo, \\(k\\) no puede factorizarse no trivialmente, es decir, \\(k\\) es primo. \\(\blacksquare\\)

**Observación 4.7.** El recíproco es **falso**: \\(11\\) es primo, pero \\(M_{11}=2047=23\cdot89\\) es compuesto. La búsqueda de primos de Mersenne —relacionada con el proyecto colaborativo GIMPS (*Great Internet Mersenne Prime Search*)— sigue siendo, hoy en día, la fuente de los mayores números primos explícitamente conocidos, gracias a un test de primalidad especialmente eficiente para esta forma (el test de Lucas–Lehmer), que queda fuera del alcance de este curso.

**Teorema 4.8 (Euclides).** *Si \\(M_k=2^k-1\\) es primo, entonces \\(n=2^{k-1}M_k=2^{k-1}(2^k-1)\\) es un número perfecto (necesariamente par).*

*Demostración.* Como \\(\gcd(2^{k-1},M_k)=1\\) (pues \\(M_k=2^k-1\\) es impar), la multiplicatividad de \\(\sigma\\) (Proposición 4.3) da
\\[ \sigma(n)=\sigma(2^{k-1})\sigma(M_k) = (2^k-1)\cdot(M_k+1) \\]
usando que \\(\sigma(2^{k-1})=2^k-1=M_k\\) (Proposición 4.3 con \\(p=2\\)) y que, como \\(M_k\\) es primo, \\(\sigma(M_k)=1+M_k\\). Como \\(M_k+1=2^k\\), obtenemos
\\[ \sigma(n) = M_k\cdot2^k = 2\cdot\big(2^{k-1}M_k\big) = 2n, \\]
es decir, \\(n\\) es perfecto. \\(\blacksquare\\)

**Ejemplo 4.9.** Con \\(k=2\\) (\\(M_2=3\\) primo): \\(n=2\cdot3=6\\). Con \\(k=3\\) (\\(M_3=7\\) primo): \\(n=4\cdot7=28\\). Con \\(k=5\\) (\\(M_5=31\\) primo): \\(n=16\cdot31=496\\). Con \\(k=7\\) (\\(M_7=127\\) primo): \\(n=64\cdot127=8128\\), recuperando los cuatro números perfectos mencionados en el Ejemplo 4.5.

**Teorema 4.10 (Euler, recíproco parcial).** *Todo número perfecto **par** es de la forma \\(2^{k-1}(2^k-1)\\) con \\(2^k-1\\) primo.*

*Demostración.* Sea \\(n\\) par y perfecto; escribamos \\(n=2^{k-1}m\\) con \\(k\ge2\\) y \\(m\\) impar. Como \\(\gcd(2^{k-1},m)=1\\), la multiplicatividad de \\(\sigma\\) da \\(\sigma(n)=\sigma(2^{k-1})\sigma(m)=(2^k-1)\sigma(m)\\). Como \\(n\\) es perfecto, \\(\sigma(n)=2n=2^k m\\), así que
\\[ (2^k-1)\sigma(m) = 2^k m. \tag{$\ast$} \\]
Como \\(\gcd(2^k-1,2^k)=1\\) (enteros consecutivos), de \\((\ast)\\) y el Lema de Euclides (Proposición 1.19(vi)) se sigue \\((2^k-1)\mid m\\); escribamos \\(m=(2^k-1)c\\). Sustituyendo en \\((\ast)\\) y cancelando \\((2^k-1)\\) (que es distinto de cero): \\(\sigma(m)=2^kc\\).

Si \\(c>1\\), entonces \\(1\\), \\(c\\) y \\(m=(2^k-1)c\\) serían tres divisores **distintos** de \\(m\\) (distintos porque \\(k\ge2\\) implica \\(2^k-1\ge3>1\\)), así que \\(\sigma(m)\ge1+c+m = 1+c+(2^k-1)c = 1+2^kc\\), lo que junto con \\(\sigma(m)=2^kc\\) daría \\(2^kc \ge 1+2^kc\\), absurdo. Luego \\(c=1\\), es decir, \\(m=2^k-1\\) y \\(\sigma(m)=2^k=m+1\\). Pero \\(\sigma(m)=m+1\\) para \\(m>1\\) significa exactamente que los únicos divisores positivos de \\(m\\) son \\(1\\) y \\(m\\), es decir, que \\(m=2^k-1\\) es primo. Por tanto \\(n=2^{k-1}m=2^{k-1}(2^k-1)\\) con \\(2^k-1\\) primo. \\(\blacksquare\\)

Los Teoremas 4.8 y 4.10 juntos establecen una **correspondencia biunívoca** entre los números perfectos pares y los primos de Mersenne — el llamado **teorema de Euclides–Euler**. La existencia de números perfectos **impares** es, hasta la fecha, uno de los problemas abiertos más antiguos de la teoría de números: no se conoce ninguno, pero tampoco se ha demostrado que no puedan existir; se sabe, eso sí, que de existir deberían ser extraordinariamente grandes (más de 1500 dígitos, según cotas computacionales actuales) y satisfacer numerosas condiciones restrictivas.
