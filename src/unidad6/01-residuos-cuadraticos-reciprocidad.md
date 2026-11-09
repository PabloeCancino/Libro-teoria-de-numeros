# 6.1 Residuos cuadráticos y la ley de reciprocidad cuadrática

*Esta unidad es material complementario y no forma parte del temario mínimo del curso CILM318; se incluye como puente hacia cursos posteriores de teoría de números.*

Ya nos hemos encontrado con la pregunta de si \\(x^2\equiv-1\pmod p\\) tiene solución (Teorema 5.19). Esta sección la generaliza: dado un entero \\(a\\) y un primo impar \\(p\\), ¿cuándo tiene solución \\(x^2\equiv a\pmod p\\)?

## El símbolo de Legendre

**Definición.** Sea \\(p\\) un primo impar y \\(a\\) un entero con \\(p\nmid a\\). Decimos que \\(a\\) es un **residuo cuadrático módulo \\(p\\)** si la congruencia \\(x^2\equiv a\pmod p\\) tiene solución, y un **no residuo cuadrático** en caso contrario. El **símbolo de Legendre** se define como
\\[
\left(\frac ap\right) = \begin{cases} 1 & \text{si } a \text{ es residuo cuadrático módulo } p,\\\\ -1 & \text{si } a \text{ es no residuo cuadrático módulo } p,\\\\ 0 & \text{si } p\mid a. \end{cases}
\\]

**Proposición 6.1.** *Entre los residuos \\(1,2,\dots,p-1\\), exactamente \\(\frac{p-1}2\\) son residuos cuadráticos y \\(\frac{p-1}2\\) son no residuos.*

*Demostración.* Los valores \\(1^2,2^2,\dots,(p-1)^2\\) módulo \\(p\\) dan todos los residuos cuadráticos, pero con repetición: \\(k^2\equiv(p-k)^2\pmod p\\), y estos son los únicos pares que coinciden, ya que \\(k^2\equiv j^2\pmod p\\) equivale a \\(p\mid(k-j)(k+j)\\), es decir (Lema de Euclides), \\(k\equiv j\\) o \\(k\equiv-j\pmod p\\). Por tanto, los valores \\(1^2,2^2,\dots,\left(\frac{p-1}2\right)^2\\) son todos distintos módulo \\(p\\) y agotan los residuos cuadráticos, dando exactamente \\(\frac{p-1}2\\) de ellos. \\(\blacksquare\\)

## El criterio de Euler

**Teorema 6.2 (Criterio de Euler).** *Para \\(p\\) primo impar y \\(p\nmid a\\),*
\\[ \left(\frac ap\right) \equiv a^{(p-1)/2} \pmod p. \\]

*Demostración.* Por el Pequeño Teorema de Fermat (Teorema 5.13), \\(a^{p-1}\equiv1\pmod p\\), es decir, \\(p\mid\big(a^{(p-1)/2}-1\big)\big(a^{(p-1)/2}+1\big)\\); por el Lema de Euclides, \\(a^{(p-1)/2}\equiv\pm1\pmod p\\).

Si \\(a\\) es residuo cuadrático, \\(a\equiv b^2\pmod p\\) para algún \\(b\\) con \\(p\nmid b\\), y entonces \\(a^{(p-1)/2}\equiv b^{p-1}\equiv1\pmod p\\) (Fermat de nuevo). Recíprocamente, se puede mostrar (usando la existencia de una **raíz primitiva** módulo \\(p\\) —un generador del grupo cíclico \\(\mathbb{Z}_p^\ast\\), tema que excede el alcance elemental de esta sección pero es estándar en cursos de álgebra— que si \\(a^{(p-1)/2}\equiv1\pmod p\\) entonces \\(a\\) es necesariamente un residuo cuadrático; combinado con la Proposición 6.1 (exactamente \\(\frac{p-1}2\\) residuos y \\(\frac{p-1}2\\) no residuos, y el polinomio \\(x^{(p-1)/2}-1\\) tiene a lo más \\(\frac{p-1}2\\) raíces módulo el primo \\(p\\)), esto establece la equivalencia completa. \\(\blacksquare\\)

**Corolario 6.3.** *El símbolo de Legendre es completamente multiplicativo en el numerador: \\(\left(\frac{ab}p\right)=\left(\frac ap\right)\left(\frac bp\right)\\).*

*Demostración.* Inmediato del Teorema 6.2: \\((ab)^{(p-1)/2}=a^{(p-1)/2}b^{(p-1)/2}\\), y ambos lados de \\(\left(\frac{ab}p\right)\equiv\left(\frac ap\right)\left(\frac bp\right)\pmod p\\) están en \\(\\{-1,0,1\\}\\) con \\(p\ge3\\), así que la congruencia implica igualdad. \\(\blacksquare\\)

**Corolario 6.4 (primera ley complementaria).** *\\(\left(\dfrac{-1}p\right)=1\\) si \\(p\equiv1\pmod4\\), y \\(\left(\dfrac{-1}p\right)=-1\\) si \\(p\equiv3\pmod4\\).*

Esto no es más que una reformulación del Teorema 5.19, ahora demostrada de forma inmediata por el criterio de Euler: \\((-1)^{(p-1)/2}=1\\) si \\(\frac{p-1}2\\) es par (\\(p\equiv1\pmod4\\)) y \\(=-1\\) si es impar (\\(p\equiv3\pmod4\\)).

## El Lema de Gauss y la segunda ley complementaria

**Lema 6.5 (Gauss).** *Sea \\(p\\) primo impar, \\(p\nmid a\\). Considérense los residuos menores en valor absoluto de \\(a,2a,\dots,\frac{p-1}2 a\\) módulo \\(p\\) (es decir, represéntese cada uno en el rango \\(\left(-\frac p2,\frac p2\right)\\)), y sea \\(\nu\\) el número de ellos que resultan negativos. Entonces*
\\[ \left(\frac ap\right) = (-1)^\nu. \\]

*Idea de la demostración.* Se verifica que los valores absolutos de estos residuos son una permutación de \\(1,2,\dots,\frac{p-1}2\\) (un argumento similar al de la Proposición 6.1). Multiplicando las \\(\frac{p-1}2\\) congruencias \\(ka\equiv\pm r_k\pmod p\\) (con signo según el residuo caiga en la mitad positiva o negativa) se obtiene \\(a^{(p-1)/2}\left(\frac{p-1}2\right)!\equiv(-1)^\nu\left(\frac{p-1}2\right)!\pmod p\\), y cancelando el factorial (coprimo con \\(p\\)) y aplicando el criterio de Euler se concluye. \\(\blacksquare\\)

**Corolario 6.6 (segunda ley complementaria).** *\\(\left(\dfrac2p\right)=1\\) si \\(p\equiv\pm1\pmod8\\), y \\(\left(\dfrac2p\right)=-1\\) si \\(p\equiv\pm3\pmod8\\).*

*Idea de la demostración.* Se aplica el Lema de Gauss a \\(a=2\\): se cuenta cuántos de \\(2,4,\dots,p-1\\) exceden \\(p/2\\), y un análisis de casos según \\(p\bmod8\\) determina la paridad de ese conteo. \\(\blacksquare\\)

## La Ley de Reciprocidad Cuadrática

El siguiente es uno de los teoremas más célebres de toda la teoría de números elemental —Gauss, quien lo llamó *theorema aureum* ("teorema dorado"), dio ocho demostraciones distintas (seis publicadas en vida y dos halladas entre sus papeles póstumos).

**Teorema 6.7 (Ley de Reciprocidad Cuadrática, Gauss, 1796).** *Sean \\(p,q\\) primos impares distintos. Entonces*
\\[ \left(\frac pq\right)\left(\frac qp\right) = (-1)^{\frac{p-1}2\cdot\frac{q-1}2}. \\]
*Equivalentemente, \\(\left(\frac pq\right)=\left(\frac qp\right)\\) salvo cuando \\(p\equiv q\equiv3\pmod4\\), en cuyo caso \\(\left(\frac pq\right)=-\left(\frac qp\right)\\).*

*Sobre la demostración.* Presentamos aquí solo el esquema de la demostración de Eisenstein (una de las más elegantes, basada en conteo de puntos reticulares), remitiendo a la bibliografía de la Unidad 6 (Apéndice C) para los detalles completos, pues un desarrollo íntegro requeriría un espacio considerablemente mayor al de esta sección introductoria. La idea central: combinando el Lema de Gauss con un argumento geométrico de conteo de puntos con coordenadas enteras dentro de un rectángulo de lados \\(\frac{p-1}2\\) y \\(\frac{q-1}2\\), dividido por la recta \\(qx=py\\), se muestra que
\\[ \nu_p + \nu_q \equiv \\#\\{(x,y)\in\mathbb{Z}^2 : 1\le x\le \tfrac{p-1}2,\ 1\le y\le\tfrac{q-1}2\\} = \frac{p-1}2\cdot\frac{q-1}2 \pmod 2, \\]
donde \\(\nu_p,\nu_q\\) son los conteos del Lema 6.5 aplicados respectivamente a \\(q\bmod p\\) y a \\(p\bmod q\\); esto da \\(\left(\frac qp\right)\left(\frac pq\right)=(-1)^{\nu_p+\nu_q}=(-1)^{\frac{p-1}2\cdot\frac{q-1}2}\\).

**Ejemplo 6.8.** Calculemos \\(\left(\dfrac{219}{383}\right)\\) (\\(383\\) es primo). Factorizando \\(219=3\times73\\), por el Corolario 6.3:
\\[ \left(\frac{219}{383}\right) = \left(\frac3{383}\right)\left(\frac{73}{383}\right). \\]
Para \\(\left(\frac3{383}\right)\\): como \\(3\equiv3\pmod4\\) y \\(383\equiv3\pmod4\\), la reciprocidad (Teorema 6.7) da \\(\left(\frac3{383}\right)=-\left(\frac{383}3\right)\\); y \\(383=127\cdot3+2\equiv2\pmod3\\), con \\(\left(\frac23\right)=-1\\) (pues \\(2\\) no es residuo cuadrático módulo 3: \\(1^2\equiv1\\)). Así, \\(\left(\frac3{383}\right)=-(-1)=1\\).

Para \\(\left(\frac{73}{383}\right)\\): como \\(73\equiv1\pmod4\\), la reciprocidad da \\(\left(\frac{73}{383}\right)=\left(\frac{383}{73}\right)\\); reduciendo, \\(383=5\cdot73+18\\), así que \\(\left(\frac{383}{73}\right)=\left(\frac{18}{73}\right)=\left(\frac2{73}\right)\left(\frac9{73}\right)\\). Como \\(9=3^2\\) es un cuadrado perfecto, \\(\left(\frac9{73}\right)=1\\); y como \\(73\equiv1\pmod8\\), el Corolario 6.6 da \\(\left(\frac2{73}\right)=1\\). Por tanto \\(\left(\frac{73}{383}\right)=1\\).

Combinando: \\(\left(\dfrac{219}{383}\right)=1\cdot1=1\\), es decir, \\(219\\) es un residuo cuadrático módulo \\(383\\), sin necesidad de exhibir explícitamente una raíz cuadrada. Este ejemplo ilustra la enorme utilidad práctica de la reciprocidad cuadrática: reduce el cálculo del símbolo de Legendre —a priori tan costoso como recorrer todos los residuos— a una recursión del tamaño del algoritmo de Euclides.
