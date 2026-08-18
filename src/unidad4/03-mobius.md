# 4.3 La función de Möbius

## Definición y multiplicatividad

**Definición.** La **función de Möbius** \\(\mu:\mathbb{Z}^+\to\{-1,0,1\}\\) se define como:
\\[
\mu(n) = \begin{cases}
1 & \text{si } n=1,\\
0 & \text{si } n \text{ tiene algún factor primo repetido (i.e., } p^2\mid n \text{ para algún primo } p\text{)},\\
(-1)^r & \text{si } n=p_1p_2\cdots p_r \text{ es producto de } r \text{ primos distintos.}
\end{cases}
\\]

Un entero se llama **libre de cuadrados** si no es divisible por \\(p^2\\) para ningún primo \\(p\\); así, \\(\mu(n)=0\\) exactamente cuando \\(n\\) no es libre de cuadrados, y \\(\mu(n)=(-1)^r\\) cuando \\(n\\) es libre de cuadrados con \\(r\\) factores primos distintos.

**Ejemplo 4.20.** \\(\mu(1)=1,\ \mu(2)=-1,\ \mu(3)=-1,\ \mu(4)=0\ (4=2^2),\ \mu(6)=\mu(2\cdot3)=1,\ \mu(30)=\mu(2\cdot3\cdot5)=-1,\ \mu(12)=0\ (12=2^2\cdot3).\\)

**Proposición 4.21.** *\\(\mu\\) es multiplicativa.*

*Demostración.* Sean \\(\gcd(m,n)=1\\). Si alguno de \\(m,n\\) no es libre de cuadrados, tampoco lo es \\(mn\\) (comparten el mismo factor primo repetido), así que \\(\mu(mn)=0=\mu(m)\mu(n)\\) (con al menos un factor derecho igual a 0). Si ambos \\(m,n\\) son libres de cuadrados, digamos \\(m\\) con \\(r\\) primos distintos y \\(n\\) con \\(s\\) primos distintos, como \\(\gcd(m,n)=1\\) estos \\(r+s\\) primos son todos distintos entre sí, y \\(mn\\) es libre de cuadrados con exactamente \\(r+s\\) factores primos, así que \\(\mu(mn)=(-1)^{r+s}=(-1)^r(-1)^s=\mu(m)\mu(n)\\). \\(\blacksquare\\)

## La propiedad fundamental de μ

**Teorema 4.22.** *Para todo \\(n\ge1\\),*
\\[ \sum_{d\mid n}\mu(d) = \begin{cases}1 & \text{si } n=1,\\ 0 & \text{si } n>1.\end{cases} \\]

*Demostración.* Para \\(n=1\\), la suma tiene un solo término, \\(\mu(1)=1\\).

Para \\(n>1\\), sea \\(n=p_1^{e_1}\cdots p_r^{e_r}\\) su factorización en primos (\\(r\ge1\\)). Los únicos divisores \\(d\\) de \\(n\\) con \\(\mu(d)\ne0\\) son los productos de subconjuntos **distintos** de \\(\{p_1,\dots,p_r\}\\) (es decir, los divisores libres de cuadrados de \\(n\\)); un tal \\(d\\), producto de \\(k\\) de estos primos, aporta \\(\mu(d)=(-1)^k\\), y hay \\(\binom rk\\) subconjuntos de tamaño \\(k\\). Por tanto,
\\[ \sum_{d\mid n}\mu(d) = \sum_{k=0}^r \binom rk(-1)^k = (1-1)^r = 0, \\]
usando el Teorema del binomio (Proposición 3.9, con \\(x=1,y=-1\\), como en la Proposición 3.15) y que \\(r\ge1\\). \\(\blacksquare\\)

Es instructivo notar que este teorema tiene una segunda demostración inmediata usando multiplicatividad: la función \\(g(n)=\sum_{d\mid n}\mu(d)\\) es multiplicativa (por ser "suma sobre divisores" de una función multiplicativa, hecho que se justifica en la Proposición 4.24 más abajo), así que basta calcular \\(g(p^e)=\mu(1)+\mu(p)+\mu(p^2)+\cdots+\mu(p^e)=1+(-1)+0+\cdots+0=0\\) para \\(e\ge1\\), y \\(g(1)=1\\) trivialmente; por multiplicatividad (Proposición 4.1), \\(g(n)=0\\) para todo \\(n>1\\) (pues algún factor \\(g(p_i^{e_i})=0\\) anula el producto).

## Inversión de Möbius

**Definición.** Si \\(f,g\\) son funciones aritméticas relacionadas por
\\[ g(n) = \sum_{d\mid n} f(d) \qquad \text{para todo } n\ge1, \\]
decimos que \\(g\\) es la **suma sobre divisores** de \\(f\\).

**Teorema 4.23 (Fórmula de inversión de Möbius).** *Si \\(g(n)=\sum_{d\mid n}f(d)\\) para todo \\(n\ge1\\), entonces*
\\[ f(n) = \sum_{d\mid n}\mu(d)\,g(n/d) = \sum_{d\mid n}\mu(n/d)\,g(d). \\]

*Demostración.* Calculamos directamente, intercambiando el orden de sumación (ambas sumas dobles recorren, de manera equivalente, todos los pares \\((d,e)\\) con \\(d\mid n\\) y \\(e\mid (n/d)\\), lo cual —vía el Corolario 2.13, comparando exponentes de primos— equivale exactamente a recorrer los pares \\((d,e)\\) con \\(de\mid n\\)):
\\[
\sum_{d\mid n}\mu(d)\,g(n/d) = \sum_{d\mid n}\mu(d)\sum_{e\mid (n/d)}f(e) = \sum_{de\mid n}\mu(d)f(e) = \sum_{e\mid n}f(e)\sum_{d\mid(n/e)}\mu(d).
\\]
Por el Teorema 4.22, la suma interior \\(\sum_{d\mid(n/e)}\mu(d)\\) vale \\(1\\) si \\(n/e=1\\) (es decir, \\(e=n\\)) y \\(0\\) en cualquier otro caso. Por tanto, de toda la suma exterior sobrevive únicamente el término \\(e=n\\), dando \\(f(n)\cdot1=f(n)\\). \\(\blacksquare\\)

**Proposición 4.24 (multiplicatividad se preserva bajo sumas de divisores).** *Si \\(f\\) es multiplicativa, entonces \\(g(n)=\sum_{d\mid n}f(d)\\) también es multiplicativa.*

*Demostración.* Sea \\(\gcd(m,n)=1\\). Como se argumentó en la demostración del Teorema 4.23, todo divisor de \\(mn\\) se escribe únicamente como \\(d_1d_2\\) con \\(d_1\mid m\\), \\(d_2\mid n\\), y \\(\gcd(d_1,d_2)=1\\) (pues \\(\gcd(m,n)=1\\)). Entonces
\\[ g(mn) = \sum_{d_1\mid m}\sum_{d_2\mid n} f(d_1d_2) = \sum_{d_1\mid m}\sum_{d_2\mid n}f(d_1)f(d_2) = \Big(\sum_{d_1\mid m}f(d_1)\Big)\Big(\sum_{d_2\mid n}f(d_2)\Big) = g(m)g(n), \\]
usando la multiplicatividad de \\(f\\) en el segundo paso. \\(\blacksquare\\)

## Aplicación: una segunda demostración de la fórmula de φ

**Corolario 4.25.** *Para todo \\(n\ge1\\),*
\\[ \varphi(n) = \sum_{d\mid n}\mu(d)\,\frac nd = n\sum_{d\mid n}\frac{\mu(d)}d. \\]

*Demostración.* Por el Teorema 4.17 (identidad de Gauss), \\(n=\sum_{d\mid n}\varphi(d)\\), es decir, con la notación de esta sección, \\(g(n)=n\\) es la suma sobre divisores de \\(f=\varphi\\). Por la fórmula de inversión de Möbius (Teorema 4.23),
\\[ \varphi(n) = \sum_{d\mid n}\mu(d)\,g(n/d) = \sum_{d\mid n}\mu(d)\cdot\frac nd. \qquad\blacksquare \\]

**Ejemplo 4.26.** Para \\(n=12\\) (divisores \\(1,2,3,4,6,12\\), con \\(\mu(1)=1,\mu(2)=-1,\mu(3)=-1,\mu(4)=0,\mu(6)=1,\mu(12)=0\\)):
\\[ \varphi(12) = \mu(1)\cdot12+\mu(2)\cdot6+\mu(3)\cdot4+\mu(4)\cdot3+\mu(6)\cdot2+\mu(12)\cdot1 = 12-6-4+0+2+0=4, \\]
coincidiendo con el cálculo directo del Ejemplo 4.18 (\\(\varphi(12)=4\\)). Esta fórmula, expandiendo el producto \\(n\prod_i(1-1/p_i)\\) del Teorema 4.14, es en realidad la misma identidad escrita de otra forma: el desarrollo del producto \\(\prod_i(1-1/p_i)\\) produce exactamente los términos \\(\mu(d)/d\\) para cada divisor libre de cuadrados \\(d\\) de \\(n\\) (Ejercicio 12).

La técnica de inversión de Möbius, aunque introducida aquí en el contexto puramente aritmético de esta unidad, es una instancia particular de un principio combinatorio mucho más general —el **principio de inclusión-exclusión**— y reaparece de manera esencial en la teoría analítica de números (por ejemplo, en la fórmula de Mertens y en la demostración analítica del Teorema de los Números Primos), un tema que se esboza brevemente en la Unidad 6.
