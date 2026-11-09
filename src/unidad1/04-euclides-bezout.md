# 1.4 El algoritmo de Euclides y el teorema de Bézout

El Teorema 1.16 garantiza que \\(\gcd(a,b)\\) existe y es una combinación lineal entera de \\(a\\) y \\(b\\), pero su demostración —vía el buen orden— no es constructiva: no indica cómo *calcular* \\(\gcd(a,b)\\) ni los coeficientes de Bézout. El **algoritmo de Euclides**, que se remonta a los *Elementos* (c. 300 a.C.), resuelve ambos problemas de manera efectiva y eficiente.

## El algoritmo de Euclides

La idea es la Proposición 1.19(iii): \\(\gcd(a,b) = \gcd(b,r)\\) si \\(a=bq+r\\). Iterando esta reducción, los números van disminuyendo hasta llegar a un residuo cero.

**Teorema 1.25 (Algoritmo de Euclides).** *Sean \\(a,b \in \mathbb{Z}^+\\), \\(a \geq b\\). Defínase la sucesión de divisiones sucesivas:*
\\[
\begin{aligned}
a &= bq_1 + r_1, & 0 &\le r_1 < b,\\\\
b &= r_1q_2 + r_2, & 0 &\le r_2 < r_1,\\\\
r_1 &= r_2q_3+r_3, & 0&\le r_3<r_2,\\\\
&\ \ \vdots & &\\\\
r_{n-2} &= r_{n-1}q_n + r_n, & 0&\le r_n < r_{n-1},\\\\
r_{n-1} &= r_n q_{n+1} + 0. & &
\end{aligned}
\\]
*(El proceso termina en un número finito de pasos porque \\(b>r_1>r_2>\cdots\ge 0\\) es una sucesión estrictamente decreciente de enteros no negativos.) Entonces el último residuo no nulo, \\(r_n\\), es igual a \\(\gcd(a,b)\\).*

*Demostración.* La sucesión \\(b>r_1>r_2>\cdots\\) de enteros no negativos no puede decrecer indefinidamente (por el PBO, o simplemente porque hay a lo más \\(b+1\\) enteros en \\([0,b]\\)), así que en algún paso se obtiene residuo \\(0\\); esto justifica que el algoritmo termina.

Aplicando repetidamente la Proposición 1.19(iii) (\\(\gcd(x,y)=\gcd(y,r)\\) si \\(x=yq+r\\)):
\\[ \gcd(a,b)=\gcd(b,r_1)=\gcd(r_1,r_2)=\cdots=\gcd(r_{n-1},r_n)=\gcd(r_n,0)=r_n, \\]
donde la última igualdad usa la Proposición 1.19(ii). \\(\blacksquare\\)

**Ejemplo 1.26.** Calculemos \\(\gcd(252,105)\\):
\\[
\begin{aligned}
252 &= 105\cdot 2 + 42\\\\
105 &= 42\cdot 2 + 21\\\\
42 &= 21 \cdot 2 + 0
\end{aligned}
\\]
El último residuo no nulo es \\(21\\), luego \\(\gcd(252,105)=21\\).

## El algoritmo de Euclides extendido

Recorriendo las igualdades del algoritmo de Euclides **hacia atrás**, podemos expresar \\(r_n = \gcd(a,b)\\) explícitamente como combinación lineal entera de \\(a\\) y \\(b\\), obteniendo así una demostración *constructiva* de la identidad de Bézout (Corolario 1.17) y un método efectivo para calcular sus coeficientes.

**Teorema 1.27 (Teorema de Bézout).** *Para cualesquiera \\(a,b \in \mathbb{Z}\\), no ambos cero, existen \\(x,y \in \mathbb{Z}\\), calculables explícitamente mediante el algoritmo de Euclides extendido, tales que*
\\[ \gcd(a,b) = ax+by. \\]

*Demostración (método constructivo).* Con la notación del Teorema 1.25, de la penúltima igualdad se despeja
\\[ r_n = r_{n-2} - r_{n-1}q_n. \\]
Sustituyendo sucesivamente \\(r_{n-1} = r_{n-3}-r_{n-2}q_{n-1}\\), luego \\(r_{n-2}=r_{n-4}-r_{n-3}q_{n-2}\\), etc., y subiendo hasta la primera igualdad \\(r_1 = a - bq_1\\), se expresa \\(r_n\\) como combinación entera de \\(a\\) y \\(b\\). Como \\(r_n=\gcd(a,b)\\) por el Teorema 1.25, esto da la identidad buscada. \\(\blacksquare\\)

**Ejemplo 1.28.** Retomando el Ejemplo 1.26 (\\(a=252,b=105\\)), despejamos los residuos:
\\[ 42 = 252 - 105\cdot 2, \qquad 21 = 105-42\cdot 2. \\]
Sustituyendo la primera igualdad en la segunda:
\\[ 21 = 105 - (252-105\cdot 2)\cdot 2 = 105 - 252\cdot 2 + 105\cdot 4 = 105\cdot 5 - 252 \cdot 2. \\]
Por tanto \\(\gcd(252,105)=21 = 252\cdot(-2) + 105\cdot 5\\), es decir, \\(x=-2\\), \\(y=5\\) son coeficientes de Bézout. (Verificación: \\(252\cdot(-2)+105\cdot 5 = -504+525=21\\). ✓)

**Observación 1.29 (tabla práctica).** En la práctica es más cómodo organizar el cálculo en una tabla que registre, en cada paso, el residuo junto con su expresión como combinación de \\(a\\) y \\(b\\), sin necesidad de "subir" al final. Si escribimos cada residuo como \\(r_i = a x_i + b y_i\\), con
\\[ x_{-1}=1,\ y_{-1}=0 \quad (\text{para } r_{-1}=a); \qquad x_0=0,\ y_0=1 \quad (\text{para } r_0=b), \\]
entonces la misma recurrencia de la división, \\(r_{i} = r_{i-2} - q_i r_{i-1}\\), se traslada a los coeficientes:
\\[ x_i = x_{i-2}-q_ix_{i-1}, \qquad y_i = y_{i-2}-q_iy_{i-1}. \\]
Este es el llamado **algoritmo de Euclides extendido**, y es el método preferido para el cálculo manual o computacional, pues evita la sustitución hacia atrás.

*Ilustración con el Ejemplo 1.26/1.28* (\\(a=252, b=105\\)):

| \\(i\\) | \\(q_i\\) | \\(r_i\\) | \\(x_i\\) | \\(y_i\\) |
|---|---|---|---|---|
| \\(-1\\) | — | \\(252\\) | \\(1\\) | \\(0\\) |
| \\(0\\) | — | \\(105\\) | \\(0\\) | \\(1\\) |
| \\(1\\) | \\(2\\) | \\(42\\) | \\(1-2\cdot0=1\\) | \\(0-2\cdot1=-2\\) |
| \\(2\\) | \\(2\\) | \\(21\\) | \\(0-2\cdot1=-2\\) | \\(1-2\cdot(-2)=5\\) |
| \\(3\\) | \\(2\\) | \\(0\\) | — | — |

La última fila con residuo no nulo da \\(21 = 252\cdot(-2)+105\cdot 5\\), coincidiendo con el Ejemplo 1.28.

## Consecuencias inmediatas

**Corolario 1.30.** *\\(\gcd(a,b)=1\\) si y solo si el algoritmo de Euclides aplicado a \\(a,b\\) termina con residuo \\(1\\) antes del residuo \\(0\\).*

**Corolario 1.31 (Eficiencia del algoritmo de Euclides).** *El número de pasos del algoritmo de Euclides aplicado a \\(a>b>0\\) es \\(O(\log b)\\).*

*Idea de la demostración.* Se puede probar que \\(r_{i+2} < r_i/2\\) para todo \\(i\\) (si \\(r_{i+1}\le r_i/2\\), esto es inmediato porque \\(r_{i+2}<r_{i+1}\\); si \\(r_{i+1}>r_i/2\\), entonces el cociente \\(q_{i+2}\\) en la división de \\(r_i\\) entre \\(r_{i+1}\\) es \\(1\\), y \\(r_{i+2}=r_i-r_{i+1}<r_i/2\\)). Por tanto, cada dos pasos el residuo al menos se reduce a la mitad, y el número total de pasos es del orden de \\(\log_2 b\\). Este es uno de los primeros algoritmos de la historia con un análisis de complejidad riguroso, atribuido a Gabriel Lamé (1844), quien además mostró que el peor caso (mayor número de pasos para un valor dado de \\(b\\)) se presenta cuando \\(a,b\\) son términos consecutivos de la sucesión de Fibonacci. \\(\blacksquare\\)

El teorema de Bézout tiene además una lectura recíproca útil, que caracteriza completamente qué enteros son combinaciones lineales de \\(a\\) y \\(b\\); la usaremos de inmediato en la siguiente sección para resolver ecuaciones diofánticas lineales.

**Proposición 1.32.** *Sean \\(a,b\in\mathbb{Z}\\), no ambos cero, \\(d=\gcd(a,b)\\). Un entero \\(n\\) se puede escribir como \\(n=ax+by\\) con \\(x,y\in\mathbb{Z}\\) si y solo si \\(d \mid n\\).*

*Demostración.* (\\(\Rightarrow\\)) Como \\(d\mid a\\) y \\(d\mid b\\), por la Proposición 1.9(ii), \\(d \mid (ax+by)=n\\).

(\\(\Leftarrow\\)) Si \\(d \mid n\\), escribimos \\(n=dm\\). Por el Teorema 1.27, existen \\(x_0,y_0\\) con \\(d=ax_0+by_0\\). Multiplicando por \\(m\\): \\(n=dm=a(x_0m)+b(y_0m)\\), así que \\(x=x_0m\\), \\(y=y_0m\\) sirven. \\(\blacksquare\\)
