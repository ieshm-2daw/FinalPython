# **Examen Final de Python**

**Instrucciones:** Responde cada pregunta con el código necesario para cumplir con los requerimientos. Asegúrate de probar tu código y que funcione correctamente.

---

### **Pregunta 1: JSON - Cargar y Guardar Datos**
Se te proporciona un archivo llamado `datos.json` que contiene una lista de diccionarios con información sobre personas:

```json
[
    {"nombre": "Ana", "edad": 28, "ciudad": "Madrid"},
    {"nombre": "Carlos", "edad": 34, "ciudad": "Barcelona"},
    {"nombre": "Lucia", "edad": 22, "ciudad": "Valencia"}
]
```

1. Escribe una función `cargar_datos(fichero)` que lea y cargue este archivo JSON, devolviendo la lista de personas como una lista de diccionarios.
2. Crea otra función `guardar_datos(fichero, datos)` que guarde cualquier lista de diccionarios proporcionada en un archivo JSON.

**Ejemplo de uso:**
```python
datos = cargar_datos("datos.json")
# Modificar algún dato
datos[0]["edad"] = 29
guardar_datos("datos_modificados.json", datos)
```

---

### **Pregunta 2: Orientación a Objetos**
Define una clase `Persona` con los siguientes atributos y métodos:

1. **Atributos**:
   - `nombre` (str)
   - `edad` (int)
   - `ciudad` (str)

2. **Métodos**:
   - `__init__(self, nombre, edad, ciudad)`: constructor que inicializa los atributos.
   - `es_mayor_de_edad(self)`: método que devuelve `True` si la persona es mayor de edad (edad >= 18) o `False` en caso contrario.
   - `__str__(self)`: devuelve una cadena con la información de la persona en el formato: `"{nombre}, {edad} años, vive en {ciudad}"`.

**Ejemplo de uso:**
```python
persona = Persona("Luis", 20, "Sevilla")
print(persona)  # Luis, 20 años, vive en Sevilla
print(persona.es_mayor_de_edad())  # True
```

---

### **Pregunta 3: Diccionarios y Listas**
Se te proporciona una lista de diccionarios que representan productos en una tienda:

```python
productos = [
    {"nombre": "manzana", "precio": 0.5, "cantidad": 50},
    {"nombre": "naranja", "precio": 0.8, "cantidad": 30},
    {"nombre": "pera", "precio": 0.75, "cantidad": 20},
    {"nombre": "platano", "precio": 0.4, "cantidad": 60}
]
```

1. Escribe una función `total_inventario(productos)` que reciba esta lista y devuelva el valor total del inventario (precio * cantidad de cada producto).
2. Escribe una función `producto_mas_caro(productos)` que devuelva el nombre del producto más caro de la lista.

**Ejemplo de uso:**
```python
print(total_inventario(productos))  # Debería devolver el valor total del inventario
print(producto_mas_caro(productos))  # Debería devolver "naranja"
```

---

### **Pregunta 4: Manipulación de Diccionarios**
Supón que tienes el siguiente diccionario que almacena las calificaciones de varios estudiantes:

```python
calificaciones = {
    "Ana": [90, 80, 85],
    "Carlos": [70, 75, 65],
    "Lucia": [88, 92, 84]
}
```

1. Escribe una función `promedio_calificaciones(calificaciones)` que reciba este diccionario y devuelva un nuevo diccionario con el promedio de calificaciones de cada estudiante.
2. Crea una función `mejor_promedio(calificaciones)` que devuelva el nombre del estudiante con el promedio más alto.
3. Escribe una función `añadir_estudiante(calificaciones, nombre, notas)` que añada un nuevo estudiante al diccionario con su lista de notas.
4. Escribe una función `borrar_estudiante(calificaciones, nombre)` que elimine del diccionario al estudiante cuyo nombre se pase como parámetro. La función debe verificar si el estudiante existe y, en caso contrario, mostrar un mensaje indicando que no se encontró.
5. Escribe una función `buscar_estudiante(calificaciones, nombre)` que busque un estudiante por su nombre y devuelva su lista de calificaciones o un mensaje si el estudiante no existe.

**Ejemplo de uso:**
```python
print(promedio_calificaciones(calificaciones))  # {'Ana': 85.0, 'Carlos': 70.0, 'Lucia': 88.0}
print(mejor_promedio(calificaciones))  # 'Lucia'
añadir_estudiante(calificaciones, "Jorge", [75, 80, 78])
print(calificaciones)  # Debería incluir a "Jorge" con sus notas
borrar_estudiante(calificaciones, "Carlos")
print(calificaciones)  # Debería haber eliminado a "Carlos"
print(buscar_estudiante(calificaciones, "Ana"))  # Debería mostrar la lista de calificaciones de Ana
print(buscar_estudiante(calificaciones, "Carlos"))  # Debería mostrar un mensaje indicando que no existe

```

---
