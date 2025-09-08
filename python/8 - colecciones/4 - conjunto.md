# Conjuntos en Python

## Concepto

Los **conjuntos** (o `set`) en Python son colecciones **no ordenadas** de elementos **únicos**.  
- **No ordenados:** no mantienen un orden específico de los elementos.  
- **Elementos únicos:** no permiten duplicados.  
- **Mutables:** se pueden agregar o eliminar elementos.  
- Se definen usando **llaves `{ }`** o la función `set()`.

---

## Crear conjuntos

```python
# Conjunto vacío
conjunto_vacio = set()  # No usar {} porque crea un diccionario

# Conjunto con elementos
numeros = {1, 2, 3, 4, 5}

# Conjunto de cadenas
frutas = {"manzana", "banana", "cereza"}

# Conjunto a partir de una lista (elimina duplicados automáticamente)
lista = [1, 2, 2, 3, 4, 4, 5]
conjunto_numeros = set(lista)  # {1, 2, 3, 4, 5}
```

## Acceder a elementos

- **No se puede acceder por índice** porque los conjuntos no están ordenados.

- Se pueden recorrer con un bucle `for`:

```python
for fruta in frutas:
    print(fruta)
```

## Métodos útiles en conjuntos (`set`)

| Método                              | Descripción                                             | Ejemplo                    | Resultado            |           |
| ----------------------------------- | ------------------------------------------------------- | -------------------------- | -------------------- | --------- |
| `add(elem)`                         | Agrega un elemento al conjunto.                         | `a = {1,2}; a.add(3)`      | `{1, 2, 3}`          |           |
| `remove(elem)`                      | Elimina un elemento. Lanza error si no existe.        | `a = {1,2}; a.remove(2)`   | `{1}`                |           |
| `discard(elem)`                     | Elimina un elemento, pero **no da error** si no existe. | `a = {1,2}; a.discard(3)`  | `{1, 2}`             |           |
| `pop()`                             | Elimina y devuelve un elemento aleatorio.               | `a = {1,2,3}; x = a.pop()` | `x → 1 (depende)`    |           |
| `clear()`                           | Elimina todos los elementos.                            | `a = {1,2}; a.clear()`     | `set()`              |           |
| `union(b)` / \`a                    | b\`                                                     | Unión de dos conjuntos.    | `{1,2}.union({2,3})` | `{1,2,3}` |
| `intersection(b)` / `a & b`         | Intersección: elementos comunes.                        | `{1,2,3} & {2,3,4}`        | `{2,3}`              |           |
| `difference(b)` / `a - b`           | Diferencia: elementos en `a` pero no en `b`.            | `{1,2,3} - {2}`            | `{1,3}`              |           |
| `symmetric_difference(b)` / `a ^ b` | Elementos que están en uno u otro, pero no en ambos.    | `{1,2,3} ^ {2,3,4}`        | `{1,4}`              |           |
| `issubset(b)`                       | Verifica si `a` está contenido en `b`.                  | `{1,2} <= {1,2,3}`         | `True`               |           |
| `issuperset(b)`                     | Verifica si `a` contiene a `b`.                         | `{1,2,3} >= {2}`           | `True`               |           |
| `isdisjoint(b)`                     | Verifica si no tienen elementos en común.               | `{1,2}.isdisjoint({3,4})`  | `True`               |           |
| `copy()`                            | Devuelve una copia del conjunto.                        | `a = {1,2}; b = a.copy()`  | `b → {1,2}`          |           |

## Agregar y eliminar elementos

- **add()** → agrega un elemento

```python
frutas.add("naranja")
print(frutas)
```

- **update()** → agrega múltiples elementos de otra colección

```python
frutas.update(["mango", "sandía"])
print(frutas)
```

- **remove()** → elimina un elemento (genera error si no existe)

```python
frutas.remove("banana")
print(frutas)
```

- **discard()** → elimina un elemento (no genera error si no existe)

```python
frutas.discard("kiwi")
print(frutas)
```

- **pop()** → elimina y devuelve un elemento aleatorio

```python
elem = frutas.pop()
print(elem)
```

- **clear()** → elimina todos los elementos

```python
frutas.clear()
print(frutas)
```

## Operaciones con conjuntos

1. Unión (`|` o `union()`)

- **Qué hace**: devuelve un nuevo conjunto con **todos los elementos que están en `a` o en `b`** (sin duplicados).

```python
a = {1, 2, 3}
b = {3, 4, 5}
union = a | b  # {1, 2, 3, 4, 5}
# o
union = a.union(b)
print(union)
```

2. Intersección (`&` o `intersection()`)

- **Qué hace**: devuelve un nuevo conjunto con **solo los elementos que están en ambos conjuntos**.

```python
a = {1, 2, 3}
b = {3, 4, 5}
interseccion = a & b  # {3}
# o
interseccion = a.intersection(b)
print(interseccion)
```

3. Diferencia (`-` o `difference()`)

- **Qué hace**: devuelve un conjunto con **los elementos que están en `a` pero no en `b`**.

```python
a = {1, 2, 3}
b = {3, 4, 5}
diferencia = a - b  # {1, 2} -> elementos en a que no están en b
print(diferencia)
```

4. Diferencia simétrica (`^` o `symmetric_difference()`)

- **Qué hace**: devuelve un conjunto con **los elementos que están en `a` o en `b` pero no en ambos**.
  
```python
a = {1, 2, 3}
b = {3, 4, 5}
simetrica = a ^ b  # {1, 2, 4, 5} -> elementos en a o b pero no en ambos
print(simetrica)
```

5. Subconjunto (`issubset()`)

- **Qué hace**: comprueba si **todos los elementos de `a` están en `b`**.

```python
a = {1, 2, 3}
b = {3, 4, 5}
resultado = a.issubset(b)  # False
print(resultado)
```

6. Superconjunto (issuperset())

- **Qué hace**: comprueba si **todos los elementos de `b` están en `a`**.

```python
a = {1, 2, 3}
b = {3, 4, 5}
resultado = a.issuperset(b)  # False
print(resultado)
```

7. Disjuntos (isdisjoint())

- **Qué hace**: comprueba si **`a` y `b` no tienen elementos en común**.

```python
a = {1, 2, 3}
b = {3, 4, 5}
resultado = a.isdisjoint(b)  # False (porque ambos tienen el 3)
print(resultado)
```

## Conjuntos anidados y operaciones avanzadas

- Los conjuntos no pueden contener **listas** ni otros conjuntos mutables, pero sí **tuplas**:

```python
c = {(1, 2), (3, 4)}
print(c)
```

- Operaciones avanzadas como unión, intersección y diferencia se pueden combinar:

```python
x = {1, 2, 3, 4}
y = {3, 4, 5, 6}
resultado = (x | y) - {2, 5}  # {1, 3, 4, 6}
print(resultado)
```

## Consejos prácticos

1. Usar conjuntos cuando **necesites elementos únicos**.

2. Para **eliminar duplicados de una lista**, convertir a `set()` es muy eficiente.

3. Usar métodos como `union`, `intersection` y `difference` para **operaciones matemáticas con conjuntos**.

4. Evitar tratar de acceder por índice; los conjuntos **no son ordenados**.

5. Pueden combinarse con bucles para recorrer elementos o realizar filtrados.

## Resumen

- Los conjuntos son **colecciones no ordenadas y mutables** de elementos únicos.

- No permiten duplicados y no tienen índice.

- Son ideales para **operaciones de teoría de conjuntos**, eliminar duplicados y pruebas de pertenencia.

- Tienen métodos para **agregar, eliminar y combinar elementos** eficientemente.
