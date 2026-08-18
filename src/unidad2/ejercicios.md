# Ejercicios de la Unidad 2

## Sección 2.1 — Primos, infinitud y la criba

1. Demuestre que si \\(2^n-1\\) es primo, entonces \\(n\\) es primo. (Sugerencia: si \\(n=ab\\) con \\(1<a,b<n\\), factorice \\(2^{ab}-1\\) usando \\(x^a-1=(x-1)(x^{a-1}+\dots+1)\\) con \\(x=2^b\\).) ¿Es cierto el recíproco?
2. Demuestre que si \\(2^n+1\\) es primo (con \\(n\ge1\\)), entonces \\(n\\) es una potencia de \\(2\\).
3. Adapte la demostración de Euclides (Teorema 2.3) para mostrar que existen infinitos primos de la forma \\(4k+3\\). (Sugerencia: considere \\(N=4p_1\cdots p_r-1\\) y analice los residuos módulo 4 de los factores primos de \\(N\\).)
4. Adapte la demostración de Euclides para mostrar que existen infinitos primos de la forma \\(6k+5\\).
5. Use la criba de Eratóstenes para listar todos los primos menores que 100.
6. Demuestre que entre \\(n!+2\\) y \\(n!+n\\) (inclusive) no hay ningún número primo, para \\(n\ge2\\). Concluya que existen "huecos" arbitrariamente grandes entre primos consecutivos.
7. Demuestre que si \\(p\\) y \\(p+2\\) son ambos primos (un "par de primos gemelos") con \\(p>3\\), entonces \\(6 \mid (p+1)\\).
8. Demuestre el recíproco de la Proposición 2.2: si \\(n>1\\) tiene la propiedad de que, para todos los enteros \\(a,b\\), \\(n\mid ab \Rightarrow n\mid a\\) o \\(n\mid b\\), entonces \\(n\\) es primo. (Sugerencia: si \\(n\\) fuera compuesto, \\(n=ab\\) con \\(1<a,b<n\\) daría un contraejemplo directo.)
9. Demuestre que si \\(a\\) y \\(b\\) son primos relativos dos a dos con \\(c\\) (es decir, \\(\gcd(a,c)=\gcd(b,c)=1\\)), entonces \\(\gcd(ab,c)=1\\).

## Sección 2.2 — Teorema Fundamental de la Aritmética

10. Encuentre la factorización en primos de \\(45\,360\\), \\(N=9699690\\) (el primorial de 19) y \\(2^{10}-1\\).
11. Use el Corolario 2.14 para calcular \\(\gcd(2^4\cdot3^3\cdot7,\ 2^2\cdot3^5\cdot5^2)\\) y su mcm.
12. Demuestre que \\(\sqrt[3]{2}\\) es irracional, generalizando el argumento de la Proposición 2.17 a raíces cúbicas (o cite y adapte cuidadosamente el resultado análogo).
13. Demuestre que \\(\log_2 3\\) es irracional.
14. Use el Corolario 2.13 para dar una demostración alternativa de que si \\(a\mid c\\), \\(b\mid c\\) y \\(\gcd(a,b)=1\\), entonces \\(ab\mid c\\) (esto ya se demostró en la Proposición 1.19(vii); dé aquí un argumento vía exponentes de primos).
15. ¿Cuántos divisores positivos tiene \\(N=2^3\cdot3^2\cdot5\cdot7^4\\)? ¿Cuántos de ellos son múltiplos de 10? ¿Cuántos son cuadrados perfectos?
16. Demuestre que un entero \\(n>1\\) es un cuadrado perfecto si y solo si \\(d(n)\\) (Proposición 2.18) es impar.
17. Demuestre, usando el TFA, que si \\(a^n=b^n\\) con \\(a,b\in\mathbb{Z}^+\\) y \\(n\ge1\\), entonces \\(a=b\\).

## Sección 2.3 — Factorización

18. Factorice \\(n=8\,051\\) usando el método de Fermat (Proposición 2.22).
19. Factorice \\(n=1\,000\,003\\) por división por tanteo, aprovechando la Proposición 2.24 para reducir los candidatos.
20. Explique por qué el método de Fermat es ineficiente para factorizar \\(n=2\cdot 9\,973\\) (con \\(9\,973\\) primo), y factorice este número por división por tanteo en su lugar.
21. Demuestre que si \\(n\\) es compuesto y no tiene ningún factor primo menor o igual que \\(\sqrt[3]{n}\\), entonces \\(n\\) es producto de exactamente dos primos (posiblemente iguales).
22. (Proyecto computacional opcional.) Implemente en un lenguaje de su elección la criba de Eratóstenes y el método de factorización de Fermat, y compare experimentalmente sus tiempos de ejecución para factorizar varios números de 6 a 8 dígitos con factores cercanos entre sí, y con factores muy separados.
