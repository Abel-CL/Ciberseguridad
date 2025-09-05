# Sentencias Condicionales en Python

## Concepto

Las **sentencias condicionales** permiten que un programa **tome decisiones** basadas en condiciones.  
Según si la condición se cumple (`True`) o no (`False`), se ejecuta un bloque de código u otro.  

En Python, las principales sentencias condicionales son:

- `if` → evalúa una condición y ejecuta un bloque si es verdadera.  
- `elif` → “else if”, evalúa otra condición si la anterior fue falsa.  
- `else` → se ejecuta si **todas las condiciones anteriores son falsas**.

---

## Sintaxis básica

```python
if condición:
    # Bloque de código si la condición es True
elif otra_condición:
    # Bloque de código si la primera condición fue False y esta es True
else:
    # Bloque de código si todas las condiciones anteriores son False
```

**Notas importantes:**

- Python usa **indentación** para definir bloques (generalmente 4 espacios o un tab).

- No se usan llaves `{}` como en otros lenguajes.

- `elif` y `else` son opcionales, pero `if` siempre es necesario.

---

## Ejemplos

**Ejemplo 1: Verificar mayor de edad**

```python
edad = 20

if edad >= 18:
    print("Eres mayor de edad")
else:
    print("Eres menor de edad")
```

**Ejemplo 2: Clasificar notas**

```python
nota = 85

if nota >= 90:
    print("Excelente")
elif nota >= 70:
    print("Bueno")
else:
    print("Insuficiente")
```

**Ejemplo 3: Comparar numeros**

```python
a = 10
b = 15

if a > b:
    print("a es mayor que b")
elif a < b:
    print("a es menor que b")
else:
    print("a y b son iguales")
```

## Consejos prácticos

1. Se pueden **combinar condiciones** usando operadores lógicos (`and`, `or`, `not`).

```python
edad = 20
tiene_ci = True

if edad >= 18 and tiene_ci:
    print("Puede ingresar")
else:
    print("No puede ingresar")
```

2. Siempre usar **indentación consistente**.

```python
if edad >= 18:
print("Mayor de edad")
```

3. Evitar condiciones redundantes; el orden de los `if` y `elif` importa.

```python
edad = 70

if edad >= 18:
    print("Adulto")
elif edad >= 65:
    print("Jubilado")
else:
    print("Menor de edad")
```

4. Para condiciones simples, también se puede usar el **operador ternario**:

  ```python
edad = 20
mensaje = "Mayor" if edad >= 18 else "Menor"
print(mensaje)
```

## Resumen
- Las sentencias condicionales permiten al programa tomar decisiones.

- `if` → condición principal.

- `elif` → condiciones adicionales si las anteriores son falsas.

- `else` → bloque final si ninguna condición se cumple.

- Se pueden combinar con **operadores lógicos** para reglas más complejas.
