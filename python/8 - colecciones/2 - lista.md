
# Listas en Python

## Concepto

Las **listas** en Python son colecciones **ordenadas y mutables** de elementos, que pueden ser de **cualquier tipo** (números, cadenas, booleanos, otras listas, etc.).
- **Ordenadas:** mantienen el orden de inserción.
- **Mutables:** se pueden modificar (agregar, eliminar o cambiar elementos).
- Se definen usando **corchetes `[ ]`** y los elementos se separan con comas.

---

## Crear listas

```python
# Lista vacía
mi_lista = []

# Lista de números
numeros = [1, 2, 3, 4, 5]

# Lista de cadenas
frutas = ["manzana", "banana", "cereza"]

# Lista mixta
mixta = [1, "Python", True, 3.14]

# Lista de listas (anidada)
matriz = [[1, 2], [3, 4], [5, 6]]
```

## Acceder a elementos

- Por índice (empieza en 0)

```python
frutas = ["manzana", "banana", "cereza"]
print(frutas[0])  # manzana
print(frutas[2])  # cereza
```

- Índices negativos (desde el final)

```python
frutas = ["manzana", "banana", "cereza"]
print(frutas[-1])  # cereza
print(frutas[-2])  # banana
```

## modificar elementos

```python
frutas = ["manzana", "banana", "cereza"]
frutas[1] = "kiwi"
print(frutas)  # ['manzana', 'kiwi', 'cereza']
```

## Agregar elementos

- append() → agrega al final

```python
frutas = ["manzana", "banana", "cereza"]
frutas.append("naranja")
```

- insert() → agrega en un índice específico

```python
frutas = ["manzana", "banana", "cereza"]
frutas.insert(1, "pera")
```

- extend() → agrega otra lista completa

```python
frutas = ["manzana", "banana", "cereza"]
frutas.extend(["mango", "sandía"])
```

## Eliminar elementos

- del → elimina por índice

```python
frutas = ["manzana", "banana", "cereza"]
del frutas[0]
```

- pop() → elimina y devuelve el elemento (último o índice específico)

```python
frutas = ["manzana", "banana", "cereza"]
frutas.pop()       # elimina último
frutas.pop(1)      # elimina el elemento en índice 1
```

- remove() → elimina por valor

```python
frutas = ["manzana", "banana", "cereza"]
frutas.remove("cereza")
```

- clear() → elimina todos los elementos

```python
frutas = ["manzana", "banana", "cereza"]
frutas.clear()
```

## Slicing (rebanadas)

```python
numeros = [1, 2, 3, 4, 5, 6]
print(numeros[1:4])   # [2, 3, 4]
print(numeros[:3])    # [1, 2, 3]
print(numeros[3:])    # [4, 5, 6]
print(numeros[::2])   # [1, 3, 5] -> salto de 2
print(numeros[::-1])  # [6, 5, 4, 3, 2, 1] -> invertir lista
```

## Operaciones con listas

- Concatenar listas

```python
a = [1, 2]
b = [3, 4]
c = a + b  # [1, 2, 3, 4]
print(c)
```

- Repetir elementos

```python
d = [0] * 3  # [0, 0, 0]
print(d)
```

- Verificar existencia

```python
5 in [1, 2, 3, 4, 5]  # True
```

## Recorrer lista

```python
frutas = ["manzana", "banana", "cereza"]

# Usando for
for fruta in frutas:
    print(fruta)

# Usando while
i = 0
while i < len(frutas):
    print(frutas[i])
    i += 1

# Usando enumerate para índice y valor
for i, fruta in enumerate(frutas):
    print(i, fruta)
```

## Metodos utiles de listas

| Método           | Descripción                                         | Ejemplo                     |
| ---------------- | --------------------------------------------------- | --------------------------- |
| append(elemento) | Agrega un elemento al final                         | lista.append(10)            |
| insert(i, elem)  | Inserta elemento en índice `i`                      | lista.insert(1, "a")        |
| extend(lista2)   | Agrega todos los elementos de otra lista            | lista.extend(\[1,2])        |
| remove(valor)    | Elimina primer aparición del valor                  | lista.remove(3)             |
| pop(i)           | Elimina y devuelve el elemento (último por defecto) | lista.pop()                 |
| clear()          | Elimina todos los elementos                         | lista.clear()               |
| index(valor)     | Devuelve el índice de la primera aparición          | lista.index(3)              |
| count(valor)     | Cuenta cuántas veces aparece el valor               | lista.count(2)              |
| sort()           | Ordena la lista (ascendente por defecto)            | lista.sort()                |
| reverse()        | Invierte el orden de la lista                       | lista.reverse()             |
| copy()           | Devuelve una copia de la lista                      | nueva\_lista = lista.copy() |

## Listas anidadas

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

# Acceder a elementos
print(matriz[0][1])  # 2

# Recorrer matriz
for fila in matriz:
    for elemento in fila:
        print(elemento, end=" ")
    print()
```

## Consejos prácticos

1. Usar listas cuando necesites **orden y mutabilidad**.

2. Evitar modificar la lista mientras la recorres; usar **copias** si es necesario.

3. Usar **slicing** para acceder a subconjuntos sin modificar la lista original.

4. Combinar métodos como `append`, `extend`, `remove` para **manipulación eficiente**.

Para listas grandes, **considerar generadores o listas por comprensión** para eficiencia.

## Resumen

- Las listas son **colecciones ordenadas y mutables**.

- Permiten **almacenar elementos de cualquier tipo**, acceder por índice, modificar, agregar, eliminar y recorrer.

- Tienen **métodos integrados** para manipulación rápida y eficiente.

- Son la **estructura de datos más versátil** en Python para manejar conjuntos de elementos.
