# Cadenas (Strings) en Python

---

## Concepto

**Cadena (String):**  
Una **cadena** o `string` es una **secuencia de caracteres** que se utiliza para almacenar **texto** en un programa.  
En Python, las cadenas se escriben entre **comillas simples `' '`** o **comillas dobles `" "`**.

**Ejemplo conceptual:**  

```python
nombre = "Abel"
mensaje = 'Hola, mundo'
```

- `nombre` y `mensaje` son variables de tipo `string`.

- Pueden contener letras, números, símbolos y espacios.

Las cadenas permiten **almacenar, manipular y mostrar información textual**, y son uno de los tipos de datos más utilizados en Python.

---

## Concatenación de Cadenas en Python

La **concatenación de cadenas** consiste en **unir dos o más strings** para formar uno solo. Python ofrece varias formas de hacerlo, dependiendo del contexto.

### 1️⃣ Usando el operador `+`

Se utiliza el operador `+` para unir cadenas.

```python
nombre = "Abel"
saludo = "Hola, " + nombre
print(saludo)  # Salida: Hola, Abel
```

**Nota**: Solo funciona con strings. Si quieres concatenar un número, debes convertirlo a string con `str()`.

```python
edad = 24
mensaje = "Tengo " + str(edad) + " años"
print(mensaje)  # Salida: Tengo 24 años
```

### 2️⃣ Usando `f-strings` (Python 3.6+)

Permite **insertar variables directamente dentro de la cadena** usando `{}`.

```python
nombre = "Abel"
edad = 24
mensaje = f"Hola, {nombre}. Tengo {edad} años"
print(mensaje)  # Salida: Hola, Abel. Tengo 24 años
```

**Ventaja**: Más legible y evita convertir números a strings manualmente.

### 3️⃣ Usando el método `.format()`

Se usa `{}` como **marcadores de posición** y `.format()` para insertar valores.

```python
nombre = "Abel"
edad = 24
mensaje = "Hola, {}. Tengo {} años".format(nombre, edad)
print(mensaje)  # Salida: Hola, Abel. Tengo 24 años
```

También se pueden usar índices o nombres:

```python
mensaje = "Hola, {0}. Tengo {1} años".format(nombre, edad)
mensaje2 = "Hola, {nombre_var}. Tengo {edad_var} años".format(nombre_var=nombre, edad_var=edad)
```

### 4️⃣ Usando el operador `%` (formato antiguo)

Se utiliza **%s** para strings y **%d** para enteros.

```python
nombre = "Abel"
edad = 24
mensaje = "Hola, %s. Tengo %d años" % (nombre, edad)
print(mensaje)  # Salida: Hola, Abel. Tengo 24 años
```

**Nota**: Esta forma es más antigua, pero todavía funciona.

### 5️⃣ Usando `join()` con listas de strings

Permite **unir varias cadenas almacenadas en una lista** usando un separador.

```python
palabras = ["Hola", "mundo"]
mensaje = " ".join(palabras)
print(mensaje)  # Salida: Hola mundo
```

```python
letras = ["P", "y", "t", "h", "o", "n"]
palabra = "-".join(letras)
print(palabra)  # Salida: P-y-t-h-o-n
```

### 6️⃣ Concatenación implícita en paréntesis

Python permite **unir cadenas literales automáticamente** si están dentro de paréntesis.

```python
mensaje = ("Hola, "
           "mundo. "
           "Bienvenido a Python.")
print(mensaje) # Salida: Hola, mundo. Bienvenido a Python.
```

### 7️⃣ Usando comas en `print()`

Se pueden separar varias cadenas o variables con **comas** dentro de `print()`.  
Python imprimirá todo en la misma línea, separado por espacios.

```python
nombre = "Abel"
edad = 24
print("Hola,", nombre, "tengo", edad, "años") # Salida: Hola, Abel tengo 24 años
```

**Nota:**

- Esto **no crea un solo string**; si quieres guardarlo en una variable, necesitas usar `+`, `.format()` o `f-strings`.

- Es útil para **imprimir varias variables juntas** sin preocuparse por convertir números a strings.

### 8️⃣ Resumen de Concatenación de Cadenas en Python

| Método                  | Descripción                                    | Ejemplo                                 | Resultado                            |
|--------------------------|-----------------------------------------------|----------------------------------------|-------------------------------------|
| `+`                      | Une cadenas directamente                       | `"Hola, " + nombre`                     | `"Hola, Abel"`                       |
| f-strings                | Inserta variables dentro de la cadena `{}`    | `f"Hola, {nombre}"`                     | `"Hola, Abel"`                       |
| `.format()`              | Usa `{}` como marcador y `.format()`          | `"Hola, {}. Tengo {} años".format(nombre, edad)` | `"Hola, Abel. Tengo 24 años"`       |
| `%`                      | Formato antiguo usando `%s` y `%d`            | `"Hola, %s" % nombre`                   | `"Hola, Abel"`                       |
| `join()`                 | Une elementos de una lista con un separador   | `" ".join(["Hola","mundo"])`            | `"Hola mundo"`                       |
| Concatenación implícita  | Une cadenas literales dentro de paréntesis    | `("Hola, " "mundo")`                    | `"Hola, mundo"`                      |
| Comas en `print()`       | Imprime varias cadenas separadas por espacios | `print("Hola,", nombre, "tengo", edad, "años")` | `Hola, Abel tengo 24 años` (impreso) |

**Nota:**  
- `+`, `f-strings`, `.format()`, `%` y `join()` crean un **nuevo string**.  
- Las comas en `print()` **solo muestran** las cadenas, no las concatenan para guardar en una variable.
