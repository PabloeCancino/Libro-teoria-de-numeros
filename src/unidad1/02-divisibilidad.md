# 1.2 Divisibilidad y el algoritmo de la división

## La relación de divisibilidad

**Definición.** Sean \\(a, b \in \mathbb{Z}\\). Decimos que \\(a\\) **divide** a \\(b\\), y escribimos \\(a \mid b\\), si existe \\(c \in \mathbb{Z}\\) tal que \\(b = ac\\). En tal caso decimos también que \\(a\\) es un **divisor** de \\(b\\), que \\(b\\) es un **múltiplo** de \\(a\\), o que \\(b\\) es **divisible** por \\(a\\). Si no existe tal \\(c\\), escribimos \\(a \nmid b\\).

**Observación 1.8.** Para todo \\(a \in \mathbb{Z}\\): \\(a \mid 0\\) (tomando \\(c=0\\)); \\(1 \mid a\\) y \\(-1 \mid a\\); y si \\(a \ne 0\\), \\(a \mid a\\). Por otro lado, \\(0 \mid a\\) si y solo si \\(a = 0\\).

**Proposición 1.9.** *Sean \\(a,b,c \in \mathbb{Z}\\). Se cumple:*

1. *Si \\(a \mid b\\) y \\(b \mid c\\), entonces \\(a \mid c\\) (transitividad).*
2. *Si \\(a \mid b\\) y \\(a \mid c\\), entonces \\(a \mid (bx + cy)\\) para cualesquiera \\(x, y \in \mathbb{Z}\\) (en particular, \\(a \mid (b+c)\\) y \\(a \mid (b - c)\\)).*
3. *Si \\(a \mid b\\) y \\(b \ne 0\\), entonces \\(|a| \le |b|\\).*
4. *\\(a \mid b\\) y \\(b \mid a\\) si y solo si \\(a = \pm b\\).*
5. *Si \\(a \mid b\\), entonces \\(ac \mid bc\\) para todo \\(c \in \mathbb{Z}\\); recíprocamente, si \\(c \neq 0\\) y \\(ac \mid bc\\), entonces \\(a \mid b\\).*

*Demostración.*

(i) Si \\(a \mid b\\) y \\(b \mid c\\), existen \\(k, l \in \mathbb{Z}\\) con \\(b = ak\\) y \\(c = bl\\). Entonces \\(c = (ak)l = a(kl)\\), y como \\(kl \in \mathbb{Z}\\), se sigue \\(a \mid c\\).

(ii) Si \\(a \mid b\\) y \\(a \mid c\\), existen \\(k,l\\) con \\(b = ak\\), \\(c = al\\). Entonces \\(bx + cy = akx + aly = a(kx+ly)\\), y \\(kx + ly \in \mathbb{Z}\\), luego \\(a \mid (bx+cy)\\).

(iii) Si \\(a \mid b\\) con \\(b \ne 0\\), existe \\(k \ne 0\\) (pues \\(b \ne 0\\)) con \\(b = ak\\). Como \\(k\\) es un entero no nulo, \\(|k| \ge 1\\), luego \\(|b| = |a||k| \ge |a|\\).

(iv) Si \\(a = \pm b\\) es inmediato que \\(a \mid b\\) y \\(b \mid a\\). Recíprocamente, si \\(a \mid b\\) y \\(b \mid a\\): si \\(a = 0\\), entonces \\(b \mid 0\\) da automáticamente, pero \\(a \mid b\\) con \\(a=0\\) fuerza \\(b=0=a\\). Si \\(a \ne 0\\) (y por tanto \\(b \ne 0\\), pues si \\(b=0\\) entonces de \\(a\mid b\\) trivial pero \\(b \mid a\\) fuerza \\(a=0\\)), la parte (iii) aplicada dos veces da \\(|a| \le |b|\\) y \\(|b| \le |a|\\), luego \\(|a|=|b|\\), es decir \\(a = \pm b\\).

(v) Si \\(b = ak\\), entonces \\(bc = (ac)k\\), luego \\(ac \mid bc\\). Recíprocamente, si \\(c \ne 0\\) y \\(bc = (ac)k\\) para algún \\(k\\), entonces \\(c(b - ak) = 0\\), y como \\(c \ne 0\\) en un dominio íntegro como \\(\mathbb{Z}\\), se sigue \\(b = ak\\), es decir \\(a \mid b\\). \\(\blacksquare\\)

La propiedad (ii), con \\(x,y\\) enteros arbitrarios, se usará constantemente y merece un nombre: decimos que \\(bx+cy\\) es una **combinación lineal entera** de \\(b\\) y \\(c\\).

## Criterios elementales de divisibilidad

Como primera aplicación, obtenemos justificaciones rigurosas de las reglas de divisibilidad aprendidas en la escuela básica. Escribamos un entero positivo \\(n\\) en notación decimal como
\\[ n = a_r 10^r + a_{r-1}10^{r-1} + \dots + a_1 10 + a_0, \qquad a_i \in \\{0,\dots,9\\}. \\]

**Proposición 1.10 (Criterios de divisibilidad por 2, 5 y 10).** *\\(n\\) es divisible por \\(2\\) (resp. \\(5\\), \\(10\\)) si y solo si su última cifra \\(a_0\\) lo es.*

*Demostración.* Como \\(10 = 2\cdot 5\\), para \\(i \ge 1\\) se tiene \\(2 \mid 10^i\\) y \\(5 \mid 10^i\\), luego \\(n - a_0 = 10(a_r10^{r-1}+\dots+a_1)\\) es divisible por \\(2\\), por \\(5\\) y por \\(10\\). Por la Proposición 1.9(ii), \\(n\\) es divisible por alguno de estos números si y solo si \\(a_0\\) lo es. \\(\blacksquare\\)

**Proposición 1.11 (Criterios de divisibilidad por 3 y 9).** *\\(n\\) es divisible por 3 (resp. 9) si y solo si la suma de sus cifras \\(a_r + a_{r-1} + \dots + a_0\\) lo es.*

Este resultado se demuestra de manera más natural con el lenguaje de congruencias, y lo probaremos formalmente en el Ejemplo 5.6 de la Unidad 5 (junto con el criterio análogo para 11, la "prueba del nueve" y la "prueba del once"). La idea, adelantada aquí, es que \\(10 \equiv 1 \pmod 3\\) y \\(10 \equiv 1 \pmod 9\\), por lo que \\(10^i \equiv 1\\) en ambos módulos y \\(n \equiv a_r + \dots + a_0\\).

## El algoritmo de la división

El siguiente resultado —el más usado de todo el curso— garantiza que la división euclidiana con residuo siempre existe y es única.

**Teorema 1.12 (Algoritmo de la división).** *Sean \\(a, b \in \mathbb{Z}\\) con \\(b > 0\\). Existen enteros únicos \\(q\\) y \\(r\\) tales que*
\\[ a = bq + r, \qquad 0 \le r < b. \\]
*Al entero \\(q\\) se le llama el **cociente** y a \\(r\\) el **residuo** de la división de \\(a\\) entre \\(b\\).*

*Demostración (existencia).* Consideremos el conjunto
\\[ S = \\{a - bk : k \in \mathbb{Z}\\} \cap \mathbb{N}. \\]
Veamos primero que \\(S \neq \emptyset\\). Si \\(a \ge 0\\), tomando \\(k=0\\) obtenemos \\(a \in S\\). Si \\(a < 0\\), tomando \\(k = a\\) (nótese \\(a<0\\)) obtenemos \\(a - ba = a(1-b) \ge 0\\), pues \\(a<0\\) y \\(1-b \le 0\\) (ya que \\(b \ge 1\\)), y el producto de un negativo por un no positivo es no negativo; así que \\(a - ba \in S\\). En cualquier caso \\(S \neq \emptyset\\).

Por el Principio del Buen Orden, \\(S\\) tiene un elemento mínimo \\(r = a - bq\\), para cierto \\(q \in \mathbb{Z}\\), con \\(r \ge 0\\). Afirmamos que \\(r < b\\). Si no, \\(r \ge b\\), y entonces \\(r - b = a - b(q+1) \ge 0\\) sería un elemento de \\(S\\) estrictamente menor que \\(r\\) (pues \\(b>0\\)), contradiciendo la minimalidad de \\(r\\). Luego \\(0 \le r < b\\), y \\(a = bq+r\\), como se quería.

*Demostración (unicidad).* Supongamos \\(a = bq+r = bq'+r'\\) con \\(0 \le r,r' < b\\). Entonces \\(b(q-q') = r'-r\\), luego \\(b \mid (r'-r)\\). Pero \\(|r'-r| < b\\) (pues ambos están en \\([0,b)\\)), así que por la Proposición 1.9(iii), la única forma de que \\(b\\) divida a \\(r'-r\\) con \\(|r'-r|<b\\) es que \\(r'-r=0\\). Luego \\(r=r'\\), y de \\(b(q-q')=0\\) con \\(b\neq0\\) se sigue \\(q=q'\\). \\(\blacksquare\\)

**Observación 1.13.** El teorema se enuncia para \\(b>0\\); si se permite \\(b<0\\), el mismo argumento (aplicado a \\(|b|\\)) da existencia y unicidad de \\(q,r\\) con \\(a = bq+r\\), \\(0 \le r < |b|\\). En este curso trabajaremos casi siempre con divisores positivos.

**Ejemplo 1.14.** Al dividir \\(a=-37\\) entre \\(b=5\\): buscamos \\(q,r\\) con \\(-37 = 5q+r\\), \\(0\le r<5\\). Como \\(-37 = 5\cdot(-8) + 3\\), se tiene \\(q=-8\\), \\(r=3\\) (nótese que **no** es correcto tomar \\(q=-7\\), \\(r=-2\\), ya que el residuo debe ser no negativo).

**Definición.** Dado \\(a \in \mathbb{Z}\\), decimos que \\(a\\) es **par** si el residuo de dividir \\(a\\) entre 2 es 0, e **impar** si el residuo es 1. Por el Teorema 1.12, todo entero es de una y solo una de estas dos clases: \\(a = 2k\\) (par) o \\(a=2k+1\\) (impar), para un único \\(k \in \mathbb{Z}\\).

**Ejemplo 1.15 (una aplicación típica del algoritmo de la división).** Demostremos que el cuadrado de todo entero es de la forma \\(4k\\) o \\(4k+1\\) (nunca \\(4k+2\\) ni \\(4k+3\\)).

Por el Teorema 1.12 (con \\(b=4\\)), todo entero \\(n\\) se escribe como \\(n=4q, 4q+1,4q+2\\) o \\(4q+3\\). Elevando al cuadrado:

- \\((4q)^2 = 16q^2 = 4(4q^2)\\), de la forma \\(4k\\).
- \\((4q+1)^2 = 16q^2+8q+1 = 4(4q^2+2q)+1\\), de la forma \\(4k+1\\).
- \\((4q+2)^2 = 16q^2+16q+4 = 4(4q^2+4q+1)\\), de la forma \\(4k\\).
- \\((4q+3)^2 = 16q^2+24q+9 = 4(4q^2+6q+2)+1\\), de la forma \\(4k+1\\).

En los cuatro casos, \\(n^2\\) es de la forma \\(4k\\) o \\(4k+1\\). \\(\blacksquare\\)

Este tipo de argumento —clasificar los enteros según su residuo módulo un entero fijo y analizar cada caso— es una de las técnicas más productivas de la teoría de números elemental, y reaparecerá sistemáticamente a lo largo del libro, formalizada en el lenguaje de congruencias en la Unidad 5.
