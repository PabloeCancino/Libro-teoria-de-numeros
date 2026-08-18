# Teoría de Números — Un curso para la Licenciatura en Matemáticas

**Autor:** Pablo Eduardo Cancino Marentes
**Institución:** Universidad Autónoma de Nayarit, Unidad Académica de Ciencias Básicas e Ingenierías, Programa Académico de Licenciatura en Matemáticas.

Este repositorio contiene el texto completo, en formato [mdBook](https://rust-lang.github.io/mdBook/), del curso de *Teoría de Números* (clave CILM318, Plan 2013) de la Licenciatura en Matemáticas de la UAN. El libro cubre las cinco unidades del programa oficial —el anillo de los enteros, primalidad, combinatoria, funciones aritméticas y el anillo de residuos módulo *n*— más una unidad complementaria de temas avanzados (residuos cuadráticos, fracciones continuas, curvas elípticas y criptografía).

## Estructura del libro

- **Unidad 1.** El anillo de los enteros ℤ (axiomas de Peano, inducción, buen orden, divisibilidad, MCD/MCM, algoritmo de Euclides, Bézout, ecuaciones diofánticas).
- **Unidad 2.** Primalidad (números primos, criba de Eratóstenes, Teorema Fundamental de la Aritmética, factorización).
- **Unidad 3.** Elementos de combinatoria (conjuntos finitos, permutaciones, combinaciones, triángulo de Pascal, Fermat y Wilson por combinatoria).
- **Unidad 4.** Funciones aritméticas (σ, d, números perfectos y de Mersenne, φ de Euler, función de Möbius).
- **Unidad 5.** El anillo de residuos módulo n (congruencias, sistemas reducidos, Euler, Fermat, pseudoprimos, congruencias lineales, Teorema Chino del Resto).
- **Unidad 6 (complementaria).** Residuos cuadráticos y reciprocidad cuadrática, fracciones continuas, curvas elípticas y criptografía.
- **Apéndices.** Técnicas de demostración, tabla de primos, bibliografía comentada.

## Cómo compilar el libro localmente

Este libro se construye con [mdBook](https://rust-lang.github.io/mdBook/). Para compilarlo localmente:

```bash
# Instalar mdBook (requiere Rust/Cargo: https://rustup.rs)
cargo install mdbook

# Clonar este repositorio
git clone https://github.com/PabloeCancino/Libro-teoria-de-numeros.git
cd Libro-teoria-de-numeros

# Compilar y ver el libro en el navegador con recarga automática
mdbook serve --open
```

El HTML compilado se genera en la carpeta `book/` (excluida del control de versiones).

## Publicación automática en GitHub Pages

Este repositorio incluye un flujo de trabajo de GitHub Actions (`.github/workflows/deploy.yml`) que reconstruye y publica el libro automáticamente en GitHub Pages con cada `push` a la rama `main`. Para activarlo:

1. En GitHub, ir a **Settings → Pages**.
2. En "Build and deployment", seleccionar **Source: GitHub Actions**.
3. Hacer `push` a `main`; el libro quedará disponible en `https://pabloecancino.github.io/Libro-teoria-de-numeros/`.

## Estado

Versión preliminar en desarrollo activo. Las cinco unidades del temario oficial y la unidad complementaria están redactadas con definiciones, proposiciones/teoremas con demostración completa, ejemplos resueltos y listas de ejercicios; el texto se seguirá revisando y ampliando.

## Licencia

Pendiente de definir por el autor. Mientras tanto, todos los derechos reservados © Pablo Eduardo Cancino Marentes.
