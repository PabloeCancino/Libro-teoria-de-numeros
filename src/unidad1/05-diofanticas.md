# 1.5 Ecuaciones diofánticas lineales y cuadráticas

Se llama **ecuación diofántica** a cualquier ecuación polinomial de la que se buscan únicamente soluciones enteras (en honor a Diofanto de Alejandría, s. III d.C.). En esta sección resolvemos completamente el caso lineal en dos variables, apoyándonos en la Proposición 1.32, y estudiamos el caso cuadrático particular de las ternas pitagóricas.

## Ecuaciones diofánticas lineales

**Teorema 1.33.** *Sean \\(a,b,c \in \mathbb{Z}\\), con \\(a,b\\) no ambos cero, y sea \\(d=\gcd(a,b)\\). La ecuación*
\\[ ax+by=c \\]
*tiene solución \\((x,y)\in\mathbb{Z}^2\\) si y solo si \\(d \mid c\\). En caso de tener solución, si \\((x_0,y_0)\\) es una solución particular, entonces **todas** las soluciones están dadas por*
\\[ x = x_0 + \frac{b}{d}t, \qquad y = y_0 - \frac{a}{d}t, \qquad t \in \mathbb{Z}. \\]

*Demostración.* La existencia de solución si y solo si \\(d\mid c\\) es exactamente la Proposición 1.32.

Supongamos ahora que \\((x_0,y_0)\\) es una solución particular, esto es, \\(ax_0+by_0=c\\). Sea \\((x,y)\\) cualquier otra solución, \\(ax+by=c\\). Restando,
\\[ a(x-x_0)+b(y-y_0)=0, \quad\text{es decir,}\quad a(x-x_0)=-b(y-y_0). \\]
Escribamos \\(a=da'\\), \\(b=db'\\) con \\(\gcd(a',b')=1\\) (Proposición 1.19(iv)). Dividiendo entre \\(d\\):
\\[ a'(x-x_0) = -b'(y-y_0). \\]
Como \\(b' \mid a'(x-x_0)\\) y \\(\gcd(a',b')=1\\), el Lema de Euclides (Proposición 1.19(vi)) da \\(b' \mid (x-x_0)\\), digamos \\(x-x_0=b't\\) para algún \\(t\in\mathbb{Z}\\), es decir, \\(x=x_0+b't=x_0+\frac{b}{d}t\\). Sustituyendo de vuelta: \\(a'b't=-b'(y-y_0)\\), y como \\(b'\neq 0\\) (pues \\(b\ne 0\\) o, si \\(b=0\\), el argumento se ajusta trivialmente), se cancela para dar \\(y-y_0=-a't=-\frac{a}{d}t\\).

Recíprocamente, se verifica directamente que para cualquier \\(t\in\mathbb{Z}\\), \\(x=x_0+\frac{b}{d}t,\ y=y_0-\frac{a}{d}t\\) es solución:
\\[ ax+by = ax_0+by_0 + t\left(\frac{ab}{d}-\frac{ab}{d}\right) = c+0=c. \qquad\blacksquare \\]

El Teorema 1.27 (Bézout, vía el algoritmo de Euclides extendido) proporciona el método práctico para hallar la solución particular \\((x_0,y_0)\\): se calcula \\(\gcd(a,b)=d=ax_0'+by_0'\\), y si \\(d\mid c\\), digamos \\(c=dm\\), entonces \\((x_0,y_0)=(mx_0',my_0')\\) es una solución particular.

**Ejemplo 1.34.** Resolvamos \\(72x+28y=8\\) (este es precisamente el sistema que retomaremos en el Ejemplo 5.10 de la Unidad 5, al estudiar congruencias lineales). Primero, \\(\gcd(72,28)\\): usando Euclides,
\\[ 72=28\cdot2+16,\quad 28=16\cdot1+12,\quad 16=12\cdot1+4,\quad 12=4\cdot3+0, \\]
así que \\(d=\gcd(72,28)=4\\). Como \\(4 \mid 8\\), la ecuación tiene solución. Con Euclides extendido (subiendo desde el penúltimo paso):
\\[ 4=16-12, \quad 12=28-16, \implies 4=16-(28-16)=2\cdot16-28, \\]
\\[ 16=72-28\cdot2 \implies 4=2(72-28\cdot2)-28=2\cdot72-5\cdot28. \\]
Verificación: \\(2\cdot72-5\cdot28=144-140=4\\). ✓. Multiplicando por \\(m=8/4=2\\): \\(72\cdot4+28\cdot(-10)=8\\), es decir, una solución particular es \\(x_0=4,y_0=-10\\). Por el Teorema 1.33, con \\(b/d=28/4=7\\) y \\(a/d=72/4=18\\), la solución general es
\\[ x=4+7t, \qquad y=-10-18t, \qquad t\in\mathbb{Z}. \\]

**Ejemplo 1.35 (un problema clásico).** Un granjero compra vacas y cerdos por un total de \\(\$1050\\); cada vaca cuesta \\(\$70\\) y cada cerdo \\(\$30\\). ¿Cuántos animales de cada tipo pudo comprar?

Buscamos soluciones enteras **no negativas** de \\(70x+30y=1050\\), es decir, \\(7x+3y=105\\) (dividiendo entre \\(10\\)). Como \\(\gcd(7,3)=1\\), hay solución. Por inspección, \\(x_0=0,y_0=35\\) es una solución particular. Como \\(\gcd(7,3)=1\\), la solución general es
\\[ x=0+3t=3t, \qquad y=35-7t, \qquad t\in\mathbb{Z}. \\]
Para que \\(x\ge0\\) y \\(y\ge0\\) simultáneamente, necesitamos \\(t\ge0\\) y \\(t \le 5\\), es decir \\(t\in\{0,1,2,3,4,5\}\\), dando seis soluciones posibles: \\((x,y)\in\{(0,35),(3,28),(6,21),(9,14),(12,7),(15,0)\}\\). Este ejemplo ilustra que, aunque la ecuación diofántica tenga infinitas soluciones enteras, al imponer restricciones adicionales (aquí, no negatividad) el conjunto de soluciones admisibles se vuelve finito.

## Ternas pitagóricas

**Definición.** Una **terna pitagórica** es una terna \\((x,y,z)\\) de enteros positivos tal que \\(x^2+y^2=z^2\\). Se dice **primitiva** si \\(\gcd(x,y,z)=1\\) (equivalentemente, si los tres son coprimos dos a dos, como se verá abajo).

La ecuación \\(x^2+y^2=z^2\\) es un ejemplo de **ecuación diofántica cuadrática** en dos (esencialmente) variables, y a diferencia del caso lineal, no basta la teoría de combinaciones lineales para resolverla: se requiere un argumento aritmético específico, que combina divisibilidad, coprimalidad y factorización.

**Lema 1.36.** *En toda terna pitagórica primitiva \\((x,y,z)\\), exactamente uno de \\(x,y\\) es par y el otro impar (y por tanto \\(z\\) es impar).*

*Demostración.* Como \\(\gcd(x,y,z)=1\\), no pueden ser los tres pares. Si \\(x,y\\) fueran ambos impares, entonces \\(x^2,y^2 \equiv 1\\) y \\(z^2=x^2+y^2\\) sería de la forma \\(4k+2\\) (usando el Ejemplo 1.15: un cuadrado es \\(4k\\) o \\(4k+1\\), luego una suma de dos cuadrados impares —cada uno \\(4k+1\\)— es \\(4k+2\\)), pero ningún cuadrado es de la forma \\(4k+2\\), contradicción. Por tanto no pueden ser ambos impares; y si fueran ambos pares, \\(2\\) dividiría a \\(x,y\\) y también a \\(z\\) (pues \\(z^2=x^2+y^2\\) sería par, luego \\(z\\) par por el criterio de paridad de cuadrados), contradiciendo \\(\gcd(x,y,z)=1\\). Luego uno es par y el otro impar, y en consecuencia \\(z^2=x^2+y^2\\) es impar (par\\({}^2\\)+impar\\({}^2\\) = par + impar = impar), así que \\(z\\) es impar. \\(\blacksquare\\)

**Teorema 1.37 (Clasificación de las ternas pitagóricas primitivas).** *Todas las ternas pitagóricas primitivas \\((x,y,z)\\) con \\(y\\) par están dadas por*
\\[ x=m^2-n^2, \qquad y=2mn, \qquad z=m^2+n^2, \\]
*donde \\(m>n>0\\) son enteros coprimos de distinta paridad. Recíprocamente, toda elección de tales \\(m,n\\) produce una terna pitagórica primitiva.*

*Demostración (recíproco).* Si \\(x=m^2-n^2,\ y=2mn,\ z=m^2+n^2\\), un cálculo directo da \\(x^2+y^2=(m^2-n^2)^2+4m^2n^2=(m^2+n^2)^2=z^2\\). Falta ver primitividad: supongamos que un primo \\(p\\) divide a \\(x,y,z\\) (usaremos aquí la noción de primo de la Unidad 2, anticipada). Como \\(p\mid z\\) y \\(p \mid x\\), \\(p\\) divide a \\(z+x=2m^2\\) y a \\(z-x=2n^2\\). Si \\(p\ne2\\), entonces \\(p\mid m^2\\) y \\(p\mid n^2\\), luego \\(p\mid m\\) y \\(p\mid n\\) (Unidad 2), contradiciendo \\(\gcd(m,n)=1\\). Si \\(p=2\\), como \\(m,n\\) tienen distinta paridad, \\(m^2+n^2\\) es impar, así que \\(2\nmid z\\), contradicción. Luego no existe tal \\(p\\), es decir, \\(\gcd(x,y,z)=1\\).

*Demostración (clasificación, esbozo).* Por el Lema 1.36, supongamos \\(y\\) par, \\(x,z\\) impares. Entonces \\(y^2=z^2-x^2=(z-x)(z+x)\\), con \\(z-x\\) y \\(z+x\\) ambos pares (suma/resta de impares); escribamos \\(z-x=2u\\), \\(z+x=2v\\), de donde \\((y/2)^2=uv\\). Se verifica que \\(\gcd(u,v)=1\\): en efecto, \\(\gcd(z-x,z+x) \mid \gcd(2z,2x)=2\gcd(z,x)=2\\) (pues \\(\gcd(x,z)=1\\) por primitividad y el Lema 1.36), y como ambos son pares, \\(\gcd(u,v)=\gcd\!\left(\tfrac{z-x}2,\tfrac{z+x}2\right)=1\\). Como \\(uv=(y/2)^2\\) es un cuadrado y \\(\gcd(u,v)=1\\), un resultado estándar de factorización única (que se demuestra en la Unidad 2, Corolario 2.16: si un producto de coprimos es una potencia \\(k\\)-ésima perfecta, cada factor lo es —aquí con \\(k=2\\)) da que \\(u=n^2\\), \\(v=m^2\\) para ciertos enteros \\(m>n>0\\). Entonces \\(z=v+u=m^2+n^2\\), \\(x=v-u=m^2-n^2\\), \\(y=2\sqrt{uv}=2mn\\), y se comprueba que \\(\gcd(m,n)=1\\) y que \\(m,n\\) tienen distinta paridad (pues \\(x=m^2-n^2\\) es impar). \\(\blacksquare\\)

**Ejemplo 1.38.** Con \\((m,n)=(2,1)\\): \\((x,y,z)=(3,4,5)\\). Con \\((m,n)=(3,2)\\): \\((5,12,13)\\). Con \\((m,n)=(4,1)\\): \\((15,8,17)\\). Con \\((m,n)=(4,3)\\): \\((7,24,25)\\). Toda terna pitagórica (no necesariamente primitiva) se obtiene multiplicando una terna primitiva por un entero positivo \\(k\\): \\((kx,ky,kz)\\); por ejemplo, \\((6,8,10)=2\cdot(3,4,5)\\).

**Corolario 1.39 (caso particular del Último Teorema de Fermat).** *No existen enteros positivos \\(x,y,z\\) tales que \\(x^4+y^4=z^4\\).*

La demostración, debida esencialmente al propio Fermat mediante su método de "descenso infinito" (una aplicación refinada del Principio del Buen Orden discutido en la Sección 1.1), se propone como problema guiado en los ejercicios de esta unidad. El caso general del Último Teorema de Fermat —que \\(x^n+y^n=z^n\\) no tiene soluciones positivas para ningún \\(n\ge3\\)— permaneció como uno de los problemas abiertos más célebres de las matemáticas durante más de 350 años, hasta su demostración por Andrew Wiles en 1994; en la Unidad 6 se ofrece una breve panorámica de las ideas (curvas elípticas y formas modulares) detrás de esta demostración.
