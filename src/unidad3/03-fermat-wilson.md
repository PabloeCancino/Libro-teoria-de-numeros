# 3.3 Los teoremas de Fermat y Wilson por combinatoria

En la Unidad 5 demostraremos el Pequeño Teorema de Fermat y el Teorema de Wilson mediante el álgebra de congruencias (Teoremas 5.13 y 5.17 respectivamente), siguiendo el enfoque clásico de la teoría de números. Aquí presentamos, como lo indica el programa de la Unidad 3, demostraciones **alternativas y autocontenidas** basadas exclusivamente en argumentos combinatorios, que iluminan estos resultados desde una perspectiva distinta.

## El Pequeño Teorema de Fermat por conteo de collares

**Teorema 3.17 (Pequeño Teorema de Fermat).** *Sea \\(p\\) un número primo y \\(a\\) un entero positivo. Entonces*
\\[ a^p \equiv a \pmod p. \\]

*Demostración (combinatoria, "conteo de collares").* Consideremos el conjunto \\(X\\) de todas las secuencias \\((x_1,x_2,\dots,x_p)\\) con cada \\(x_i \in \{1,2,\dots,a\}\\); claramente \\(|X|=a^p\\) (regla del producto). El grupo cíclico de rotaciones \\(\mathbb{Z}_p\\) actúa sobre \\(X\\) mediante
\\[ \rho(x_1,\dots,x_p) = (x_2,x_3,\dots,x_p,x_1) \\]
(rotación cíclica de un lugar), y sus iteradas \\(\rho^0=\mathrm{id},\rho,\rho^2,\dots,\rho^{p-1}\\).

Separamos \\(X\\) en dos tipos de secuencias: las **constantes** (\\(x_1=x_2=\cdots=x_p\\)), de las cuales hay exactamente \\(a\\) (una por cada valor posible), y las **no constantes**, de las cuales hay \\(a^p-a\\).

*Afirmación: cada órbita de una secuencia no constante bajo las rotaciones \\(\rho^0,\dots,\rho^{p-1}\\) tiene exactamente \\(p\\) elementos distintos.* En efecto, si una secuencia no constante \\((x_1,\dots,x_p)\\) fuera fijada por alguna rotación \\(\rho^j\\) con \\(0<j<p\\), entonces la secuencia sería periódica con periodo \\(d=\gcd(j,p)\\) (un hecho estándar sobre rotaciones cíclicas: el conjunto de \\(j\\) tales que \\(\rho^j\\) fija la secuencia es un subgrupo de \\(\mathbb{Z}_p\\), y todo subgrupo de \\(\mathbb{Z}_p\\) es \\(\{0\}\\) o todo \\(\mathbb{Z}_p\\), pues \\(p\\) es primo —Corolario 1.18 aplicado al orden del subgrupo, que debe dividir a \\(p\\)). Como \\(0<j<p\\) y \\(p\\) es primo, \\(\gcd(j,p)=1\\), lo que fuerza periodo \\(d=1\\), es decir, la secuencia sería constante, contradicción. Por tanto, ninguna rotación no trivial fija una secuencia no constante, así que las \\(p\\) rotaciones \\(\rho^0,\dots,\rho^{p-1}\\) producen \\(p\\) secuencias distintas: la órbita tiene exactamente \\(p\\) elementos.

Como las órbitas particionan el conjunto de las \\(a^p-a\\) secuencias no constantes en bloques de tamaño exactamente \\(p\\) (regla de la suma), se sigue \\(p \mid (a^p-a)\\), es decir, \\(a^p\equiv a\pmod p\\). \\(\blacksquare\\)

**Corolario 3.18.** *Si además \\(p \nmid a\\), entonces \\(a^{p-1}\equiv1\pmod p\\).*

*Demostración.* De \\(a^p\equiv a\pmod p\\), es decir \\(p\mid a(a^{p-1}-1)\\); como \\(p\nmid a\\) y \\(p\\) es primo, el Lema de Euclides (Proposición 2.2) da \\(p\mid(a^{p-1}-1)\\), es decir, \\(a^{p-1}\equiv1\pmod p\\). \\(\blacksquare\\)

Este es exactamente el enunciado del Teorema 5.13 (Fermat) que se re-demostrará mediante congruencias en la Unidad 5; comparar ambas demostraciones —la combinatoria, vía la acción de rotación, y la aritmética, vía sistemas completos de residuos— es un ejercicio muy instructivo sobre cómo distintas áreas de las matemáticas iluminan el mismo hecho.

*Demostración alternativa (vía el Corolario 3.13).* Damos también una segunda demostración, más corta, que usa directamente la divisibilidad de los coeficientes binomiales centrales establecida en la Sección 3.2. Procedemos por inducción sobre \\(a\ge0\\). Para \\(a=0\\), \\(0^p=0\\) trivialmente (\\(p\ge2\\)). Supongamos \\(a^p\equiv a\pmod p\\) para cierto \\(a\ge0\\); por el Corolario 3.13 (con \\(x=a,\,y=1\\)),
\\[ (a+1)^p \equiv a^p+1^p = a^p+1 \equiv a+1 \pmod p, \\]
usando la hipótesis de inducción en el último paso. Por inducción, \\(a^p\equiv a\pmod p\\) para todo \\(a\ge0\\), y el caso de \\(a\\) negativo se obtiene con un argumento similar o reduciéndolo al caso positivo. \\(\blacksquare\\)

## El Teorema de Wilson por emparejamiento de inversos

**Teorema 3.19 (Teorema de Wilson).** *Si \\(p\\) es primo, entonces*
\\[ (p-1)! \equiv -1 \pmod p. \\]

*Demostración (combinatoria, por emparejamiento).* Los casos \\(p=2\\) (\\(1!=1\equiv-1\pmod2\\)) y \\(p=3\\) (\\(2!=2\equiv-1\pmod3\\)) se verifican directamente. Supongamos \\(p\ge5\\) y consideremos el conjunto \\(A=\{2,3,\dots,p-2\}\\) (es decir, \\(\{1,\dots,p-1\}\\) sin los extremos \\(1\\) y \\(p-1\\), que analizaremos aparte). Este conjunto contiene los "compañeros de accidente multiplicativo" de cada elemento: para cada \\(a \in A\\), la ecuación \\(ax\equiv1\pmod p\\) tiene una única solución \\(x=a' \in \{1,\dots,p-1\}\\) (este es un caso particular de la Proposición 5.9 de la Unidad 5, que garantiza solución única de congruencias lineales \\(ax\equiv b\pmod p\\) cuando \\(\gcd(a,p)=1\\); aquí lo tomamos como conocido de la teoría elemental de congruencias, o se puede verificar directamente usando que las clases \\(a,2a,\dots,(p-1)a\\) recorren todos los residuos no nulos módulo \\(p\\) exactamente una vez).

Se verifica que \\(a=a'\\) (es decir, \\(a\\) es su propio "compañero", \\(a^2\equiv1\pmod p\\)) exactamente cuando \\(p\mid(a-1)(a+1)\\) (pues \\(a^2-1=(a-1)(a+1)\\)), lo que por el Lema de Euclides (Proposición 2.2) ocurre exactamente cuando \\(a\equiv1\\) o \\(a\equiv-1\equiv p-1\pmod p\\); ambos casos quedan **fuera** de \\(A=\{2,\dots,p-2\}\\) por construcción. Por tanto, para todo \\(a\in A\\), su compañero \\(a'\\) también está en \\(A\\) y es distinto de \\(a\\), y la relación "ser compañero de" empareja los elementos de \\(A\\) en \\(\frac{p-3}{2}\\) parejas disjuntas \\(\{a,a'\}\\) con \\(aa'\equiv1\pmod p\\) (nótese que \\(|A|=p-3\\), un número par, ya que \\(p\\) es impar).

Multiplicando los elementos de \\(A\\) agrupados por parejas:
\\[ \prod_{a\in A} a \equiv 1\cdot1\cdots1 = 1 \pmod p \qquad (\text{producto de } \tfrac{p-3}2 \text{ unos}). \\]
Finalmente,
\\[ (p-1)! = 1\cdot\Big(\prod_{a\in A}a\Big)\cdot(p-1) \equiv 1\cdot1\cdot(p-1) \equiv -1 \pmod p, \\]
usando que \\(p-1\equiv-1\pmod p\\). \\(\blacksquare\\)

**Ejemplo 3.20.** Para \\(p=11\\): \\(A=\{2,3,4,5,6,7,8,9\}\\), y las parejas de compañeros son \\(\{2,6\}\\) (\\(2\cdot6=12\equiv1\\)), \\(\{3,4\}\\) (\\(3\cdot4=12\equiv1\\)), \\(\{5,9\}\\) (\\(5\cdot9=45\equiv1\\), pues \\(45=44+1\\)), \\(\{7,8\}\\) (\\(7\cdot8=56\equiv1\\), pues \\(56=55+1\\)) — coincidiendo exactamente con el Ejemplo 2.16 del material de congruencias de la Unidad 5. Entonces \\(10!\equiv1\cdot1\cdot1\cdot1\cdot10\equiv-1\pmod{11}\\), es decir, \\(10!=3\,628\,800=329\,890\cdot11-10\\)... en efecto, \\(3\,628\,800+1=3\,628\,801=11\cdot329\,891\\), confirmando \\(10!\equiv-1\pmod{11}\\).

## El recíproco del Teorema de Wilson

**Proposición 3.21.** *Si \\(n>1\\) es compuesto, entonces \\((n-1)!\equiv0\pmod n\\) (salvo el caso \\(n=4\\), donde \\((n-1)!=3!=6\equiv2\pmod4\\)).*

*Demostración (esbozo).* Si \\(n\\) es compuesto y \\(n\neq4\\), se puede escribir \\(n=ab\\) con \\(1<a<b<n\\) (factores distintos), y entonces tanto \\(a\\) como \\(b\\) aparecen como factores separados en \\((n-1)!=1\cdot2\cdots(n-1)\\), así que \\(ab=n\\) divide a \\((n-1)!\\). Si \\(n=p^2\\) para algún primo \\(p\ge3\\), entonces \\(p\\) y \\(2p\\) son ambos menores que \\(n-1=p^2-1\\) (pues \\(p\ge3\\)) y aparecen como factores distintos en \\((n-1)!\\), dando de nuevo \\(p^2\mid(n-1)!\\). El caso \\(n=4=2^2\\) es una excepción genuina, verificable directamente. \\(\blacksquare\\)

Junto con el Teorema 3.19, esta proposición muestra que, salvo por el caso trivial \\(n=4\\), la congruencia de Wilson **caracteriza** a los números primos: \\((n-1)!\equiv-1\pmod n\\) si y solo si \\(n\\) es primo. Esto contrasta con el Pequeño Teorema de Fermat (Teorema 3.17/5.13), que —como se verá en la Unidad 5 al estudiar los **pseudoprimos** y los **números de Carmichael**— **no** es una condición suficiente para la primalidad: existen enteros compuestos \\(n\\) que satisfacen \\(a^n\equiv a\pmod n\\) para algunas (o incluso todas) las bases \\(a\\).
