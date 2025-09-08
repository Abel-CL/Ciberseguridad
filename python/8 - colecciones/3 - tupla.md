# Tuplas en Python

## Concepto

Las **tuplas** son colecciones **ordenadas e inmutables** de elementos en Python.
- **Ordenadas:** mantienen el orden de inserción.
- **Inmutables:** una vez creadas, **no se pueden modificar** (no se puede agregar, eliminar ni cambiar elementos).
- Se definen usando **paréntesis `( )`** y los elementos se separan con comas.

---

## Crear tuplas

```python
# Tupla vacía
tupla_vacia = ()

# Tupla con elementos
numeros = (1, 2, 3, 4, 5)

# Tupla de cadenas
frutas = ("manzana", "banana", "cereza")

# Tupla mixta
mixta = (1, "Python", True, 3.14)

# Tupla con un solo elemento (importante la coma)
un_elemento = (5,)
```

## Acceder a elementos

- Por índice (empieza en 0)

```python
frutas = ("manzana", "banana", "cereza")
print(frutas[0])  # manzana
print(frutas[2])  # cereza
```

- Índices negativos (desde el final)

```python
print(frutas[-1])  # cereza
print(frutas[-2])  # banana
```

## Slicing (rebanadas)

```python
numeros = (1, 2, 3, 4, 5, 6)
print(numeros[1:4])   # (2, 3, 4)
print(numeros[:3])    # (1, 2, 3)
print(numeros[3:])    # (4, 5, 6)
print(numeros[::2])   # (1, 3, 5) -> salto de 2
print(numeros[::-1])  # (6, 5, 4, 3, 2, 1) -> invertir tupla
```

## Recorrer tuplas

```python
frutas = ("manzana", "banana", "cereza")

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

## Operaciones con tuplas

- Concatenar tuplas

```python
a = (1, 2)
b = (3, 4)
c = a + b  # (1, 2, 3, 4)
print(c)
```

- Repetir elementos

```python
d = (0,) * 3  # (0, 0, 0)
print(d)
```

- Verificar existencia

```python
print(5 in (1, 2, 3, 4, 5))  # True
```

## Métodos útiles de tuplas

| Método       | Descripción                                | Ejemplo        |
| ------------ | ------------------------------------------ | -------------- |
| count(valor) | Cuenta cuántas veces aparece el valor      | tupla.count(2) |
| index(valor) | Devuelve el índice de la primera aparición | tupla.index(3) |

`Nota`: las tuplas tienen menos **métodos que las listas** debido a su inmutabilidad.

### Ejemplo con `count(valor)`

```python
tupla = (1, 2, 2, 3, 4, 2, 5)
print(tupla.count(2))
```

### Ejemplo con `index(valor)`

```python
tupla = (10, 20, 30, 40, 50, 30)
print(tupla.index(30))
```

## Tuplas anidadas

```python
matriz = (
    (1, 2, 3),
    (4, 5, 6),
    (7, 8, 9)
)

# Acceder a elementos
print(matriz[0][1])  # 2

# Recorrer matriz
for fila in matriz:
    for elemento in fila:
        print(elemento, end=" ")
    print()
```

## Ventajas de usar tuplas

1. Son **más rápidas** que las listas en acceso y almacenamiento.

2. **Seguras**: los datos no pueden modificarse accidentalmente.

3. Se pueden usar como **claves de diccionarios** (las listas no pueden).

4. Útiles para **retornar múltiples valores** de funciones.

## Resumen

- Las tuplas son **colecciones ordenadas e inmutables**.

- Permiten **almacenar elementos de cualquier tipo**, acceder por índice y recorrer.

- Menos métodos que las listas debido a su inmutabilidad.

- Se usan cuando **no se desea modificar los datos** y se requiere eficiencia o seguridad.
