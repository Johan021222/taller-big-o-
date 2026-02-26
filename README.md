# Taller de Complejidad Algorítmica (Big O)

Autor: Johan Cardona  
Asignatura: Complejidad Algorítmica  
Lenguaje: Python  

---

# 1. Módulo 1: Criterio del Límite

Usamos el límite:

lim (n → ∞) f(n) / g(n)

- Si el límite = 0 → f(n) = O(g(n))
- Si el límite = constante positiva → f(n) = Θ(g(n))
- Si el límite = ∞ → f(n) crece más rápido que g(n)

---

## 1.1 Función Cuadrática

Demostrar que:

f(n) = 7n² + 5n + 2

es O(n²).

Tomamos:

g(n) = n²

Calculamos:

lim (n → ∞) (7n² + 5n + 2) / n²

Dividimos cada término entre n²:

= 7 + 5/n + 2/n²

Cuando n → ∞:

= 7

Como el resultado es una constante positiva:

f(n) = Θ(n²)

Por lo tanto:

f(n) = O(n²)

---

## 1.2 Función Logarítmica

Demostrar que:

ln(n) = O(n)

Calculamos:

lim (n → ∞) ln(n) / n

El resultado es:

= 0

Como el límite es 0:

ln(n) = O(n)

---

## 1.3 Factorial vs Exponencial

Comparar:

n!   y   2ⁿ

Calculamos:

lim (n → ∞) n! / 2ⁿ

El resultado es:

= ∞

Entonces:

n! crece más rápido que 2ⁿ  
n! = ω(2ⁿ)

---

## Orden de crecimiento (menor a mayor)

ln(n) < n < n² < 2ⁿ < n!

---

# 2. Módulo 2: Análisis de Algoritmos

## 2.1 Buscador de pares

El algoritmo recorre una lista buscando un número par igual al objetivo.

- Mejor caso: O(1) → lo encuentra en la primera posición.
- Peor caso: O(n) → recorre toda la lista.

Complejidad final: O(n)

---

## 2.2 Salto de índices

El algoritmo duplica el valor de i en cada iteración:

1 → 2 → 4 → 8 → ...

El número de iteraciones es log₂(n).

- Mejor caso: O(1)
- Peor caso: O(log n)

Complejidad final: O(log n)

---

# 3. Módulo 3: Implementación

## 3.1 Intersección de Listas

### Versión Ingenua (O(n²))

```python
def interseccion_ingenua(lista1, lista2):
    resultado = []
    for a in lista1:
        for b in lista2:
            if a == b:
                resultado.append(a)
    return resultado
