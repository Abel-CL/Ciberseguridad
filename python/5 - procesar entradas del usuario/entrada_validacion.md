# Entradas, Validaciones en python

Este apunte combina teoría y práctica sobre **cómo procesar y validar entradas del usuario**, y cómo usar **operadores lógicos** (`and`, `or`, `not`) en Python.

---

## 1. Procesar Entradas del Usuario

### Concepto
- **`input()`** permite al usuario ingresar datos durante la ejecución del programa.  
- Por defecto, devuelve un **string (`str`)**.  
- Para usar valores numéricos, se deben convertir con (`int()`, `float()`).

### Ejemplos

**Entrada de texto**

```python
nombre = input("Escribe tu nombre: ")
print("Hola,", nombre)
```

**Entrada de número entero**

```python
edad = int(input("Escribe tu edad: "))
print("En 5 años tendrás:", edad + 5)
```

**Entrada de número decimal**

```python
altura = float(input("Escribe tu altura en metros: "))
print("Tu altura es:", altura, "metros")
```

---

## 2. Validación de Entradas

### Concepto

- Validar significa verificar que los datos ingresados cumplen reglas antes de ser usados.

- Evita errores y asegura que el programa funcione correctamente.

### Ejemplos

**Validación de números**
```python
while True:
    try:
        edad = int(input("Ingresa tu edad: "))
        if edad > 0:
            print("Edad registrada:", edad)
            break
        else:
            print("Debes ingresar un número positivo.")
    except ValueError:
        print("Entrada inválida. Debes ingresar un número entero.")
```

**Validacion de texto**
```python
while True:
    nombre = input("Escribe tu nombre: ").strip()
    if nombre != "":
        print("Hola,", nombre)
        break
    else:
        print("No puedes dejar el nombre vacío.")
```

**Validacion con opciones limitadas**
```python
while True:
    color = input("Elige un color (rojo/azul/verde): ").lower()
    if color in ["rojo", "azul", "verde"]:
        print("Has elegido:", color)
        break
    else:
        print("Opción inválida. Intenta de nuevo.")
```

**Resumen**
- `input()` permite recibir datos del usuario.
- Validar entradas asegura que los datos sean correctos.