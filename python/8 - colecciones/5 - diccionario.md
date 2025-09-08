# Diccionarios en Python (`dict`)

Un **diccionario** es una colección **desordenada, mutable y con pares clave-valor**.  
Cada valor se accede a través de su **clave** (que debe ser inmutable: string, número, tupla).  

**Sintaxis básica**:

```python
diccionario = {
    "clave1": "valor1",
    "clave2": "valor2",
    "clave3": "valor3"
}
```

## Características principales

- Se definen con `{}`.

- Cada elemento tiene un par `clave: valor`.

- Las claves deben ser **únicas**.

- Son **mutables**, se pueden cambiar valores.

- Desde **Python 3.7** mantienen el **orden de inserción**.

## Crear diccionarios

```python
# Diccionario vacío
d1 = {}

# Con elementos
d2 = {
    "nombre": "Maria",
    "edad": 25,
    "profesion": "Ingeniera"
}

# Usando dict()
d3 = dict(nombre="Pedro", edad=30)

# Con lista de pares
d4 = dict([("a", 1), ("b", 2)])
```

## Acceder a valores

```python
persona = {
    "nombre": "Carlos",
    "edad": 28
}
print(persona["nombre"])   # Carlos
print(persona.get("edad")) # 28
print(persona.get("altura", "No existe"))  # Evita error
```

- `get()` es más seguro que acceder directamente, porque no lanza error si la clave no existe.

## Modificar y agregar elementos

```python
persona = {
    "nombre": "Carlos",
    "edad": 28
}
persona["edad"] = 29           # Modificar valor
persona["ciudad"] = "Madrid"   # Agregar nueva clave
print(persona) # {'nombre': 'Carlos', 'edad': 29, 'ciudad': 'Madrid'}
```

## Eliminar elementos

- `del persona["clave"]` → elimina la clave indicada, no devuelve nada.

```python
persona = {
    "nombre": "Maria",
    "edad": 25,
    "pais": "España"
}
del persona["pais"]
print(persona)
```

- `pop("clave")` → elimina la clave indicada y devuelve su valor.

```python
persona = {
    "nombre": "Maria",
    "edad": 25,
    "pais": "España"
}
eliminar = persona.pop("edad")
print(eliminar)
```

- `popitem()` → elimina el último par `(clave, valor)` y lo devuelve como tupla.

```python
persona = {
    "nombre": "Maria",
    "edad": 25,
    "pais": "España"
}
eliminar = persona.popitem()
print(eliminar)
```

- `clear()` → elimina **todos los elementos** del diccionario, quedando vacío.

```python
persona = {
    "nombre": "Maria",
    "edad": 25,
    "pais": "España"
}
persona.clear()
print(persona)
```

## Metodos utiles

| Método      | Descripción                      | Ejemplo                  | Resultado                       |
| ----------- | -------------------------------- | ------------------------ | ------------------------------- |
| `keys()`    | Devuelve todas las claves.       | `{"a":1,"b":2}.keys()`   | `dict_keys(['a','b'])`          |
| `values()`  | Devuelve todos los valores.      | `{"a":1,"b":2}.values()` | `dict_values([1,2])`            |
| `items()`   | Devuelve pares `(clave, valor)`. | `{"a":1,"b":2}.items()`  | `dict_items([('a',1),('b',2)])` |
| `update(d)` | Actualiza con otro diccionario.  | `d.update({"c":3})`      | `{'a':1,'b':2,'c':3}`           |
| `copy()`    | Devuelve una copia.              | `nuevo = d.copy()`       | Copia independiente             |

```python
persona = {
    "nombre": "Maria",
    "edad": 25
}
persona.update({"edad": 26, "ciudad": "Madrid"})
print(persona)
```

## Recorrer diccionarios

- Recorrer claves

```python
persona = {
    "nombre": "Maria",
    "edad": 25,
    "pais": "España"
}
for clave in persona:
    print(clave)
```

- Recorrer valores

```python 
persona = {
    "nombre": "Maria",
    "edad": 25,
    "pais": "España"
}
for valor in persona.values():
    print(valor)
```

- Recorrer pares clave-valor

```python
persona = {
    "nombre": "Maria",
    "edad": 25,
    "pais": "España"
}
for clave, valor in persona.items():
    print(f"{clave}: {valor}")
```

## Diccionarios anidados

```python
usuarios = {
    "usuario1": {"nombre": "Maria", "edad": 25},
    "usuario2": {"nombre": "Luis", "edad": 30}
}
print(usuarios["usuario1"]["nombre"])  # Ana
```

## Operadores con diccionarios

```python
persona = {
    "nombre": "Pedro",
    "edad": 25
}
print("nombre" in persona)   # True
print("Pedro" in persona)      # False (busca claves, no valores)
print(len(persona))          # 2
```

## Usos comunes

- Almacenar datos estructurados (ejemplo: JSON en APIs).

```python
# Simulando una respuesta de una API en formato JSON
usuario = {
    "id": 101,
    "nombre": "Juana",
    "email": "ana@example.com",
    "activo": True,
    "roles": ["admin", "editor"],
    "perfil": {
        "edad": 29,
        "pais": "España"
    }
}

# Accediendo a los datos
print(usuario["nombre"])      # Juana
print(usuario["roles"])       # ['admin', 'editor']
print(usuario["perfil"]["pais"])  # España

# Modificar un valor
usuario["activo"] = False
print(usuario["activo"])      # False

# Agregar un nuevo campo
usuario["telefono"] = "78894556"
print(usuario["telefono"])    # 78894556
```

- Contar frecuencias:

```python
texto = "banana"
conteo = {}
for letra in texto:
    conteo[letra] = conteo.get(letra, 0) + 1
print(conteo)  # {'b':1, 'a':3, 'n':2}
```

- Representar tablas en memoria.

```python
# Representar una "tabla" de estudiantes
estudiantes = {
    1: {"nombre": "Juana", "edad": 20, "carrera": "Ingeniería"},
    2: {"nombre": "Luis", "edad": 22, "carrera": "Medicina"},
    3: {"nombre": "María", "edad": 21, "carrera": "Arquitectura"}
}

# Acceder a un registro (fila)
print(estudiantes[1])
# {'nombre': 'Ana', 'edad': 20, 'carrera': 'Ingeniería'}

# Acceder a un valor específico (columna de una fila)
print(estudiantes[2]["carrera"])  
# Medicina

# Recorrer toda la "tabla"
for id_est, datos in estudiantes.items():
    print(f"ID {id_est} → Nombre: {datos['nombre']}, Edad: {datos['edad']}, Carrera: {datos['carrera']}")
```

## Resumen

- Los diccionarios son colecciones de pares clave-valor.

- Permiten acceso rápido a valores mediante la clave.

- Son mutables y flexibles.

- Muy usados en programación real (APIs, manejo de datos, conteo de elementos, etc.).
