# 5.1 Congruencias y sus propiedades elementales

## Definición

**Definición.** Fijado un número entero positivo \\(n\\), y dados enteros \\(a,b\\), decimos que \\(a\\) es **congruente con \\(b\\) módulo \\(n\\)**, y escribimos
\\[ a \equiv b \pmod n, \\]
si \\(n \mid (a-b)\\), es decir, si \\(a\\) y \\(b\\) dejan el mismo residuo al dividirse entre \\(n\\) (esto último se justifica en la Proposición 5.3). Si \\(n\nmid(a-b)\\), escribimos \\(a\not\equiv b\pmod n\\).

## Propiedades elementales

**Proposición 5.1.** *Fijado un entero \\(n>0\\) y dados enteros \\(a,b,c,d\\), se cumple:*

1. *\\(a\equiv a\pmod n\\) (reflexividad).*
2. *\\(a\equiv b\pmod n\\) si y solo si \\(b\equiv a\pmod n\\) (simetría).*
3. *Si \\(a\equiv b\pmod n\\) y \\(b\equiv c\pmod n\\), entonces \\(a\equiv c\pmod n\\) (transitividad).*
4. *Si \\(a\equiv b\pmod n\\) y \\(c\equiv d\pmod n\\), entonces \\(a+c\equiv b+d\pmod n\\).*
5. *Si \\(a\equiv b\pmod n\\) y \\(c\equiv d\pmod n\\), entonces \\(ac\equiv bd\pmod n\\).*
6. *Si \\(ac\equiv bc\pmod n\\), entonces \\(a\equiv b\pmod{n/d}\\), donde \\(d=\gcd(c,n)\\). En particular, si \\(\gcd(c,n)=1\\), entonces \\(ac\equiv bc\pmod n\\) si y solo si \\(a\equiv b\pmod n\\).*

*Demostración.* Las partes (i)–(v) se siguen directamente de la Proposición 1.9 (propiedades de la divisibilidad de la Unidad 1). Por ejemplo, (i): \\(n\mid(a-a)=0\\), lo cual siempre es cierto (Observación 1.8). (iii): de \\(n\mid(a-b)\\) y \\(n\mid(b-c)\\), la Proposición 1.9(ii) da \\(n\mid\big((a-b)+(b-c)\big)=a-c\\). (iv): de \\(n\mid(a-b)\\) y \\(n\mid(c-d)\\), \\(n\mid\big((a-b)+(c-d)\big)=(a+c)-(b+d)\\). (v): escribiendo \\(a-b=nk\\), \\(c-d=nl\\), se tiene \\(ac-bd = ac-bc+bc-bd = c(a-b)+b(c-d) = c\cdot nk+b\cdot nl = n(ck+bl)\\), luego \\(n\mid(ac-bd)\\).

Para (vi): por hipótesis \\(n\mid(ac-bc)=(a-b)c\\), es decir, \\(\frac nd \mid \frac{(a-b)c}{d}\\) (dividiendo entre \\(d=\gcd(c,n)\\), lo cual es legítimo pues \\(d\mid n\\) y las cantidades involucradas son enteras). Como \\(\gcd(n/d,\\,c/d)=1\\) (Proposición 1.19(iv)), el Lema de Euclides (Proposición 1.19(vi)) aplicado a \\(\frac nd \mid (a-b)\cdot\frac cd\\) da \\(\frac nd \mid (a-b)\\), es decir, \\(a\equiv b\pmod{n/d}\\). El caso particular \\(\gcd(c,n)=1\\) corresponde a \\(d=1\\). \\(\blacksquare\\)

**Observación 5.2.** Las tres primeras propiedades de la Proposición 5.1 dicen exactamente que la relación \\(\equiv\pmod n\\) es una **relación de equivalencia** sobre \\(\mathbb{Z}\\) ((i) reflexiva, (ii) simétrica, (iii) transitiva). El conjunto cociente de \\(\mathbb{Z}\\) por esta relación se denota \\(\mathbb{Z}_n\\) (o \\(\mathbb{Z}/n\mathbb{Z}\\)), y las propiedades (iv) y (v) dicen que la suma y el producto de enteros pasan bien al cociente, dotando a \\(\mathbb{Z}_n\\) de estructura de **anillo conmutativo** —el anillo de residuos módulo \\(n\\) que da nombre a esta unidad. Por la propiedad (ii), el orden de los términos en una congruencia es indistinto, y se habla simplemente de que \\(a\\) y \\(b\\) son **congruentes entre sí** módulo \\(n\\).

## Representantes canónicos y sistemas completos de residuos

**Proposición 5.3.** *Dado \\(n\\) un entero positivo, cada entero \\(a\\) es congruente módulo \\(n\\) con uno y solo uno de los elementos del conjunto \\(\\{0,1,\dots,n-1\\}\\), precisamente el residuo de la división euclídea de \\(a\\) entre \\(n\\). En particular, dos enteros \\(a,b\\) son congruentes módulo \\(n\\) si y solo si tienen el mismo residuo al dividirse entre \\(n\\).*

*Demostración.* Sea \\(a=qn+r\\) la división euclídea de \\(a\\) entre \\(n\\) (Teorema 1.12), con \\(0\le r<n\\). Como \\(n\mid(a-r)\\), se tiene \\(a\equiv r\pmod n\\). Por otro lado, si \\(a\equiv s\pmod n\\) para algún \\(s\in\\{0,\dots,n-1\\}\\), entonces \\(n\mid(a-s)\\), así que \\(a=cn+s\\) para algún \\(c\in\mathbb{Z}\\); como \\(0\le s<n\\), la unicidad del cociente y residuo (Teorema 1.12) implica que esta es precisamente la división euclídea de \\(a\\) entre \\(n\\), luego \\(s=r\\). \\(\blacksquare\\)

Este resultado no es más que la traducción, al lenguaje de congruencias, del hecho ya conocido de que cada entero se escribe de una sola manera como \\(nk+r\\), \\(r\in\\{0,\dots,n-1\\}\\); si se cambia el conjunto \\(\\{0,\dots,n-1\\}\\) por cualquier otro conjunto de representantes, se llega a la siguiente definición.

**Definición.** Un **sistema completo de residuos módulo \\(n\\)** es un conjunto \\(R\\) de enteros tal que todo \\(a\in\mathbb{Z}\\) es congruente módulo \\(n\\) con uno y solo uno de los elementos de \\(R\\).

**Ejemplo.** \\(\\{8,-3,6,-1\\}\\) es un sistema completo de residuos módulo 4: \\(8\equiv0\\), \\(-3\equiv1\\), \\(6\equiv2\\), \\(-1\equiv3\pmod4\\). Dicho de otro modo, todo entero es de una y solo una de las formas \\(4k+8,\\,4k-3,\\,4k+6,\\,4k-1\\).

**Lema 5.4.** *Sea \\(n\\) un entero positivo y \\(R=\\{r_1,\dots,r_m\\}\\) un conjunto de enteros. Sean \\(r_1',\dots,r_m'\\) los residuos respectivos de \\(r_1,\dots,r_m\\) al dividirlos entre \\(n\\). Son equivalentes:*

1. *\\(R\\) es un sistema completo de residuos módulo \\(n\\).*
2. *\\(m\ge n\\) y, para \\(i\ne j\\), \\(r_i\not\equiv r_j\pmod n\\).*
3. *Los números \\(r_1',\dots,r_m'\\) coinciden, en algún orden, con \\(0,1,\dots,n-1\\).*

*Demostración.* **(i)⟹(ii).** Como cada uno de \\(0,1,\dots,n-1\\) es congruente con algún elemento de \\(R\\), y dos de ellos nunca son congruentes entre sí (Proposición 5.3), \\(R\\) debe contener al menos \\(n\\) elementos, así que \\(m\ge n\\). Si para algún \\(i\ne j\\) fuera \\(r_i\equiv r_j\pmod n\\), entonces algún entero (por ejemplo \\(r_i\\)) sería simultáneamente congruente con dos elementos distintos de \\(R\\), contradiciendo que \\(R\\) es un sistema completo.

**(ii)⟹(iii).** Si \\(i\ne j\\), por hipótesis \\(r_i\not\equiv r_j\pmod n\\), luego por la Proposición 5.3, \\(r_i'\ne r_j'\\). Así, \\(r_1',\dots,r_m'\\) son \\(m\\) elementos distintos entre los \\(n\\) elementos \\(0,1,\dots,n-1\\); como \\(m\ge n\\), ambos conjuntos deben coincidir.

**(iii)⟹(i).** Por la Proposición 5.3, cada entero es congruente con uno y solo uno de \\(0,1,\dots,n-1\\), que por hipótesis son precisamente \\(r_1',\dots,r_m'\\). Y como, de nuevo por la Proposición 5.3, un entero es congruente con \\(r_i'\\) si y solo si lo es con \\(r_i\\) (pues \\(r_i\equiv r_i'\pmod n\\) por definición de residuo), se concluye que cada entero es congruente con uno y solo uno de \\(r_1,\dots,r_m\\), es decir, \\(R\\) es un sistema completo de residuos módulo \\(n\\). \\(\blacksquare\\)

**Proposición 5.5.** *Dado un entero positivo \\(n\\), los siguientes conjuntos son sistemas completos de residuos módulo \\(n\\):*

1. *Cualquier conjunto de \\(n\\) enteros consecutivos.*
2. *\\(\\{ar_1+b,\dots,ar_n+b\\}\\), donde \\(\\{r_1,\dots,r_n\\}\\) es un sistema completo de residuos módulo \\(n\\), \\(\gcd(a,n)=1\\) y \\(b\\) es cualquier entero.*
3. *\\(\\{b,a+b,2a+b,\dots,(n-1)a+b\\}\\), donde \\(\gcd(a,n)=1\\) y \\(b\\) es cualquier entero (caso particular de (ii)).*

*Demostración.* (i) tiene \\(n\\) elementos y claramente no hay dos que sean congruentes entre sí (su diferencia, en valor absoluto, es menor que \\(n\\) y no nula), así que el Lema 5.4(ii) da el resultado. Para (ii): como \\(\\{r_1,\dots,r_n\\}\\) es sistema completo, si \\(i\ne j\\) entonces \\(r_i\not\equiv r_j\pmod n\\) (Lema 5.4). Como \\(\gcd(a,n)=1\\), la Proposición 5.1(vi) da \\(ar_i\not\equiv ar_j\pmod n\\), y por tanto \\(ar_i+b\not\equiv ar_j+b\pmod n\\). El Lema 5.4(ii) concluye que este conjunto (que tiene \\(n\\) elementos) es un sistema completo. (iii) es el caso particular de (ii) con \\(\\{r_1,\dots,r_n\\}=\\{0,1,\dots,n-1\\}\\). \\(\blacksquare\\)

## Aplicación: criterios de divisibilidad

**Ejemplo 5.6 (criterios de divisibilidad por 3, 9 y 11; pruebas del nueve y del once).** Recordemos que un número con expresión decimal \\(a_ra_{r-1}\cdots a_1a_0\\) representa \\(n=a_r10^r+a_{r-1}10^{r-1}+\cdots+a_110+a_0\\).

- Como \\(10\equiv1\pmod3\\), la Proposición 5.1(v) da \\(10^i\equiv1\pmod3\\) para todo \\(i\ge0\\), y sumando (Proposición 5.1(iv)), \\(n\equiv a_r+a_{r-1}+\cdots+a_1+a_0\pmod3\\). En particular: **un número es divisible por 3 si y solo si la suma de sus cifras lo es** (justificando así, con rigor, la Proposición 1.11 de la Unidad 1).
- Igualmente, \\(10\equiv1\pmod9\\), así que **un número es divisible por 9 si y solo si la suma de sus cifras lo es**. Esto da lugar a la clásica **prueba del nueve**: por ejemplo, para verificar el producto \\(53914\times13518=728\\,809\\,452\\), calculamos las sumas de cifras módulo 9 reducidas: \\(53914\equiv5+3+9+1+4=22\equiv4\pmod9\\), \\(13518\equiv1+3+5+1+8=18\equiv0\pmod9\\); el producto de residuos es \\(4\cdot0=0\pmod9\\), así que el resultado debe ser \\(\equiv0\pmod9\\): en efecto, \\(7+2+8+8+0+9+4+5+2=45\equiv0\pmod9\\). Si esta comprobación *no* coincidiera, sabríamos con certeza que la multiplicación está mal hecha (aunque, como se aprecia, que la prueba "salga bien" no garantiza que el cálculo sea correcto, pues números distintos pueden compartir residuo módulo 9).
- Como \\(10\equiv-1\pmod{11}\\), se tiene \\(10^i\equiv(-1)^i\pmod{11}\\), así que \\(n\equiv(-1)^ra_r+(-1)^{r-1}a_{r-1}+\cdots-a_1+a_0\pmod{11}\\). Es decir, **un número es divisible por 11 si y solo si la suma alternada de sus cifras (de derecha a izquierda) es divisible por 11**, dando lugar de manera análoga a una **prueba del once**, que puede usarse junto con la prueba del nueve para reforzar la verificación de un cálculo.

## Reducción de módulos

**Proposición 5.7.** *Sean \\(n_1,n_2,\dots,n_r\\) enteros positivos primos relativos dos a dos (\\(\gcd(n_i,n_j)=1\\) si \\(i\ne j\\)). Entonces, para cualesquiera enteros \\(a,b\\),*
\\[ a\equiv b\pmod{n_1n_2\cdots n_r} \iff a\equiv b\pmod{n_i} \text{ para cada } i=1,\dots,r. \\]

*Demostración.* Por definición, \\(a\equiv b\pmod{n_1\cdots n_r}\\) si y solo si \\(n_1n_2\cdots n_r\mid(a-b)\\). Como los \\(n_i\\) son coprimos dos a dos, aplicando repetidamente la Proposición 1.19(vii) (si \\(a\mid c,b\mid c,\gcd(a,b)=1\Rightarrow ab\mid c\\)), esto equivale a que \\(n_i\mid(a-b)\\) para cada \\(i\\), es decir, a que \\(a\equiv b\pmod{n_i}\\) para cada \\(i\\). \\(\blacksquare\\)

Este resultado será la clave del Teorema Chino del Resto (Sección 5.5): reduce el estudio de congruencias módulo un producto de coprimos al estudio simultáneo de congruencias módulo cada factor.

**Proposición 5.8 (reducción por un divisor).** *Si \\(d\mid n\\), entonces \\(a\equiv b\pmod{n/d}\\) si y solo si \\(a\equiv b+i\cdot(n/d)\pmod n\\) para algún \\(i\in\\{0,1,\dots,d-1\\}\\). Además, los números \\(b,\\,b+n/d,\\,\dots,\\,b+(d-1)(n/d)\\) son dos a dos incongruentes módulo \\(n\\).*

*Demostración.* (\\(\Leftarrow\\)) Si \\(a\equiv b+i(n/d)\pmod n\\), existe \\(c\in\mathbb{Z}\\) con \\(a-b-i(n/d)=cn\\), es decir, \\(a-b=(n/d)(i+cd)\\), luego \\((n/d)\mid(a-b)\\), es decir, \\(a\equiv b\pmod{n/d}\\).

(\\(\Rightarrow\\)) Si \\(a\equiv b\pmod{n/d}\\), existe \\(t\in\mathbb{Z}\\) tal que \\(a=b+(n/d)t\\). Dividiendo \\(t\\) entre \\(d\\) (Teorema 1.12): \\(t=qd+i\\), \\(0\le i<d\\). Entonces \\(a=b+(n/d)(qd+i)=b+nq+i(n/d)\\), de donde \\(a\equiv b+i(n/d)\pmod n\\), con \\(0\le i<d\\).

Finalmente, los \\(d\\) números \\(b,b+n/d,\dots,b+(d-1)(n/d)\\) son un subconjunto de \\(\\{b,b+1,\dots,b+(n-1)\\}\\), que es un sistema completo de residuos módulo \\(n\\) (Proposición 5.5(i)), y por tanto son dos a dos incongruentes módulo \\(n\\) (Lema 5.4(ii)). \\(\blacksquare\\)

Esta proposición se usará en la Sección 5.4, al contar el número de soluciones de una congruencia lineal.
