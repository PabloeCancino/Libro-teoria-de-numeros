# Prefacio

La teoría de números es la rama de las matemáticas puras que estudia las propiedades de los números, centrándose de manera particular en el conjunto de los enteros, aunque en su forma más general estudia las propiedades de los elementos de dominios enteros y los problemas que de ellos se derivan. Es, a la vez, una de las áreas más accesibles de la matemática —muchos de sus enunciados pueden formularse con una preparación elemental— y una de las más profundas, pues aloja algunos de los problemas abiertos más antiguos de toda la disciplina.

Este libro nace del curso-taller *Teoría de Números* que se imparte en el Programa Académico de Licenciatura en Matemáticas (PALMAT) de la Universidad Autónoma de Nayarit, y sigue de cerca el programa vigente del **Plan de Estudios 2024**. El objetivo del curso, y por tanto de este texto, es que el estudiante sea capaz de manejar los métodos analíticos y algebraicos elementales de la teoría de números: divisibilidad, primalidad, funciones aritméticas y congruencias, con énfasis particular en el dominio de las demostraciones rigurosas —inducción, buen orden, algoritmo de Euclides, Bézout, el Teorema Fundamental de la Aritmética, y el Teorema Chino del Resto, entre otros.

## Organización del libro

El texto sigue las cinco unidades del programa oficial:

1. **El anillo de los enteros ℤ.** Se construyen desde los axiomas de Peano el principio de inducción y el buen orden, y sobre esa base la divisibilidad, el máximo común divisor, el mínimo común múltiplo, el algoritmo de Euclides, el teorema de Bézout y las ecuaciones diofánticas lineales y cuadráticas.
2. **Primalidad.** Números primos, la criba de Eratóstenes, el Teorema Fundamental de la Aritmética y métodos elementales de factorización.
3. **Elementos de combinatoria.** Conjuntos finitos, combinaciones, permutaciones y el triángulo de Pascal, con sus aplicaciones a la teoría de números —en particular, demostraciones combinatorias de los teoremas de Fermat y Wilson.
4. **Funciones aritméticas.** Las funciones σ, d, la función φ de Euler y la función de Möbius, junto con los números perfectos y de Mersenne.
5. **El anillo de residuos módulo n.** Congruencias, sistemas reducidos de residuos, los teoremas de Euler y Fermat, pseudoprimos, unidades módulo *n*, congruencias lineales y el Teorema Chino del Resto.

A estas cinco unidades se añade una **Unidad 6, complementaria**, que no forma parte del programa mínimo pero que aprovecha la rica bibliografía disponible sobre el tema para ofrecer una puerta de entrada a temas más avanzados: residuos cuadráticos y la ley de reciprocidad cuadrática de Gauss, fracciones continuas, y una introducción a las curvas elípticas y sus aplicaciones criptográficas. Esta unidad es material de enriquecimiento, pensado para estudiantes que deseen profundizar más allá del temario mínimo, o como puente hacia cursos posteriores de teoría analítica o algebraica de números.

Cada sección incluye ejemplos resueltos completamente, y cada unidad cierra con una lista de ejercicios graduada en dificultad. Los apéndices recogen un breve resumen de técnicas de demostración, una tabla de referencia de números primos, y una bibliografía comentada.

## Aplicación interactiva y simuladores computacionales

Para enriquecer el aprendizaje activo y facilitar la experimentación numérica, este texto está articulado con la aplicación web e interactiva **Teoría de Números UAN** (desarrollada bajo la norma técnica institucional *NTE-UAN-APK-001 v1.3*).

La aplicación incluye simuladores dedicados para cada unidad del libro:
- **Algoritmo de Euclides y Bézout:** Cálculo paso a paso de divisiones sucesivas y obtención formal de la combinación lineal \\(ax + by = \operatorname{mcd}(a,b)\\).
- **Criba de Eratóstenes:** Animación dinámica del proceso de filtrado de números compuestos y cómputo de la función contadora de primos \\(\pi(N)\\).
- **Resolutor de Ecuaciones Diofánticas:** Determinación de solubilidad y cálculo de la familia paramétrica general de soluciones enteras.
- **Calculadora de Funciones Aritméticas:** Descomposición en factores primos y evaluación exacta de \\(d(n)\\), \\(\sigma(n)\\), \\(\varphi(n)\\) y \\(\mu(n)\\).
- **Reloj Modular y Sistemas de Residuos:** Rueda interactiva para visualización de órbitas, cálculo de inversos modulares y unidades coprimas en \\(\mathbb{Z}/n\mathbb{Z}\\).
- **Teorema Chino del Resto (CRT):** Resolución analítica detallada de sistemas de congruencias lineales simultáneas.
- **Simulador de Demostraciones:** Recorrido interactivo y justificado de demostraciones formales clásicas.
- **Centro de Evaluaciones:** Banco de reactivos formativos por unidad y examen global integrador con retroalimentación KaTeX.

La aplicación está disponible en línea en [https://PabloeCancino.github.io/uan-apk-teoria-de-numeros/](https://PabloeCancino.github.io/uan-apk-teoria-de-numeros/) y su código fuente en el repositorio [uan-apk-teoria-de-numeros](https://github.com/PabloeCancino/uan-apk-teoria-de-numeros).

## A quién está dirigido

El texto está escrito para estudiantes de licenciatura en matemáticas que ya han cursado álgebra básica y tienen familiaridad con el método axiomático y la demostración formal. No se requiere análisis matemático, salvo en pasajes puntuales de la Unidad 6 donde se señala explícitamente.

## Agradecimientos

Este material se apoya en la tradición de textos clásicos de teoría de números —Niven y Zuckerman, Burton, Apostol, Hardy y Wright, Vinogradov, Koblitz, Gauss, entre otros— y en el trabajo previo del autor en las notas de clase, presentaciones y bancos de ejercicios desarrollados a lo largo de varias generaciones del curso de Teoría de Números en la UAN.
