# Ejercicios de la Unidad 3

## Sección 3.1 — Conjuntos finitos, permutaciones y combinaciones

1. ¿De cuántas maneras se pueden ordenar las letras de la palabra MATEMATICA? (Sugerencia: use permutaciones con repetición, \\(\frac{n!}{n_1!n_2!\cdots}\\), y justifíquela con un argumento de conteo doble similar al del Teorema 3.6.)
2. ¿Cuántos números de 4 dígitos (sin ceros a la izquierda) tienen todos sus dígitos distintos?
3. Un comité de 5 personas debe elegirse de un grupo de 8 hombres y 6 mujeres, con exactamente 2 mujeres. ¿De cuántas maneras puede formarse?
4. Demuestre, usando el principio del palomar, que entre cualesquiera 13 personas, al menos dos cumplen años en el mismo mes.
5. Demuestre que entre cualesquiera \\(n+1\\) enteros elegidos del conjunto \\(\\{1,2,\dots,2n\\}\\), siempre hay dos que son primos relativos. (Sugerencia: agrupe en \\(n\\) parejas de consecutivos \\(\\{2k-1,2k\\}\\).)
6. Demuestre que \\(\binom{2n}{n}\\) es siempre par para \\(n\ge1\\).
7. Use el Corolario 2.16 (o un argumento de exponentes de primos) para dar una demostración *aritmética* (no combinatoria) de que \\(\binom nk\\) es siempre un entero.

## Sección 3.2 — Triángulo de Pascal

8. Calcule las filas \\(n=8\\) y \\(n=9\\) del triángulo de Pascal.
9. Demuestre que \\(\displaystyle\sum_{k=0}^n k\binom nk = n2^{n-1}\\) para \\(n\ge1\\). (Sugerencia: derive la identidad del binomio respecto de \\(x\\), o use un argumento combinatorio de "elegir un comité con un presidente".)
10. Determine para qué primos \\(p\\) se cumple que **todas** las entradas interiores de la fila \\(n=p^2\\) del triángulo de Pascal son divisibles por \\(p\\) (es decir, generalice la Proposición 3.11 a \\(\binom{p^2}{k}\\); investigue el Teorema de Kummer o Lucas si desea una respuesta completa).
11. Demuestre, usando el Corolario 3.13 aplicado dos veces, que \\((x+y)^{p^2}\equiv x^{p^2}+y^{p^2}\pmod p\\) para \\(p\\) primo.
12. Verifique la identidad de Vandermonde (Proposición 3.16) para \\(m=3,n=2,k=3\\), calculando ambos lados directamente.

## Sección 3.3 — Fermat y Wilson por combinatoria

13. Use el Teorema 3.17 (Pequeño Teorema de Fermat, vía collares) para calcular el residuo de \\(2^{101}\\) al dividirse entre \\(101\\).
14. Complete los detalles omitidos en la demostración del Teorema 3.19 (Wilson) para el caso \\(p=5\\): liste explícitamente el conjunto \\(A\\), las parejas de compañeros, y verifique la congruencia final.
15. Use el Teorema de Wilson para determinar si \\(97\\) es primo, calculando \\(96! \bmod 97\\) mediante las propiedades de congruencias (sin calcular \\(96!\\) directamente; puede usar propiedades que se demostrarán formalmente en la Unidad 5, o razonar por contradicción usando la Proposición 3.21).
16. Demuestre la Proposición 3.21 en detalle para el caso \\(n=p^2\\) con \\(p\ge3\\) primo, verificando explícitamente que \\(p\\) y \\(2p\\) son enteros distintos menores que \\(n-1\\).
17. (Desafío.) Adapte la demostración combinatoria del Teorema 3.17 (acción de rotación sobre secuencias) para dar una demostración alternativa, puramente combinatoria, del Corolario 3.18 sin pasar por el Lema de Euclides —es decir, contando directamente cuántas secuencias no constantes hay módulo la acción del grupo generado por \\(a\\) coprimo con \\(p\\).
