# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting.
Herramienta de IA usada: (escribe aqui cual usaste)

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo      | Aciertos (de 5) | Formato de la respuesta                   | Todas con el mismo formato (Si/No) |
| --------- | --------------- | ----------------------------------------- | ---------------------------------- |
| Zero-shot | 5               | Texto libre con explicaciones             | No                                 |
| One-shot  | 5               | Lista con comillas y etiquetas            | No                                 |
| Few-shot  | 5               | Formato estricto 'comentario -> Etiqueta' | Si                                 |

## Ejercicio 3: Chain of Thought

| Pedido      | Respuesta de la IA  | Muestra los pasos (Si/No) | Correcta (Si/No) |
| ----------- | ------------------- | ------------------------- | ---------------- |
| Directo     | (el numero que dio) | No                        | (Si/No)          |
| Paso a paso | (el numero que dio) | Si                        | (Si/No)          |

## Ejercicio 4: Role prompting

| Version        | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo          | A quien le sirve mas           |
| -------------- | ------------------------------ | ------------------------------ | ------------------------------ |
| A. Sin rol     | Tecnico                        | Da un ejemplo corto            | Cualquier persona              |
| B. Rol docente | Sencillo                       | Usa la comparacion de una caja | Quien nunca ha programado      |
| C. Rol senior  | Tecnico                        | Usa codigo Java                | Un programador con experiencia |

## Ejercicio 5: Descomposicion

- Paso 1: La IA listo 5 requisitos (registrar productos, controlar stock, etc.).
- Paso 2: Diseno las clases con sus atributos y tipos de dato.
- Paso 3: Escribio la clase Producto con constructor, get y set, coherente con el diseno.
- Paso 4: Propuso 3 mejoras concretas para el codigo.
- Comparacion: El pedido de una sola vez fue mas general, y por pasos pude revisar cada parte antes de seguir.

## Ejercicio 6: Prompt estructurado y autocritica

### Prompt basico

Prompt: "Dame casos de prueba para un login."

### Prompt estructurado y autocritica

```text
<rol>Actua como analista de pruebas de software.</rol>
<contexto>Login web con correo y contrasena. La cuenta se bloquea
despues de 3 intentos fallidos.</contexto>
<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada,
resultado esperado.</formato>

Revisa tu tabla: faltan casos limite como campos vacios, correo sin @
o contrasena con espacios? Agrega los que falten e indica cuales agregaste.
```

### Evaluacion de la tabla final

| Que revisar                                     | Cumple (Si / No) |
| ----------------------------------------------- | ---------------- |
| Tiene las 4 columnas pedidas?                   | Si               |
| Incluye el bloqueo despues de 3 intentos?       | Si               |
| Incluye casos con campos vacios?                | Si               |
| Indica que casos agrego en la autocritica?      | Si               |
| Hay algun caso repetido o que no tenga sentido? | No               |
