# Bucle `while` en Python

## Concepto

El bucle **`while`** permite ejecutar un bloque de código **mientras una condición sea verdadera** (`True`).
Se utiliza cuando **no se sabe de antemano cuántas veces se repetirá** el ciclo, a diferencia del `for` que itera sobre una secuencia conocida.

- La condición se evalúa **antes de cada iteración**.
- Si la condición es **False**, el bucle termina.
- Es importante **evitar bucles infinitos**, asegurando que la condición eventualmente se vuelva False.

---

## Sintaxis básica

```python
while condición:
    # Bloque de código a repetir
    # Debe modificarse alguna variable para evitar bucle infinito
```

## Ejemplos básicos

**1. Contar de 1 a 5**

```python
i = 1
while i <= 5:
    print(f"Número: {i}")
    i += 1  # Incremento para evitar bucle infinito
```

**2. Solicitar entrada hasta que sea correcta**

```python
while True:
    contraseña = input("Ingresa la contraseña: ")
    if contraseña == "1234":
        print("Acceso permitido")
        break  # Sale del bucle
    else:
        print("Contraseña incorrecta")
```

**3. Sumar números hasta que el usuario diga "0"**

```python
suma = 0
numero = int(input("Ingresa un número (0 para terminar): "))
while numero != 0:
    suma += numero
    numero = int(input("Ingresa otro número (0 para terminar): "))
print(f"Suma total: {suma}")
```

## Control de flujo dentro del `while`

- `break` → termina el bucle inmediatamente.

- `continue` → salta a la siguiente iteración sin ejecutar el resto del bloque.

- `pass` → marcador de posición (no hace nada, útil para estructuras vacías).

**Ejemplo con `break` y `continue`**

```python
i = 0
while i < 10:
    i += 1
    if i == 3:
        continue  # Salta el número 3
    if i == 8:
        break     # Termina el bucle en 8
    print(i)
```

## Bucle `while` con `else`

- Python permite un bloque `else` después de un while.

- Se ejecuta **cuando la condición del while se vuelve False**, pero **no se ejecuta si el bucle termina con** `break`.

```python
i = 1
while i <= 3:
    print(f"Número: {i}")
    i += 1
else:
    print("Bucle terminado")
```

## Bucle anidado `while`

- Se pueden colocar **bucles dentro de bucles** para operaciones más complejas.

```python
i = 1
while i <= 3:
    j = 1
    while j <= 2:
        print(f"i={i}, j={j}")
        j += 1
    i += 1
```

## Consejos prácticos

1. **Evitar bucles infinitos:** siempre modificar la variable de control o usar `break`.

2. **Usar `break` para salir anticipadamente** cuando se cumpla una condición especial.

3. **Usar `continue` para saltar iteraciones** según reglas específicas.

4. **Bucle con `else`:** útil para ejecutar código cuando el bucle termina normalmente.

5. Si necesitas **contar iteraciones**, inicializa un contador antes del bucle.

6. **Indentación consistente**: Python usa indentación para definir bloques; siempre usar 4 espacios.

## Resumen

- `while` repite un bloque de código mientras la condición sea **True**.

- Ideal cuando **no se conoce el número exacto de iteraciones**.

- Se puede combinar con `break`, `continue` y `else` para **mayor control del flujo**.

- Permite **bucles anidados** para operaciones complejas.
