# 1.3 Máximo común divisor y mínimo común múltiplo

## Máximo común divisor

**Definición.** Sean \\(a,b \in \mathbb{Z}\\), no ambos cero. El **máximo común divisor** de \\(a\\) y \\(b\\), denotado \\(\gcd(a,b)\\) o \\(\mathrm{mcd}(a,b)\\), es el mayor entero positivo que divide simultáneamente a \\(a\\) y a \\(b\\).

La existencia de este máximo no es evidente por sí sola —requiere justificación— y la damos a continuación usando el buen orden. De paso obtenemos la caracterización más importante del máximo común divisor: es una combinación lineal entera de \\(a\\) y \\(b\\).

**Teorema 1.16 (Existencia del mcd).** *Sean \\(a,b \in \mathbb{Z}\\), no ambos cero. Existe \\(d = \gcd(a,b)\\), y además \\(d\\) es el menor entero positivo que se puede escribir como combinación lineal entera de \\(a\\) y \\(b\\), es decir,*
\\[ d = \min\{ax+by : x,y\in\mathbb{Z},\ ax+by>0\}. \\]

*Demostración.* Sea \\(C = \{ax+by : x,y \in \mathbb{Z}\} \cap \mathbb{Z}^+\\). Como no ambos de \\(a,b\\) son cero, digamos \\(a \neq 0\\); entonces \\(a\cdot a + b \cdot 0 = a^2 > 0\\) pertenece a \\(C\\) (tomando \\(x=a,y=0\\)), luego \\(C \neq \emptyset\\). Por el Principio del Buen Orden, \\(C\\) tiene un elemento mínimo \\(d = ax_0+by_0\\), para ciertos \\(x_0,y_0 \in \mathbb{Z}\\).

*Afirmación: \\(d \mid a\\) y \\(d \mid b\\).* Dividimos \\(a\\) entre \\(d\\) (Teorema 1.12): \\(a = dq+r\\), \\(0 \le r < d\\). Entonces
\\[ r = a - dq = a - (ax_0+by_0)q = a(1-x_0q) + b(-y_0q), \\]
que es una combinación lineal entera de \\(a\\) y \\(b\\). Si \\(r>0\\), entonces \\(r \in C\\) y \\(r<d\\), contradiciendo la minimalidad de \\(d\\). Luego \\(r=0\\), es decir, \\(d \mid a\\). El mismo argumento con \\(b\\) en lugar de \\(a\\) da \\(d \mid b\\).

*Afirmación: \\(d\\) es el máximo de los divisores comunes.* Sea \\(c\\) cualquier divisor común de \\(a\\) y \\(b\\). Por la Proposición 1.9(ii), \\(c \mid (ax_0+by_0) = d\\), y por la Proposición 1.9(iii) (como \\(d>0\\)), \\(c \le |c| \le d\\). Luego todo divisor común de \\(a,b\\) es \\(\le d\\), y como \\(d\\) mismo es un divisor común, \\(d = \gcd(a,b)\\).

Esto también muestra que \\(d\\) es el menor elemento positivo de \\(C\\), que es justamente la afirmación del enunciado. \\(\blacksquare\\)

**Corolario 1.17 (Identidad de Bézout — versión preliminar).** *Para cualesquiera \\(a,b \in \mathbb{Z}\\) no ambos cero, existen \\(x,y \in \mathbb{Z}\\) tales que \\(\gcd(a,b) = ax+by\\).*

Esto es exactamente lo demostrado en el Teorema 1.16; en la Sección 1.4 daremos un método **algorítmico** (el algoritmo de Euclides extendido) para calcular explícitamente tales \\(x,y\\), en vez de solo garantizar su existencia por el buen orden.

**Definición.** Decimos que \\(a\\) y \\(b\\) son **primos relativos** (o **coprimos**) si \\(\gcd(a,b)=1\\).

**Corolario 1.18.** *\\(a\\) y \\(b\\) son primos relativos si y solo si existen \\(x,y\in\mathbb{Z}\\) con \\(ax+by=1\\).*

*Demostración.* Si \\(\gcd(a,b)=1\\), el Corolario 1.17 da tales \\(x,y\\). Recíprocamente, si \\(ax+by=1\\) para algunos \\(x,y\\), sea \\(d=\gcd(a,b)\\); como \\(d\mid a\\) y \\(d \mid b\\), la Proposición 1.9(ii) da \\(d \mid (ax+by) = 1\\), y como \\(d \geq 1\\), se sigue \\(d=1\\). \\(\blacksquare\\)

## Propiedades del máximo común divisor

**Proposición 1.19.** *Sean \\(a,b,c \in \mathbb{Z}\\), con los que se formen las expresiones abajo (siempre con al menos un argumento no nulo en cada mcd). Se cumple:*

1. *\\(\gcd(a,b) = \gcd(b,a) = \gcd(|a|,|b|)\\).*
2. *\\(\gcd(a,0) = |a|\\) para \\(a \neq 0\\).*
3. *\\(\gcd(a,b) = \gcd(a, b+ka)\\) para todo \\(k \in \mathbb{Z}\\). En particular, \\(\gcd(a,b)=\gcd(a,b-a)\\) y, si \\(b=aq+r\\), \\(\gcd(a,b)=\gcd(a,r)\\).*
4. *(Existencia de "mcd normalizado") Si \\(d=\gcd(a,b)\\), entonces \\(\gcd(a/d,\,b/d)=1\\).*
5. *Si \\(c>0\\), \\(\gcd(ca,cb) = c\gcd(a,b)\\).*
6. *(Lema de Euclides) Si \\(\gcd(a,b)=1\\) y \\(a \mid bc\\), entonces \\(a \mid c\\).*
7. *Si \\(a \mid c\\), \\(b \mid c\\) y \\(\gcd(a,b)=1\\), entonces \\(ab \mid c\\).*

*Demostración.*

(i) y (ii) son inmediatas de la definición.

(iii) Basta ver que el conjunto de divisores comunes de \\(a\\) y \\(b\\) coincide con el conjunto de divisores comunes de \\(a\\) y \\(b+ka\\): si \\(e \mid a\\) y \\(e \mid b\\), entonces \\(e \mid (b+ka)\\) por la Proposición 1.9(ii); recíprocamente, si \\(e \mid a\\) y \\(e \mid (b+ka)\\), entonces \\(e \mid \big((b+ka) - ka\big) = b\\). Como ambos conjuntos de divisores comunes coinciden, también coincide el máximo de cada uno.

(iv) Como \\(d=\gcd(a,b)\\), por el Corolario 1.17 existen \\(x,y\\) con \\(ax+by=d\\); dividiendo entre \\(d\\) (nótese \\(d\ne 0\\)), \\((a/d)x + (b/d)y = 1\\), y como \\(a/d,b/d \in \mathbb{Z}\\) (porque \\(d\\) divide a ambos), el Corolario 1.18 da \\(\gcd(a/d,b/d)=1\\).

(v) Por el Teorema 1.16, \\(\gcd(ca,cb)\\) es el menor entero positivo de la forma \\(cax+cby = c(ax+by)\\); como \\(c>0\\), esto equivale a \\(c\\) veces el menor valor positivo de \\(ax+by\\), que es \\(c\cdot\gcd(a,b)\\).

(vi) Como \\(\gcd(a,b)=1\\), por el Corolario 1.18 existen \\(x,y\\) con \\(ax+by=1\\). Multiplicando por \\(c\\): \\(acx+bcy=c\\). Como \\(a \mid ac\\) (trivialmente) y \\(a \mid bc\\) (por hipótesis), la Proposición 1.9(ii) da \\(a \mid (acx+bcy) = c\\).

(vii) Como \\(a \mid c\\), escribimos \\(c=am\\). Como \\(b \mid c = am\\) y \\(\gcd(a,b)=1\\) (equivalentemente \\(\gcd(b,a)=1\\)), la parte (vi) (con los papeles de \\(a,b\\) intercambiados) da \\(b \mid m\\), digamos \\(m=bn\\). Entonces \\(c=am=abn\\), luego \\(ab \mid c\\). \\(\blacksquare\\)

El Lema de Euclides (parte (vi)) es, junto con el algoritmo de la división, el resultado técnico más usado del curso: es la clave, entre otras cosas, de la unicidad de la factorización en primos (Unidad 2) y de buena parte de la teoría de congruencias (Unidad 5).

**Ejemplo 1.20.** Calculemos \\(\gcd(48,18)\\) usando la Proposición 1.19(iii) repetidamente (esto es, de hecho, el germen del algoritmo de Euclides que formalizaremos en la Sección 1.4):
\\[ \gcd(48,18) = \gcd(18, 48-2\cdot 18) = \gcd(18,12) = \gcd(12, 18-12) = \gcd(12,6) = \gcd(6, 12-2\cdot6)=\gcd(6,0)=6. \\]

## Mínimo común múltiplo

**Definición.** Sean \\(a,b \in \mathbb{Z}\\) no nulos. El **mínimo común múltiplo** de \\(a\\) y \\(b\\), denotado \\(\mathrm{mcm}(a,b)\\), es el menor entero positivo que es múltiplo simultáneamente de \\(a\\) y de \\(b\\).

La existencia de \\(\mathrm{mcm}(a,b)\\) se sigue directamente del PBO: el conjunto de los múltiplos comunes positivos de \\(a\\) y \\(b\\) es no vacío (contiene a \\(|ab|\\)) y por tanto tiene mínimo.

**Teorema 1.21 (Relación fundamental entre mcd y mcm).** *Para \\(a,b \in \mathbb{Z}^+\\),*
\\[ \gcd(a,b)\cdot \mathrm{mcm}(a,b) = ab. \\]

*Demostración.* Sea \\(d=\gcd(a,b)\\) y sea \\(m = ab/d\\) (que es un entero, pues \\(d \mid a\\) implica \\(d \mid ab\\)... más precisamente, \\(a=da'\\) con \\(a'\in \mathbb{Z}\\), luego \\(m=a'b \in \mathbb{Z}\\)). Veamos que \\(m = \mathrm{mcm}(a,b)\\).

*\\(m\\) es múltiplo común.* Escribiendo \\(a=da'\\), \\(b=db'\\) con \\(\gcd(a',b')=1\\) (Proposición 1.19(iv)), tenemos \\(m = ab/d = a'b'd = a\cdot b' = b \cdot a'\\), luego \\(a \mid m\\) y \\(b \mid m\\).

*\\(m\\) es el menor tal.* Sea \\(c\\) cualquier múltiplo común positivo de \\(a\\) y \\(b\\); escribamos \\(c=a k\\) para algún entero \\(k\\). Como \\(b \mid c = ak = da'k\\) y \\(b=db'\\), se sigue \\(b' \mid a'k\\). Pero \\(\gcd(a',b')=1\\), así que por el Lema de Euclides (Proposición 1.19(vi)), \\(b' \mid k\\), digamos \\(k=b't\\). Entonces \\(c = ak = ab't = mt\\), es decir, \\(m \mid c\\), y como \\(c>0\\) y \\(m>0\\), la Proposición 1.9(iii) da \\(m \le c\\).

Por tanto \\(m\\) es el menor múltiplo común positivo, es decir, \\(m=\mathrm{mcm}(a,b)\\), y \\(d\cdot m = d \cdot (ab/d) = ab\\). \\(\blacksquare\\)

**Corolario 1.22.** *Si \\(\gcd(a,b)=1\\), entonces \\(\mathrm{mcm}(a,b)=ab\\).*

**Ejemplo 1.23.** Como \\(\gcd(48,18)=6\\) (Ejemplo 1.20), \\(\mathrm{mcm}(48,18) = \dfrac{48\cdot 18}{6} = \dfrac{864}{6}=144\\).

## Propiedades del mínimo común múltiplo

**Proposición 1.24.** *Sean \\(a,b,c \in \mathbb{Z}^+\\). Se cumple:*

1. *\\(\mathrm{mcm}(a,b)=\mathrm{mcm}(b,a)\\).*
2. *Si \\(a \mid b\\), entonces \\(\mathrm{mcm}(a,b)=b\\).*
3. *\\(\mathrm{mcm}(ca,cb) = c\cdot\mathrm{mcm}(a,b)\\).*
4. *Todo múltiplo común de \\(a\\) y \\(b\\) es múltiplo de \\(\mathrm{mcm}(a,b)\\).*

*Demostración.* (i) y (ii) son inmediatas. (iii) se sigue de (v) de la Proposición 1.19 y del Teorema 1.21: \\(\mathrm{mcm}(ca,cb) = \dfrac{ca\cdot cb}{\gcd(ca,cb)} = \dfrac{c^2ab}{c\gcd(a,b)} = c\cdot\dfrac{ab}{\gcd(a,b)}=c\cdot\mathrm{mcm}(a,b)\\). (iv) ya se demostró dentro de la prueba del Teorema 1.21. \\(\blacksquare\\)

La noción de mcd (y, dualmente, la de mcm) se extiende de manera natural a más de dos enteros: \\(\gcd(a_1,\dots,a_n)\\) es el mayor entero positivo que divide a todos los \\(a_i\\), y puede calcularse recursivamente mediante \\(\gcd(a_1,\dots,a_n) = \gcd(a_1,\gcd(a_2,\dots,a_n))\\); análogamente para el mcm. Estas generalizaciones se explorarán en los ejercicios.
