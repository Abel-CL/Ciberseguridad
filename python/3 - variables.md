# Variables en Python

---

## Concepto

Una variable es un espacio en la memoria de un programa que almacena un valor, el cual puede cambiar durante la ejecución del programa.
Se le asigna un nombre único que permite referirse a ese valor y manipularlo dentro del código.

Ejemplo conceptual:
Si pensamos en una caja con una etiqueta, la etiqueta sería el nombre de la variable y el contenido de la caja sería el valor almacenado.

## Reglas para nombrar variables en Python

### Solo usar letras, números y guion bajo (_)

```python
#Correcto
edad = abel
nombre_usuario = pedro
precio1 = 150

#Incorrecto
nombre-usuario = pedro
@precio = 150
```

### No empezar con un número

```python
edad = 24 #Correcto
1edad = 24 #Incorrecto
```

### No usar palabras reservadas de Python

Palabras como if, for, while, print, True no pueden ser nombres de variables.

```python
or = 10 #Incorrecto -> Error
```

### Usar nombres descriptivos

Ayuda a entender el propósito de la variable.

```python
total_venta = 150
x = 150
```

### Sensibles a mayúsculas y minúsculas

Edad y edad son variables diferentes.

```python
Edad = 15
edad = 20
```

### Evitar caracteres especiales y espacios

```python
nombre_completo = pedro mendez #Correcto
nombre completo = edgar lopez #Incorrecto
nombre$ = abel #Incorrecto
```

### Seguir convenciones de estilo

Python recomienda snake_case: todas las palabras en minúscula y separadas por guion bajo (_)

```python
numero_telefono = 78345689
fecha_nacimiento = "15 de agosto de 2020"
```