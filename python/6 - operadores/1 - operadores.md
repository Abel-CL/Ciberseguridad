# Operadores en Python

Los **operadores** en Python son símbolos especiales que permiten realizar operaciones sobre **valores y variables**.
Se utilizan en expresiones matemáticas, lógicas y de manipulación de datos.

---

## 1. Operadores Aritméticos

Se usan para realizar operaciones matemáticas.

| Operador | Descripción              | Ejemplo | Resultado |
|----------|--------------------------|---------|-----------|
| `+`      | Suma                     | `5 + 3` | `8`       |
| `-`      | Resta                    | `5 - 3` | `2`       |
| `*`      | Multiplicación           | `5 * 3` | `15`      |
| `/`      | División (float)         | `5 / 2` | `2.5`     |
| `//`     | División entera          | `5 // 2`| `2`       |
| `%`      | Módulo (residuo)         | `5 % 2` | `1`       |
| `**`     | Exponenciación           | `2 ** 3`| `8`       |

**Ejemplo en código:**

```python
```
```python
a = 10
b = 3
print(a + b)   # 13
print(a - b)   # 7
print(a * b)   # 30
print(a / b)   # 3.333...
print(a // b)  # 3
print(a % b)   # 1
print(a ** b)  # 1000
```

## 2. Operadores de Comparación

Sirven para comparar valores y devuelven un booleano (True o False).

| Operador | Descripción       | Ejemplo  | Resultado |
| -------- | ----------------- | -------- | --------- |
| `==`     | Igual a           | `5 == 3` | `False`   |
| `!=`     | Distinto de       | `5 != 3` | `True`    |
| `>`      | Mayor que         | `5 > 3`  | `True`    |
| `<`      | Menor que         | `5 < 3`  | `False`   |
| `>=`     | Mayor o igual que | `5 >= 3` | `True`    |
| `<=`     | Menor o igual que | `5 <= 3` | `False`   |

**Ejemplo en código:**

```python
x = 7
y = 10
print(x == y)  # False
print(x != y)  # True
print(x > y)   # False
print(x < y)   # True
print(x >= 7)  # True
print(y <= 10) # True
```

## 3. Operadores Lógicos

Se usan para combinar expresiones booleanas.

| Operador | Descripción                               | Ejemplo             | Resultado |
| -------- | ----------------------------------------- | ------------------- | --------- |
| `and`    | Devuelve `True` si ambas son `True`       | `(5 > 2 and 3 > 1)` | `True`    |
| `or`     | Devuelve `True` si al menos una es `True` | `(5 > 10 or 3 > 1)` | `True`    |
| `not`    | Invierte el valor lógico                  | `not (5 > 2)`       | `False`   |

**Ejemplo en código:**

```python
```
```python
a = True
b = False
print(a and b)  # False
print(a or b)   # True
print(not a)    # False
```

## 4. Operadores de Asignación

Sirven para asignar valores a variables, con posibilidad de realizar operaciones en el mismo paso.

| Operador | Ejemplo   | Equivalente a |
| -------- | --------- | ------------- |
| `=`      | `x = 5`   | `x = 5`       |
| `+=`     | `x += 3`  | `x = x + 3`   |
| `-=`     | `x -= 3`  | `x = x - 3`   |
| `*=`     | `x *= 3`  | `x = x * 3`   |
| `/=`     | `x /= 3`  | `x = x / 3`   |
| `//=`    | `x //= 3` | `x = x // 3`  |
| `%=`     | `x %= 3`  | `x = x % 3`   |
| `**=`    | `x **= 3` | `x = x ** 3`  |

**Ejemplo en código:**

```python
x = 10
x += 5   # x = 15
x *= 2   # x = 30
print(x)
```

## 5. Operadores de Pertenencia

Verifican si un elemento está o no dentro de una secuencia (lista, cadena, tupla).

| Operador | Descripción                         | Ejemplo               | Resultado |
| -------- | ----------------------------------- | --------------------- | --------- |
| `in`     | Devuelve `True` si el valor está    | `"a" in "Python"`     | `False`   |
| `not in` | Devuelve `True` si el valor no está | `"z" not in "Python"` | `True`    |

**Ejemplo en código:**

```python
texto = "Hola mundo"
print("Hola" in texto)      # True
print("Python" not in texto) # True
```

## 6. Operadores de Identidad

Comprueban si dos objetos ocupan la misma posición en memoria.

| Operador | Descripción                            | Ejemplo      |
| -------- | -------------------------------------- | ------------ |
| `is`     | Devuelve `True` si son el mismo objeto | `x is y`     |
| `is not` | Devuelve `True` si no lo son           | `x is not y` |

**Ejemplo en código:**

```python
a = [1, 2, 3]
b = a
c = [1, 2, 3]

print(a is b)      # True (misma referencia)
print(a is c)      # False (objetos diferentes)
print(a == c)      # True (valores iguales)
```

**Resumen**

- Aritméticos → operaciones matemáticas.

- Comparación → devuelven True/False.

- Lógicos → combinan condiciones booleanas.

- Asignación → asignan y modifican valores en variables.

- Pertenencia → verifican si un valor está en una secuencia.

- Identidad → comparan referencias de objetos en memoria.
