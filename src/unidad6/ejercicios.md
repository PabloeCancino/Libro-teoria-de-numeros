# Ejercicios de la Unidad 6

## Sección 6.1 — Residuos cuadráticos y reciprocidad

1. Determine, usando el criterio de Euler (Teorema 6.2), si \\(7\\) es residuo cuadrático módulo \\(23\\).
2. Calcule \\(\left(\dfrac{5}{11}\right)\\) directamente (listando los residuos cuadráticos módulo 11) y verifique el resultado usando la Ley de Reciprocidad Cuadrática.
3. Use la Ley de Reciprocidad Cuadrática y las leyes complementarias para calcular \\(\left(\dfrac{-3}p\right)\\) en términos de la clase de \\(p\\) módulo \\(12\\) (esta es la clave para caracterizar los primos representables como \\(x^2+3y^2\\)).
4. Calcule \\(\left(\dfrac{105}{439}\right)\\), sabiendo que \\(439\\) es primo (factorice \\(105\\) primero).
5. Demuestre, usando reciprocidad cuadrática, que \\(3\\) es residuo cuadrático módulo \\(p\\) (para \\(p>3\\) primo) si y solo si \\(p\equiv\pm1\pmod{12}\\).

## Sección 6.2 — Fracciones continuas

6. Calcule la fracción continua de \\(\frac{355}{113}\\) usando el algoritmo de Euclides, y compare con la fracción continua de \\(\pi\\) mencionada en el texto.
7. Calcule los primeros cinco convergentes de \\(\sqrt3=[1;\overline{1,2}]\\) y verifique la fórmula del Corolario 6.13 para dos de ellos consecutivos.
8. Encuentre la solución fundamental de la ecuación de Pell \\(x^2-3y^2=1\\) usando los convergentes de \\(\sqrt3\\).
9. Demuestre que la fracción continua de un número racional siempre termina (esto ya se demostró en el Teorema 6.9; dé aquí una segunda justificación explícita usando el Principio del Buen Orden aplicado a la sucesión de denominadores).
10. (Desafío.) Investigue y explique, sin necesariamente dar una demostración completa, por qué el número áureo \\(\varphi=\frac{1+\sqrt5}2=[1;1,1,1,\dots]\\) es, en un sentido preciso, "el número irracional peor aproximable por racionales" (relaciónelo con la sucesión de Fibonacci del Ejercicio 6 de la Unidad 1).

## Sección 6.3 — Curvas elípticas y criptografía

11. Verifique que el punto \\(2P=\left(\frac94,-\frac{21}8\right)\\) calculado en el Ejemplo 6.22 efectivamente satisface la ecuación \\(y^2=x^3-2x\\).
12. En el Ejemplo 6.21 (RSA de juguete), verifique que \\(d=2753\\) es efectivamente el inverso de \\(e=17\\) módulo \\(\varphi(n)=3120\\), sin recalcularlo desde cero (solo compruebe \\(17\cdot2753\bmod3120\\)).
13. Explique, en sus propias palabras y apoyándose en el Teorema Chino del Resto (Sección 5.5), cómo se podría acelerar el paso de descifrado de RSA (calcular \\(c^d\bmod n\\)) trabajando módulo \\(p\\) y módulo \\(q\\) por separado.
14. Investigue qué es la "exponenciación rápida" (elevar al cuadrado y multiplicar) mencionada en el Ejemplo 6.21, y estime cuántas multiplicaciones modulares se necesitan para calcular \\(m^{2753}\bmod n\\) con este método, comparado con la multiplicación repetida ingenua.
15. (Proyecto de investigación.) Escriba un breve ensayo (una o dos páginas) explicando, a su propio nivel de comprensión, la relación esbozada en el texto entre la curva de Frey, la conjetura de Taniyama–Shimura–Weil, y la demostración del Último Teorema de Fermat. No se espera rigor técnico completo, sino una síntesis clara de las ideas y de por qué la estrategia de Wiles fue tan revolucionaria.
