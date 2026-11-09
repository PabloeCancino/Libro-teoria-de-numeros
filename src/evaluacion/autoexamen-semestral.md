# Auto-examen Semestral

Este auto-examen es un **simulacro del examen final** de Teoría de Números (CBIMAT-256). Cubre las seis unidades del curso con la misma estructura y el mismo nivel de exigencia de un examen final: reactivos de opción múltiple, problemas de respuesta corta y cálculo, y demostraciones formales.

Su propósito no es asignarte una calificación, sino **mostrarte con precisión qué temas dominas y cuáles debes repasar** antes del examen verdadero. Por eso cada reactivo está vinculado a la sección del libro donde se estudia su contenido.

---

## 📋 Instrucciones de aplicación

1. **Momento recomendado:** resuélvelo entre dos y tres semanas antes del examen final. Así tendrás tiempo de repasar los temas débiles y, si lo deseas, de volver a intentar los reactivos que fallaste.
2. **Condiciones de examen real:** reserva **3 horas continuas**, sin apuntes, sin formulario, sin el libro, sin la tabla de primos y sin consultar las soluciones. **No se permite calculadora**: todos los cálculos están pensados para hacerse a mano en poco tiempo, y parte de lo que se evalúa es precisamente que sepas reducir módulo \\(n\\), factorizar y aplicar el algoritmo de Euclides sin ayuda. Escribe tus respuestas en hojas aparte.
3. **Distribución del tiempo sugerida:**

| Parte | Contenido | Reactivos | Puntos | Tiempo sugerido |
| :---: | :--- | :---: | :---: | :---: |
| I | Opción múltiple | 1 a 20 | 20 | 30 min |
| II | Respuesta corta y cálculo | 21 a 28 | 32 | 60 min |
| III | Demostraciones | 29 a 34 | 48 | 90 min |
| | **Total** | **34** | **100** | **3 h** |

4. **Al terminar:** califícate con la clave y las rúbricas del final de esta página. Sé estricto: en un cálculo, un resultado correcto sin planteamiento no recibe el puntaje completo, y en una demostración, una idea correcta mal justificada tampoco. Después llena la **tabla de diagnóstico** para decidir qué repasar.

**Convenciones del libro:** \\(\mathbb{N} = \\{0, 1, 2, \dots\\}\\) incluye al cero; \\(\gcd(a, b)\\) y \\(\mathrm{mcm}(a, b)\\) denotan el máximo común divisor y el mínimo común múltiplo; el residuo de dividir \\(a\\) entre \\(b > 0\\) cumple \\(0 \le r < b\\); \\(d(n)\\) es el número de divisores positivos de \\(n\\), \\(\sigma(n)\\) su suma, \\(\varphi(n)\\) la función de Euler y \\(\mu(n)\\) la función de Möbius; para un primo impar \\(p\\), \\(\left(\frac{a}{p}\right)\\) es el símbolo de Legendre. En las demostraciones puedes citar los resultados del libro por su nombre (Lema de Euclides, Teorema de Bézout, Teorema Fundamental de la Aritmética, Pequeño Teorema de Fermat, Teorema de Wilson, Teorema de Euler, Teorema Chino del Resto, etc.), salvo que el enunciado pida demostrarlos.

---

## 📝 Parte I. Opción múltiple (20 puntos, 1 punto cada reactivo)

Elige **una sola** respuesta en cada reactivo.

### Unidad 1. El anillo de los enteros \\(\mathbb{Z}\\)

**1.** ¿Cuál de los siguientes conjuntos **no** tiene elemento mínimo?

- A) \\(\\{n \in \mathbb{N} : n^2 > 200\\}\\)
- B) \\(\\{2^k - 1000 : k \in \mathbb{N}\\}\\)
- C) \\(\\{7k + 3 : k \in \mathbb{Z}\\}\\)
- D) \\(\\{n \in \mathbb{Z}^+ : 7 \mid n \text{ y } 5 \mid (n + 1)\\}\\)

**2.** Por el algoritmo de la división, el cociente \\(q\\) y el residuo \\(r\\) de dividir \\(a = -83\\) entre \\(b = 9\\) son:

- A) \\(q = -10\\), \\(r = 7\\)
- B) \\(q = -9\\), \\(r = -2\\)
- C) \\(q = -9\\), \\(r = 2\\)
- D) \\(q = -10\\), \\(r = -7\\)

**3.** ¿Cuál de los siguientes enteros **sí** puede escribirse en la forma \\(84x + 120y\\) con \\(x, y \in \mathbb{Z}\\)?

- A) \\(18\\)
- B) \\(30\\)
- C) \\(100\\)
- D) \\(-48\\)

**4.** El par \\((x\_0, y\_0) = (1, 1)\\) es una solución de la ecuación diofántica \\(12x + 18y = 30\\). ¿Cuál expresión describe **todas** sus soluciones enteras?

- A) \\(x = 1 + 18t\\), \\(y = 1 - 12t\\), \\(t \in \mathbb{Z}\\)
- B) \\(x = 1 + 3t\\), \\(y = 1 - 2t\\), \\(t \in \mathbb{Z}\\)
- C) \\(x = 1 + 2t\\), \\(y = 1 - 3t\\), \\(t \in \mathbb{Z}\\)
- D) \\(x = 1 + 3t\\), \\(y = 1 + 2t\\), \\(t \in \mathbb{Z}\\)

### Unidad 2. Primalidad

**5.** ¿Cuántos divisores positivos de \\(720\\) son múltiplos de \\(6\\)?

- A) 30
- B) 16
- C) 14
- D) 12

**6.** Sobre el entero \\(391\\), ¿cuál de las siguientes afirmaciones es **verdadera**?

- A) \\(391\\) es primo, pues no es divisible por ningún primo \\(p \le 13\\).
- B) \\(391 = 13 \cdot 31\\).
- C) \\(391\\) es compuesto y su menor factor primo es \\(23\\).
- D) \\(391\\) es compuesto y su menor factor primo es \\(17\\).

**7.** Sean \\(a = 2^5 \cdot 3 \cdot 7^2\\) y \\(b = 2^2 \cdot 3^4 \cdot 5 \cdot 7\\). Entonces \\(\gcd(a, b)\\) es:

- A) \\(2^2 \cdot 3 \cdot 7\\)
- B) \\(2^5 \cdot 3^4 \cdot 5 \cdot 7^2\\)
- C) \\(2^2 \cdot 3 \cdot 5 \cdot 7\\)
- D) \\(2^3 \cdot 3^3 \cdot 7\\)

### Unidad 3. Elementos de combinatoria

**8.** De un grupo de 9 personas se quiere formar un comité de 4 integrantes y, dentro de él, designar a un presidente. ¿De cuántas maneras puede hacerse?

- A) 126
- B) 3 024
- C) 504
- D) 630

**9.** ¿Cuál de las siguientes afirmaciones es **verdadera**?

- A) \\(8 \mid \binom{8}{2}\\)
- B) \\(9 \mid \binom{9}{3}\\)
- C) \\(10 \mid \binom{10}{5}\\)
- D) \\(11 \mid \binom{11}{4}\\)

**10.** ¿Cuál es el residuo de \\(15!\\) al dividirse entre \\(17\\)?

- A) 1
- B) 16
- C) 0
- D) 15

### Unidad 4. Funciones aritméticas

**11.** ¿Cuánto vale \\(\varphi(1260)\\)?

- A) 96
- B) 288
- C) 336
- D) 576

**12.** ¿Cuál de las siguientes afirmaciones es **verdadera**?

- A) Si \\(p\\) es primo, entonces \\(2^p - 1\\) es primo.
- B) \\(2^{10}(2^{11} - 1)\\) es un número perfecto.
- C) Si \\(2^k - 1\\) es primo, entonces \\(k\\) es primo.
- D) Si \\(n\\) es perfecto, entonces \\(\sigma(n) = n\\).

**13.** Para \\(n = 392\\), los valores de \\(d(n)\\) y \\(\sigma(n)\\) son:

- A) \\(d(392) = 12\\) y \\(\sigma(392) = 855\\).
- B) \\(d(392) = 5\\) y \\(\sigma(392) = 855\\).
- C) \\(d(392) = 12\\) y \\(\sigma(392) = 56\\).
- D) \\(d(392) = 12\\) y \\(\sigma(392) = 784\\).

**14.** ¿Cuál de las siguientes igualdades es **falsa**?

- A) \\(\mu(210) = 1\\)
- B) \\(\mu(98) = 0\\)
- C) \\(\displaystyle\sum\_{d \mid 72} \mu(d) = 0\\)
- D) \\(\mu(1001) = 1\\)

### Unidad 5. El anillo de residuos módulo \\(n\\)

**15.** ¿Cuál es el residuo de \\(3^{100}\\) al dividirse entre \\(7\\)?

- A) 2
- B) 1
- C) 4
- D) 3

**16.** ¿Para qué dígito \\(x\\) el número de seis cifras \\(27x493\\) es divisible por \\(11\\)?

- A) \\(x = 2\\)
- B) \\(x = 3\\)
- C) \\(x = 8\\)
- D) \\(x = 5\\)

**17.** Sobre la congruencia lineal \\(18x \equiv 30 \pmod{42}\\), ¿cuál afirmación es **correcta**?

- A) No tiene solución, porque \\(18 \nmid 30\\).
- B) Tiene solución única: \\(x \equiv 4 \pmod{42}\\).
- C) Tiene 7 soluciones incongruentes: \\(x \equiv 4 + 6k \pmod{42}\\), \\(k = 0, 1, \dots, 6\\).
- D) Tiene 6 soluciones incongruentes: \\(x \equiv 4, 11, 18, 25, 32, 39 \pmod{42}\\).

**18.** ¿Cuál de los siguientes enteros, producto de primos distintos, cumple que \\((p - 1) \mid (n - 1)\\) para cada uno de sus factores primos \\(p\\), y es por tanto un número de Carmichael?

- A) \\(2465 = 5 \cdot 17 \cdot 29\\)
- B) \\(1155 = 3 \cdot 5 \cdot 7 \cdot 11\\)
- C) \\(341 = 11 \cdot 31\\)
- D) \\(91 = 7 \cdot 13\\)

**19.** El menor entero positivo \\(x\\) que satisface simultáneamente \\(x \equiv 2 \pmod 5\\), \\(x \equiv 3 \pmod 8\\) y \\(x \equiv 1 \pmod 3\\) es:

- A) 27
- B) 187
- C) 67
- D) 107

### Unidad 6. Temas complementarios

**20.** Sabiendo que \\(31\\) es primo, el valor del símbolo de Legendre \\(\left(\frac{7}{31}\right)\\) es:

- A) \\(-1\\)
- B) \\(1\\)
- C) \\(0\\)
- D) No puede determinarse sin listar los cuadrados módulo \\(31\\).

---

## 📝 Parte II. Respuesta corta y cálculo (32 puntos, 4 puntos cada reactivo)

Muestra tu procedimiento: escribe el resultado del libro que usas (algoritmo, teorema o fórmula) y después sustituye. Una respuesta final sin justificación recibe a lo sumo 1 punto.

**21.** *(Algoritmo de Euclides extendido.)* Sean \\(a = 1547\\) y \\(b = 560\\).

- a) Calcula \\(\gcd(1547, 560)\\) con el algoritmo de Euclides, mostrando todas las divisiones.
- b) Con el algoritmo de Euclides extendido (en tabla o por sustitución hacia atrás), encuentra enteros \\(x, y\\) tales que \\(1547x + 560y = \gcd(1547, 560)\\), y comprueba tu resultado.
- c) Calcula \\(\mathrm{mcm}(1547, 560)\\) sin factorizar.

**22.** *(Ecuación diofántica con restricciones.)* Un museo vende boletos de adulto a 45 pesos y de estudiante a 27 pesos.

- a) Demuestra que es imposible que la taquilla recaude exactamente 1 000 pesos.
- b) Encuentra todas las soluciones enteras de \\(45x + 27y = 1260\\).
- c) Un grupo pagó exactamente 1 260 pesos y compró al menos un boleto de cada tipo. ¿Cuántas composiciones del grupo son posibles? ¿Cuál de ellas tiene el mayor número de personas?

**23.** *(Factorización.)* Sea \\(n = 5141\\).

- a) Factoriza \\(n\\) con el método de Fermat, indicando cada valor de \\(x\\) que pruebas.
- b) Demuestra que los dos factores obtenidos son primos, indicando qué primos basta ensayar en cada caso.
- c) Sea \\(N = 6n^2\\). Calcula el número de divisores positivos de \\(N\\) y cuántos de ellos son cuadrados perfectos.

**24.** *(Conteo, triángulo de Pascal y Wilson.)*

- a) ¿Cuántos subconjuntos de \\(\\{1, 2, \dots, 12\\}\\) de tamaño 5 contienen al \\(1\\) y no contienen al \\(2\\)?
- b) ¿Cuántos subconjuntos de tamaño 5 tiene \\(\\{1, 2, \dots, 12\\}\\) en total? ¿Cuántos de ellos contienen al menos un número par?
- c) Sin calcular ningún factorial completo, encuentra el residuo de \\(\binom{13}{6} + 12!\\) al dividirse entre \\(13\\). Cita los resultados que usas.

**25.** *(Funciones aritméticas.)* Sea \\(n = 1800\\).

- a) Escribe la factorización en primos de \\(n\\) y calcula \\(d(n)\\), \\(\sigma(n)\\) y \\(\varphi(n)\\).
- b) Calcula \\(\mu(1800)\\). Después calcula \\(\displaystyle\sum\_{d \mid 1800} \mu(d)\\,\frac{1800}{d}\\) indicando qué divisores aportan un término no nulo, y comprueba que coincide con \\(\varphi(1800)\\).
- c) Sin calcular término por término, ¿cuánto vale \\(\displaystyle\sum\_{d \mid 1800} \varphi(d)\\)? Cita el resultado.

**26.** *(Teoremas de Euler y Wilson.)*

- a) Encuentra los dos últimos dígitos de \\(13^{2026}\\).
- b) Encuentra el residuo de \\(18!\\) al dividirse entre \\(23\\).

**27.** *(Inversos y congruencias lineales.)*

- a) Con el algoritmo de Euclides extendido, encuentra el inverso de \\(23\\) módulo \\(60\\) como un entero de \\(\\{0, 1, \dots, 59\\}\\).
- b) Encuentra todas las soluciones incongruentes módulo \\(120\\) de \\(46x \equiv 14 \pmod{120}\\).
- c) Explica por qué \\(46x \equiv 15 \pmod{120}\\) no tiene solución.

**28.** *(Teorema Chino del Resto con módulos no coprimos.)* Considera el sistema

\\[
\begin{cases} x \equiv 5 \pmod{12}, \\\\ x \equiv 11 \pmod{18}, \\\\ x \equiv 3 \pmod{10}. \end{cases}
\\]

- a) Sustituye cada congruencia por congruencias módulo potencias de primos, verifica que no hay contradicciones y escribe un sistema equivalente con módulos coprimos dos a dos.
- b) Resuelve el sistema con el algoritmo del Teorema Chino del Resto y comprueba la solución en las tres congruencias originales.
- c) Explica por qué el sistema deja de tener solución si la tercera congruencia se cambia por \\(x \equiv 4 \pmod{10}\\).

---

## 📝 Parte III. Demostraciones (48 puntos, 8 puntos cada una)

Redacta cada demostración en prosa matemática completa: declara lo que supones y lo que quieres probar, justifica cada paso con una definición o un resultado previo, y cierra con una conclusión explícita.

**29.** *(Máximo común divisor.)*

- a) Demuestra que \\(\gcd(3n + 2,\\, 5n + 3) = 1\\) para todo \\(n \in \mathbb{Z}\\).
- b) Sean \\(a, b \in \mathbb{Z}^+\\) con \\(\gcd(a, b) = 1\\). Demuestra que \\(\gcd(a + b,\\, ab) = 1\\).
- c) Con las mismas hipótesis, demuestra que \\(\gcd(a + b,\\, a - b) \in \\{1, 2\\}\\), y muestra con ejemplos que ambos valores son posibles.

**30.** *(Teorema Fundamental de la Aritmética.)*

- a) Sean \\(a, b \in \mathbb{Z}^+\\). Usando la factorización en primos, demuestra que si \\(a^2 \mid b^2\\), entonces \\(a \mid b\\).
- b) Demuestra que \\(n^4 + 4\\) es compuesto para todo entero \\(n \ge 2\\). (Sugerencia: escribe \\(n^4 + 4 = (n^2 + 2)^2 - (2n)^2\\).) ¿Qué ocurre con \\(n = 1\\)?

**31.** *(Coeficientes binomiales y primos.)*

- a) Demuestra que \\(k\binom{n}{k} = n\binom{n - 1}{k - 1}\\) para \\(1 \le k \le n\\).
- b) Usando a) (y no la Proposición del libro que lo afirma directamente), demuestra que si \\(p\\) es primo y \\(1 \le k \le p - 1\\), entonces \\(p \mid \binom{p}{k}\\).
- c) Demuestra que si \\(p\\) es primo, entonces \\(\binom{2p}{p} \equiv 2 \pmod p\\). Puedes usar la identidad de Vandermonde.

**32.** *(Funciones multiplicativas e inversión de Möbius.)* Sea \\(f\\) una función aritmética multiplicativa y sea \\(F(n) = \displaystyle\sum\_{d \mid n} \mu(d)\\, f(d)\\).

- a) Demuestra que \\(F\\) es multiplicativa y que, si \\(n = p\_1^{e\_1} \cdots p\_r^{e\_r} > 1\\), entonces \\(F(n) = \displaystyle\prod\_{i=1}^{r} \big(1 - f(p\_i)\big)\\).
- b) Deduce que \\(\displaystyle\sum\_{d \mid n} \mu(d)\\,\sigma(d) = (-1)^r p\_1 p\_2 \cdots p\_r\\).
- c) Aplicando a) a \\(f(n) = 1/n\\) y la identidad \\(\varphi(n) = \displaystyle\sum\_{d \mid n} \mu(d)\\,\frac{n}{d}\\) (obtenida de la identidad de Gauss por inversión de Möbius), deduce la fórmula del producto \\(\varphi(n) = n \displaystyle\prod\_{i=1}^{r}\left(1 - \frac{1}{p\_i}\right)\\).

**33.** *(Congruencias, Fermat y Wilson.)*

- a) Demuestra por inducción que si \\(a \equiv b \pmod n\\), entonces \\(a^k \equiv b^k \pmod n\\) para todo entero \\(k \ge 1\\).
- b) Demuestra que \\(42 \mid (n^7 - n)\\) para todo \\(n \in \mathbb{Z}\\).
- c) Sea \\(p \ge 3\\) primo. Demuestra que \\(2\\,(p - 3)! \equiv -1 \pmod p\\).

**34.** *(Unidades y Teorema Chino del Resto.)* Sean \\(m, n\\) enteros positivos.

- a) Demuestra que \\(a\\) tiene inverso módulo \\(n\\) si y solo si \\(\gcd(a, n) = 1\\), y que en ese caso el inverso es único módulo \\(n\\).
- b) Sin usar el Teorema Chino del Resto, demuestra que si \\(\gcd(m, n) = 1\\), el sistema \\(x \equiv a \pmod m\\), \\(x \equiv b \pmod n\\) tiene solución para cualesquiera \\(a, b \in \mathbb{Z}\\), y que esta es única módulo \\(mn\\).
- c) Usando b), demuestra que la congruencia \\(x^2 \equiv 1 \pmod{15}\\) tiene exactamente 4 soluciones incongruentes módulo \\(15\\), y encuéntralas.

---

## 🔑 Clave de respuestas y soluciones

No abras estos bloques hasta haber terminado el examen completo.

<details>
<summary><strong>Mostrar / ocultar la clave de la Parte I</strong></summary>

| Reactivo | Respuesta | Justificación breve |
| :---: | :---: | :--- |
| 1 | C | \\(\\{7k + 3\\}\\) no está acotado inferiormente: para cada elemento \\(7k + 3\\), el elemento \\(7(k - 1) + 3\\) es menor. A tiene mínimo 15, D tiene mínimo 14, y B es un subconjunto de \\(\mathbb{Z}\\) acotado inferiormente (todos sus elementos son \\(\ge -999\\)), cuyo mínimo es \\(-999\\) (con \\(k = 0\\)): quien elige B olvida que el buen orden vale en todo subconjunto de \\(\mathbb{Z}\\) acotado inferiormente. |
| 2 | A | \\(-83 = 9 \cdot (-10) + 7\\) con \\(0 \le 7 < 9\\). B «trunca» la división y deja un residuo negativo, que no está permitido; C copia el signo de la división \\(83 = 9 \cdot 9 + 2\\), pero \\(9 \cdot (-9) + 2 = -79\\); D tampoco cumple \\(0 \le r < b\\). |
| 3 | D | Por Euclides, \\(120 = 84 + 36\\), \\(84 = 2 \cdot 36 + 12\\), \\(36 = 3 \cdot 12\\), así que \\(\gcd(84, 120) = 12\\), y \\(n = 84x + 120y\\) tiene solución si y solo si \\(12 \mid n\\). Como \\(12 = 84 \cdot 3 - 120 \cdot 2\\), se tiene \\(-48 = 84(-12) + 120 \cdot 8\\). A y B son múltiplos de 6 pero no de 12 (error de calcular mal el mcd), y C solo es múltiplo de 4. |
| 4 | B | Con \\(d = \gcd(12, 18) = 6\\): \\(x = x\_0 + \frac{18}{6}t\\), \\(y = y\_0 - \frac{12}{6}t\\). A no divide entre \\(d\\) y pierde soluciones, como \\((4, -1)\\); C intercambia los coeficientes y D tiene el signo equivocado: con \\(t = 1\\) ninguna de las dos da una solución. |
| 5 | B | \\(720 = 2^4 \cdot 3^2 \cdot 5\\); los divisores múltiplos de 6 son \\(2^{\alpha}3^{\beta}5^{\gamma}\\) con \\(1 \le \alpha \le 4\\), \\(1 \le \beta \le 2\\), \\(0 \le \gamma \le 1\\): \\(4 \cdot 2 \cdot 2 = 16\\). A es \\(d(720)\\), el total; C cuenta los que **no** son múltiplos de 6; D toma mal el rango del exponente de 2. |
| 6 | D | \\(\sqrt{391} \approx 19.8\\), así que hay que ensayar hasta el 19: \\(391 = 17 \cdot 23\\). A se detiene antes de \\(\sqrt{391}\\); B es falsa (\\(13 \cdot 31 = 403\\)); C da un factor que no es el menor. |
| 7 | A | El mcd toma el **mínimo** de cada exponente: \\(2^{\min(5,2)}3^{\min(1,4)}5^{\min(0,1)}7^{\min(2,1)} = 2^2 \cdot 3 \cdot 7 = 84\\). B es el mcm (máximos); C incluye al 5, cuyo exponente mínimo es 0; D resta exponentes. |
| 8 | C | Regla del producto: \\(\binom{9}{4} \cdot 4 = 126 \cdot 4 = 504\\). A olvida al presidente; B es \\(P(9, 4)\\), que ordena a los cuatro integrantes; D es \\(9 \cdot \binom{8}{4}\\), que elige al presidente y **otros cuatro**, es decir, un comité de 5. |
| 9 | D | \\(\binom{11}{4} = 330 = 11 \cdot 30\\), como garantiza la divisibilidad de \\(\binom{p}{k}\\) por un primo \\(p\\). Esa propiedad requiere que el módulo sea **primo**: \\(\binom{8}{2} = 28\\), \\(\binom{9}{3} = 84\\) y \\(\binom{10}{5} = 252\\) no son múltiplos de 8, 9 y 10, respectivamente. |
| 10 | A | Por Wilson, \\(16! \equiv -1 \pmod{17}\\), y \\(16 \equiv -1\\), así que \\(-15! \equiv -1\\) y \\(15! \equiv 1\\). B aplica Wilson a \\(15!\\) en lugar de \\(16!\\); C confunde el caso primo con el compuesto (\\((n - 1)! \equiv 0\\)); D supone erróneamente que \\((p - 2)! \equiv p - 2\\). |
| 11 | B | \\(1260 = 2^2 \cdot 3^2 \cdot 5 \cdot 7\\) y \\(\varphi(1260) = (4 - 2)(9 - 3)(5 - 1)(7 - 1) = 2 \cdot 6 \cdot 4 \cdot 6 = 288\\). A trata a \\(\varphi\\) como completamente multiplicativa (\\(\varphi(4) = \varphi(2)^2 = 1\\) y \\(\varphi(9) = \varphi(3)^2 = 4\\), lo que da \\(1 \cdot 4 \cdot 4 \cdot 6 = 96\\)); C olvida el factor \\(1 - \frac{1}{7}\\); D usa \\(\varphi(p^e) = p^e - 1\\). |
| 12 | C | Si \\(k = ab\\) con \\(1 < a, b < k\\), entonces \\(2^b - 1\\) es un divisor propio de \\(2^k - 1\\). A es falsa: \\(2^{11} - 1 = 2047 = 23 \cdot 89\\); por eso B también es falsa (todo perfecto par exige \\(2^k - 1\\) primo); D confunde la definición: un número es perfecto si \\(\sigma(n) = 2n\\). |
| 13 | A | \\(392 = 2^3 \cdot 7^2\\): \\(d = (3 + 1)(2 + 1) = 12\\) y \\(\sigma = (1 + 2 + 4 + 8)(1 + 7 + 49) = 15 \cdot 57 = 855\\). B suma los exponentes; C usa \\(\frac{p^e - 1}{p - 1}\\) en lugar de \\(\frac{p^{e+1} - 1}{p - 1}\\); D supone que 392 es perfecto. |
| 14 | D | \\(1001 = 7 \cdot 11 \cdot 13\\) tiene tres factores primos distintos, así que \\(\mu(1001) = (-1)^3 = -1\\). A es verdadera (\\(210 = 2 \cdot 3 \cdot 5 \cdot 7\\)), B también (\\(98 = 2 \cdot 7^2\\)) y C también, porque \\(\sum\_{d \mid n} \mu(d) = 0\\) para todo \\(n > 1\\). |
| 15 | C | Por Fermat, \\(3^6 \equiv 1 \pmod 7\\); como \\(100 = 6 \cdot 16 + 4\\), \\(3^{100} \equiv 3^4 = 81 \equiv 4\\). A reduce el exponente módulo 7 en lugar de módulo \\(p - 1 = 6\\); D aplica \\(a^n \equiv a\\) a un exponente que no es el primo. |
| 16 | B | Como \\(10 \equiv -1 \pmod{11}\\), la suma alternada de las cifras (de derecha a izquierda) es \\(3 - 9 + 4 - x + 7 - 2 = 3 - x\\), que es múltiplo de 11 solo si \\(x = 3\\). A usa el criterio del 9, C reduce la suma ordinaria de cifras módulo 11, y D hace al número divisible por 3, no por 11. |
| 17 | D | \\(\gcd(18, 42) = 6\\) y \\(6 \mid 30\\), luego hay exactamente 6 soluciones. Dividiendo entre 6, \\(3x \equiv 5 \pmod 7\\), es decir, \\(x \equiv 4 \pmod 7\\), que da \\(4, 11, 18, 25, 32, 39\\) módulo 42. A confunde la condición: lo que debe dividir a 30 es el mcd, no 18; B olvida que hay \\(d\\) soluciones; C intercambia \\(d = 6\\) con \\(n/d = 7\\). |
| 18 | A | \\(2464 = 4 \cdot 616 = 16 \cdot 154 = 28 \cdot 88\\), así que se cumple el criterio. En B, \\(4 \nmid 1154\\); en C, \\(30 \nmid 340\\) (341 es pseudoprimo en base 2, pero no número de Carmichael); en D, \\(12 \nmid 90\\). |
| 19 | C | De \\(x \equiv 3 \pmod 8\\) y \\(x \equiv 2 \pmod 5\\) se obtiene \\(x \equiv 27 \pmod{40}\\); los candidatos \\(27, 67, 107\\) módulo 120 dan residuos \\(0, 1, 2\\) módulo 3, así que \\(x \equiv 67 \pmod{120}\\). A olvida la tercera congruencia, D no la cumple y B es solución, pero no la menor. |
| 20 | B | Como \\(7 \equiv 31 \equiv 3 \pmod 4\\), la reciprocidad da \\(\left(\frac{7}{31}\right) = -\left(\frac{31}{7}\right) = -\left(\frac{3}{7}\right)\\), y de nuevo \\(\left(\frac{3}{7}\right) = -\left(\frac{7}{3}\right) = -\left(\frac{1}{3}\right) = -1\\). Luego \\(\left(\frac{7}{31}\right) = 1\\) (en efecto, \\(10^2 = 100 \equiv 7 \pmod{31}\\)). A olvida uno de los dos cambios de signo; D desconoce que la reciprocidad evita listar los cuadrados. |

</details>

<details>
<summary><strong>Mostrar / ocultar las soluciones de la Parte II</strong></summary>

**Reactivo 21.**

- a) Las divisiones sucesivas son:

\\[
\begin{aligned}
1547 &= 560 \cdot 2 + 427, \\\\
560 &= 427 \cdot 1 + 133, \\\\
427 &= 133 \cdot 3 + 28, \\\\
133 &= 28 \cdot 4 + 21, \\\\
28 &= 21 \cdot 1 + 7, \\\\
21 &= 7 \cdot 3 + 0.
\end{aligned}
\\]

El último residuo no nulo es 7, luego \\(\gcd(1547, 560) = 7\\).

- b) Con la recurrencia \\(x\_i = x\_{i-2} - q\_i x\_{i-1}\\), \\(y\_i = y\_{i-2} - q\_i y\_{i-1}\\):

| \\(i\\) | \\(q\_i\\) | \\(r\_i\\) | \\(x\_i\\) | \\(y\_i\\) |
| :---: | :---: | :---: | :---: | :---: |
| \\(-1\\) | — | 1547 | 1 | 0 |
| \\(0\\) | — | 560 | 0 | 1 |
| \\(1\\) | 2 | 427 | 1 | \\(-2\\) |
| \\(2\\) | 1 | 133 | \\(-1\\) | 3 |
| \\(3\\) | 3 | 28 | 4 | \\(-11\\) |
| \\(4\\) | 4 | 21 | \\(-17\\) | 47 |
| \\(5\\) | 1 | 7 | 21 | \\(-58\\) |

Así, \\(7 = 1547 \cdot 21 + 560 \cdot (-58)\\). Comprobación: \\(32\\,487 - 32\\,480 = 7\\).

- c) Por la relación \\(\gcd(a, b)\cdot\mathrm{mcm}(a, b) = ab\\): \\(\mathrm{mcm}(1547, 560) = \dfrac{1547 \cdot 560}{7} = 1547 \cdot 80 = 123\\,760\\).

*Puntaje:* 1.5 por a) con todas las divisiones, 1.5 por b) incluyendo la comprobación, 1 por c).

**Reactivo 22.** Por Euclides, \\(45 = 27 + 18\\), \\(27 = 18 + 9\\), \\(18 = 2 \cdot 9\\), así que \\(\gcd(45, 27) = 9\\).

- a) Si \\(45x + 27y = 1000\\) tuviera solución entera, \\(9\\) dividiría a \\(1000\\); pero la suma de cifras de 1000 es 1, así que \\(9 \nmid 1000\\). La ecuación no tiene solución.
- b) Como \\(9 \mid 1260\\), hay solución. Dividiendo entre 9: \\(5x + 3y = 140\\), con solución particular \\((x\_0, y\_0) = (1, 45)\\). Con \\(b/d = 3\\) y \\(a/d = 5\\), la solución general es

\\[
x = 1 + 3t, \qquad y = 45 - 5t, \qquad t \in \mathbb{Z}.
\\]

- c) Se necesita \\(x \ge 1\\) y \\(y \ge 1\\): \\(1 + 3t \ge 1\\) da \\(t \ge 0\\), y \\(45 - 5t \ge 1\\) da \\(t \le 8\\). Hay **9** composiciones posibles: \\((1, 45), (4, 40), (7, 35), \dots, (25, 5)\\). El número de personas es \\(x + y = 46 - 2t\\), máximo con \\(t = 0\\): 1 adulto y 45 estudiantes, 46 personas.

*Puntaje:* 1 por a), 2 por b) (1 por el mcd y la solución particular, 1 por la solución general), 1 por c).

**Reactivo 23.**

- a) Como \\(71^2 = 5041 < 5141 < 5184 = 72^2\\), se empieza en \\(x = 72\\):
  - \\(x = 72\\): \\(5184 - 5141 = 43\\), no es cuadrado.
  - \\(x = 73\\): \\(5329 - 5141 = 188\\), no es cuadrado.
  - \\(x = 74\\): \\(5476 - 5141 = 335\\), no es cuadrado.
  - \\(x = 75\\): \\(5625 - 5141 = 484 = 22^2\\).

  Luego \\(5141 = (75 + 22)(75 - 22) = 97 \cdot 53\\).
- b) Por el criterio de ensayo de divisiones, basta probar los primos \\(p \le \sqrt{53} < 8\\) y \\(p \le \sqrt{97} < 10\\); en ambos casos son \\(2, 3, 5, 7\\). Ninguno divide a 53 ni a 97, así que ambos son primos.
- c) \\(N = 2 \cdot 3 \cdot 53^2 \cdot 97^2\\), luego \\(d(N) = 2 \cdot 2 \cdot 3 \cdot 3 = 36\\). Un divisor \\(2^{\alpha}3^{\beta}53^{\gamma}97^{\delta}\\) es cuadrado si y solo si todos los exponentes son pares: \\(\alpha = \beta = 0\\) y \\(\gamma, \delta \in \\{0, 2\\}\\), lo que da **4** divisores cuadrados (\\(1\\), \\(53^2\\), \\(97^2\\) y \\(53^2 \cdot 97^2\\)).

*Puntaje:* 1.5 por a), 1 por b), 1.5 por c).

**Reactivo 24.**

- a) Fijado el 1 y excluido el 2, se eligen los 4 elementos restantes entre los 10 números \\(\\{3, \dots, 12\\}\\): \\(\binom{10}{4} = 210\\).
- b) En total hay \\(\binom{12}{5} = 792\\). Los que **no** contienen pares se forman con los 6 impares: \\(\binom{6}{5} = 6\\). Por complemento, \\(792 - 6 = 786\\) contienen al menos un par.
- c) Como 13 es primo y \\(1 \le 6 \le 12\\), se tiene \\(13 \mid \binom{13}{6}\\). Por el Teorema de Wilson, \\(12! \equiv -1 \pmod{13}\\). Luego \\(\binom{13}{6} + 12! \equiv 0 - 1 \equiv 12 \pmod{13}\\): el residuo es **12**.

*Puntaje:* 1 por a), 1.5 por b), 1.5 por c) (0.5 por cada resultado citado y 0.5 por el residuo).

**Reactivo 25.**

- a) \\(1800 = 2^3 \cdot 3^2 \cdot 5^2\\). Por la multiplicatividad:
  - \\(d(1800) = 4 \cdot 3 \cdot 3 = 36\\).
  - \\(\sigma(1800) = (1 + 2 + 4 + 8)(1 + 3 + 9)(1 + 5 + 25) = 15 \cdot 13 \cdot 31 = 6045\\).
  - \\(\varphi(1800) = (8 - 4)(9 - 3)(25 - 5) = 4 \cdot 6 \cdot 20 = 480\\).
- b) \\(\mu(1800) = 0\\), porque \\(2^2 \mid 1800\\). En la suma solo aportan los divisores libres de cuadrados, \\(1, 2, 3, 5, 6, 10, 15, 30\\):

\\[
1800 - 900 - 600 - 360 + 300 + 180 + 120 - 60 = 480 = \varphi(1800).
\\]

- c) Por la identidad de Gauss, \\(\sum\_{d \mid n} \varphi(d) = n\\), así que la suma vale **1800**.

*Puntaje:* 2 por a) (0.5 por la factorización y 0.5 por cada función), 1.5 por b), 0.5 por c).

**Reactivo 26.**

- a) Como \\(\gcd(13, 100) = 1\\) y \\(\varphi(100) = 100 \cdot \frac{1}{2} \cdot \frac{4}{5} = 40\\), el Teorema de Euler da \\(13^{40} \equiv 1 \pmod{100}\\). Como \\(2026 = 40 \cdot 50 + 26\\), se tiene \\(13^{2026} \equiv 13^{26}\\). Elevando al cuadrado repetidamente y reduciendo módulo 100:

\\[
13^2 = 169 \equiv 69, \quad 13^4 \equiv 69^2 = 4761 \equiv 61, \quad 13^8 \equiv 61^2 = 3721 \equiv 21, \quad 13^{16} \equiv 21^2 = 441 \equiv 41.
\\]

Como \\(26 = 16 + 8 + 2\\): \\(13^{26} \equiv 41 \cdot 21 \cdot 69\\); \\(41 \cdot 21 = 861 \equiv 61\\) y \\(61 \cdot 69 = 4209 \equiv 9\\). Los dos últimos dígitos son **09**.

- b) Por Wilson, \\(22! \equiv -1 \pmod{23}\\). Además, \\(22 \cdot 21 \cdot 20 \cdot 19 \equiv (-1)(-2)(-3)(-4) = 24 \equiv 1 \pmod{23}\\), así que \\(22! = (22 \cdot 21 \cdot 20 \cdot 19) \cdot 18! \equiv 18!\\). Luego \\(18! \equiv -1 \equiv 22 \pmod{23}\\): el residuo es **22**.

*Puntaje:* 2.5 por a) (1 por \\(\varphi(100)\\) y la reducción del exponente, 1.5 por el cálculo), 1.5 por b).

**Reactivo 27.**

- a) Euclides: \\(60 = 23 \cdot 2 + 14\\), \\(23 = 14 + 9\\), \\(14 = 9 + 5\\), \\(9 = 5 + 4\\), \\(5 = 4 + 1\\). Sustituyendo hacia atrás:

\\[
1 = 5 - 4 = 2 \cdot 5 - 9 = 2 \cdot 14 - 3 \cdot 9 = 5 \cdot 14 - 3 \cdot 23 = 5 \cdot 60 - 13 \cdot 23.
\\]

Así, \\(23 \cdot (-13) \equiv 1 \pmod{60}\\), y el inverso es \\(-13 \equiv 47\\). Comprobación: \\(23 \cdot 47 = 1081 = 18 \cdot 60 + 1\\).

- b) \\(\gcd(46, 120) = 2\\) y \\(2 \mid 14\\), así que hay exactamente 2 soluciones módulo 120. La congruencia equivale a \\(46x - 14 = 120k\\), es decir, a \\(23x - 7 = 60k\\): \\(23x \equiv 7 \pmod{60}\\). Multiplicando por el inverso 47: \\(x \equiv 7 \cdot 47 = 329 \equiv 29 \pmod{60}\\). Las soluciones módulo 120 son \\(x \equiv 29\\) y \\(x \equiv 89\\). Comprobación: \\(46 \cdot 29 = 1334 = 11 \cdot 120 + 14\\).
- c) \\(ax \equiv b \pmod n\\) tiene solución si y solo si \\(\gcd(a, n) \mid b\\); aquí \\(\gcd(46, 120) = 2 \nmid 15\\). (Directamente: \\(46x - 120k\\) es par y no puede valer 15.)

*Puntaje:* 1.5 por a), 2 por b) (0.5 por el número de soluciones, 1 por la reducción y 0.5 por las dos clases), 0.5 por c).

**Reactivo 28.**

- a) Por la reducción a módulos coprimos (\\(12 = 4 \cdot 3\\), \\(18 = 2 \cdot 9\\), \\(10 = 2 \cdot 5\\)):
  - \\(x \equiv 5 \pmod{12} \iff x \equiv 1 \pmod 4\\) y \\(x \equiv 2 \pmod 3\\).
  - \\(x \equiv 11 \pmod{18} \iff x \equiv 1 \pmod 2\\) y \\(x \equiv 2 \pmod 9\\).
  - \\(x \equiv 3 \pmod{10} \iff x \equiv 1 \pmod 2\\) y \\(x \equiv 3 \pmod 5\\).

  No hay contradicciones: \\(x \equiv 1 \pmod 4\\) implica \\(x \equiv 1 \pmod 2\\), y \\(x \equiv 2 \pmod 9\\) implica \\(x \equiv 2 \pmod 3\\). Eliminando las redundantes queda el sistema equivalente \\(x \equiv 1 \pmod 4\\), \\(x \equiv 2 \pmod 9\\), \\(x \equiv 3 \pmod 5\\).
- b) \\(N = 4 \cdot 9 \cdot 5 = 180\\):

| \\(n\_i\\) | \\(a\_i\\) | \\(N\_i\\) | \\(x\_i\\) (inverso de \\(N\_i\\) módulo \\(n\_i\\)) |
| :---: | :---: | :---: | :--- |
| 4 | 1 | 45 | \\(45 \equiv 1 \pmod 4\\), luego \\(x\_1 = 1\\) |
| 9 | 2 | 20 | \\(20 \equiv 2 \pmod 9\\) y \\(2 \cdot 5 \equiv 1\\), luego \\(x\_2 = 5\\) |
| 5 | 3 | 36 | \\(36 \equiv 1 \pmod 5\\), luego \\(x\_3 = 1\\) |

\\[
x\_0 = 45 \cdot 1 \cdot 1 + 20 \cdot 5 \cdot 2 + 36 \cdot 1 \cdot 3 = 45 + 200 + 108 = 353 \equiv 173 \pmod{180}.
\\]

Comprobación: \\(173 = 14 \cdot 12 + 5 = 9 \cdot 18 + 11 = 17 \cdot 10 + 3\\). La solución es \\(x \equiv 173 \pmod{180}\\).

- c) \\(x \equiv 4 \pmod{10}\\) implica \\(x \equiv 0 \pmod 2\\), mientras que \\(x \equiv 5 \pmod{12}\\) implica \\(x \equiv 1 \pmod 2\\): las dos condiciones módulo 2 son incompatibles.

*Puntaje:* 1.5 por a) (incluyendo la verificación de compatibilidad), 2 por b) (1 por los inversos, 0.5 por \\(x\_0\\), 0.5 por la comprobación), 0.5 por c).

</details>

<details>
<summary><strong>Mostrar / ocultar las soluciones y rúbricas de la Parte III</strong></summary>

### Rúbrica general (8 puntos por demostración)

| Criterio | Puntos | Se otorga cuando… |
| :--- | :---: | :--- |
| Estructura | 2 | Queda claro qué se supone y qué se quiere probar; las variables, los primos y los módulos están declarados. |
| Desarrollo | 4 | Cada paso es correcto y está justificado por una definición o un resultado previo citado. |
| Cierre y redacción | 2 | Se enuncia la conclusión y no se usa como hipótesis lo que se quiere probar. |

**Errores que cuestan puntos:** cancelar un factor en una congruencia sin verificar que es coprimo con el módulo, aplicar el Lema de Euclides para primos a un número compuesto, confundir \\(a \mid b\\) con \\(b \mid a\\), «demostrar» con ejemplos numéricos una afirmación general, y omitir los casos extremos (por ejemplo, \\(a = 1\\) o \\(p = 2\\)) cuando el argumento general no los cubre.

**Demostración 29.**

a) Se cumple \\(5(3n + 2) - 3(5n + 3) = 15n + 10 - 15n - 9 = 1\\). Así, \\(1\\) es combinación lineal entera de \\(3n + 2\\) y \\(5n + 3\\), y por la caracterización de los primos relativos (existen \\(x, y\\) con \\(ax + by = 1\\) si y solo si \\(\gcd(a, b) = 1\\)), \\(\gcd(3n + 2, 5n + 3) = 1\\).

b) Como \\(\gcd(a, b + ka) = \gcd(a, b)\\) para todo \\(k \in \mathbb{Z}\\), se tiene \\(\gcd(a, a + b) = \gcd(a, b) = 1\\) y, del mismo modo, \\(\gcd(b, a + b) = 1\\). Por Bézout existen enteros \\(x, y, u, v\\) con

\\[
ax + (a + b)y = 1, \qquad bu + (a + b)v = 1.
\\]

Multiplicando ambas igualdades:

\\[
1 = ab\\,(xu) + (a + b)\big[axv + buy + (a + b)yv\big],
\\]

que expresa 1 como combinación lineal entera de \\(ab\\) y \\(a + b\\). Luego \\(\gcd(a + b, ab) = 1\\).

c) Sea \\(g = \gcd(a + b, a - b)\\) (está definido, pues \\(a + b > 0\\)). Como \\(g\\) divide a \\(a + b\\) y a \\(a - b\\), divide a su suma \\(2a\\) y a su diferencia \\(2b\\). Todo divisor común de \\(2a\\) y \\(2b\\) divide a \\(\gcd(2a, 2b)\\) (porque este es combinación lineal entera de \\(2a\\) y \\(2b\\)), y \\(\gcd(2a, 2b) = 2\gcd(a, b) = 2\\). Luego \\(g \mid 2\\) y, como \\(g > 0\\), \\(g \in \\{1, 2\\}\\). Ambos valores ocurren: con \\((a, b) = (2, 1)\\), \\(\gcd(3, 1) = 1\\); con \\((a, b) = (3, 1)\\), \\(\gcd(4, 2) = 2\\). \\(\blacksquare\\)

*Rúbrica específica:* a) vale 2 puntos, b) vale 3 (1 por las dos coprimalidades, 2 por combinarlas correctamente) y c) vale 3 (2 por la divisibilidad \\(g \mid 2\\), 1 por los ejemplos).

**Demostración 30.**

a) Si \\(a = 1\\), no hay nada que probar. Si \\(b = 1\\), entonces \\(a^2 \mid 1\\) obliga a \\(a = 1\\). Supongamos \\(a, b > 1\\) y escribamos, con el mismo conjunto de primos \\(p\_1, \dots, p\_r\\) y exponentes \\(e\_i, f\_i \ge 0\\),

\\[
a = p\_1^{e\_1} \cdots p\_r^{e\_r}, \qquad b = p\_1^{f\_1} \cdots p\_r^{f\_r}.
\\]

Por la unicidad de la factorización, \\(a^2 = \prod p\_i^{2e\_i}\\) y \\(b^2 = \prod p\_i^{2f\_i}\\) son las factorizaciones de \\(a^2\\) y \\(b^2\\). Por la caracterización de la divisibilidad mediante exponentes, \\(a^2 \mid b^2\\) implica \\(2e\_i \le 2f\_i\\), es decir, \\(e\_i \le f\_i\\) para todo \\(i\\), y la misma caracterización da \\(a \mid b\\).

b) Se tiene \\(n^4 + 4 = (n^2 + 2)^2 - (2n)^2 = (n^2 + 2n + 2)(n^2 - 2n + 2)\\). Para \\(n \ge 2\\), el segundo factor cumple \\(n^2 - 2n + 2 = (n - 1)^2 + 1 \ge 2\\), y el primero es mayor que el segundo (pues \\(4n > 0\\)), así que también es \\(\ge 2\\). Como ambos factores son \\(\ge 2\\), cada uno es menor que su producto \\(n^4 + 4\\). Así, \\(n^4 + 4\\) tiene un divisor \\(c\\) con \\(1 < c < n^4 + 4\\), es decir, es compuesto. Para \\(n = 1\\), el segundo factor vale \\(1\\) y \\(n^4 + 4 = 5\\) es primo: la hipótesis \\(n \ge 2\\) es necesaria. \\(\blacksquare\\)

*Rúbrica específica:* a) vale 4 puntos (1 por los casos \\(a = 1\\) o \\(b = 1\\), 1 por plantear las factorizaciones, 2 por la comparación de exponentes con su justificación); b) vale 4 (1 por la factorización, 2 por probar que ambos factores son \\(\ge 2\\), 1 por el caso \\(n = 1\\)).

**Demostración 31.**

a) Por la fórmula de los coeficientes binomiales, para \\(1 \le k \le n\\):

\\[
k\binom{n}{k} = \frac{k \cdot n!}{k!\\,(n - k)!} = \frac{n!}{(k - 1)!\\,(n - k)!} = n \cdot \frac{(n - 1)!}{(k - 1)!\\,\big((n - 1) - (k - 1)\big)!} = n\binom{n - 1}{k - 1}.
\\]

(Combinatoriamente, ambos lados cuentan los comités de \\(k\\) personas elegidas entre \\(n\\) con un presidente: se elige el comité y luego su presidente, o el presidente y luego los otros \\(k - 1\\) integrantes.)

b) Por a) con \\(n = p\\): \\(k\binom{p}{k} = p\binom{p - 1}{k - 1}\\), de modo que \\(p \mid k\binom{p}{k}\\). Como \\(1 \le k \le p - 1\\) y \\(p\\) es primo, \\(p \nmid k\\), así que \\(\gcd(p, k) = 1\\). Por el Lema de Euclides, \\(p \mid \binom{p}{k}\\).

c) Por la identidad de Vandermonde con \\(m = n = k = p\\) y la simetría \\(\binom{p}{p - i} = \binom{p}{i}\\):

\\[
\binom{2p}{p} = \sum\_{i=0}^{p} \binom{p}{i}\binom{p}{p - i} = \sum\_{i=0}^{p} \binom{p}{i}^2 = 1 + \sum\_{i=1}^{p-1} \binom{p}{i}^2 + 1.
\\]

Por b), cada término con \\(1 \le i \le p - 1\\) es múltiplo de \\(p\\). Luego \\(\binom{2p}{p} \equiv 2 \pmod p\\). \\(\blacksquare\\)

*Rúbrica específica:* a) vale 2 puntos, b) vale 3 (1 por usar a), 1 por \\(\gcd(p, k) = 1\\), 1 por invocar el Lema de Euclides) y c) vale 3 (1 por Vandermonde y la simetría, 2 por la reducción módulo \\(p\\)).

**Demostración 32.**

a) Sea \\(g(n) = \mu(n) f(n)\\). Entonces \\(g(1) = \mu(1) f(1) = 1\\) y, si \\(\gcd(m, n) = 1\\), por la multiplicatividad de \\(\mu\\) y de \\(f\\):

\\[
g(mn) = \mu(mn) f(mn) = \mu(m)\mu(n) f(m) f(n) = g(m)\\,g(n).
\\]

Así, \\(g\\) es multiplicativa, y \\(F(n) = \sum\_{d \mid n} g(d)\\) es la suma sobre divisores de una función multiplicativa; por la proposición correspondiente del libro, \\(F\\) es multiplicativa. Para una potencia de primo \\(p^e\\) con \\(e \ge 1\\), los divisores son \\(1, p, \dots, p^e\\) y \\(\mu(p^j) = 0\\) para \\(j \ge 2\\), luego

\\[
F(p^e) = \mu(1) f(1) + \mu(p) f(p) = 1 - f(p).
\\]

Por la multiplicatividad, \\(F(n) = F(p\_1^{e\_1}) \cdots F(p\_r^{e\_r}) = \prod\_{i=1}^{r} \big(1 - f(p\_i)\big)\\).

b) \\(\sigma\\) es multiplicativa y \\(\sigma(p) = 1 + p\\), así que \\(1 - \sigma(p\_i) = -p\_i\\). Por a), \\(\sum\_{d \mid n} \mu(d)\sigma(d) = \prod\_{i=1}^{r}(-p\_i) = (-1)^r p\_1 \cdots p\_r\\).

c) \\(f(n) = 1/n\\) es multiplicativa: \\(f(1) = 1\\) y \\(f(mn) = \frac{1}{mn} = f(m) f(n)\\). Por a), \\(\sum\_{d \mid n} \frac{\mu(d)}{d} = \prod\_{i=1}^{r}\left(1 - \frac{1}{p\_i}\right)\\). Multiplicando la identidad \\(\varphi(n) = \sum\_{d \mid n} \mu(d)\frac{n}{d} = n\sum\_{d \mid n}\frac{\mu(d)}{d}\\) se obtiene \\(\varphi(n) = n\prod\_{i=1}^{r}\left(1 - \frac{1}{p\_i}\right)\\). El argumento no es circular: la identidad usada proviene de la identidad de Gauss y de la inversión de Möbius, no de la fórmula del producto. \\(\blacksquare\\)

*Rúbrica específica:* a) vale 4 puntos (1 por la multiplicatividad de \\(\mu f\\), 1 por la de \\(F\\), 1 por \\(F(p^e)\\), 1 por el producto); b) vale 2 y c) vale 2.

**Demostración 33.**

a) Para \\(k = 1\\) es la hipótesis. Si \\(a^k \equiv b^k \pmod n\\) para algún \\(k \ge 1\\), multiplicando esta congruencia por \\(a \equiv b \pmod n\\) (la congruencia es compatible con el producto) se obtiene \\(a^{k+1} \equiv b^{k+1} \pmod n\\). Por el principio de inducción, la afirmación vale para todo \\(k \ge 1\\).

b) Como \\(42 = 2 \cdot 3 \cdot 7\\) con factores coprimos dos a dos, por la reducción a módulos coprimos basta probar \\(n^7 \equiv n\\) módulo 2, 3 y 7. Por el Pequeño Teorema de Fermat, \\(a^p \equiv a \pmod p\\) para todo entero \\(a\\).

- Módulo 7: \\(n^7 \equiv n\\) directamente.
- Módulo 3: \\(n^3 \equiv n\\), luego \\(n^7 = n^3 \cdot n^3 \cdot n \equiv n \cdot n \cdot n = n^3 \equiv n\\).
- Módulo 2: \\(n^2 \equiv n\\); por inducción, \\(n^k \equiv n\\) para todo \\(k \ge 1\\) (si \\(n^k \equiv n\\), entonces \\(n^{k+1} \equiv n^2 \equiv n\\)); en particular, \\(n^7 \equiv n\\).

Por tanto \\(n^7 \equiv n \pmod{42}\\), es decir, \\(42 \mid (n^7 - n)\\).

c) Como \\(p \ge 3\\), se tiene \\(p - 3 \ge 0\\) y \\((p - 1)! = (p - 1)(p - 2)\\,(p - 3)!\\). Como \\(p - 1 \equiv -1\\) y \\(p - 2 \equiv -2 \pmod p\\), resulta \\((p - 1)! \equiv (-1)(-2)(p - 3)! = 2\\,(p - 3)!\\). Por el Teorema de Wilson, \\((p - 1)! \equiv -1\\), luego \\(2\\,(p - 3)! \equiv -1 \pmod p\\). \\(\blacksquare\\)

*Rúbrica específica:* a) vale 2 puntos; b) vale 4 (1 por la reducción a 2, 3 y 7 citando la coprimalidad, 1 por cada módulo 3 y 2, 1 por la conclusión); c) vale 2.

**Demostración 34.**

a) Si \\(\gcd(a, n) = 1\\), por Bézout existen \\(x, y\\) con \\(ax + ny = 1\\), es decir, \\(ax \equiv 1 \pmod n\\): \\(x\\) es un inverso de \\(a\\). Recíprocamente, si \\(ab \equiv 1 \pmod n\\), existe \\(k\\) con \\(ab - nk = 1\\); todo divisor común de \\(a\\) y \\(n\\) divide a \\(ab - nk = 1\\), luego \\(\gcd(a, n) = 1\\). Unicidad: si \\(ab \equiv 1\\) y \\(ab' \equiv 1 \pmod n\\), entonces \\(ab \equiv ab'\\), y como \\(\gcd(a, n) = 1\\) se puede cancelar \\(a\\): \\(b \equiv b' \pmod n\\).

b) *Existencia.* Por Bézout existen \\(u, v\\) con \\(mu + nv = 1\\). Sea \\(x\_0 = a\\,nv + b\\,mu\\). Como \\(nv = 1 - mu \equiv 1 \pmod m\\), se tiene \\(x\_0 \equiv a \cdot 1 + 0 = a \pmod m\\); análogamente, \\(mu \equiv 1 \pmod n\\) da \\(x\_0 \equiv b \pmod n\\).

*Unicidad.* Si \\(x \equiv x\_0 \pmod{mn}\\), entonces \\(x \equiv x\_0\\) módulo \\(m\\) y módulo \\(n\\), así que \\(x\\) también es solución. Recíprocamente, si \\(x\\) y \\(x\_0\\) son soluciones, \\(m \mid (x - x\_0)\\) y \\(n \mid (x - x\_0)\\); como \\(\gcd(m, n) = 1\\), se sigue \\(mn \mid (x - x\_0)\\). Luego la solución es única módulo \\(mn\\).

c) Por la reducción a módulos coprimos, \\(x^2 \equiv 1 \pmod{15}\\) si y solo si \\(x^2 \equiv 1 \pmod 3\\) y \\(x^2 \equiv 1 \pmod 5\\). Para un primo \\(p\\), \\(x^2 \equiv 1 \pmod p\\) equivale a \\(p \mid (x - 1)(x + 1)\\), y por el Lema de Euclides para primos, a \\(x \equiv 1\\) o \\(x \equiv -1 \pmod p\\); para \\(p\\) impar, estas dos clases son distintas. Así, las soluciones son las \\(x\\) con \\(x \equiv \pm 1 \pmod 3\\) y \\(x \equiv \pm 1 \pmod 5\\). Por b), cada una de las \\(2 \cdot 2 = 4\\) elecciones de signos determina exactamente una clase módulo 15, y clases distintas corresponden a elecciones distintas. Resolviendo: \\(x \equiv 1, 4, 11, 14 \pmod{15}\\) (en efecto, \\(4^2 = 16\\), \\(11^2 = 121 = 8 \cdot 15 + 1\\) y \\(14^2 = 196 = 13 \cdot 15 + 1\\)). \\(\blacksquare\\)

*Rúbrica específica:* a) vale 3 puntos (1 por cada implicación, 1 por la unicidad); b) vale 3 (2 por la existencia, 1 por la unicidad); c) vale 2 (1 por las dos raíces módulo cada primo, 1 por el conteo vía b)).

</details>

---

## 📊 Diagnóstico y plan de repaso

### Tabla de diagnóstico

Anota tus puntos por unidad y calcula tu porcentaje de dominio.

| Unidad | Reactivos | Puntos posibles | Mis puntos | Mi porcentaje |
| :--- | :--- | :---: | :---: | :---: |
| 1. El anillo de los enteros \\(\mathbb{Z}\\) | 1 a 4, 21, 22, 29 | 20 | | |
| 2. Primalidad | 5 a 7, 23, 30 | 15 | | |
| 3. Elementos de combinatoria | 8 a 10, 24, 31 | 15 | | |
| 4. Funciones aritméticas | 11 a 14, 25, 32 | 16 | | |
| 5. El anillo de residuos módulo \\(n\\) | 15 a 19, 26 a 28, 33, 34 | 33 | | |
| 6. Temas complementarios | 20 | 1 | | |
| **Total** | | **100** | | |

La Unidad 5 pesa más porque las congruencias son el lenguaje en el que se expresan y se usan casi todos los resultados del curso: los teoremas de Fermat, Euler y Wilson, las congruencias lineales y el Teorema Chino del Resto. La Unidad 1 le sigue porque la divisibilidad, el algoritmo de Euclides y Bézout son la base de todas las demás. La Unidad 6 tiene un peso simbólico porque es complementaria.

### Interpretación del resultado

| Puntaje total | Diagnóstico | Qué hacer |
| :---: | :--- | :--- |
| 85 a 100 | Preparación sólida | Repasa solo los reactivos fallados y practica la redacción de demostraciones con un límite de tiempo. |
| 70 a 84 | Preparación aceptable con huecos | Repasa las unidades con menos del 70 % y rehaz tus reactivos sin ver las soluciones. |
| 50 a 69 | Preparación insuficiente | Estudia de nuevo las secciones señaladas abajo y resuelve los ejercicios de cada unidad antes de repetir el auto-examen. |
| Menos de 50 | Se requiere un plan de estudio completo | Empieza por las Unidades 1 y 2, que son la base de todo lo demás, y busca asesoría con tu profesor. |

Más allá del total, **cualquier unidad por debajo del 60 %** merece atención prioritaria, aunque tu puntaje global sea bueno.

### Mapa de repaso

| Si fallaste el reactivo… | Repasa la sección |
| :--- | :--- |
| 1, 33 (a) | [1.1 Los axiomas de Peano y el principio del buen orden](../unidad1/01-fundamentos.md) |
| 2 | [1.2 Divisibilidad y el algoritmo de la división](../unidad1/02-divisibilidad.md) |
| 21 (c), 29 | [1.3 Máximo común divisor y mínimo común múltiplo](../unidad1/03-mcd-mcm.md) |
| 3, 21 (a, b), 27 (a) | [1.4 El algoritmo de Euclides y el teorema de Bézout](../unidad1/04-euclides-bezout.md) |
| 4, 22 | [1.5 Ecuaciones diofánticas lineales y cuadráticas](../unidad1/05-diofanticas.md) |
| 6, 23 (b), 30 (b) | [2.1 Números primos, números relativos y la criba de Eratóstenes](../unidad2/01-primos.md) |
| 5, 7, 23 (c), 30 (a) | [2.2 El Teorema Fundamental de la Aritmética](../unidad2/02-teorema-fundamental.md) |
| 23 (a) | [2.3 Métodos elementales de factorización](../unidad2/03-factorizacion.md) |
| 8, 24 (a, b), 31 (a) | [3.1 Conjuntos finitos, combinaciones y permutaciones](../unidad3/01-conjuntos-finitos-combinatoria.md) |
| 9, 24 (c), 31 (b, c) | [3.2 El triángulo de Pascal y sus aplicaciones aritméticas](../unidad3/02-triangulo-pascal.md) |
| 10, 24 (c) | [3.3 Los teoremas de Fermat y Wilson por combinatoria](../unidad3/03-fermat-wilson.md) |
| 12, 13, 25 (a), 32 (b) | [4.1 Las funciones σ(n) y d(n): números perfectos y de Mersenne](../unidad4/01-sigma-d-perfectos.md) |
| 11, 25 (a, c), 32 (c) | [4.2 La función φ de Euler](../unidad4/02-phi-euler.md) |
| 14, 25 (b), 32 | [4.3 La función de Möbius](../unidad4/03-mobius.md) |
| 16, 28 (a), 33 (a), 34 (c) | [5.1 Congruencias y sus propiedades elementales](../unidad5/01-congruencias.md) |
| 26 (a) | [5.2 Sistemas reducidos de residuos y la función de Euler](../unidad5/02-sistemas-reducidos-euler.md) |
| 15, 18, 26 (b), 33 (b, c) | [5.3 Los teoremas de Euler y Fermat; pseudoprimos](../unidad5/03-fermat-wilson-pseudoprimos.md) |
| 17, 27, 34 (a) | [5.4 Unidades módulo n y congruencias lineales](../unidad5/04-unidades-congruencias-lineales.md) |
| 19, 28 (b, c), 34 (b, c) | [5.5 El Teorema Chino del Resto](../unidad5/05-teorema-chino-resto.md) |
| 20 | [6.1 Residuos cuadráticos y la ley de reciprocidad cuadrática](../unidad6/01-residuos-cuadraticos-reciprocidad.md) |

Para practicar más, resuelve los ejercicios de cada unidad ([Unidad 1](../unidad1/ejercicios.md), [Unidad 2](../unidad2/ejercicios.md), [Unidad 3](../unidad3/ejercicios.md), [Unidad 4](../unidad4/ejercicios.md), [Unidad 5](../unidad5/ejercicios.md) y [Unidad 6](../unidad6/ejercicios.md)); para mejorar la redacción de la Parte III, consulta el [Apéndice A. Técnicas de demostración](../apendices/a-tecnicas-demostracion.md), y para comprobar factorizaciones después del examen, la [Tabla de los primeros números primos](../apendices/b-tabla-primos.md).
