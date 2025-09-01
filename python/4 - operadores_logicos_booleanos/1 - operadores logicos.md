# Operadores Lógicos Booleanos en Python

Los **operadores lógicos booleanos** son símbolos o palabras clave que permiten combinar o modificar valores de tipo **booleano** (`True` o `False`) en Python y en muchos otros lenguajes de programación.  
Se utilizan principalmente dentro de **condiciones** y **estructuras de control** (como `if`, `elif`, `while`) para tomar decisiones más complejas.

Estos operadores no trabajan con números directamente, sino con **expresiones lógicas** que devuelven resultados booleanos.  
El objetivo principal es evaluar si una condición es **verdadera** o **falsa**, y en base a ello ejecutar ciertas instrucciones.

En Python, los principales operadores lógicos booleanos son:

- **and** → Devuelve `True` si **ambas condiciones** son verdaderas.  
- **or** → Devuelve `True` si **al menos una** de las condiciones es verdadera.  
- **not** → Invierte el valor lógico de la condición (`True` → `False`, `False` → `True`).

Estos operadores son fundamentales para el **control de flujo** en los programas, ya que permiten crear decisiones complejas al combinar múltiples condiciones.

---

# Operador Lógico `and` en Python

## Concepto
El operador **`and`** devuelve `True` solo si **todas las condiciones** que conecta son verdaderas.  
Si **alguna condición es falsa**, el resultado será `False`.

Se utiliza mucho en **estructuras de control** como `if`, `elif`, `while` para evaluar múltiples condiciones al mismo tiempo.

---

## Tabla de verdad de `and`

| A     | B     | A and B |
|-------|-------|---------|
| True  | True  | True    |
| True  | False | False   |
| False | True  | False   |
| False | False | False   |

---

## Ejemplos en Python

### Ejemplo 1: Condición simple
```python
a = True
b = False

print(a and b)
```

### Ejemplo 2: Uso en un `if`
```python
edad = 20
tiene_dni = True

if edad >= 18 and tiene_dni:
    print("Puede ingresar al evento.")
else:
    print("No puede ingresar.")
```

### Ejemplo 3: Combinando varias condiciones
```python
x = 10
y = 5
z = 7

if x > 5 and y < 10 and z == 7:
    print("Todas las condiciones se cumplen")
else:
    print("Alguna condición es falsa")
```

---

# Operador Lógico `or` en Python

## Concepto
El operador **`or`** devuelve `True` si **al menos una de las condiciones** que conecta es verdadera.  
Solo devolverá `False` si **todas las condiciones son falsas**.

Se usa en **estructuras de control** (`if`, `elif`, `while`) para evaluar múltiples condiciones y permitir que se cumpla al menos una.

---

## Tabla de verdad de `or`

| A     | B     | A or B |
|-------|-------|--------|
| True  | True  | True   |
| True  | False | True   |
| False | True  | True   |
| False | False | False  |

---

## Ejemplos en Python

### Ejemplo 1: Condición simple
```python
a = True
b = False

print(a or b)
```

### Ejemplo 2: Uso en un `if`
```python
edad = 16
permiso_padres = True

if edad >= 18 or permiso_padres:
    print("Puedes entrar al cine.")
else:
    print("No puedes entrar al cine.")
```

### Combinando varias condiciones
```python
usuario = "admin"
clave = "1234"

if usuario == "admin" or clave == "admin123":
    print("Acceso permitido")
else:
    print("Acceso denegado")
```

---

# Operador Lógico `not` en Python

## Concepto
El operador **`not`** invierte el valor de una condición booleana:  
- Si la condición es `True`, `not` la convierte en `False`.  
- Si la condición es `False`, `not` la convierte en `True`.  

Se utiliza para **negar condiciones** dentro de estructuras de control (`if`, `elif`, `while`) o en expresiones booleanas.

---

## Tabla de verdad de `not`

| A     | not A |
|-------|-------|
| True  | False |
| False | True  |

---

## Ejemplos en Python

### Ejemplo 1: Negación simple
```python
estado = True
print(not estado)
```

### Ejemplo 2: Uso en un `if`
```python
lluvia = False

if not lluvia:
    print("Hoy podemos salir a caminar.")
else:
    print("Mejor quedarnos en casa.")
```

### Ejemplo 3: Combinando con otros operadores
```python
a = True
b = False

resultado = not (a and b)
print(resultado)
```