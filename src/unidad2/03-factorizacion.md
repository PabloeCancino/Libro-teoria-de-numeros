# 2.3 Métodos elementales de factorización

El TFA garantiza que la factorización en primos existe y es única, pero no dice cómo hallarla eficientemente. En esta sección revisamos algunos métodos elementales —suficientes para números de tamaño moderado, aunque insuficientes para las magnitudes usadas en criptografía moderna (Unidad 6)— junto con algunas herramientas para decidir primalidad sin factorizar completamente.

## División por tanteo (trial division)

El método más directo se sigue inmediatamente del Corolario 2.8: para factorizar \\(n\\), se prueba a dividir sucesivamente entre \\(2,3,5,7,11,\dots\\) (los primos en orden creciente), extrayendo cada factor primo tantas veces como sea posible antes de pasar al siguiente, y deteniéndose cuando el cociente restante es \\(1\\) o es menor que el cuadrado del último primo probado (en cuyo caso el cociente restante, si es mayor que 1, es primo).

**Ejemplo 2.20.** Factoricemos \\(n=2\,310\\):
\\[ 2310 = 2\cdot1155 = 2\cdot3\cdot385=2\cdot3\cdot5\cdot77=2\cdot3\cdot5\cdot7\cdot11. \\]
Como el cociente final \\(11\\) es primo, la factorización es \\(2310=2\cdot3\cdot5\cdot7\cdot11\\) (el producto de los primeros cinco primos —de hecho, \\(2310\\) es conocido como el "primorial" \\(11\#\\)).

**Ejemplo 2.21.** Factoricemos \\(n=9\,409\\). Como \\(\sqrt{9409}=97\\), basta probar primos hasta \\(97\\). Ninguno de \\(2,3,5,7,\dots,89\\) divide a \\(9409\\) (se deja la verificación al lector), pero \\(97^2=9409\\), así que \\(9409=97^2\\).

## El método de factorización de Fermat

Cuando \\(n\\) es impar y tiene dos factores relativamente cercanos entre sí, el siguiente método —debido a Fermat— suele ser mucho más rápido que la división por tanteo.

**Proposición 2.22.** *Sea \\(n\\) un entero positivo impar. Existe una correspondencia biunívoca entre las factorizaciones \\(n=ab\\) con \\(a\ge b>0\\) y las representaciones \\(n=x^2-y^2\\) con \\(x,y\ge0\\) enteros, dada por*
\\[ x=\frac{a+b}{2}, \qquad y=\frac{a-b}{2} \qquad\Longleftrightarrow\qquad a=x+y,\ \ b=x-y. \\]

*Demostración.* Como \\(n\\) es impar, \\(a\\) y \\(b\\) son ambos impares (si \\(n=ab\\)), así que \\(a+b\\) y \\(a-b\\) son ambos pares, y \\(x,y\\) resultan enteros. Es inmediato verificar que \\(x^2-y^2=\left(\frac{a+b}2\right)^2-\left(\frac{a-b}2\right)^2=ab=n\\), y recíprocamente que si \\(n=x^2-y^2=(x+y)(x-y)\\), entonces \\(a=x+y,b=x-y\\) es una factorización de \\(n\\) (con \\(a\ge b>0\\) si \\(x>y\ge0\\)). Se comprueba directamente que ambas asignaciones son inversas entre sí. \\(\blacksquare\\)

**Algoritmo (método de Fermat).** Dado \\(n\\) impar, se buscan enteros \\(x \geq \lceil\sqrt n\rceil\\) tales que \\(x^2-n\\) sea un cuadrado perfecto \\(y^2\\); una vez hallado tal \\(x\\), la Proposición 2.22 da la factorización \\(n=(x+y)(x-y)\\). Concretamente: se prueba con \\(x=\lceil\sqrt n\rceil, \lceil\sqrt n\rceil+1,\dots\\) hasta que \\(x^2-n\\) sea un cuadrado perfecto.

**Ejemplo 2.23.** Factoricemos \\(n=5959\\) por el método de Fermat. Como \\(\sqrt{5959}\approx77.19\\), comenzamos en \\(x=78\\):

- \\(x=78\\): \\(x^2-n=6084-5959=125\\), no es cuadrado perfecto (\\(11^2=121\\), \\(12^2=144\\)).
- \\(x=79\\): \\(6241-5959=282\\), no es cuadrado.
- \\(x=80\\): \\(6400-5959=441=21^2\\). ¡Es cuadrado!

Luego \\(y=21\\), y \\(n=(80+21)(80-21)=101\cdot59\\). En efecto, \\(101\\) y \\(59\\) son ambos primos, así que esta es la factorización completa de \\(5959\\).

El método de Fermat es especialmente eficaz cuando \\(n\\) tiene un factor cercano a \\(\sqrt n\\) (pocos pasos), pero degenera al peor caso posible —tan lento como la división por tanteo, o peor— cuando los factores de \\(n\\) están muy separados (por ejemplo, si \\(n\\) es primo, o si \\(n=2\cdot m\\) con \\(m\\) primo grande, aunque en tal caso conviene primero extraer el factor 2). En la práctica, los algoritmos de factorización modernos (curvas elípticas de Lenstra, criba cuadrática, criba general del cuerpo de números) combinan y refinan estas ideas básicas.

## Criterios de primalidad basados en la criba

Recordemos del Corolario 2.8 que basta ensayar divisiones entre primos \\(p\le\sqrt n\\) para decidir si \\(n\\) es primo. Esto se puede refinar ligeramente:

**Proposición 2.24.** *Para decidir si \\(n>3\\) es primo, basta comprobar que \\(n\\) no es divisible por \\(2\\), por \\(3\\), ni por ningún entero de la forma \\(6k\pm1\\) con \\(6k\pm1 \le \sqrt n\\).*

*Demostración.* Todo entero es congruente, módulo 6, a uno de \\(0,1,2,3,4,5\\), es decir, tiene la forma \\(6k, 6k\pm1, 6k+2 (=6k'-4), 6k+3, 6k+4\\)... Más simplemente: todo primo \\(p>3\\) no puede ser de la forma \\(6k,6k+2,6k+3,6k+4\\), pues estos son divisibles por \\(2\\) o por \\(3\\) (\\(6k\\) y \\(6k+2=2(3k+1)\\) y \\(6k+4=2(3k+2)\\) son pares; \\(6k+3=3(2k+1)\\) es múltiplo de 3). Luego todo primo \\(p>3\\) es de la forma \\(6k+1\\) o \\(6k-1\\). Por el Corolario 2.8, basta entonces ensayar divisores primos —o, más simplemente y de forma suficiente, todos los enteros, primos o no— de esa forma hasta \\(\sqrt n\\), además de comprobar 2 y 3 directamente. \\(\blacksquare\\)

Esta observación reduce el número de candidatos a ensayar aproximadamente a un tercio (solo los enteros \\(\equiv\pm1\pmod 6\\)), lo cual es una mejora práctica modesta pero ilustra un patrón importante: los primos mayores que un cierto umbral están restringidos a ciertas clases de residuos, idea que se explota sistemáticamente y con mucha más fuerza en la Unidad 5 (Fermat, Miller-Rabin) para diseñar tests de primalidad probabilísticos mucho más rápidos que la factorización.

**Ejemplo 2.25.** Para verificar la primalidad de \\(n=211\\): como \\(\sqrt{211}\approx14.5\\), los candidatos de la forma \\(6k\pm1\\) hasta 14 son \\(5,7,11,13\\) (además de comprobar \\(2\\) y \\(3\\) por separado). Ninguno de \\(2,3,5,7,11,13\\) divide a \\(211\\), luego \\(211\\) es primo.
