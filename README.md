# Teoría de Números — Un curso para la Licenciatura en Matemáticas

[![Libro en Línea](https://img.shields.io/badge/Libro-mdBook%20en%20Línea-orange?style=for-the-badge&logo=mdbook)](https://pabloecancino.github.io/Libro-teoria-de-numeros/)
[![Ver Web App Interactiva](https://img.shields.io/badge/Web%20App-Simuladores%20Interactivas-blue?style=for-the-badge&logo=githubpages)](https://PabloeCancino.github.io/uan-apk-teoria-de-numeros/)
[![Descargar APK Android](https://img.shields.io/badge/Descargar-APK%20Android-green?style=for-the-badge&logo=android)](https://github.com/PabloeCancino/uan-apk-teoria-de-numeros/releases/download/v1.0.0/TeoriaNumeros.apk)
[![Norma](https://img.shields.io/badge/Norma-NTE--UAN--APK--001%20v1.3-purple?style=for-the-badge)](https://github.com/PabloeCancino/uan-apk-plantilla-arquetipo)

**Autor:** Dr. Pablo Eduardo Cancino Marentes  
**Institución:** Universidad Autónoma de Nayarit, Unidad Académica de Ciencias Básicas e Ingenierías, Programa Académico de Licenciatura en Matemáticas (PALMAT).  

Este repositorio contiene el texto completo, en formato [mdBook](https://rust-lang.github.io/mdBook/), del curso de *Teoría de Números* (clave CBIMAT-256, Plan de Estudios 2024) de la Licenciatura en Matemáticas de la UAN. El libro cubre las cinco unidades del programa oficial —el anillo de los enteros, primalidad, combinatoria, funciones aritméticas y el anillo de residuos módulo *n*— más una unidad complementaria de temas avanzados (residuos cuadráticos, fracciones continuas, curvas elípticas y criptografía).

## 📖 Libro en formato mdBook

Disponible para lectura en línea en:  
👉 **[https://pabloecancino.github.io/Libro-teoria-de-numeros/](https://pabloecancino.github.io/Libro-teoria-de-numeros/)**

## 📱 Aplicación Interactiva y Simuladores (APK / Web App)

Este libro de texto está vinculado formal y didácticamente con la aplicación interactiva de modelado y simulación computacional de la UAN:

- **Web App en vivo:** [https://PabloeCancino.github.io/uan-apk-teoria-de-numeros/](https://PabloeCancino.github.io/uan-apk-teoria-de-numeros/)
- **Repositorio de la App:** [uan-apk-teoria-de-numeros](https://github.com/PabloeCancino/uan-apk-teoria-de-numeros)
- **Simuladores disponibles:** Algoritmo de Euclides y Bézout paso a paso, Criba de Eratóstenes interactiva, Resolutor de Ecuaciones Diofánticas, Calculadora de Funciones Aritméticas ($d, \sigma, \varphi, \mu$), Reloj y Aritmética Modular, Teorema Chino del Residuo (CRT), Triángulo de Pascal y Simulador de Demostraciones Formales paso a paso.

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
3. El libro se despliega automáticamente en `https://pabloecancino.github.io/Libro-teoria-de-numeros/`.

## Estado

Versión preliminar en desarrollo activo. Las cinco unidades del temario oficial y la unidad complementaria están redactadas con definiciones, proposiciones/teoremas con demostración completa, ejemplos resueltos y listas de ejercicios; el texto se seguirá revisando y ampliando.

## Licencia

Este texto se publica bajo **[Creative Commons Atribución-NoComercial-SinDerivadas 4.0 Internacional (CC BY-NC-ND 4.0)](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.es)**. Ver [LICENSE.md](LICENSE.md).

En resumen: puedes leer, descargar y compartir el libro completo citando la autoría, siempre que no lo modifiques ni le des uso comercial. Para permisos adicionales (traducción, adaptación, uso comercial), contacta al autor.

## Cómo citar

> Cancino Marentes, P. E. (2026). *Teoría de Números: Un curso para la Licenciatura en Matemáticas*. Manuscrito publicado como texto abierto en GitHub. Disponible en: https://pabloecancino.github.io/Libro-teoria-de-numeros/

## Contacto

Dr. Pablo Eduardo Cancino Marentes — pabloe.cancino@uan.edu.mx
