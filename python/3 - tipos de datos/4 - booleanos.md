# Booleanos en Python

## Concepto
En Python, los **booleanos** (`bool`) son un tipo de dato lógico que solo puede tener **dos valores**:

- `True` (Verdadero)  
- `False` (Falso)  

Se utilizan principalmente en **condiciones**, **comparaciones** y **estructuras de control** (como `if`, `while`, etc.).  


### Características de los booleanos:
- Son una **subclase de los enteros** (`int`).  
  - `True` se representa como `1`.  
  - `False` se representa como `0`.  
- Se obtienen a partir de **comparaciones**, resultados de funciones lógicas, o conversiones con `bool()`.  
- Permiten controlar el flujo de ejecución en los programas.  


#### Ejemplo básico:
```python
x = True
y = False

print(type(x))   # <class 'bool'>
print(5 > 3)     # True
print(10 == 5)   # False
```



## Operaciones y funciones con Booleanos en Python

Los valores booleanos (`True` y `False`) se combinan y manipulan mediante **operadores lógicos** y la función `bool()`.

---

### 1. Operadores lógicos
Los principales operadores que trabajan con booleanos son:

- **`and` (y lógico):** Devuelve `True` solo si *ambas* condiciones son verdaderas.  
- **`or` (o lógico):** Devuelve `True` si *al menos una* de las condiciones es verdadera.  
- **`not` (no lógico):** Invierte el valor lógico (`True` → `False`, `False` → `True`).  

#### Ejemplo:
```python
a = True
b = False

print(a and b)  # False
print(a or b)   # True
print(not a)    # False
```

### 2. Comparaciones que generan booleanos

Los operadores de comparación devuelven siempre un valor booleano (`True` o `False`):

- `==` : Igual a

- `!=` : Diferente de

- `>` : Mayor que

- `<` : Menor que

- `>=` : Mayor o igual

- `<=` : Menor o igual

Ejemplo:

```python
print(10 == 10)   # True
print(5 != 3)     # True
print(7 > 9)      # False
```

### 3. La función `bool()`

Convierte un valor en su equivalente booleano:

`bool(0)` → `False`

`bool("")` → `False`

`bool(None)` → `False`

**Cualquier otro valor** → `True`

Ejemplo:

```python
print(bool(0))       # False
print(bool(42))      # True
print(bool(""))      # False
print(bool("Hola"))  # True
```

## Tabla de valores booleanos en Python

| Valor evaluado                        | Resultado (`bool(valor)`) |
|---------------------------------------|---------------------------|
| `True`                                | `True`                    |
| `False`                               | `False`                   |
| `1`, `2`, `-5` (cualquier número ≠ 0) | `True`                    |
| `0`                                   | `False`                   |
| `"Hola"` (cualquier string no vacío)  | `True`                    |
| `""` (string vacío)                   | `False`                   |
| `[1, 2, 3]` (lista con elementos)     | `True`                    |
| `[]` (lista vacía)                    | `False`                   |
| `(1, 2)` (tupla con elementos)        | `True`                    |
| `()` (tupla vacía)                    | `False`                   |
| `{"a":1}` (diccionario con datos)     | `True`                    |
| `{}` (diccionario vacío)              | `False`                   |
| `None`                                | `False`                   |

---

## Ejemplos

```python
# 1. Valores booleanos directos
print(bool(True))    # True
print(bool(False))   # False

# 2. Números
print(bool(1))       # True
print(bool(0))       # False
print(bool(-5))      # True

# 3. Cadenas
print(bool("Hola"))  # True (cadena no vacía)
print(bool(""))      # False (cadena vacía)

# 4. Listas
print(bool([1, 2]))  # True (lista con elementos)
print(bool([]))      # False (lista vacía)

# 5. Tuplas
print(bool((1,)))    # True (tupla con elementos)
print(bool(()))      # False (tupla vacía)

# 6. Diccionarios
print(bool({"a": 1})) # True (diccionario con elementos)
print(bool({}))       # False (diccionario vacío)

# 7. None
print(bool(None))    # False
```

---


### Con if

```python
x = 10

if x > 5:   # condición booleana True
    print("x es mayor que 5")
```
- Aquí, la condición `x > 5` devuelve `True`, por lo tanto entra al bloque.


### Con if...else

```python
x = 3

if x % 2 == 0:  # False porque 3 no es par
    print("x es par")
else:
    print("x es impar")
```
- Si la condición es **False**, se ejecuta el bloque del `else`.


### Con if...elif...else

```python
nota = 75

if nota >= 90:
    print("Excelente")
elif nota >= 70:
    print("Aprobado")
else:
    print("Reprobado")
```
- El programa evalúa de arriba hacia abajo hasta encontrar un `True`.


### Con operadores logicos (`and`, `or`, `not`)

```python
edad = 20
tiene_entrada = True

if edad >= 18 and tiene_entrada:
    print("Puedes entrar al evento")
else:
    print("No puedes entrar")
```
- Los booleanos combinados con operadores lógicos permiten condiciones más complejas.


### Con `while` (Bucle controlado por booleano)

```python
contador = 0

while contador < 5:  # mientras sea True
    print("Contador:", contador)
    contador += 1
```
- El bucle sigue ejecutándose mientras la condición sea `True`.


### Con `for` (usando condiciones dentro del ciclo)

```python
numeros = [1, 2, 3, 4, 5]

for n in numeros:
    if n % 2 == 0:   # condición booleana
        print(n, "es par")
    else:
        print(n, "es impar")
```
- Dentro de `for` también podemos usar booleanos para decidir acciones.

**Los booleanos son la base de todas las decisiones en programación. Se usan tanto en estructuras condicionales (`if`, `elif`, `else`) como en bucles (`while`, `for`) para controlar el flujo del programa.**

# Tabla: Uso de Booleanos en Estructuras de Control

| Estructura      | Ejemplo de código                              | Descripción / Resultado                       |
|-----------------|------------------------------------------------|-----------------------------------------------|
| `if`            | if x > 5: print("x > 5")                      | Ejecuta el bloque solo si la condición es True |
| `if...else`     | if x % 2 == 0: print("Par") else: print("Impar") | Ejecuta el bloque del `if` si True, sino `else` |
| `if...elif...else` | if nota >= 90: print("Excelente")<br>elif nota >= 70: print("Aprobado")<br>else: print("Reprobado") | Evalúa varias condiciones secuenciales, ejecuta la primera True |
| `while`         | contador = 0<br>while contador < 5:<br> print(contador)<br> contador += 1 | Se repite mientras la condición booleana sea True |
| `for` + `if`    | for n in [1,2,3]:<br> if n%2==0: print("Par")<br> else: print("Impar") | Dentro de un bucle `for`, se usan booleanos para decidir acciones |
| Operadores lógicos | edad = 20<br>tiene_entrada = True<br>if edad>=18 and tiene_entrada:<br> print("Puedes entrar") | Combina condiciones booleanas para tomar decisiones más complejas |
