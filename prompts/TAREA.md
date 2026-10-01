# Tarea: Mi prompt avanzado

## Tarea elegida

Generar casos de prueba para el módulo de registro de nuevos usuarios en un sistema web.

## Version 1: prompt basico

````text
Dame casos de prueba para un registro de usuarios.

## Version 2:
```text
<rol>Actúa como un analista de calidad de software (QA Senior).</rol>
<tarea>Escribe casos de prueba para un módulo de registro de usuarios que requiere nombre, correo y contraseña.</tarea>
<formato>Tabla con las columnas: ID, Escenario, Datos de entrada, Resultado esperado.</formato>
````

## Version 3:

```text
<rol>Actúa como un analista de pruebas de software (QA Engineer Senior) especializado en seguridad y validación de formularios.</rol>

<contexto>
Estamos probando el formulario de registro de usuarios de una plataforma web.
El formulario incluye los campos: Nombre completo, Correo electrónico y Contraseña.
Reglas de negocio:
1. El correo debe ser único y tener un formato válido.
2. La contraseña debe tener al menos 8 caracteres, incluir un número y un carácter especial.
3. Si un campo obligatorio está vacío, se debe mostrar un mensaje de error correspondiente.
</contexto>

<ejemplos>
Ejemplo de formato:
| ID | Escenario | Datos de entrada | Resultado esperado |
| TC01 | Registro exitoso con datos válidos | Nombre: "Juan Perez", Correo: "juan@test.com", Pass: "Clave123!" | Mensaje "Registro exitoso" y redirección al Login. |
| TC02 | Correo inválido sin arroba | Nombre: "Ana", Correo: "anagmail.com", Pass: "Clave123!" | Mensaje "Formato de correo no válido". |
</ejemplos>

<tarea>
Piensa paso a paso qué validaciones, límites y escenarios de fallo pueden presentarse. Escribe 6 casos de prueba siguiendo strictly la estructura del ejemplo.
</tarea>

<autocritica>
Después de generar la tabla, revisa tu respuesta e indica si faltaron casos límite (como campos vacíos o inyección de scripts). Si faltan, agrégalos e indica cuáles fueron incorporados en la revisión.
</autocritica>

<formato>
Responde únicamente con la tabla en Markdown seguida de la sección de autocrítica.
</formato>
```
