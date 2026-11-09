# 5.4 Unidades módulo n y congruencias lineales

## El grupo de unidades \\(\mathbb{Z}_n^\ast\\)

**Definición.** Un elemento \\(a\in\mathbb{Z}\\) (o su clase de congruencia módulo \\(n\\)) se llama una **unidad módulo \\(n\\)** si existe \\(b\in\mathbb{Z}\\) tal que \\(ab\equiv1\pmod n\\); a tal \\(b\\) se le llama un **inverso de \\(a\\) módulo \\(n\\)**. El conjunto de las clases de unidades módulo \\(n\\) se denota
\\[ \mathbb{Z}_n^\ast = \\{a\in\\{0,1,\dots,n-1\\} : a \text{ es unidad módulo } n\\}. \\]

**Proposición 5.22.** *\\(a\\) es unidad módulo \\(n\\) si y solo si \\(\gcd(a,n)=1\\). En consecuencia, \\(|\mathbb{Z}_n^\ast|=\varphi(n)\\), y el inverso de una unidad es único módulo \\(n\\).*

*Demostración.* Si \\(\gcd(a,n)=1\\), por el Corolario 1.18, existen \\(x,y\in\mathbb{Z}\\) con \\(ax+ny=1\\); reduciendo módulo \\(n\\), \\(ax\equiv1\pmod n\\), así que \\(b=x\\) es un inverso de \\(a\\). Recíprocamente, si \\(ab\equiv1\pmod n\\), entonces \\(n\mid(ab-1)\\), digamos \\(ab-1=nk\\), es decir, \\(ab-nk=1\\); por la Proposición 1.32, esto implica \\(\gcd(a,n)\mid1\\), luego \\(\gcd(a,n)=1\\).

La cardinalidad \\(|\mathbb{Z}_n^\ast|=\varphi(n)\\) es entonces inmediata de la definición de φ (Sección 4.2). Para la unicidad del inverso: si \\(ab\equiv1\pmod n\\) y \\(ab'\equiv1\pmod n\\), entonces \\(ab\equiv ab'\pmod n\\), y como \\(\gcd(a,n)=1\\), la Proposición 5.1(vi) permite cancelar \\(a\\), dando \\(b\equiv b'\pmod n\\). \\(\blacksquare\\)

**Observación 5.23.** El conjunto \\(\mathbb{Z}_n^\ast\\), con la multiplicación módulo \\(n\\), forma un **grupo abeliano finito** de orden \\(\varphi(n)\\) (cerradura: producto de unidades es unidad, por la Proposición 1.19(vi)-tipo argumento con primos; asociatividad y conmutatividad heredadas de \\(\mathbb{Z}\\); neutro \\(1\\); inversos por la Proposición 5.22). El Teorema de Euler (Teorema 5.10) es, en este lenguaje, la afirmación de que **todo elemento de un grupo finito de orden \\(m\\) satisface \\(g^m=e\\)** (el elemento neutro), aplicada a \\(\mathbb{Z}_n^\ast\\); esta es una de las conexiones más directas entre la teoría de números elemental y la teoría de grupos, que se explora con más profundidad en cursos de álgebra abstracta.

## Congruencias lineales

**Definición.** Una **congruencia lineal** es una expresión de la forma \\(ax\equiv b\pmod n\\), donde \\(a,b,n\\) son enteros dados (\\(n>0\\), \\(a\ne0\\)) y \\(x\\) es la incógnita. Dos soluciones \\(x_1,x_2\\) se consideran **la misma solución** si \\(x_1\equiv x_2\pmod n\\); así, "el número de soluciones" de una congruencia lineal se entiende siempre como el número de soluciones incongruentes módulo \\(n\\), es decir, distintas dentro de un sistema completo de residuos.

**Proposición 5.24 (existencia y número de soluciones).** *Sean \\(a,b,n\in\mathbb{Z}\\), \\(n>0\\), \\(a\ne0\\), y sea \\(d=\gcd(a,n)\\). La congruencia \\(ax\equiv b\pmod n\\) tiene solución si y solo si \\(d\mid b\\). En tal caso, tiene exactamente \\(d\\) soluciones incongruentes módulo \\(n\\).*

*Demostración.* La congruencia \\(ax\equiv b\pmod n\\) tiene solución \\(x\\) si y solo si existe \\(y\in\mathbb{Z}\\) tal que \\(b-ax=ny\\), es decir, si y solo si la ecuación diofántica \\(ax+ny=b\\) tiene solución. Por el Teorema 1.33 (Unidad 1), esto ocurre si y solo si \\(d=\gcd(a,n)\mid b\\).

Supongamos ahora \\(d\mid b\\). Por el Teorema 1.33, todas las soluciones \\(x\\) de \\(ax+ny=b\\) (para algún \\(y\\)) son de la forma
\\[ x = x_0 + \frac nd\\, t, \qquad t\in\mathbb{Z}, \\]
donde \\(x_0\\) es una solución particular. Por la Proposición 5.8 (con \\(b\\) ahí sustituido por \\(x_0\\)), los valores \\(x_0, x_0+\frac nd, x_0+2\frac nd,\dots,x_0+(d-1)\frac nd\\) son dos a dos **incongruentes módulo \\(n\\)**, y todo entero de la forma \\(x_0+\frac nd t\\) es congruente módulo \\(n\\) con exactamente uno de ellos. Por tanto, hay exactamente \\(d\\) soluciones incongruentes módulo \\(n\\). \\(\blacksquare\\)

**Corolario 5.25.** *Si \\(\gcd(a,n)=1\\), la congruencia \\(ax\equiv b\pmod n\\) tiene solución única módulo \\(n\\) para cualquier \\(b\\).*

Este corolario justifica formalmente el paso, usado sin demostrar en el Teorema 5.17 (Wilson): la existencia y unicidad del inverso multiplicativo de cada \\(a\in\\{1,\dots,p-1\\}\\) módulo un primo \\(p\\).

**Ejemplo 5.26.** Resolvamos la congruencia lineal \\(72x\equiv8\pmod{28}\\). Como se calculó en el Ejemplo 1.34 (Unidad 1), \\(d=\gcd(72,28)=4\\), y \\(4\mid8\\), así que la congruencia tiene exactamente \\(4\\) soluciones módulo \\(28\\). Resolviendo la ecuación diofántica asociada \\(72x+28y=8\\) (Ejemplo 1.34), obtuvimos la solución general
\\[ x=4+7t, \qquad t\in\mathbb{Z}. \\]
Es decir, \\(x\equiv4\pmod7\\), lo que —expresado módulo \\(28\\), como pide el enunciado original— da las \\(4\\) soluciones incongruentes:
\\[ x\equiv4,\ 11,\ 18,\ 25 \pmod{28}. \\]

Este ejemplo ilustra el principio general (Proposición 5.24): la congruencia \\(ax\equiv b\pmod n\\) siempre se reduce a una congruencia de la forma \\(x\equiv x_0\pmod{n/d}\\) (equivalentemente, a \\(d\\) clases residuales módulo \\(n\\)), lo que —junto con el resultado análogo para **sistemas** de tales congruencias— motiva directamente el Teorema Chino del Resto de la siguiente sección.
