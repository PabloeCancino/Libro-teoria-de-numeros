# 5.2 Sistemas reducidos de residuos y la función de Euler

## Sistemas reducidos de residuos

De los \\(n\\) elementos de un sistema completo de residuos módulo \\(n\\), solo algunos son relevantes cuando lo que interesa es la estructura **multiplicativa** de \\(\mathbb{Z}_n\\): concretamente, aquellos que son coprimos con \\(n\\), pues por la Proposición 5.1(vi), solo estos se pueden "cancelar" libremente en una congruencia.

**Definición.** Un **sistema reducido de residuos módulo \\(n\\)** es un conjunto \\(R\\) de enteros tal que:

1. \\(\gcd(r,n)=1\\) para todo \\(r\in R\\);
2. todo entero \\(a\\) con \\(\gcd(a,n)=1\\) es congruente módulo \\(n\\) con uno y solo uno de los elementos de \\(R\\).

Equivalentemente (comparando con la Proposición 5.3 y recordando la definición de la función φ de Euler, Sección 4.2), el conjunto
\\[ \{a\in\{1,\dots,n\} : \gcd(a,n)=1\} \\]
es, por construcción, un sistema reducido de residuos módulo \\(n\\), y tiene exactamente \\(\varphi(n)\\) elementos. El siguiente resultado muestra que esto no es casualidad: **todo** sistema reducido de residuos módulo \\(n\\) tiene exactamente \\(\varphi(n)\\) elementos.

**Proposición 5.9.** *Todo sistema reducido de residuos módulo \\(n\\) tiene exactamente \\(\varphi(n)\\) elementos. Además, si \\(R=\{r_1,\dots,r_{\varphi(n)}\}\\) es un sistema reducido de residuos módulo \\(n\\) y \\(\gcd(a,n)=1\\), entonces \\(aR=\{ar_1,\dots,ar_{\varphi(n)}\}\\) también es un sistema reducido de residuos módulo \\(n\\).*

*Demostración.* La primera afirmación se sigue de que \\(R\\) está, por definición, en correspondencia biunívoca (vía congruencia módulo \\(n\\)) con el conjunto \\(\{a\in\{1,\dots,n\}:\gcd(a,n)=1\}\\), que tiene \\(\varphi(n)\\) elementos.

Para la segunda afirmación: como \\(\gcd(a,n)=1\\) y \\(\gcd(r_i,n)=1\\) para cada \\(i\\), la Proposición 1.19(vii)-tipo argumento (o directamente, ningún primo que divida a \\(n\\) puede dividir a \\(a\\) ni a \\(r_i\\), luego tampoco a \\(ar_i\\)) da \\(\gcd(ar_i,n)=1\\) para cada \\(i\\). Además, si \\(i\ne j\\), entonces \\(r_i\not\equiv r_j\pmod n\\) (por ser \\(R\\) un sistema reducido, en particular un subconjunto "sin repeticiones módulo \\(n\\)" de un sistema completo); como \\(\gcd(a,n)=1\\), la Proposición 5.1(vi) da \\(ar_i\not\equiv ar_j\pmod n\\). Así, \\(aR\\) consta de \\(\varphi(n)\\) elementos, todos coprimos con \\(n\\) y dos a dos incongruentes módulo \\(n\\); como hay exactamente \\(\varphi(n)\\) clases de congruencia coprimas con \\(n\\), \\(aR\\) debe representarlas todas, es decir, \\(aR\\) es también un sistema reducido de residuos módulo \\(n\\). \\(\blacksquare\\)

## El Teorema de Euler

**Teorema 5.10 (Euler).** *Si \\(\gcd(a,n)=1\\), entonces*
\\[ a^{\varphi(n)} \equiv 1 \pmod n. \\]

*Demostración.* Sea \\(R=\{r_1,r_2,\dots,r_{\varphi(n)}\}=\{a\in\{1,\dots,n\}:\gcd(a,n)=1\}\\), el sistema reducido de residuos "canónico". Por la Proposición 5.9, como \\(\gcd(a,n)=1\\), el conjunto \\(aR=\{ar_1,\dots,ar_{\varphi(n)}\}\\) es también un sistema reducido de residuos módulo \\(n\\). Esto significa que, en algún orden, cada \\(ar_i\\) es congruente módulo \\(n\\) con exactamente uno de los \\(r_j\\), y viceversa; es decir, existe una permutación \\(\pi\\) de \\(\{1,\dots,\varphi(n)\}\\) tal que
\\[ ar_i \equiv r_{\pi(i)} \pmod n, \qquad i=1,\dots,\varphi(n). \\]
Multiplicando estas \\(\varphi(n)\\) congruencias entre sí (Proposición 5.1(v), aplicada repetidamente):
\\[ a^{\varphi(n)}\,r_1r_2\cdots r_{\varphi(n)} \equiv r_{\pi(1)}r_{\pi(2)}\cdots r_{\pi(\varphi(n))} = r_1r_2\cdots r_{\varphi(n)} \pmod n, \\]
donde la última igualdad se debe a que \\(\pi\\) es una permutación, así que el producto de la derecha es el mismo que el de la izquierda, solo reordenado.

Sea \\(P=r_1r_2\cdots r_{\varphi(n)}\\). Como cada \\(r_i\\) es coprimo con \\(n\\), también lo es su producto \\(P\\) (aplicando repetidamente el hecho de que un primo que divida a \\(n\\) no puede dividir a ningún \\(r_i\\), luego tampoco al producto). Por tanto, de \\(a^{\varphi(n)}P \equiv P \pmod n\\) y \\(\gcd(P,n)=1\\), la Proposición 5.1(vi) permite cancelar \\(P\\), obteniendo
\\[ a^{\varphi(n)} \equiv 1 \pmod n. \qquad\blacksquare \\]

**Ejemplo 5.11.** Calculemos el residuo de \\(7^{100}\\) al dividirse entre \\(12\\). Como \\(\gcd(7,12)=1\\) y \\(\varphi(12)=4\\) (Ejemplo 4.18), el Teorema de Euler da \\(7^4\equiv1\pmod{12}\\). Escribiendo \\(100=4\cdot25\\), obtenemos \\(7^{100}=(7^4)^{25}\equiv1^{25}=1\pmod{12}\\).

**Ejemplo 5.12.** Calculemos los dos últimos dígitos de \\(3^{1000}\\), es decir, \\(3^{1000}\bmod100\\). Como \\(\gcd(3,100)=1\\) y \\(\varphi(100)=\varphi(2^2\cdot5^2)=100\cdot\frac12\cdot\frac45=40\\), el Teorema de Euler da \\(3^{40}\equiv1\pmod{100}\\). Como \\(1000=40\cdot25\\), se sigue \\(3^{1000}=(3^{40})^{25}\equiv1\pmod{100}\\): los dos últimos dígitos de \\(3^{1000}\\) son \\(01\\).

El Teorema de Euler es, como veremos en la siguiente sección, una generalización estricta del Pequeño Teorema de Fermat (que corresponde al caso \\(n=p\\) primo, donde \\(\varphi(p)=p-1\\)), y es la base teórica del criptosistema RSA, que se presenta en la Unidad 6.
