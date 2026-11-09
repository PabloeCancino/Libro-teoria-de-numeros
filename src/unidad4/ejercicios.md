# Ejercicios de la Unidad 4

## Sección 4.1 — σ(n), d(n), perfectos y Mersenne

1. Calcule \\(d(n)\\) y \\(\sigma(n)\\) para \\(n=1000\\), \\(n=2^6\cdot3^4\cdot5^2\\) y \\(n=1001\\).
2. Demuestre que \\(n\\) es primo si y solo si \\(\sigma(n)=n+1\\).
3. Demuestre que si \\(f\\) y \\(g\\) son ambas multiplicativas, entonces su producto \\(h(n)=f(n)g(n)\\) también es multiplicativo. Use esto para dar una demostración alternativa de que \\(n\mapsto n\cdot d(n)\\) es multiplicativa.
4. Demuestre que \\(\displaystyle\sum_{d\mid n} d(d) \\) no es, en general, igual a \\(d(n)^2\\) (dé un contraejemplo con \\(n=4\\)), pero investigue si existe alguna fórmula cerrada para \\(\sum_{d\mid n}d(d)\\).
5. Verifique que \\(M_{13}=2^{13}-1=8191\\) es primo (por ensayo de divisiones, usando el Corolario 2.8 de la Unidad 2) y calcule el número perfecto asociado mediante el Teorema 4.8.
6. Demuestre que todo número perfecto par mayor que 6 es de la forma \\(9k+1\\) para algún entero \\(k\ge1\\) (con la posible excepción de \\(n=6\\); verifique este caso aparte). (Sugerencia: analice \\(2^{k-1}(2^k-1) \bmod 9\\) según el residuo de \\(k\\) módulo 6, o busque un argumento más directo.)
7. Demuestre que ningún número perfecto puede ser un cuadrado perfecto.
8. Investigue (o demuestre, si se siente cómodo) por qué todo número perfecto impar, de existir, debe ser mayor que \\(10^{300}\\) es una afirmación fuera del alcance elemental; en su lugar, demuestre la afirmación más modesta de que ningún número perfecto impar puede ser divisible por 105 sin verificar antes ciertas condiciones (explore qué se puede decir usando solamente la multiplicatividad de σ).

## Sección 4.2 — La función φ de Euler

9. Calcule \\(\varphi(n)\\) para \\(n=100,\ 2\\,001,\ 5!\\), usando la fórmula del Teorema 4.14.
10. Demuestre que \\(\varphi(n)=n/2\\) si y solo si \\(n=2^k\\) para algún \\(k\ge1\\).
11. Encuentre todos los \\(n\\) tales que \\(\varphi(n)=12\\).
12. Demuestre que si \\(m\mid n\\), entonces \\(\varphi(m)\mid\varphi(n)\\).
13. Demuestre que \\(\varphi(n^2)=n\cdot\varphi(n)\\) para todo \\(n\ge1\\).
14. Dé una demostración directa (sin usar el Teorema Chino del Resto de la Unidad 5) de que la función \\(f(k)=(k\bmod m,\\,k\bmod n)\\) del Teorema 4.13 es inyectiva cuando \\(\gcd(m,n)=1\\) y \\(0\le k<mn\\), y concluya que es biyectiva por un argumento de conteo (principio del palomar).
15. Verifique la identidad de Gauss (Teorema 4.17) para \\(n=30\\), listando explícitamente todos los divisores y sus valores de φ.

## Sección 4.3 — La función de Möbius

16. Calcule \\(\mu(n)\\) para \\(n=1\\) a \\(n=20\\), y tabule los resultados.
17. Demuestre que \\(\mu(n)\mu(n+1)\mu(n+2)\mu(n+3)=0\\) para todo \\(n\ge1\\). (Sugerencia: entre cuatro enteros consecutivos, alguno es divisible por 4.)
18. Use la fórmula de inversión de Möbius para expresar \\(d(n)\\) en términos de una suma que involucre a \\(\mu\\), sabiendo que la función constante \\(\mathbf{1}(n)=1\\) satisface \\(d(n)=\sum_{d\mid n}\mathbf1(d)\\).
19. Demuestre directamente (expandiendo el producto) que \\(n\prod_{p\mid n}(1-1/p) = \sum_{d\mid n}\mu(d)\\,(n/d)\\), verificando así la afirmación hecha al final del Ejemplo 4.26.
20. (Proyecto.) Investigue la función de Liouville \\(\lambda(n)=(-1)^{\Omega(n)}\\), donde \\(\Omega(n)\\) es el número total de factores primos de \\(n\\) contados con multiplicidad, demuestre que es completamente multiplicativa, y compare su comportamiento con el de \\(\mu(n)\\).
