# Sintaxis y Semántica en Programación

En programación, es fundamental entender los conceptos de **Sintaxis** y **Semántica**, ya que son complementarios pero distintos.

**Sintaxis:** es el conjunto de reglas que determina **cómo escribir correctamente el código** en un lenguaje de programación.  
Es como la **gramática de un idioma**: si no se respeta, el código **no se ejecuta**.  

**Ejemplo de sintaxis en Python:**

```python
print("Hola, mundo")  # Correcto
print "Hola, mundo"   # Incorrecto: SyntaxError
```

**Semántica:** se refiere al significado del código, es decir, lo que realmente hace cuando se ejecuta.
Un programa puede tener sintaxis correcta pero producir resultados incorrectos si la semántica falla.

**Ejemplo de semántica correcta en Python:**

Ejemplo 1: la semántica refleja correctamente la intención del desarrollador.
```python
edad = 10
if edad > 18:
    print("Es mayor de edad")
else:
    print("Es menor de edad")  # Correcto según la intención
```

Ejemplo 2: aunque la sintaxis sea válida, el resultado es incorrecto porque la operación no cumple la intención lógica.
```python
precio = 100
descuento = 20
total = precio + descuento  # Debería ser resta
print("Total a pagar:", total)
```