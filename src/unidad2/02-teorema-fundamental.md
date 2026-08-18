# 2.2 El Teorema Fundamental de la Aritmética

## Enunciado y demostración

**Teorema 2.11 (Teorema Fundamental de la Aritmética, TFA).** *Todo entero \\(n>1\\) puede escribirse como producto de números primos,*
\\[ n = p_1p_2\cdots p_k, \\]
*y esta factorización es única salvo el orden de los factores. Equivalentemente, agrupando primos iguales,*
\\[ n = p_1^{e_1}p_2^{e_2}\cdots p_r^{e_r}, \\]
*con \\(p_1<p_2<\cdots<p_r\\) primos distintos y \\(e_i\ge1\\), y esta representación es única.*

*Demostración (existencia).* Procedemos por inducción fuerte sobre \\(n\\) (Teorema 1.4). Para \\(n=2\\), \\(2\\) mismo es primo, así que es "producto" de un solo primo. Supongamos que todo entero \\(m\\) con \\(2\le m<n\\) se puede escribir como producto de primos, y consideremos \\(n\\). Si \\(n\\) es primo, ya está. Si \\(n\\) es compuesto, \\(n=ab\\) con \\(1<a,b<n\\); por hipótesis de inducción, \\(a\\) y \\(b\\) son cada uno producto de primos, y concatenando estas factorizaciones se obtiene una factorización en primos de \\(n=ab\\).

*Demostración (unicidad).* Supongamos, por reducción al absurdo, que existen enteros \\(n>1\\) con dos factorizaciones en primos distintas (distintas como multiconjuntos, es decir, no relacionadas solo por reordenamiento). Por el Principio del Buen Orden, sea \\(n\\) el **menor** tal entero, con
\\[ n = p_1p_2\cdots p_k = q_1q_2\cdots q_l, \\]
dos factorizaciones sin ningún \\(p_i\\) igual a algún \\(q_j\\) que se puedan cancelar directamente entre sí (si algún \\(p_i=q_j\\), se cancelarían y \\(n/p_i<n\\) tendría dos factorizaciones distintas, contradiciendo la minimalidad de \\(n\\); así que asumimos que ningún primo es común a ambas listas).

Como \\(p_1 \mid n = q_1q_2\cdots q_l\\), por la Proposición 2.2 (Lema de Euclides para primos), \\(p_1 \mid q_j\\) para algún \\(j\\). Pero \\(q_j\\) es primo, así que sus únicos divisores positivos son \\(1\\) y \\(q_j\\); como \\(p_1>1\\), se sigue \\(p_1=q_j\\). Esto contradice que ningún \\(p_i\\) coincide con ningún \\(q_j\\). Esta contradicción muestra que no existe tal \\(n\\), es decir, la factorización en primos es única salvo orden. \\(\blacksquare\\)

**Observación 2.12.** El TFA es la razón última por la que se excluye a \\(1\\) del conjunto de los primos (ver la observación al inicio de la Sección 2.1): si \\(1\\) fuera primo, cualquier factorización podría alargarse arbitrariamente insertando factores de \\(1\\), destruyendo la unicidad. Los primos son, en este sentido preciso, los "átomos multiplicativos" de \\(\mathbb{Z}^+\\): todo entero mayor que 1 se construye de una única manera a partir de ellos, así como todo entero (mediante la suma) se construye de manera única a partir de sumas de "unos" —esta es la analogía entre el TFA y el papel del \\(1\\) en la construcción aditiva de \\(\mathbb{N}\\) via los axiomas de Peano de la Sección 1.1.

**Corolario 2.13 (caracterización de la divisibilidad vía exponentes).** *Sean \\(a=p_1^{e_1}\cdots p_r^{e_r}\\) y \\(b=p_1^{f_1}\cdots p_r^{f_r}\\) las factorizaciones en primos de \\(a,b>1\\) (usando el mismo conjunto de primos \\(p_1,\dots,p_r\\), permitiendo exponentes \\(e_i\\) o \\(f_i\\) iguales a cero). Entonces:*
\\[ a \mid b \iff e_i \le f_i \ \text{ para todo } i. \\]

*Demostración.* (\\(\Leftarrow\\)) Si \\(e_i\le f_i\\) para todo \\(i\\), entonces \\(b = a \cdot \prod_i p_i^{f_i-e_i}\\), y el producto de la derecha es un entero, luego \\(a\mid b\\).

(\\(\Rightarrow\\)) Si \\(a \mid b\\), escribamos \\(b=ac\\). Por la existencia de factorización (Teorema 2.11), \\(c\\) se factoriza en primos (o \\(c=1\\)); multiplicando la factorización de \\(a\\) por la de \\(c\\) se obtiene una factorización de \\(b\\), que por unicidad debe coincidir (salvo orden) con \\(p_1^{f_1}\cdots p_r^{f_r}\\). Comparando el exponente de cada \\(p_i\\), el de \\(a\\) (que es \\(e_i\\)) más el de \\(c\\) (que es \\(\ge0\\)) da \\(f_i\\), luego \\(e_i \le f_i\\). \\(\blacksquare\\)

**Corolario 2.14 (mcd y mcm vía exponentes).** *Con la notación anterior,*
\\[ \gcd(a,b) = \prod_i p_i^{\min(e_i,f_i)}, \qquad \mathrm{mcm}(a,b) = \prod_i p_i^{\max(e_i,f_i)}. \\]

*Demostración.* Por el Corolario 2.13, un entero \\(d=\prod_i p_i^{g_i}\\) divide a la vez a \\(a\\) y a \\(b\\) si y solo si \\(g_i \le e_i\\) y \\(g_i \le f_i\\) para todo \\(i\\), es decir, \\(g_i \le \min(e_i,f_i)\\). El mayor tal \\(d\\) se obtiene tomando \\(g_i=\min(e_i,f_i)\\) para todo \\(i\\), lo cual da la fórmula para el mcd. El argumento para el mcm es análogo, con \\(\max\\) en lugar de \\(\min\\). \\(\blacksquare\\)

Esta caracterización explica de inmediato la identidad \\(\gcd(a,b)\cdot\mathrm{mcm}(a,b)=ab\\) (Teorema 1.21), pues para cada \\(i\\), \\(\min(e_i,f_i)+\max(e_i,f_i)=e_i+f_i\\).

**Ejemplo 2.15.** Con \\(a=2^3\cdot3^2\cdot5=360\\) y \\(b=2\cdot3^3\cdot7=378\\), se obtiene \\(\gcd(a,b)=2^{\min(3,1)}3^{\min(2,3)}5^{\min(1,0)}7^{\min(0,1)}=2^1\cdot3^2=18\\), y \\(\mathrm{mcm}(a,b)=2^3\cdot3^3\cdot5\cdot7=7560\\). (Verificación: \\(18\cdot7560=136080=360\cdot378\\). ✓)

**Corolario 2.16 (raíces y potencias de coprimos).** *Si \\(\gcd(a,b)=1\\) y \\(ab=c^k\\) para algún entero \\(k\ge1\\), entonces \\(a\\) y \\(b\\) son, cada uno, la \\(k\\)-ésima potencia de un entero.*

*Demostración.* Sea \\(p\\) un primo cualquiera, con exponente \\(e\\) en \\(a\\), \\(f\\) en \\(b\\) y \\(g\\) en \\(c\\) (posiblemente cero). Como \\(\gcd(a,b)=1\\), por la Proposición 2.6, ningún primo divide a la vez a \\(a\\) y a \\(b\\), así que al menos uno de \\(e,f\\) es cero. Como \\(ab=c^k\\), comparando exponentes de \\(p\\) en ambos lados (Teorema 2.11): \\(e+f=kg\\). Si \\(f=0\\), entonces \\(e=kg\\), múltiplo de \\(k\\); si \\(e=0\\), entonces \\(f=kg\\), también múltiplo de \\(k\\). En cualquier caso, cada primo aparece en \\(a\\) (y en \\(b\\)) con exponente múltiplo de \\(k\\), lo que significa exactamente que \\(a\\) y \\(b\\) son potencias \\(k\\)-ésimas perfectas. \\(\blacksquare\\)

Este corolario es precisamente el resultado que se usó (bajo el nombre de "factorización única", con \\(k=2\\)) en la demostración del Teorema 1.37 sobre ternas pitagóricas.

## Aplicaciones

**Proposición 2.17 (irracionalidad de \\(\sqrt2\\), y generalización).** *Si \\(n\\) es un entero positivo que no es un cuadrado perfecto, entonces \\(\sqrt n\\) es irracional.*

*Demostración.* Supongamos, por reducción al absurdo, que \\(\sqrt n = a/b\\) con \\(a,b\in\mathbb{Z}^+\\), \\(\gcd(a,b)=1\\) (toda fracción se puede llevar a esta forma reducida, Proposición 1.19(iv)). Entonces \\(a^2=nb^2\\). Sea \\(p\\) un primo cualquiera y sean \\(e,f\\) sus exponentes en \\(a,b\\) respectivamente; como \\(\gcd(a,b)=1\\), al menos uno de \\(e,f\\) es \\(0\\). El exponente de \\(p\\) en \\(a^2\\) es \\(2e\\) y en \\(nb^2\\) es (exponente de \\(p\\) en \\(n\\)) \\(+\ 2f\\). Como \\(a^2=nb^2\\), estos deben ser iguales para todo primo \\(p\\); si \\(f>0\\) entonces \\(e=0\\) (pues no pueden ambos ser positivos), y la igualdad \\(0 = (\text{exp. de } p \text{ en } n) + 2f\\) con \\(f>0\\) forzaría un exponente negativo en \\(n\\), imposible. Luego \\(f=0\\) para todo primo \\(p\\), es decir, \\(b=1\\), y entonces \\(n=a^2\\), un cuadrado perfecto, contradiciendo la hipótesis. \\(\blacksquare\\)

**Proposición 2.18 (número de divisores).** *Si \\(n=p_1^{e_1}\cdots p_r^{e_r}\\), el número de divisores positivos de \\(n\\) es*
\\[ d(n) = (e_1+1)(e_2+1)\cdots(e_r+1). \\]

*Demostración.* Por el Corolario 2.13, los divisores positivos de \\(n\\) son exactamente los enteros \\(p_1^{g_1}\cdots p_r^{g_r}\\) con \\(0\le g_i\le e_i\\) para cada \\(i\\). Hay \\(e_i+1\\) elecciones posibles para cada \\(g_i\\), independientemente unas de otras, así que por la regla del producto hay \\((e_1+1)\cdots(e_r+1)\\) divisores en total. \\(\blacksquare\\)

Esta fórmula se retomará y generalizará en la Unidad 4, donde \\(d(n)\\) se estudia sistemáticamente como **función aritmética**.

**Ejemplo 2.19.** \\(360=2^3\cdot3^2\cdot5^1\\) tiene \\(d(360)=4\cdot3\cdot2=24\\) divisores positivos.
