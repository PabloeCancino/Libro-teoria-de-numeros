# 4.2 La función φ de Euler

**Definición.** Para \\(n\ge1\\), la **función φ de Euler** (o **indicatriz de Euler**) se define como
\\[ \varphi(n) = \\#\\{k \in \\{1,2,\dots,n\\} : \gcd(k,n)=1\\}, \\]
es decir, el número de enteros en \\(\\{1,\dots,n\\}\\) que son primos relativos con \\(n\\).

**Ejemplo 4.11.** \\(\varphi(1)=1\\) (por convención, \\(\gcd(1,1)=1\\)); \\(\varphi(6)=2\\) (solo \\(1\\) y \\(5\\) son coprimos con \\(6\\) en \\(\\{1,\dots,6\\}\\)); \\(\varphi(p)=p-1\\) para todo primo \\(p\\) (todos los elementos de \\(\\{1,\dots,p-1\\}\\) son coprimos con \\(p\\), ya que \\(p\\) es primo).

Esta función tendrá un papel absolutamente central en la Unidad 5, donde se relacionará con los **sistemas reducidos de residuos módulo \\(n\\)** y el **Teorema de Euler** (una generalización de gran alcance del Pequeño Teorema de Fermat); aquí la estudiamos como función aritmética, estableciendo su multiplicatividad y una fórmula cerrada.

## φ en potencias de primos

**Proposición 4.12.** *Para \\(p\\) primo y \\(e\ge1\\),*
\\[ \varphi(p^e) = p^e - p^{e-1} = p^e\left(1-\frac1p\right). \\]

*Demostración.* Los enteros de \\(\\{1,\dots,p^e\\}\\) que **no** son coprimos con \\(p^e\\) son exactamente los múltiplos de \\(p\\) (pues el único divisor primo de \\(p^e\\) es \\(p\\)), a saber, \\(p,2p,3p,\dots,p^{e-1}\cdot p=p^e\\), que son \\(p^{e-1}\\) en total. Por complemento, \\(\varphi(p^e)=p^e-p^{e-1}\\). \\(\blacksquare\\)

## Multiplicatividad de φ

**Teorema 4.13.** *φ es multiplicativa: si \\(\gcd(m,n)=1\\), entonces \\(\varphi(mn)=\varphi(m)\varphi(n)\\).*

*Demostración.* Consideremos la función \\(f:\\{0,\dots,mn-1\\}\to\\{0,\dots,m-1\\}\times\\{0,\dots,n-1\\}\\) dada por \\(f(k)=(k \bmod m,\ k\bmod n)\\) (los residuos de \\(k\\) al dividirlo entre \\(m\\) y entre \\(n\\), respectivamente). Como \\(\gcd(m,n)=1\\), el Teorema Chino del Resto (que demostraremos en la Sección 5.5 como Teorema 5.27; aquí lo anticipamos, o alternativamente se puede dar un argumento directo vía el principio del palomar, ver el Ejercicio 14) garantiza que \\(f\\) es una **biyección**.

Además, \\(f\\) respeta la coprimalidad: \\(\gcd(k,mn)=1\\) si y solo si \\(\gcd(k,m)=1\\) **y** \\(\gcd(k,n)=1\\) (por la Proposición 2.6, ya que los divisores primos de \\(mn\\) son la unión de los de \\(m\\) y los de \\(n\\), al ser coprimos); y esto ocurre si y solo si \\(\gcd(k\bmod m,\\,m)=1\\) y \\(\gcd(k\bmod n,\\,n)=1\\) (pues \\(\gcd(k,m)=\gcd(k\bmod m,m)\\), por la Proposición 1.19(iii)).

Por tanto, \\(f\\) restringe a una biyección entre \\(\\{k\in\\{0,\dots,mn-1\\}:\gcd(k,mn)=1\\}\\) (que tiene \\(\varphi(mn)\\) elementos) y \\(\\{a\in\\{0,\dots,m-1\\}:\gcd(a,m)=1\\}\times\\{b\in\\{0,\dots,n-1\\}:\gcd(b,n)=1\\}\\) (que tiene \\(\varphi(m)\varphi(n)\\) elementos, por la regla del producto, Proposición 3.2). Luego \\(\varphi(mn)=\varphi(m)\varphi(n)\\). \\(\blacksquare\\)

## Fórmula del producto

**Teorema 4.14 (fórmula de Euler para φ).** *Si \\(n=p_1^{e_1}p_2^{e_2}\cdots p_r^{e_r}\\) es la factorización en primos de \\(n>1\\), entonces*
\\[ \varphi(n) = n\prod_{i=1}^r\left(1-\frac1{p_i}\right) = \prod_{i=1}^r p_i^{e_i-1}(p_i-1). \\]

*Demostración.* Por la Proposición 4.1 (multiplicatividad, aplicada a φ vía el Teorema 4.13) y la Proposición 4.12:
\\[ \varphi(n) = \prod_{i=1}^r \varphi(p_i^{e_i}) = \prod_{i=1}^r p_i^{e_i}\left(1-\frac1{p_i}\right) = \left(\prod_{i=1}^r p_i^{e_i}\right)\prod_{i=1}^r\left(1-\frac1{p_i}\right) = n\prod_{i=1}^r\left(1-\frac1{p_i}\right). \qquad\blacksquare \\]

**Ejemplo 4.15.** \\(\varphi(360)=\varphi(2^3\cdot3^2\cdot5) = 360\left(1-\frac12\right)\left(1-\frac13\right)\left(1-\frac15\right) = 360\cdot\frac12\cdot\frac23\cdot\frac45 = 96.\\)

**Ejemplo 4.16.** \\(\varphi(1000)=\varphi(2^3\cdot5^3)=1000\left(1-\frac12\right)\left(1-\frac15\right)=1000\cdot\frac12\cdot\frac45=400.\\)

## La identidad de Gauss

**Teorema 4.17 (Gauss).** *Para todo \\(n\ge1\\),*
\\[ \sum_{d\mid n} \varphi(d) = n, \\]
*donde la suma recorre todos los divisores positivos \\(d\\) de \\(n\\).*

*Demostración (combinatoria).* Particionamos el conjunto \\(\\{1,2,\dots,n\\}\\) según el valor de \\(\gcd(k,n)\\): para cada divisor \\(d\mid n\\), sea
\\[ S_d = \\{k\in\\{1,\dots,n\\} : \gcd(k,n)=d\\}. \\]
Como \\(\gcd(k,n)\\) siempre es un divisor de \\(n\\), estos conjuntos \\(S_d\\) (uno por cada divisor \\(d\\) de \\(n\\)) particionan \\(\\{1,\dots,n\\}\\), así que por la regla de la suma, \\(n=\sum_{d\mid n}|S_d|\\).

Afirmamos que \\(|S_d|=\varphi(n/d)\\). En efecto, \\(k\in S_d\\) si y solo si \\(k=dj\\) para algún \\(j\in\\{1,\dots,n/d\\}\\) con \\(\gcd(dj,n)=d\\), es decir (dividiendo entre \\(d\\)) con \\(\gcd(j,\\,n/d)=1\\); hay exactamente \\(\varphi(n/d)\\) tales \\(j\\), por definición de φ. Por tanto,
\\[ n = \sum_{d\mid n}\varphi(n/d) = \sum_{d\mid n}\varphi(d), \\]
donde la última igualdad se obtiene reindexando la suma (a cada divisor \\(d\\) de \\(n\\) le corresponde el divisor \\(n/d\\), y la correspondencia \\(d\leftrightarrow n/d\\) es una biyección del conjunto de divisores de \\(n\\) en sí mismo). \\(\blacksquare\\)

**Ejemplo 4.18.** Para \\(n=12\\), los divisores son \\(1,2,3,4,6,12\\), con \\(\varphi(1)=1,\varphi(2)=1,\varphi(3)=2,\varphi(4)=2,\varphi(6)=2,\varphi(12)=4\\). Suma: \\(1+1+2+2+2+4=12\\). ✓

Esta identidad puede demostrarse alternativamente usando la **función de Möbius** (Sección 4.3) y el principio de **inversión de Möbius**, del cual es uno de los ejemplos más clásicos; conviene comparar ambas demostraciones: la combinatoria de arriba y la basada en Möbius (Sección 4.3).

**Proposición 4.19 (φ(n) es par para \\(n\ge3\\)).** *Si \\(n\ge3\\), entonces \\(\varphi(n)\\) es par.*

*Demostración.* Si \\(k\in\\{1,\dots,n-1\\}\\) satisface \\(\gcd(k,n)=1\\), también \\(\gcd(n-k,n)=1\\) (Proposición 1.19(iii) aplicada a \\(\gcd(n,n-k)=\gcd(n,-k)=\gcd(n,k)\\), usando la Proposición 1.19(i)), y como \\(n\ge3\\), \\(k\ne n-k\\) salvo si \\(n=2k\\), pero en tal caso \\(\gcd(k,2k)=k>1\\) si \\(k>1\\), o si \\(k=1\\), \\(n=2\\), caso excluido por \\(n\ge3\\). Por tanto, los enteros coprimos con \\(n\\) en \\(\\{1,\dots,n-1\\}\\) se agrupan en parejas \\(\\{k,n-k\\}\\) sin elementos fijos, así que su número total, \\(\varphi(n)\\), es par. \\(\blacksquare\\)
