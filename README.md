#
---

Módulo 1: Criterio del Límite

Usamos:

\[
\lim_{n \to \infty} \frac{f(n)}{g(n)}
\]

- Si el límite = 0 →  f(n) = O(g(n))
- Si el límite = c (constante positiva) → f(n) = Θ(g(n))
- Si el límite = ∞ → f(n) crece más rápido que g(n)

---

 Ejercicio 1.1

Demostrar que:

\[
f(n) = 7n^2 + 5n + 2
\]

es \( O(n^2) \).

### Solución

Tomamos:

\[
g(n) = n^2
\]

\[
\lim_{n \to \infty} \frac{7n^2 + 5n + 2}{n^2}
\]

Dividiendo por \( n^2 \):

\[
= \lim_{n \to \infty} \left( 7 + \frac{5}{n} + \frac{2}{n^2} \right)
\]

Cuando \( n \to \infty \):

\[
= 7
\]

Como el resultado es una constante positiva:

\[
f(n) = \Theta(n^2)
\]

Por lo tanto:

\[
f(n) = O(n^2)
\]

---

# Ejercicio 1.2

Demostrar que:

\[
\ln(n) = O(n)
\]

### Solución

Tomamos:

\[
\lim_{n \to \infty} \frac{\ln(n)}{n}
\]

Sabemos que el logaritmo crece más lento que la función lineal, entonces:

\[
= 0
\]

Como el límite es 0:

\[
\ln(n) = O(n)
\]

---

## Ejercicio 1.3

Comparar:

\[
f(n) = n!
\]

y

\[
g(n) = 2^n
\]

### Solución

Analizamos:

\[
\lim_{n \to \infty} \frac{n!}{2^n}
\]

El factorial multiplica números cada vez más grandes, mientras que \(2^n\) siempre multiplica por 2.

El límite es:

\[
= \infty
\]

Entonces:

\[
n! \text{ crece más rápido que } 2^n
\]

Es decir:

\[
n! = \omega(2^n)
\]

---

#  Orden de crecimiento (de menor a mayor)

\[
\ln(n) < n < n^2 < 2^n < n!
\]

---

#  Conclusión

Mediante el criterio del límite se demuestra que:

- \(7n^2 + 5n + 2\) es de orden cuadrático.
- El logaritmo crece más lento que la función lineal.
- El factorial crece más rápido que la función exponencial.





Módulo 2: Análisis de Algoritmos

##  Ejercicio 2.1 – Buscador de pares

El algoritmo recorre una lista buscando un número par igual al objetivo.

- Mejor caso: O(1) (lo encuentra en la primera posición)
- Peor caso: O(n) (recorre toda la lista)

Complejidad final: O(n)

---

##  Ejercicio 2.2 – Salto de índices

El algoritmo duplica el valor de i en cada iteración:

1 → 2 → 4 → 8 → ...

El número de iteraciones es log₂(n).

- Mejor caso: O(1)
- Peor caso: O(log n)

Complejidad final: O(log n)

---

#  Orden de crecimiento (menor a mayor)

ln(n) < n < n² < 2ⁿ < n!

---

#  Conclusión

- El término de mayor grado domina el crecimiento.
- Los logaritmos crecen más lento que las funciones lineales.
- Los factoriales crecen más rápido que las exponenciales.
- Recorrer una lista es O(n).
- Duplicar o dividir el problema produce O(log n).

---

#  Módulo 3: Implementación (Programación)

En este módulo se implementan soluciones en Python cumpliendo las restricciones de eficiencia solicitadas.

---

## Ejercicio 3.1 – Intersección de Listas

Se debe crear una función que retorne los elementos comunes entre dos listas.

---

###  Versión Ingenua (O(n²))

```python
def interseccion_ingenua(lista1, lista2):
    resultado = []
    for a in lista1:
        for b in lista2:
            if a == b:
                resultado.append(a)
    return resultado

---

**Autor:** Johan Cardona  
**Asignatura:** Complejidad Algorítmica  
**Lenguaje:** Python  
**Entrega:** Repositorio GitHub



