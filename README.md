# Programacion de Software
## Tarea #1:
Se aplican los tipo de variables a cada atributo de los metodos y su tipo de variable retornado

## Tarea #2 

## Que es Pydantic.
Pydantic es una biblioteca de Python para validación y serialización de datos, utilizando sugerencias de tipo. En esencia, te permite definir la estructura de tus datos (modelos) usando tipos de datos de Python y Pydantic se encarga de verificar que los datos recibidos coincidan con esa estructura, convirtiéndolos si es necesario. Esto simplifica la validación de datos y la gestión de configuraciones, haciendo el código más robusto y fácil de mantener. 
Es especialmente útil cuando necesitas asegurarte de que los datos que manejas cumplen con ciertas estructuras o formatos, como en APIs, aplicaciones web, o cualquier sistema que procese datos externos.

## Ejemplo básico:
Basta con crear una clase que herede de BaseModel y definir los atributos con tipos de Python:

from pydantic import BaseModel

-- class Usuario(BaseModel):
    -- id: int
    -- nombre: str
   -- email: str

-- Los datos se validan y convierten automáticamente
 -- usuario = Usuario(id='123', nombre='Juan', email='juan@ejemplo.com')

 -- print(usuario)

## Salida
 -- Usuario(id=123, nombre='Juan', email='juan@ejemplo.com')

Pydantic convierte el id de string a entero automáticamente, y verifica que nombre y email sean cadenas válidas.

## Ventajas de usar Pydantic

🧠 Validación inteligente: Detecta errores de tipo y formato sin necesidad de código adicional.

🔄 Conversión automática: Transforma datos al tipo correcto si es posible.

🛡️ Código más seguro y mantenible: Ayuda a detectar errores temprano en el desarrollo.

⚙️ Gestión de configuraciones: Útil para cargar y validar configuraciones desde archivos o entornos.

🌐 Ideal para APIs modernas: Es la base de validación en FastAPI, donde los modelos se usan para validar entradas y salidas.
