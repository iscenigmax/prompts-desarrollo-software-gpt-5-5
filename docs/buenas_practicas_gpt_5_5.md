# Buenas prácticas para prompts con GPT-5.5

GPT-5.5 puede encargarse de tareas más amplias y ambiguas, pero necesita una definición clara del resultado esperado. Para desarrollo de software, conviene usar prompts orientados a objetivos, restricciones y validación.

Fuentes oficiales:

- https://openai.com/index/introducing-gpt-5-5/
- https://developers.openai.com/api/docs/guides/prompt-guidance?model=gpt-5.5

## Recomendaciones

### 1. Define el resultado, no solo la actividad

Menos útil:

```text
Ayúdame con una API.
```

Mejor:

```text
Diseña e implementa una API REST para gestión de usuarios con Express.js, validación de datos, manejo de errores y ejemplos con curl.
```

### 2. Usa criterios de éxito verificables

Ejemplo:

```text
# Success criteria
- Endpoints CRUD definidos correctamente
- Validación de datos implementada
- Manejo de errores consistente
- Código listo para ejecutarse
```

### 3. Declara restricciones explícitas

Ejemplo:

```text
# Constraints
- Usar SQL Server y T-SQL
- No concatenar entradas de usuario
- No incluir credenciales reales
```

### 4. Pide validación

Para tareas de código, agrega una sección de validación:

```text
# Validation
- Indicar cómo ejecutar el código
- Incluir comandos de prueba
- Mencionar riesgos o supuestos
```

### 5. Usa reglas de detención

Las stop rules evitan que el modelo invente información cuando falta contexto.

Ejemplo:

```text
# Stop rules
- Si falta el esquema de base de datos, pedir tablas y campos
- Si hay ambigüedad menor, declarar supuestos y continuar
- Si el cambio puede afectar datos productivos, advertir antes de proponer ejecución
```
