# Acceder a caracteres individuales en Python

---

## Concepto

En Python, las **cadenas (strings)** son **secuencias de caracteres**.  
Cada carácter dentro de una cadena tiene una **posición o índice**, lo que permite acceder a ellos individualmente.

### 1️⃣ Índices de los caracteres

- Los **índices comienzan en 0** para el primer carácter.  
- También se pueden usar **índices negativos**, donde `-1` representa el **último carácter**, `-2` el penúltimo, y así sucesivamente.

```python
texto = "Python"

print(texto[0])   # Salida: P  (primer carácter)
print(texto[5])   # Salida: n  (último carácter)
print(texto[-1])  # Salida: n  (último carácter usando índice negativo)
print(texto[-6])  # Salida: P  (primer carácter usando índice negativo)
```

### 2️⃣ Resumen de reglas

1. Acceso individual: Se usa la sintaxis `cadena[indice]`.

2. Índices positivos: Empiezan desde 0, contando desde el inicio.

3. Índices negativos: Empiezan desde -1, contando desde el final.

4. Error por índice fuera de rango: Si se usa un índice que no existe, Python genera un `IndexError`.

```python
texto = "Hola"
print(texto[4])  # IndexError: índice fuera de rango
```

### 3️⃣ Concepto clave

Acceder a caracteres individuales permite **manipular, analizar o extraer partes específicas** de un string sin modificar el original.
Esta técnica es fundamental para operaciones como:

- Validación de contraseñas

- Extracción de subcadenas

- Conteo de caracteres

- Aplicaciones de procesamiento de texto

---

## Subcadenas (`Slicing`)

Además de acceder a caracteres individuales, Python permite **extraer partes de una cadena** mediante **slicing** o rebanado.

### 1️⃣ Sintaxis básica

```python
subcadena = cadena[inicio:fin]
```

- `inicio` → índice donde comienza la subcadena (incluido).

- `fin` → índice donde termina la subcadena (excluido).

- El resultado es un **nuevo string** que va desde `inicio` hasta `fin-1`.

```python
texto = "Python"
print(texto[0:4])  # Salida: Pyth
print(texto[2:])   # Salida: thon  (desde índice 2 hasta el final)
print(texto[:4])   # Salida: Pyth  (desde inicio hasta índice 3)
```

### 2️⃣ Slicing con pasos (`step`)

Se puede usar un **tercer parámetro** para indicar el **salto de índices**.

```python
texto = "Python"
print(texto[0:6:2])  # Salida: Pto  (cada 2 caracteres)
print(texto[::2])    # Salida: Pto  (de inicio a fin, saltando 2)
print(texto[::-1])   # Salida: nohtyP  (cadena invertida)
```

**Resumen de la sintaxis:**

```python
cadena[inicio:fin:paso]
```
### 3️⃣ Conceptos clave

1. Los índices siguen **el mismo sistema que para acceder a caracteres individuales**.

2. El slicing **no modifica la cadena original**, sino que crea un nuevo string.

3. Es útil para:

- Extraer subcadenas

- Invertir cadenas

- Saltar caracteres o patrones específicos

### 4️⃣ Ejemplos prácticos

```python
texto = "Hola mundo"

# Extraer "Hola"
print(texto[0:4])  # Salida: Hola

# Extraer "mundo"
print(texto[5:])   # Salida: mundo

# Extraer cada segunda letra
print(texto[::2])  # Salida: Hl ud

# Invertir la cadena
print(texto[::-1]) # Salida: odnum aloH
```

---

## Métodos y funciones útiles para cadenas en Python

Python ofrece múltiples **métodos integrados** para trabajar con strings, que permiten **manipular, buscar, modificar y formatear** texto de manera sencilla.

### 1️⃣ Métodos de transformación

| Método         | Descripción                               | Ejemplo                         | Salida                  |
|----------------|-------------------------------------------|---------------------------------|-------------------------|
| `.upper()`     | Convierte la cadena a mayúsculas          | `"hola".upper()`                 | `"HOLA"`               |
| `.lower()`     | Convierte la cadena a minúsculas          | `"HOLA".lower()`                 | `"hola"`               |
| `.capitalize()`| Convierte la primera letra en mayúscula   | `"python".capitalize()`          | `"Python"`             |
| `.title()`     | Convierte la primera letra de cada palabra en mayúscula | `"hola mundo".title()` | `"Hola Mundo"`         |
| `.swapcase()`  | Invierte mayúsculas y minúsculas          | `"PyThOn".swapcase()`            | `"pYtHoN"`             |
| `.strip()`     | Elimina espacios al inicio y fin          | `"  hola  ".strip()`             | `"hola"`               |
| `.lstrip()`    | Elimina espacios a la izquierda           | `"  hola".lstrip()`              | `"hola"`               |
| `.rstrip()`    | Elimina espacios a la derecha             | `"hola  ".rstrip()`              | `"hola"`               |

---

### 2️⃣ Métodos de búsqueda y conteo

| Método         | Descripción                               | Ejemplo                         | Salida                  |
|----------------|-------------------------------------------|---------------------------------|-------------------------|
| `.find(sub)`   | Devuelve el índice de la primera aparición de `sub`, -1 si no existe | `"hola".find("l")` | `2`                     |
| `.rfind(sub)`  | Índice de la última aparición             | `"hola hola".rfind("l")`       | `7`                     |
| `.index(sub)`  | Igual que find pero lanza error si no existe | `"hola".index("l")`           | `2`                     |
| `.count(sub)`  | Cuenta cuántas veces aparece la subcadena | `"hola hola".count("hola")`    | `2`                     |
| `.startswith(sub)` | Devuelve True si la cadena empieza con `sub` | `"Hola".startswith("H")`  | `True`                  |
| `.endswith(sub)`   | Devuelve True si la cadena termina con `sub` | `"Hola".endswith("a")`    | `True`                  |

---

### 3️⃣ Métodos de reemplazo y división

| Método         | Descripción                               | Ejemplo                         | Salida                  |
|----------------|-------------------------------------------|---------------------------------|-------------------------|
| `.replace(a,b)`| Reemplaza todas las apariciones de `a` por `b` | `"hola mundo".replace("mundo","Python")` | `"hola Python"` |
| `.split(sep)`  | Divide la cadena en una lista usando separador | `"a,b,c".split(",")`           | `["a","b","c"]`         |
| `.rsplit(sep)` | Divide la cadena desde el final           | `"a,b,c".rsplit(",",1)`         | `["a,b","c"]`           |
| `.splitlines()`| Divide la cadena en una lista por saltos de línea | `"linea1\nlinea2".splitlines()` | `["linea1","linea2"]` |
| `.join(lista)` | Une los elementos de una lista en una cadena | `"-".join(["a","b","c"])`      | `"a-b-c"`               |

---

### 4️⃣ Métodos de alineación y relleno

| Método         | Descripción                               | Ejemplo                         | Salida                  |
|----------------|-------------------------------------------|---------------------------------|-------------------------|
| `.center(ancho, relleno)` | Centra la cadena en un ancho dado | `"Hola".center(10,"-")`        | `"---Hola---"`          |
| `.ljust(ancho, relleno)`  | Alinea a la izquierda             | `"Hola".ljust(10,"-")`         | `"Hola------"`          |
| `.rjust(ancho, relleno)`  | Alinea a la derecha                | `"Hola".rjust(10,"-")`         | `"------Hola"`          |
| `.zfill(ancho)`           | Rellena con ceros a la izquierda  | `"42".zfill(5)`                 | `"00042"`               |

---

### 5️⃣ Métodos de verificación

| Método             | Descripción                               | Ejemplo                         | Salida                  |
|-------------------|-------------------------------------------|---------------------------------|-------------------------|
| `.isalpha()`       | True si todos los caracteres son letras   | `"Hola".isalpha()`              | `True`                  |
| `.isdigit()`       | True si todos los caracteres son dígitos | `"123".isdigit()`               | `True`                  |
| `.isalnum()`       | True si todos son letras o dígitos        | `"Hola123".isalnum()`           | `True`                  |
| `.isspace()`       | True si todos son espacios                | `"   ".isspace()`               | `True`                  |
| `.islower()`       | True si todos los caracteres son minúsculas | `"hola".islower()`            | `True`                  |
| `.isupper()`       | True si todos los caracteres son mayúsculas | `"HOLA".isupper()`            | `True`                  |
| `.istitle()`       | True si la cadena está en formato título | `"Hola Mundo".istitle()`        | `True`                  |

---

## Resumen

- Los strings en Python tienen **métodos incorporados** que permiten **transformar, buscar, reemplazar, dividir, unir y verificar** cadenas.  
- Estos métodos **no modifican la cadena original**, sino que devuelven **nuevos strings** con el resultado.  
- Son fundamentales para **procesamiento de texto, validación de datos y manipulación de información**.
