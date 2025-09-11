# Funciones en Python

## Concepto

Una **función** es un bloque de código independiente que realiza una tarea específica y que se puede **reutilizar** varias veces dentro de un programa.

Las funciones permiten:
- Organizar el código de manera **más clara y legible**.
- Evitar **repetición de código**, escribiendo una vez y reutilizando.
- Dividir problemas grandes en **subproblemas más pequeños y manejables**.
- Facilitar el **mantenimiento y escalabilidad** del programa.

---

## Sintaxis básica

Para definir una función en Python se utiliza la palabra clave `def`, seguida del **nombre de la función**, paréntesis `()` y dos puntos `:`.
El código de la función se escribe con **indentación** (normalmente 4 espacios).

```python
def nombre_funcion(parametros):
    """
    Documentación opcional (docstring) que explica qué hace la función.
    """
    # Bloque de código
    return resultado  # Opcional
```

### Explicación:

- `def` → palabra clave para definir la función.

- `nombre_funcion` → nombre único que identifica la función (debe seguir las reglas de los nombres de variables).

- `parametros` → variables de entrada que recibe la función (pueden ser cero o más).

- `return` → devuelve un valor desde la función (opcional).

## Ejemplo basico

```python
def saludar():
    print("Hola, bienvenido a Python")

# Llamar la función
saludar()
```

### Explicación:

- La función `saludar` no recibe parámetros.

- Dentro de la función, se ejecuta la instrucción `print`.

- La función se ejecuta al llamarla usando `saludar()`.

## Ventajas de usar funciones

1. **Reutilización de código**: se puede llamar la función varias veces sin repetir código.

2. **Modularidad**: divide programas grandes en partes más pequeñas y entendibles.

3. **Legibilidad**: hace que el código sea más claro y fácil de mantener.

4. **Escalabilidad**: permite agregar nuevas funcionalidades sin afectar otras partes del programa.

## Ejemplo comparativo

**Sin función (código repetido)**

```python
print("Hola, Ana")
print("Hola, Luis")
print("Hola, María")
```

**Con función (reutilización)**

```python
def saludar(nombre):
    print(f"Hola, {nombre}")

saludar("Ana")
saludar("Luis")
saludar("María")
```

### Explicación:

- La función `saludar` recibe un parámetro `nombre`.

- Se puede llamar varias veces pasando diferentes argumentos.

- Evita repetir `print` y mejora la legibilidad del código.

## Buenas prácticas

- Nombrar las funciones de forma **clara y descriptiva** (`calcular_area`, `sumar_numeros`).

- Usar **docstrings** para documentar qué hace la función.

- Mantener **indentación consistente** (4 espacios).

- Evitar funciones muy largas; una función debe hacer **una sola tarea**.
