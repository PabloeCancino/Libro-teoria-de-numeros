# Ejercicios de la Unidad 1

## Sección 1.1 — Axiomas de Peano, inducción y buen orden

1. Demuestre por inducción que para todo \\(n\ge1\\): \\(1^2+2^2+\dots+n^2 = \dfrac{n(n+1)(2n+1)}{6}\\).
2. Demuestre por inducción que para todo \\(n\ge1\\): \\(1^3+2^3+\dots+n^3 = (1+2+\dots+n)^2\\).
3. Demuestre que \\(2^n > n^2\\) para todo entero \\(n \ge 5\\). (Sugerencia: la base no es \\(n=1\\).)
4. Demuestre que \\(n! > 2^n\\) para todo entero \\(n \ge 4\\).
5. Demuestre, usando inducción fuerte, que todo entero \\(n\ge2\\) puede escribirse como producto de números primos (sin usar aún el Teorema Fundamental de la Aritmética de la Unidad 2; solo la *existencia* de tal descomposición, no la unicidad).
6. Sea \\(F_n\\) la sucesión de Fibonacci (\\(F_1=F_2=1\\), \\(F_{n+2}=F_{n+1}+F_n\\)). Demuestre que \\(F_1+F_2+\dots+F_n=F_{n+2}-1\\) para todo \\(n\ge1\\).
7. Demuestre, usando el principio del buen orden (sin usar inducción directamente), que todo subconjunto no vacío de \\(\mathbb{Z}\\) acotado superiormente tiene un elemento máximo.
8. Encuentre el error en el siguiente "teorema" y explique por qué la demostración es inválida: *"Todos los caballos son del mismo color."* Demostración por inducción sobre el número \\(n\\) de caballos en un conjunto: para \\(n=1\\) es trivial. Supóngase cierto para conjuntos de \\(k\\) caballos; dado un conjunto de \\(k+1\\) caballos, quitando el último se tienen \\(k\\) caballos del mismo color por hipótesis de inducción; quitando el primero, se tienen otros \\(k\\) caballos del mismo color; como ambos subconjuntos se traslapan, todos son del mismo color.

## Sección 1.2 — Divisibilidad y algoritmo de la división

9. Demuestre que si \\(a\mid b\\) y \\(a \mid (b+c)\\), entonces \\(a \mid c\\).
10. Demuestre que el producto de tres enteros consecutivos siempre es divisible por 6.
11. Demuestre que \\(n^3-n\\) es divisible por 6 para todo entero \\(n\\).
12. Encuentre el cociente y el residuo de dividir \\(a\\) entre \\(b\\) en los casos: (a) \\(a=-58,\ b=7\\); (b) \\(a=100,\ b=-11\\); (c) \\(a=-13,\ b=-4\\).
13. Demuestre, usando el algoritmo de la división con \\(b=3\\), que el cubo de todo entero es de la forma \\(9k\\), \\(9k+1\\) o \\(9k+8\\).
14. Demuestre el criterio de divisibilidad por 4: \\(n\\) es divisible por \\(4\\) si y solo si el número formado por sus dos últimas cifras lo es. (Sugerencia: \\(100=4\cdot25\\).)
15. ¿Es cierto que si \\(a \mid (b^2)\\) entonces \\(a \mid b\\)? Justifique con una demostración o un contraejemplo.

## Sección 1.3 — Máximo común divisor y mínimo común múltiplo

16. Calcule \\(\gcd(1071,462)\\) y exprese el resultado como combinación lineal entera de \\(1071\\) y \\(462\\).
17. Demuestre que si \\(\gcd(a,b)=1\\) y \\(\gcd(a,c)=1\\), entonces \\(\gcd(a,bc)=1\\).
18. Demuestre que \\(\gcd(a,a+2)\\) es \\(1\\) si \\(a\\) es impar, y \\(2\\) si \\(a\\) es par.
19. Demuestre que \\(\gcd(2a+1,\\,9a+4)=1\\) para todo entero \\(a\\).
20. Sean \\(a,b\\) enteros positivos con \\(\gcd(a,b)=d\\). Demuestre que \\(\gcd(a/d,b/d)=1\\) sin usar la identidad de Bézout (es decir, directamente de la definición de mcd).
21. Calcule \\(\mathrm{mcm}(24,36)\\) y \\(\mathrm{mcm}(17,25)\\).
22. Demuestre que para tres enteros positivos \\(a,b,c\\), en general **no** se cumple que \\(\gcd(a,b,c)\cdot\mathrm{mcm}(a,b,c)=abc\\). Encuentre un contraejemplo explícito.
23. Demuestre que si \\(a\mid c\\), \\(b \mid c\\), entonces \\(\mathrm{mcm}(a,b) \mid c\\) (esto generaliza la Proposición 1.24(iv), que ya lo prueba; dé aquí una demostración alternativa usando el Teorema 1.21).

## Sección 1.4 — Algoritmo de Euclides y teorema de Bézout

24. Aplique el algoritmo de Euclides para calcular \\(\gcd(841,160)\\), mostrando todos los pasos.
25. Use el algoritmo de Euclides extendido (tabla de la Observación 1.29) para encontrar \\(x,y\\) enteros tales que \\(841x+160y=\gcd(841,160)\\).
26. Demuestre que si \\(a=bq+r\\), los coeficientes de Bézout de \\((a,b)\\) pueden obtenerse a partir de los de \\((b,r)\\): si \\(\gcd(b,r)=bx'+ry'\\), entonces \\(\gcd(a,b)=bx'+ (a-bq)y' = ay'+b(x'-qy')\\).
27. Demuestre que el número de pasos del algoritmo de Euclides aplicado a dos números de Fibonacci consecutivos \\(F_{n+1}>F_n\\) es exactamente \\(n-1\\).
28. Sea \\(d=\gcd(a,b)\\). Demuestre que el conjunto de **todos** los pares \\((x,y)\\) que satisfacen \\(ax+by=d\\) es \\(\\{(x_0+\tfrac{b}{d}t,\ y_0-\tfrac{a}{d}t) : t\in\mathbb{Z}\\}\\), donde \\((x_0,y_0)\\) es una solución particular (esto es un caso particular del Teorema 1.33 con \\(c=d\\); redemuéstrelo directamente).

## Sección 1.5 — Ecuaciones diofánticas

29. Resuelva completamente, cuando tengan solución, las ecuaciones diofánticas: (a) \\(15x+21y=6\\); (b) \\(15x+21y=7\\); (c) \\(56x-72y=40\\).
30. Un comerciante compra plumas a \\(\$12\\) y lápices a \\(\$5\\), gastando exactamente \\(\$183\\). ¿De cuántas maneras pudo hacerlo, si compró al menos una pluma y al menos un lápiz?
31. Encuentre todas las ternas pitagóricas primitivas con \\(z \le 30\\).
32. Demuestre que en toda terna pitagórica \\((x,y,z)\\) (no necesariamente primitiva), el producto \\(xy\\) es siempre divisible por 12, y que \\(xyz\\) es divisible por 60.
33. (Descenso infinito de Fermat, guiado.) Demuestre el Corolario 1.39 (\\(x^4+y^4=z^4\\) no tiene soluciones positivas) siguiendo estos pasos: (a) basta demostrar que \\(x^4+y^4=z^2\\) no tiene soluciones positivas; (b) suponga que sí las tiene, y tome una solución \\((x,y,z)\\) con \\(z\\) **mínimo** (use el PBO); (c) muestre que \\((x^2,y^2,z)\\) es (esencialmente) una terna pitagórica primitiva y aplique el Teorema 1.37 para obtener \\(m,n\\); (d) deduzca la existencia de una nueva solución \\((x',y',z')\\) de \\(x^4+y^4=z^2\\) con \\(0<z'<z\\), contradiciendo la minimalidad de \\(z\\).
34. Demuestre que la ecuación \\(x^2+y^2=3z^2\\) no tiene soluciones enteras positivas. (Sugerencia: analice la ecuación módulo 4, anticipando el lenguaje de congruencias de la Unidad 5; alternativamente, use un argumento de descenso infinito.)
