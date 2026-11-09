# 6.2 Fracciones continuas

Las fracciones continuas ofrecen una manera alternativa —y en muchos sentidos más natural— de representar números racionales e irracionales, íntimamente ligada al algoritmo de Euclides (Sección 1.4), y con aplicaciones que van desde las mejores aproximaciones racionales de un número real hasta la solución de la ecuación de Pell.

## Fracciones continuas finitas

**Definición.** Una **fracción continua finita** (simple) es una expresión de la forma
\\[ [a_0;a_1,a_2,\dots,a_k] = a_0+\cfrac1{a_1+\cfrac1{a_2+\cfrac1{\ddots+\cfrac1{a_k}}}}, \\]
donde \\(a_0\in\mathbb{Z}\\) y \\(a_1,\dots,a_k\in\mathbb{Z}^+\\).

**Teorema 6.9.** *Todo número racional \\(x=p/q\\) admite una representación finita como fracción continua, obtenida mediante el algoritmo de Euclides aplicado a \\(p,q\\).*

*Demostración.* Sea \\(x=p/q\\), \\(q>0\\). Escribamos la división euclídea \\(p=a_0q+r_0\\), \\(0\le r_0<q\\) (Teorema 1.12), es decir, \\(x=a_0+\frac{r_0}q\\). Si \\(r_0=0\\), \\(x=a_0=[a_0]\\) y terminamos. Si no, sea \\(x_1=q/r_0>1\\), de modo que \\(x=a_0+\frac1{x_1}\\); repetimos el proceso con \\(x_1\\) en lugar de \\(x\\). Como los residuos sucesivos \\(q>r_0>r_1>\cdots\ge0\\) forman una sucesión estrictamente decreciente de enteros no negativos (exactamente como en el algoritmo de Euclides, Teorema 1.25), el proceso termina en un número finito de pasos, dando \\(x=[a_0;a_1,\dots,a_k]\\). \\(\blacksquare\\)

**Ejemplo 6.10.** Calculemos la fracción continua de \\(x=\frac{67}{29}\\), usando exactamente el mismo algoritmo de Euclides de la Sección 1.4 (como en el Ejemplo 1.26):
\\[ 67=2\cdot29+9,\quad29=3\cdot9+2,\quad9=4\cdot2+1,\quad2=2\cdot1+0. \\]
Los cocientes sucesivos dan \\(\frac{67}{29}=[2;3,4,2]\\). Verificación: \\([2;3,4,2]=2+\cfrac1{3+\cfrac1{4+\cfrac12}}=2+\cfrac1{3+\cfrac1{9/2}}=2+\cfrac1{3+2/9}=2+\cfrac1{29/9}=2+\frac9{29}=\frac{67}{29}\\). ✓

**Observación 6.11.** La representación no es del todo única: \\([a_0;a_1,\dots,a_k]=[a_0;a_1,\dots,a_k-1,1]\\) si \\(a_k>1\\) (o, si \\(k=0\\), simplemente \\([a_0]=[a_0-1;1]\\)); por convención, se suele exigir \\(a_k\ge2\\) (para \\(k\ge1\\)) para fijar una representación canónica única.

## Convergentes

**Definición.** Dada una fracción continua (finita o infinita) \\(a_0,a_1,a_2,\dots\\), sus **convergentes** son las fracciones \\(\frac{h_n}{k_n}=[a_0;a_1,\dots,a_n]\\), definidas recursivamente por
\\[ h_{-1}=1,\ h_{-2}=0,\qquad h_n=a_nh_{n-1}+h_{n-2}; \\]
\\[ k_{-1}=0,\ k_{-2}=1,\qquad k_n=a_nk_{n-1}+k_{n-2}. \\]

**Proposición 6.12.** *Para todo \\(n\ge0\\), \\([a_0;a_1,\dots,a_n]=\dfrac{h_n}{k_n}\\), y además \\(h_nk_{n-1}-h_{n-1}k_n=(-1)^{n-1}\\).*

*Demostración (esbozo).* Ambas afirmaciones se demuestran por inducción simultánea sobre \\(n\\), usando las relaciones de recurrencia. La primera es una verificación algebraica directa a partir de la definición de fracción continua (se sustituye la definición recursiva de \\([a_0;\dots,a_n]\\) en términos de \\([a_1;\dots,a_n]\\) y se usa la hipótesis de inducción). La segunda —el determinante \\(h_nk_{n-1}-h_{n-1}k_n\\)— se sigue directamente de las fórmulas de recurrencia:
\\[ h_nk_{n-1}-h_{n-1}k_n = (a_nh_{n-1}+h_{n-2})k_{n-1}-h_{n-1}(a_nk_{n-1}+k_{n-2}) = -(h_{n-1}k_{n-2}-h_{n-2}k_{n-1}), \\]
lo que da una recursión de signo alternante que, junto con el caso base, produce \\((-1)^{n-1}\\). \\(\blacksquare\\)

**Corolario 6.13.** *\\(\gcd(h_n,k_n)=1\\) para todo \\(n\\): cada convergente está en su forma reducida.*

*Demostración.* De \\(h_nk_{n-1}-h_{n-1}k_n=\pm1\\), cualquier divisor común de \\(h_n,k_n\\) divide a \\(\pm1\\) (Proposición 1.9(ii)), luego es \\(1\\). \\(\blacksquare\\)

## Fracciones continuas infinitas y números irracionales

**Teorema 6.14.** *Todo número irracional \\(\alpha\\) admite una representación única como fracción continua **infinita** \\(\alpha=[a_0;a_1,a_2,\dots]\\), definida mediante el algoritmo:*
\\[ a_0=\lfloor\alpha\rfloor, \qquad \alpha_0=\alpha, \qquad \alpha_{n+1}=\frac1{\alpha_n-a_n}, \qquad a_{n+1}=\lfloor\alpha_{n+1}\rfloor, \\]
*y los convergentes \\(h_n/k_n\\) (definidos como arriba) satisfacen \\(h_n/k_n \to \alpha\\) cuando \\(n\to\infty\\), con*
\\[ \left|\alpha-\frac{h_n}{k_n}\right| < \frac1{k_nk_{n+1}}. \\]

*Idea de la demostración.* El proceso nunca termina precisamente porque \\(\alpha\\) es irracional (si terminara, \\(\alpha\\) sería racional, por el mismo cálculo del Teorema 6.9). La estimación del error se obtiene de la identidad de la Proposición 6.12 aplicada a los convergentes consecutivos, junto con el hecho de que \\(\alpha\\) está siempre "entre" dos convergentes consecutivos. \\(\blacksquare\\)

**Proposición 6.15 (mejor aproximación).** *Cada convergente \\(h_n/k_n\\) es la mejor aproximación racional a \\(\alpha\\) entre todas las fracciones con denominador \\(\le k_n\\): para \\(n\ge1\\), si \\(p/q\neq h_n/k_n\\) con \\(0<q\le k_n\\), entonces \\(|\alpha-p/q|>|\alpha-h_n/k_n|\\).* (Para \\(n=0\\) puede fallar: con \\(\varphi=[1;1,1,\dots]\\), la fracción \\(2/1\\) está más cerca de \\(\varphi\\) que \\(h_0/k_0=1\\).)

Esta propiedad —que hace de las fracciones continuas la herramienta óptima para aproximar irracionales por racionales— explica su uso histórico en calendarios y engranajes astronómicos, y es la razón de que \\(\frac{22}7\\) y \\(\frac{355}{113}\\) (convergentes de \\(\pi=[3;7,15,1,292,\dots]\\)) sean aproximaciones tan eficientes.

**Ejemplo 6.16 (fracción continua de \\(\sqrt2\\)).** Como \\(\sqrt2=1+(\sqrt2-1)\\) y \\(\frac1{\sqrt2-1}=\sqrt2+1=2+(\sqrt2-1)\\), se obtiene la representación **periódica**
\\[ \sqrt2 = [1;2,2,2,\dots] = [1;\overline2]. \\]
Sus primeros convergentes son \\(1,\ \frac32,\ \frac75,\ \frac{17}{12},\ \frac{41}{29},\dots\\), aproximaciones racionales cada vez mejores de \\(\sqrt2\approx1.41421356\dots\\) (nótese, por ejemplo, \\(\frac{41}{29}\approx1.41379\\)).

**Teorema 6.17 (Lagrange, sin demostración).** *La fracción continua de un número irracional \\(\alpha\\) es eventualmente periódica si y solo si \\(\alpha\\) es un irracional cuadrático (es decir, raíz de un polinomio de segundo grado con coeficientes enteros).*

## Aplicación: la ecuación de Pell

**Definición.** La **ecuación de Pell** es \\(x^2-dy^2=1\\), donde \\(d\\) es un entero positivo que no es un cuadrado perfecto, y se buscan soluciones \\((x,y)\in\mathbb{Z}^2\\).

**Teorema 6.18 (sin demostración completa).** *La ecuación de Pell \\(x^2-dy^2=1\\) siempre tiene soluciones no triviales (\\(y\ne0\\)), y todas ellas se obtienen a partir de los convergentes de la fracción continua (periódica, por el Teorema 6.17) de \\(\sqrt d\\).*

**Ejemplo 6.19.** Para \\(d=2\\): usando los convergentes \\(h_n/k_n\\) de \\(\sqrt2=[1;\overline2]\\) calculados arriba, se verifica que \\((h,k)=(3,2)\\) satisface \\(3^2-2\cdot2^2=9-8=1\\): la solución fundamental es \\((x,y)=(3,2)\\). A partir de ella, todas las demás soluciones positivas se obtienen mediante \\(x_n+y_n\sqrt2=(3+2\sqrt2)^n\\), \\(n=1,2,3,\dots\\); por ejemplo, \\((3+2\sqrt2)^2=17+12\sqrt2\\), dando la siguiente solución \\((17,12)\\): en efecto, \\(17^2-2\cdot12^2=289-288=1\\). ✓

La ecuación de Pell tiene una historia milenaria (India, siglo VII, con Brahmagupta; Europa, siglo XVII, con Fermat retando a sus contemporáneos ingleses a resolverla) y aparece hoy en día en problemas de teoría algebraica de números relacionados con unidades de anillos de enteros cuadráticos, un tema que se estudia en cursos de álgebra y teoría de números avanzada.
