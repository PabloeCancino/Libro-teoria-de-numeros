# Ejercicios de la Unidad 5

## Sección 5.1 — Congruencias

1. Demuestre que si \\(a\equiv b\pmod n\\), entonces \\(\gcd(a,n)=\gcd(b,n)\\).
2. Encuentre el residuo de \\(2^{50}\\) al dividirse entre \\(7\\), trabajando directamente con congruencias (sin usar todavía el Teorema de Euler o Fermat).
3. Demuestre el criterio de divisibilidad por 7 basado en congruencias: describa y justifique un método práctico (puede no ser tan simple como los de 3, 9 u 11).
4. Verifique, usando la prueba del nueve y del once simultáneamente (Ejemplo 5.6), si el producto \\(4127\times2856=11\\,786\\,712\\) puede ser correcto.
5. Determine todos los sistemas completos de residuos módulo 5 de la forma \\(\\{0,\pm a,\pm b\\}\\) con \\(0<a<b<5\\).
6. Demuestre la Proposición 5.7 sin usar la Proposición 1.19(vii), sino directamente a partir de la definición y del Teorema Fundamental de la Aritmética (comparando exponentes de primos).

## Sección 5.2 — Sistemas reducidos y Teorema de Euler

7. Encuentre un sistema reducido de residuos módulo 18 distinto del conjunto canónico \\(\\{a\in\\{1,\dots,18\\}:\gcd(a,18)=1\\}\\).
8. Calcule el residuo de \\(7^{222}\\) al dividirse entre \\(15\\), usando el Teorema de Euler.
9. Encuentre los dos últimos dígitos de \\(7^{300}\\).
10. Demuestre que si \\(\gcd(a,n)=1\\), el **orden** de \\(a\\) módulo \\(n\\) (el menor entero positivo \\(k\\) tal que \\(a^k\equiv1\pmod n\\)) siempre divide a \\(\varphi(n)\\). (Sugerencia: use el algoritmo de la división para escribir \\(\varphi(n)=qk+r\\) y analice \\(a^r\\).)
11. Use el resultado del ejercicio anterior para verificar, sin calcular \\(3^{16}\\) directamente, que el orden de \\(3\\) módulo \\(17\\) debe ser un divisor de \\(16\\), y determínelo por ensayo.

## Sección 5.3 — Fermat, Wilson y pseudoprimos

12. Demuestre que \\(1105=5\times13\times17\\) es un número de Carmichael, verificando la condición de la Proposición 5.14.
13. Demuestre que \\(341=11\times31\\) es un pseudoprimo en base 2 (es decir, \\(2^{341}\equiv2\pmod{341}\\)) pero no es un número de Carmichael, exhibiendo una base \\(a\\) para la cual falla \\(a^{341}\equiv a\pmod{341}\\).
14. Use el Teorema de Wilson para determinar si \\(571\\) es primo (sin factorizarlo directamente, razone sobre la congruencia, aunque el cálculo de \\(570!\bmod571\\) a mano es en la práctica poco viable; discuta por qué el Teorema de Wilson, pese a caracterizar la primalidad, no es un test de primalidad práctico).
15. Determine, usando el Teorema 5.19, cuáles de los primos \\(13,17,19,23\\) admiten solución a \\(x^2\equiv-1\\) en su módulo respectivo, y encuentre una solución explícita en los casos afirmativos usando la fórmula \\(x=\left(\frac{p-1}2\right)!\\).
16. Complete los detalles de la demostración del Corolario 5.21 explicando por qué "el producto de números \\(\equiv1\pmod8\\) es \\(\equiv1\pmod8\\)" (es decir, demuestre esta afirmación auxiliar).

## Sección 5.4 — Unidades y congruencias lineales

17. Encuentre el inverso de \\(17\\) módulo \\(101\\).
18. Resuelva la congruencia \\(15x\equiv9\pmod{21}\\) (encuentre todas las soluciones incongruentes módulo 21).
19. Resuelva \\(20x\equiv15\pmod{35}\\), o explique por qué no tiene solución.
20. Demuestre que si \\(p\\) es primo y \\(1\le a\le p-1\\), el inverso de \\(a\\) módulo \\(p\\) puede calcularse como \\(a^{p-2}\bmod p\\) (relacione esto con el Teorema de Euler/Fermat).

## Sección 5.5 — Teorema Chino del Resto

21. Resuelva el sistema \\(x\equiv2\pmod5,\ x\equiv3\pmod7,\ x\equiv4\pmod9\\).
22. Resuelva el sistema \\(x\equiv7\pmod{15},\ x\equiv4\pmod{21}\\) (los módulos **no** son coprimos; reduzca primero a módulos potencia de primo, como en el Ejemplo 5.28).
23. Un número al dividirse entre 6 deja residuo 5, al dividirse entre 11 deja residuo 7, y al dividirse entre 13 deja residuo 3. Encuentre el menor entero positivo con estas propiedades.
24. Demuestre, usando el Teorema Chino del Resto, que si \\(\gcd(m,n)=1\\), la función \\(\mathbb{Z}_{mn}^\ast \to \mathbb{Z}_m^\ast\times\mathbb{Z}_n^\ast\\) dada por \\(a\mapsto(a\bmod m,\ a\bmod n)\\) es una biyección, dando así una tercera demostración (además de las dadas en el Teorema 4.13) de la multiplicatividad de φ.
25. (Proyecto.) Investigue cómo el Teorema Chino del Resto se usa para acelerar el descifrado en el criptosistema RSA (mencionado brevemente en la Unidad 6), calculando las operaciones módulo \\(p\\) y módulo \\(q\\) por separado en vez de módulo \\(n=pq\\).
