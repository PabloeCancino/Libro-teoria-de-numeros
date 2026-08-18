# Notación y convenciones

A lo largo del libro se usa la siguiente notación estándar, salvo indicación expresa en contrario.

| Símbolo | Significado |
|---|---|
| \\(\mathbb{N}\\) | Conjunto de los números naturales. Se usará \\(\mathbb{N} = \{0, 1, 2, 3, \dots\}\\), señalando explícitamente cuándo se excluye el cero. |
| \\(\mathbb{Z}\\) | Conjunto de los números enteros. |
| \\(\mathbb{Z}^+\\) | Conjunto de los enteros positivos, \\(\{1, 2, 3, \dots\}\\). |
| \\(\mathbb{Q}\\), \\(\mathbb{R}\\), \\(\mathbb{C}\\) | Números racionales, reales y complejos. |
| \\(a \mid b\\) | "\\(a\\) divide a \\(b\\)": existe \\(c \in \mathbb{Z}\\) tal que \\(b = ac\\). |
| \\(a \nmid b\\) | \\(a\\) no divide a \\(b\\). |
| \\(\gcd(a,b)\\) o \\(\mathrm{mcd}(a,b)\\) | Máximo común divisor de \\(a\\) y \\(b\\). |
| \\(\mathrm{mcm}(a,b)\\) | Mínimo común múltiplo de \\(a\\) y \\(b\\). |
| \\(a \equiv b \pmod{n}\\) | \\(a\\) es congruente con \\(b\\) módulo \\(n\\): \\(n \mid (a-b)\\). |
| \\(\mathbb{Z}_n\\) o \\(\mathbb{Z}/n\mathbb{Z}\\) | Anillo de clases residuales módulo \\(n\\). |
| \\(\mathbb{Z}_n^{\ast}\\) | Grupo de unidades (elementos invertibles) de \\(\mathbb{Z}_n\\). |
| \\(\varphi(n)\\) | Función phi de Euler. |
| \\(\mu(n)\\) | Función de Möbius. |
| \\(d(n)\\) o \\(\tau(n)\\) | Número de divisores positivos de \\(n\\). |
| \\(\sigma(n)\\) | Suma de los divisores positivos de \\(n\\). |
| \\(\binom{n}{k}\\) | Coeficiente binomial, número de subconjuntos de tamaño \\(k\\) de un conjunto de tamaño \\(n\\). |
| \\(p, q\\) | Salvo indicación contraria, letras reservadas para números primos. |
| \\(\lfloor x \rfloor\\) | Función parte entera (piso) de \\(x\\). |
| \\(\left(\dfrac{a}{p}\right)\\) | Símbolo de Legendre (Unidad 6). |
| \\(\blacksquare\\) o "∎" | Marca el final de una demostración. |

## Convenciones sobre enunciados

- Las **definiciones** se enuncian en recuadros con la palabra **Definición**.
- Los resultados demostrados se clasifican, según su papel en la exposición, como **Proposición**, **Teorema**, **Lema** o **Corolario**; esta jerarquía es tradicional y no indica una diferencia formal de estatus lógico.
- La numeración de definiciones, proposiciones, teoremas, ejemplos y ejercicios sigue el esquema `Unidad.Consecutivo` (por ejemplo, la Proposición 4.3 es una proposición numerada de la Unidad 4), y es independiente entre unidades.
- El símbolo \\(\blacksquare\\) señala el final de una demostración; cuando una demostración se deja como ejercicio, se indica explícitamente.
- Todas las demostraciones son autocontenidas dentro del libro: solo se apela a resultados previamente establecidos en el propio texto, citando el número correspondiente.

## Fórmulas matemáticas

Las fórmulas se escriben en \\(\LaTeX\\), representadas mediante MathJax. Las fórmulas en línea usan la sintaxis \\( \dots \\) y las fórmulas centradas usan \\[ \dots \\].
