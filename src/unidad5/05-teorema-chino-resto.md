# 5.5 El Teorema Chino del Resto

La Proposición 5.24 nos dice que toda congruencia lineal \\(ax\equiv b\pmod n\\) es equivalente a una (o varias) congruencias de la forma \\(x\equiv x_0\pmod{n/d}\\). Por tanto, resolver **simultáneamente** varias congruencias lineales se reduce a resolver un **sistema de congruencias** todas del tipo \\(x\equiv a_i\pmod{n_i}\\). El siguiente teorema clásico —conocido en China desde al menos el siglo III d.C. (tratado *Sunzi Suanjing*, en el contexto de problemas de cómputo del calendario y de conteo de tropas)— resuelve completamente este problema cuando los módulos son coprimos dos a dos.

**Teorema 5.27 (Teorema Chino del Resto).** *Sean \\(n_1,n_2,\dots,n_r\\) enteros positivos primos relativos dos a dos. Entonces el sistema de congruencias*
\\[
\begin{cases}
x\equiv a_1 \pmod{n_1}\\
x\equiv a_2 \pmod{n_2}\\
\quad\vdots\\
x\equiv a_r \pmod{n_r}
\end{cases}
\\]
*tiene solución, y esta es única módulo \\(N=n_1n_2\cdots n_r\\).*

*Demostración.* Para cada \\(i=1,\dots,r\\), sea
\\[ N_i = \frac N{n_i} = n_1\cdots n_{i-1}n_{i+1}\cdots n_r. \\]
Como los \\(n_j\\) son coprimos dos a dos, \\(\gcd(n_i,N_i)=1\\) (por la Proposición 1.19-tipo argumento aplicado repetidamente: \\(n_i\\) es coprimo con cada uno de los factores de \\(N_i\\), luego con su producto). Por la Proposición 5.22 (o el Corolario 1.18), \\(N_i\\) tiene un inverso módulo \\(n_i\\): existe \\(x_i\in\mathbb{Z}\\) tal que
\\[ N_ix_i\equiv1\pmod{n_i}. \\]

Definamos
\\[ x_0 = N_1x_1a_1+N_2x_2a_2+\cdots+N_rx_ra_r. \\]

*Verificación de que \\(x_0\\) es solución.* Fijado \\(i\\), obsérvese que para \\(j\ne i\\), \\(n_i\mid N_j\\) (pues \\(N_j\\) es producto de todos los \\(n_k\\) con \\(k\ne j\\), y en particular incluye a \\(n_i\\)), así que \\(N_j\equiv0\pmod{n_i}\\), y por tanto todos los términos de \\(x_0\\) salvo el \\(i\\)-ésimo se anulan módulo \\(n_i\\):
\\[ x_0 \equiv N_ix_ia_i \equiv 1\cdot a_i = a_i \pmod{n_i}, \\]
usando \\(N_ix_i\equiv1\pmod{n_i}\\) en el último paso. Como esto vale para cada \\(i=1,\dots,r\\), \\(x_0\\) satisface todo el sistema.

*Unicidad módulo \\(N\\).* Es inmediato que si \\(x\equiv x_0\pmod N\\), entonces (como \\(n_i\mid N\\) para cada \\(i\\)) \\(x\equiv x_0\equiv a_i\pmod{n_i}\\) para cada \\(i\\), así que \\(x\\) también resuelve el sistema. Recíprocamente, si \\(x\\) es cualquier solución del sistema, entonces \\(x\equiv x_0\pmod{n_i}\\) para cada \\(i\\) (pues ambos son \\(\equiv a_i\\)), y por la Proposición 5.7 (reducción de congruencias a módulos coprimos), \\(x\equiv x_0\pmod{n_1n_2\cdots n_r}=N\\). \\(\blacksquare\\)

La demostración es **constructiva**: proporciona un algoritmo explícito para hallar la solución, resumido a continuación.

**Algoritmo (Teorema Chino del Resto).**

1. Calcule \\(N=n_1n_2\cdots n_r\\) y, para cada \\(i\\), \\(N_i=N/n_i\\).
2. Para cada \\(i\\), resuelva la congruencia lineal \\(N_ix_i\equiv1\pmod{n_i}\\) (por ejemplo, con el algoritmo de Euclides extendido, Sección 1.4).
3. La solución es \\(x_0\equiv N_1x_1a_1+N_2x_2a_2+\cdots+N_rx_ra_r \pmod N\\).

**Ejemplo 5.28.** Ilustramos el algoritmo, junto con la técnica de **reducción previa** cuando los módulos originales no son coprimos entre sí, resolviendo el sistema
\\[
\begin{cases}
x\equiv5\pmod{24}\\
x\equiv1\pmod{28}\\
x\equiv-4\pmod{15}
\end{cases}
\\]

Como \\(\gcd(24,28)=4\ne1\\), no estamos aún en las hipótesis del Teorema 5.27. Descomponemos cada módulo en potencias de primos (\\(24=8\cdot3\\), \\(28=4\cdot7\\), \\(15=3\cdot5\\)) y usamos la Proposición 5.7 para sustituir cada congruencia por el sistema equivalente módulo cada potencia prima:
\\[
\begin{cases}
x\equiv5\pmod8\\
x\equiv5\pmod3
\end{cases}
\qquad
\begin{cases}
x\equiv1\pmod4\\
x\equiv1\pmod7
\end{cases}
\qquad
\begin{cases}
x\equiv-4\pmod3\\
x\equiv-4\pmod5
\end{cases}
\]

Ahora eliminamos redundancias: \\(x\equiv5\pmod3\\) y \\(x\equiv-4\pmod3\\) son la misma condición, pues \\(5\equiv-4\equiv2\pmod3\\); nos quedamos con una sola. También, \\(x\equiv5\pmod8\\) implica \\(x\equiv5\equiv1\pmod4\\), que coincide con la otra condición módulo \\(4\\); eliminamos la redundante. (Si en algún punto hubiéramos encontrado congruencias **incompatibles** en el mismo módulo, el sistema original no tendría solución.) Queda el sistema reducido, ya con módulos coprimos dos a dos:
\\[
\begin{cases}
x\equiv5\pmod8\\
x\equiv2\pmod3\\
x\equiv1\pmod7\\
x\equiv1\pmod5
\end{cases}
\]

Aplicamos el algoritmo con \\(N=8\cdot3\cdot7\cdot5=840\\):

| \\(i\\) | \\(n_i\\) | \\(a_i\\) | \\(N_i=N/n_i\\) | \\(x_i\\) (inverso de \\(N_i\\) mód \\(n_i\\)) |
|---|---|---|---|---|
| 1 | 8 | 5 | 105 | \\(105\equiv1\pmod8\Rightarrow x_1=1\\) |
| 2 | 3 | 2 | 280 | \\(280\equiv1\pmod3\Rightarrow x_2=1\\) |
| 3 | 7 | 1 | 120 | \\(120\equiv1\pmod7\Rightarrow x_3=1\\) |
| 4 | 5 | 1 | 168 | \\(168\equiv3\pmod5\Rightarrow x_4=2\\) (pues \\(3\cdot2=6\equiv1\\)) |

(En cada renglón, el inverso se verifica o calcula directamente por ser módulos pequeños; para módulos grandes se usaría el algoritmo de Euclides extendido de la Sección 1.4.)

\\[ x_0 \equiv 105\cdot1\cdot5 + 280\cdot1\cdot2+120\cdot1\cdot1+168\cdot2\cdot1 = 525+560+120+336=1541\equiv701\pmod{840}, \\]
pues \\(1541-840=701\\). Por tanto, la solución del sistema original es \\(x\equiv701\pmod{840}\\).

**Ejemplo 5.29 (el problema clásico chino, versión simplificada).** *Un grupo de soldados se forma en filas de 3 y sobran 2; se forma en filas de 5 y sobran 3; se forma en filas de 7 y sobran 2. ¿Cuántos soldados hay, como mínimo (mayor que cero)?* Se busca \\(x\\) con \\(x\equiv2\pmod3\\), \\(x\equiv3\pmod5\\), \\(x\equiv2\pmod7\\). Con \\(N=105\\), \\(N_1=35,N_2=21,N_3=15\\); los inversos son \\(x_1=2\\) (pues \\(35\equiv2\pmod3\\) y \\(2\cdot2=4\equiv1\\)), \\(x_2=1\\) (pues \\(21\equiv1\pmod5\\)), \\(x_3=1\\) (pues \\(15\equiv1\pmod7\\)). Entonces \\(x_0\equiv35\cdot2\cdot2+21\cdot1\cdot3+15\cdot1\cdot2=140+63+30=233\equiv23\pmod{105}\\). La menor solución positiva es \\(23\\) soldados.

El Teorema Chino del Resto tiene aplicaciones que van mucho más allá de acertijos recreativos: es la base de algoritmos eficientes de cómputo modular (por ejemplo, para acelerar operaciones en el criptosistema RSA, calculando módulo \\(p\\) y módulo \\(q\\) por separado en vez de módulo \\(n=pq\\) directamente), y ya se usó, sin demostrarlo explícitamente entonces, en la demostración de la multiplicatividad de la función φ de Euler (Teorema 4.13 de la Unidad 4).
