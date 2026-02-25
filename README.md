
Para cada ejercicio utilizamos la definición basada en el límite:

\[
\lim_{n \to \infty} \frac{f(n)}{g(n)}
\]

- Si el límite es 0 → \( f(n) = O(g(n)) \)
- Si el límite es una constante positiva \( c \) → \( f(n) = \Theta(g(n)) \)

---

##  Ejercicio 1.1 (Nivel Básico)

### Enunciado
Demostrar que:

\[
f(n) = 7n^2 + 5n + 2
\]

es de orden \( O(n^2) \).

---

##  Solución usando el Criterio del Límite

Para demostrar que:

\[
f(n) = 7n^2 + 5n + 2 \in O(n^2)
\]

Tomamos como función de comparación:

\[
g(n) = n^2
\]

Aplicamos el límite:

\[
\lim_{n \to \infty} \frac{7n^2 + 5n + 2}{n^2}
\]

Dividimos cada término por \( n^2 \):

\[
= \lim_{n \to \infty} \left( 7 + \frac{5}{n} + \frac{2}{n^2} \right)
\]

Ahora evaluamos el límite:

- \( \frac{5}{n} \to 0 \)
- \( \frac{2}{n^2} \to 0 \)

Entonces:

\[
\lim_{n \to \infty} \left( 7 + 0 + 0 \right) = 7
\]

---
