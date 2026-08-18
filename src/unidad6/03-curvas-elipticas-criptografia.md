# 6.3 Introducción a las curvas elípticas y a la criptografía

Cerramos el libro con un vistazo panorámico —deliberadamente informal, sin las demostraciones completas que sí exigimos en las unidades anteriores— a dos de las aplicaciones más influyentes de la teoría de números elemental desarrollada en este texto: la criptografía de clave pública y la teoría de curvas elípticas, esta última protagonista de una de las historias más notables de las matemáticas del siglo XX, la demostración del Último Teorema de Fermat.

## Criptografía de clave pública: RSA

Toda la maquinaria de las Unidades 2, 4 y 5 —primos, la función φ de Euler, y el Teorema de Euler— confluye en el algoritmo **RSA** (Rivest, Shamir, Adleman, 1977), el primer criptosistema de clave pública práctico.

**Construcción.** Se eligen dos primos grandes distintos \\(p,q\\) (en la práctica, de cientos de dígitos), y se calcula \\(n=pq\\) y \\(\varphi(n)=(p-1)(q-1)\\) (Teorema 4.13, multiplicatividad de φ, ya que \\(\gcd(p,q)=1\\)). Se elige un entero \\(e\\) con \\(1<e<\varphi(n)\\) y \\(\gcd(e,\varphi(n))=1\\), y se calcula su inverso \\(d\\) módulo \\(\varphi(n)\\) (Proposición 5.22 / Corolario 1.18): \\(ed\equiv1\pmod{\varphi(n)}\\).

La **clave pública** es el par \\((n,e)\\); la **clave privada** es \\(d\\) (junto con \\(p,q\\), que se descartan o se protegen). Un mensaje \\(m\\) (codificado como entero, \\(0\le m<n\\)) se **cifra** como \\(c\equiv m^e\pmod n\\), y se **descifra** calculando \\(c^d\bmod n\\).

**Proposición 6.20 (corrección de RSA).** *Si \\(\gcd(m,n)=1\\), entonces \\((m^e)^d\equiv m\pmod n\\).*

*Demostración.* Como \\(ed\equiv1\pmod{\varphi(n)}\\), escribamos \\(ed=1+k\varphi(n)\\) para algún \\(k\in\mathbb{Z}\\). Entonces
\\[ (m^e)^d = m^{ed} = m^{1+k\varphi(n)} = m\cdot\big(m^{\varphi(n)}\big)^k \equiv m\cdot1^k = m \pmod n, \\]
usando el Teorema de Euler (Teorema 5.10), que exige precisamente \\(\gcd(m,n)=1\\). \\(\blacksquare\\)

(El caso \\(\gcd(m,n)>1\\), que ocurre con probabilidad despreciable si \\(m\\) se elige apropiadamente frente a los primos gigantescos \\(p,q\\), se puede tratar por separado usando el Teorema Chino del Resto, Sección 5.5, aplicando el Pequeño Teorema de Fermat módulo \\(p\\) y módulo \\(q\\) por separado.)

**Seguridad.** La seguridad de RSA descansa en que, dado \\(n=pq\\), **factorizar** \\(n\\) para recuperar \\(p,q\\) (y de ahí \\(\varphi(n)\\) y \\(d\\)) es computacionalmente muy costoso cuando \\(p,q\\) son suficientemente grandes: los mejores algoritmos conocidos (criba general del cuerpo de números) tienen complejidad subexponencial en el número de dígitos de \\(n\\), muy por encima de lo alcanzable en tiempo razonable para módulos de más de 2000 bits. Esto contrasta con los métodos de la Sección 2.3 (división por tanteo, método de Fermat), que son adecuados para enseñar los principios pero completamente inviables a esta escala. Nótese, además, que el algoritmo de Euclides (Sección 1.4) —usado para calcular \\(d\\) a partir de \\(e\\) y \\(\varphi(n)\\)— sí es eficiente incluso para números de esta magnitud (Corolario 1.31), lo cual es esencial para que el sistema sea práctico tanto para cifrar como para generar las claves.

**Ejemplo 6.21 (RSA de juguete, solo con fines ilustrativos).** Sean \\(p=61,q=53\\), así \\(n=3233\\), \\(\varphi(n)=60\cdot52=3120\\). Elegimos \\(e=17\\) (\\(\gcd(17,3120)=1\\)); usando el algoritmo de Euclides extendido (Sección 1.4) se calcula \\(d=2753\\) (pues \\(17\cdot2753=46\,801=15\cdot3120+1\\)). Para cifrar \\(m=65\\): \\(c=65^{17}\bmod3233=2790\\); para descifrar: \\(2790^{2753}\bmod3233=65\\). (Los cálculos intermedios de estas potencias modulares se realizan eficientemente mediante **exponenciación rápida**, elevando al cuadrado repetidamente y reduciendo módulo \\(n\\) en cada paso, en vez de calcular la potencia completa antes de reducir.)

## Curvas elípticas

**Definición.** Una **curva elíptica** sobre \\(\mathbb{Q}\\) (o sobre cualquier cuerpo de característica distinta de \\(2,3\\)) es el conjunto de soluciones de una ecuación de **Weierstrass**
\\[ E:\ y^2 = x^3+Ax+B, \qquad A,B\in\mathbb{Q}, \\]
junto con un punto adicional "en el infinito" \\(\mathcal O\\), sujeto a la condición de no singularidad \\(4A^3+27B^2\ne0\\) (que garantiza que la curva no tiene autointersecciones ni cúspides).

**La ley de grupo (descripción geométrica, sin demostración).** El hecho más notable —y la razón de la enorme utilidad de las curvas elípticas— es que el conjunto de puntos de \\(E\\) admite una **operación de suma** que lo convierte en un grupo abeliano, definida geométricamente: dados dos puntos \\(P,Q\in E\\), la recta que los une corta a la curva en un tercer punto \\(R'\\) (contando multiplicidad e incluyendo el punto al infinito cuando la recta es vertical); se define \\(P+Q\\) como el reflejo de \\(R'\\) respecto al eje \\(x\\). El punto al infinito \\(\mathcal O\\) actúa como neutro, y esta operación resulta asociativa (la parte no trivial de la verificación) y conmutativa.

**Fórmulas explícitas.** Si \\(P=(x_1,y_1)\\), \\(Q=(x_2,y_2)\\), con \\(P\ne\pm Q\\), la pendiente de la recta secante es \\(\lambda=\frac{y_2-y_1}{x_2-x_1}\\), y
\\[ x_3 = \lambda^2-x_1-x_2, \qquad y_3=\lambda(x_1-x_3)-y_1, \qquad P+Q=(x_3,y_3). \\]
Para "duplicar" un punto (\\(P+P\\)), se usa la pendiente de la tangente, \\(\lambda=\frac{3x_1^2+A}{2y_1}\\), con las mismas fórmulas para \\(x_3,y_3\\).

**Ejemplo 6.22.** En la curva \\(E:y^2=x^3-2x\\) (con \\(A=-2,B=0\\)), el punto \\(P=(2,2)\\) satisface \\(2^2=4\\) y \\(2^3-2\cdot2=8-4=4\\), así que \\(P\in E\\). Calculemos \\(2P=P+P\\): \\(\lambda=\frac{3\cdot4-2}{4}=\frac{10}4=\frac52\\); \\(x_3=\frac{25}4-2-2=\frac94\\); \\(y_3=\frac52\left(2-\frac94\right)-2=\frac52\cdot\left(-\frac14\right)-2=-\frac58-2=-\frac{21}8\\). Así, \\(2P=\left(\frac94,-\frac{21}8\right)\\), que puede verificarse que satisface la ecuación de \\(E\\).

## El problema del logaritmo discreto y ECDH

Sobre un **cuerpo finito** \\(\mathbb{F}_p\\) (es decir, trabajando módulo un primo \\(p\\), como en toda la Unidad 5), el conjunto de puntos de una curva elíptica \\(E(\mathbb{F}_p)\\) es un grupo abeliano **finito**. Dado un punto base \\(G\\) y un entero \\(k\\), calcular \\(kG=G+G+\cdots+G\\) (\\(k\\) veces) es rápido mediante duplicación repetida (análogo a la exponenciación rápida mencionada en RSA); pero el problema inverso —dado \\(G\\) y \\(kG\\), encontrar \\(k\\)— el **problema del logaritmo discreto en curvas elípticas** (ECDLP), se considera computacionalmente muy difícil, sin ataques sub-exponenciales conocidos, a diferencia de la factorización de enteros.

Esta asimetría (fácil de calcular, difícil de invertir) es la base del protocolo de intercambio de claves de **Diffie–Hellman sobre curvas elípticas (ECDH)**: dos partes, con un punto público \\(G\\) de orden grande sobre una curva pública \\(E(\mathbb{F}_p)\\), eligen en secreto enteros \\(k_A,k_B\\), intercambian \\(k_AG\\) y \\(k_BG\\), y cada una calcula \\(k_A(k_BG)=k_B(k_AG)=k_Ak_BG\\), un secreto compartido que un observador externo —que solo ve \\(G,k_AG,k_BG\\)— no puede reconstruir eficientemente (bajo la presunción de dificultad del ECDLP). Frente a RSA, las curvas elípticas permiten seguridad comparable con claves considerablemente más cortas, lo que las ha hecho el estándar dominante en protocolos modernos (TLS, criptomonedas, etc.).

## Una mirada al Último Teorema de Fermat

Cerramos con una nota histórica que conecta directamente con el Corolario 1.39 de la Unidad 1. El **Último Teorema de Fermat** afirma que \\(x^n+y^n=z^n\\) no tiene soluciones enteras positivas para \\(n\ge3\\); Fermat lo escribió en el margen de su copia de la *Arithmetica* de Diofanto (c. 1637), afirmando tener una demostración "demasiado extensa para caber en el margen", pero esta nunca se encontró, y el problema permaneció abierto —salvo casos particulares, como \\(n=4\\) (Corolario 1.39) y algunos otros exponentes específicos— durante más de 350 años.

La demostración, completada por **Andrew Wiles** en 1994 (con una contribución técnica crucial de Richard Taylor), no ataca la ecuación directamente, sino que pasa por las curvas elípticas: a toda hipotética solución \\(a^p+b^p=c^p\\) (\\(p\\) primo \\(\ge5\\)) se le asocia la **curva de Frey**
\\[ E:\ y^2=x(x-a^p)(x+b^p), \\]
y se demuestra (Ribet, construyendo sobre la *conjetura épsilon* de Serre) que esta curva tendría propiedades tan patológicas que contradirían la **conjetura de modularidad de Taniyama–Shimura–Weil** (que afirma que toda curva elíptica racional es "modular", es decir, está parametrizada por formas modulares). Wiles y Taylor demostraron esta conjetura para la familia de curvas relevante (curvas semiestables), cerrando así, indirectamente, la demostración del teorema de Fermat.

Esta historia —desde la aritmética elemental de las ternas pitagóricas de la Unidad 1 hasta la maquinaria de curvas elípticas y formas modulares aquí esbozada— ilustra de manera vívida el propósito de esta Unidad 6 y, en cierto sentido, de todo el libro: mostrar cómo las herramientas más elementales de la teoría de números —divisibilidad, congruencias, factorización— son la puerta de entrada a algunas de las matemáticas más profundas y activas de la actualidad.
