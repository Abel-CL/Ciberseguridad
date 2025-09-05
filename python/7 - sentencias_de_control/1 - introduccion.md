# Sentencias de Control en Python

## Concepto

Las **sentencias de control** en Python son instrucciones que permiten **modificar el flujo de ejecución** de un programa.
En lugar de ejecutar las instrucciones de manera secuencial (de arriba hacia abajo), las sentencias de control permiten:

1. **Tomar decisiones** (ejecutar un bloque de código u otro según una condición).
2. **Repetir acciones** (ejecutar un bloque varias veces con bucles).
3. **Alterar la ejecución** dentro de un bucle (saltando, rompiendo o continuando).

En otras palabras, las sentencias de control le dan al programa la capacidad de **ser dinámico y adaptable** según las condiciones que se presenten.

---

## Tipos principales de sentencias de control en Python

1. **Condicionales (`if`, `elif`, `else`)** → permiten ejecutar código dependiendo de condiciones.
2. **Bucles (`for`, `while`)** → permiten repetir bloques de código.
3. **Control de flujo dentro de bucles (`break`, `continue`, `pass`)** → permiten modificar el comportamiento del ciclo.

---

## Ejemplo general

```python
# Ejemplo de condicional
edad = 18
if edad >= 18:
    print("Eres mayor de edad")
else:
    print("Eres menor de edad")

# Ejemplo de bucle
for i in range(3):
    print(f"Iteración: {i}")

# Ejemplo de control de flujo
for i in range(5):
    if i == 3:
        break
    print(i)
```

**Gracias a estas sentencias, los programas en Python pueden pensar, decidir y repetir tareas.**
