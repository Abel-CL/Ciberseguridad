# Tipos de datos en Python

---

## Concepto

Un tipo de dato define la naturaleza del valor que una variable puede almacenar y qué operaciones se pueden realizar sobre él.
Es decir, determina cómo interpreta el programa la información que guardamos en la variable.

Ejemplo conceptual:

- Si una variable contiene `24`, su tipo de dato es entero (int).

- Si contiene `"Hola"`, su tipo es cadena de texto (str).

- Si contiene `True` o `False`, su tipo es booleano (bool).

Los tipos de datos permiten al lenguaje de programación organizar, procesar y manipular la información correctamente según su naturaleza.

---

## 1️⃣ Tipos de datos básicos

### 1. Enteros (`int`)
- Almacenan **números enteros**, sin decimales.  
- Ejemplos: `10`, `-5`, `0`

```python
edad = 24
año = 2025
```

### 2. Flotantes (`float`)

Almacenan **números con decimales**.

Ejemplos: `3.14`, `-0.75`, `2.0`

```python
altura = 1.75
precio = 99.99
```

### 3. Cadenas de texto (`str`)

Almacenan **texto** o secuencias de caracteres.

Se escriben entre comillas simples `' '` o dobles `" "`.

```python
nombre = "Abel"
saludo = 'Hola, mundo'
```

### 4. Booleanos (`bool`)

Almacenan **valores lógicos**: `True` o `False`.

Se usan para **decisiones y condiciones**.

```python
activo = True
mayor_de_edad = False
```

---

## 2️⃣ Tipos de datos compuestos

### 1. Listas (`list`)

Colección ordenada y mutable de elementos.

Se escriben entre corchetes `[ ]` y pueden contener distintos tipos de datos.

```python
numeros = [1, 2, 3, 4, 5]
nombres = ["Ana", "Luis", "Pedro"]
mixta = [1, "Hola", True]
```

### 2. Tuplas (`tuple`)

Colección **ordenada e inmutable** de elementos.

Se escriben entre paréntesis `( )`.

```python
coordenadas = (10.0, 20.0)
dias_semana = ("Lunes", "Martes", "Miércoles")
```

### 3. Conjuntos (`set`)

Colección **no ordenada** de elementos únicos.

Se escriben entre llaves `{ }`.

```python
frutas = {"manzana", "banana", "naranja"}
```

### 4. Diccionarios (`dict`)

Colección de **pares clave-valor**.

Se escriben entre llaves `{ }` con `clave: valor`.

---

## 3️⃣ Tipo especial

### 1. NoneType

Representa **la ausencia de valor**.

Solo existe un valor: `None`.

```python
resultado = None
```

---

## 4️⃣ Resumen de tipos de datos en Python

| Tipo     | Ejemplo      | Descripción                  |
| -------- | ------------ | ---------------------------- |
| int      | 10           | Número entero                |
| float    | 3.14         | Número decimal               |
| str      | "Hola"       | Cadena de texto              |
| bool     | True / False | Valor lógico                 |
| list     | \[1, 2, 3]   | Lista de elementos           |
| tuple    | (1, 2, 3)    | Tupla inmutable              |
| set      | {1, 2, 3}    | Conjunto de elementos únicos |
| dict     | {"clave": 1} | Diccionario clave-valor      |
| NoneType | None         | Representa ausencia de valor |

Los **tipos de datos** son fundamentales porque permiten al lenguaje **interpretar, almacenar y manipular la información correctamente.**

---

## 5️⃣ Cómo ver el tipo de dato de una variable

En Python, se usa la función `type()` para conocer el tipo de dato almacenado en una variable.

```python
edad = 24
nombre = "Abel"
altura = 1.75
activo = True
numeros = [1, 2, 3]

print(type(edad))     # <class 'int'>
print(type(nombre))   # <class 'str'>
print(type(altura))   # <class 'float'>
print(type(activo))   # <class 'bool'>
print(type(numeros))  # <class 'list'>
```

Explicación:

- `<class 'int'>` → entero

- `<class 'str'>` → cadena de texto

- `<class 'float'>` → decimal

- `<class 'bool'>` → booleano

- `<class 'list'>` → lista

La función `type()` ayuda a verificar el tipo de dato de cualquier variable.