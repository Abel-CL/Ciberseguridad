# Parámetros y Argumentos en Python

## Concepto

- **Parámetro**: es la variable que se define dentro de la función y que recibe un valor cuando la función es llamada.  
- **Argumento**: es el valor concreto que se pasa a la función al momento de llamarla.  

En pocas palabras:  
> Los **parámetros** son los nombres definidos en la función y los **argumentos** son los valores reales que se envían.

---

## Ejemplo básico

```python
def saludar(nombre):  # 'nombre' es el parámetro
    print(f"Hola, {nombre}!")

saludar("Ana")        # "Ana" es el argumento
saludar("Luis")       # "Luis" es otro argumento
```

### Explicación:

- Definimos la función `saludar` con un parámetro `nombre`.

- Al llamar la función, le pasamos un argumento (`"Ana"` o `"Luis"`).

- La función usa ese valor dentro de su bloque de código.

## Tipos de parámetros

1. **Parámetros posicionales**

- Los argumentos se pasan en **el mismo orden** en que se definieron los parámetros.

```python
def resta(a, b):
    return a - b

print(resta(10, 5))  # 5
```

### Explicación:

- `a` toma el primer argumento (`10`) y `b` el segundo (`5`).

2. **Parámetros con valores por defecto**

- Se puede asignar un valor por defecto a un parámetro.

- Si no se pasa un argumento, se usa el valor predeterminado.

```python
def saludar(nombre="Invitado"):
    print(f"Hola, {nombre}!")

saludar()         # Hola, Invitado!
saludar("Ana")    # Hola, Ana!
```

3. **Argumentos nombrados (keyword arguments)**

- Se especifica el **nombre del parámetro** al llamar la función, sin importar el orden.

```python
def mostrar_info(nombre, edad):
    print(f"Nombre: {nombre}, Edad: {edad}")

mostrar_info(edad=25, nombre="Ana")
```

4. **Número variable de argumentos (`*args`)**

- Permite enviar cualquier cantidad de argumentos **posicionales**.

- Se reciben como una **tupla** dentro de la función.

```python
def sumar(*numeros):
    resultado = sum(numeros)
    print(f"Suma: {resultado}")

sumar(1, 2)           # 3
sumar(5, 10, 15, 20)  # 50
```

5. **Número variable de argumentos nombrados (`**kwargs`)**

- Permite enviar **cualquier cantidad de argumentos con nombre**.

- Se reciben como un **diccionario** dentro de la función.

## Combinar `*args` y `**kwargs`

- Se pueden usar ambos en la misma función.

- Siempre el orden debe ser: parámetros normales, `*args`, luego `**kwargs`.

```python
def demo(x, *args, **kwargs):
    print("x:", x)
    print("args:", args)
    print("kwargs:", kwargs)

demo(10, 20, 30, nombre="Ana", edad=25)
```

## Buenas prácticas

- Nombrar los parámetros de forma descriptiva.

- Usar valores por defecto solo cuando tenga sentido lógico.

- Evitar mezclar demasiados `*args` y `**kwargs` si no es necesario; puede dificultar la lectura.

- Documentar la función indicando qué tipo de argumentos espera y qué devuelve.

## Resumen

| Concepto    | Descripción                                                         |
| ----------- | ------------------------------------------------------------------- |
| Parámetro   | Variable definida en la función que recibirá un valor.              |
| Argumento   | Valor que se pasa a la función al llamarla.                         |
| Posicional  | Se pasa según el orden de los parámetros.                           |
| Por defecto | Tiene un valor predeterminado si no se pasa argumento.              |
| Keyword     | Se pasa usando el nombre del parámetro.                             |
| `*args`     | Recibe cualquier cantidad de argumentos posicionales como tupla.    |
| `**kwargs`  | Recibe cualquier cantidad de argumentos nombrados como diccionario. |

