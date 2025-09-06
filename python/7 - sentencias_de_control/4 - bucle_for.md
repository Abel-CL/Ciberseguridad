# Bucle `for` en Python

## Concepto

El bucle **`for`** en Python se utiliza para **iterar sobre una secuencia** (listas, tuplas, cadenas, rangos, diccionarios, etc.).
Es ideal cuando **se conoce de antemano el número de iteraciones** o se quiere recorrer elementos de una colección.

- En cada iteración, el bucle toma un elemento de la secuencia y lo asigna a una variable temporal.
- Después ejecuta el bloque de código asociado.

---

## Sintaxis básica

```python
for variable in secuencia:
    # Bloque de código a ejecutar por cada elemento
```

- `variable`: recibe cada elemento de la secuencia en cada iteración.

- `secuencia`: puede ser cualquier objeto iterable (lista, tupla, cadena, rango, diccionario).

## Ejemplos básicos

**1. Iterar sobre una lista**

```python
frutas = ["manzana", "banana", "cereza"]

for fruta in frutas:
    print(f"Me gusta la {fruta}")
```

**2. Iterar sobre una cadena**

```python
for letra in "Python":
    print(letra)
```

**3. Iterar usando `range()`**

```python
for i in range(5):  # 0,1,2,3,4
    print(f"Número: {i}")
```

- `range(inicio, fin, paso)` → permite definir inicio, fin (no incluido) y paso.

```python
for i in range(1, 10, 2):
    print(i)
```

## Bucle `for` con `else`

- Se puede agregar un bloque `else` que se ejecuta **cuando el bucle termina normalmente**, pero **no se ejecuta si se rompe con `break`.**

```python
for i in range(3):
    print(f"Iteración: {i}")
else:
    print("Bucle terminado")
```

## Control de flujo dentro del `for`

- `break` → termina el bucle inmediatamente.

- `continue` → salta a la siguiente iteración sin ejecutar el resto del bloque.

- `pass` → marcador de posición, no hace nada.

**Ejemplo con `break` y `continue`**

```python
for i in range(10):
    if i == 3:
        continue  # Salta la iteración donde i==3
    if i == 8:
        break     # Termina el bucle cuando i==8
    print(i)
```

## Bucles anidados `for`

- Se pueden colocar **bucles dentro de bucles** para recorrer matrices o combinaciones.

```python
for i in range(1, 4):
    for j in range(1, 3):
        print(f"i={i}, j={j}")
```

## Iterar sobre diccionarios

**Iterar sobre `claves`**

```python
persona = {"nombre": "Pedro", "edad": 25, "ciudad": "La Paz"}
for clave in persona:
  print(f"{clave} : {persona[clave]")
```

**Iterar sobre items (clave, valor)**

```python
persona = {"nombre": "Pedro", "edad": 25, "ciudad": "La Paz"}
for clave, valor in persona.items():
    print(clave, ":", valor)
```

## Consejos prácticos

1. Para **numerar iteraciones**, usar `range()`.

```python
# Contar del 1 al 5
for i in range(1, 6):
    print(f"Iteración número: {i}")
```

2. **Evitar modificar la secuencia dentro del bucle**, puede causar errores inesperados.

```python
frutas = ["manzana", "banana", "cereza"]

# Evita hacer esto:
for fruta in frutas:
    frutas.remove(fruta)  # Puede causar errores o saltar elementos

print(frutas)

# Forma correcta: crear una copia si necesitas modificar
for fruta in frutas[:]:  # Copia de la lista
    if fruta == "banana":
        frutas.remove(fruta)

print(frutas)
```

3. **Combinar con `break` y `continue`** para controlar el flujo.

```python
for i in range(10):
    if i == 3:
        continue  # Salta la iteración donde i == 3
    if i == 7:
        break     # Termina el bucle cuando i == 7
    print(i)
```

4. Se pueden usar **bucles anidados** para estructuras complejas.

```python
for fila in range(1, 4):
    for columna in range(1, 4):
        print(f"Fila {fila}, Columna {columna}")
```

5. Siempre mantener **indentación consistente** (4 espacios por nivel).

```python
for i in range(3):
    print("Correcto")  # 4 espacios de indentación

# Incorrecto: mezcla de espacios y tabulaciones
for i in range(3):
 print("Incorrecto")  # Puede causar errores de indentación
```

## Resumen

- `for` recorre elementos de una **secuencia o iterable**.

Útil cuando **conocemos la cantidad de iteraciones** o queremos recorrer una colección.

Compatible con `break`, `continue` y `else` para control **completo del flujo**.

Permite **bucles anidados** y trabajar con **listas, cadenas, tuplas, diccionarios, rangos**.
