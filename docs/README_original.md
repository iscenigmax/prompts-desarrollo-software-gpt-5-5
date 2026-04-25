# Prompts para desarrollo de software

Este paquete contiene ejemplos de prompts estructurados para tareas comunes de desarrollo de software usando el siguiente esquema:

```text
# Role
# Personality
# Goal
# Success criteria
# Constraints
# Output
# Stop rules
```

## Contenido

- `prompts/01_api_rest_node.md`
- `prompts/02_refactorizacion_codigo.md`
- `prompts/03_debugging_errores.md`
- `prompts/04_arquitectura_software.md`
- `prompts/05_tests_unitarios.md`
- `prompts/06_documentacion_tecnica.md`
- `prompts/07_sql_server_consultas.md`
- `prompts/08_sql_server_procedimientos_almacenados.md`
- `prompts/09_sql_server_vistas.md`
- `prompts/10_vbnet_framework_40_windows_forms.md`
- `prompts/11_csharp_general.md`
- `prompts/12_csharp_adonet_sql_server.md`
- `prompts/13_vbnet_framework_40_aspnet_webforms.md`
- `plantillas/plantilla_prompt.md`
- `plantillas/checklist_prompt.md`

## Cómo crear prompts nuevos

### 1. Define el trabajo real

Antes de escribir el prompt, identifica qué quieres que haga el modelo.

Ejemplos:

- Generar una consulta SQL.
- Refactorizar una clase.
- Crear un procedimiento almacenado.
- Diseñar una API.
- Escribir pruebas unitarias.
- Revisar código legacy.
- Crear una página ASP.NET Web Forms.

Evita objetivos vagos como “ayúdame con código”. Es mejor escribir “genera un procedimiento almacenado en SQL Server para registrar una venta con transacción y validación de stock”.

---

### 2. Escribe el `Role`

El `Role` define quién debe ser el modelo para esa tarea.

Debe incluir:

- Especialidad técnica.
- Tecnología principal.
- Nivel de experiencia esperado.
- Contexto si aplica.

Ejemplo:

```text
# Role
Eres un desarrollador senior en VB.NET Framework 4.0 especializado en aplicaciones ASP.NET Web Forms legacy.
```

---

### 3. Define la `Personality`

Aquí defines el estilo de colaboración.

Puedes usar palabras como:

- Preciso
- Directo
- Pragmático
- Conservador
- Orientado a seguridad
- Enfocado en rendimiento
- Didáctico
- Crítico pero constructivo

Ejemplo:

```text
# Personality
Pragmático, claro, cuidadoso con compatibilidad legacy y mantenimiento.
```

---

### 4. Especifica el `Goal`

El `Goal` debe describir el resultado visible que quieres obtener.

Ejemplo:

```text
# Goal
Crear una página ASP.NET Web Forms en VB.NET Framework 4.0 para consultar clientes por nombre y mostrar los resultados en un GridView.
```

---

### 5. Define `Success criteria`

Los criterios de éxito indican cuándo la respuesta ya está completa.

Ejemplo:

```text
# Success criteria
- Código compatible con .NET Framework 4.0
- Consulta SQL parametrizada
- Manejo básico de errores
- Separación entre .aspx y code-behind
```

Usa esta sección para evitar respuestas incompletas.

---

### 6. Agrega `Constraints`

Los constraints son límites técnicos, de negocio o seguridad.

Ejemplos:

```text
# Constraints
- Usar SQL Server y T-SQL
- No usar SQL dinámico salvo que sea necesario
- No concatenar valores de usuario en consultas SQL
- No usar características posteriores a .NET Framework 4.0
```

Esta sección es especialmente importante cuando trabajas con sistemas legacy o bases de datos productivas.

---

### 7. Define el formato en `Output`

Indica cómo quieres recibir la respuesta.

Ejemplo:

```text
# Output
- Código .aspx
- Código .vb code-behind
- Consulta SQL usada
- Explicación breve
```

Mientras más claro sea el formato, más fácil será revisar y usar la respuesta.

---

### 8. Escribe `Stop rules`

Las stop rules indican cuándo el modelo debe detenerse, preguntar, asumir o abstenerse.

Ejemplo:

```text
# Stop rules
- Si falta el esquema de base de datos, pedir tablas y campos
- Si hay ambigüedad menor, declarar supuestos y continuar
- Si el cambio puede afectar datos productivos, advertir antes de proponer ejecución
```

---

## Reglas prácticas

### Para SQL Server

Incluye siempre que puedas:

- Tablas involucradas
- Campos relevantes
- Volumen aproximado de datos
- Índices existentes
- Versión aproximada de SQL Server
- Ejemplo de entrada y salida esperada

Buen prompt:

```text
Genera una consulta en SQL Server para obtener ventas por cliente entre fechas. Las tablas son Ventas(IdVenta, IdCliente, Fecha, Total) y Clientes(IdCliente, Nombre). Debe filtrar por rango de fechas y ordenar por Total descendente.
```

---

### Para VB.NET Framework 4.0 / ASP.NET Web Forms

Incluye:

- Página o control afectado
- Eventos esperados
- Controles Web Forms usados
- Si usa GridView, DropDownList, TextBox, Button, etc.
- Fuente de datos
- Restricciones de compatibilidad

Buen prompt:

```text
Crea una página ASP.NET Web Forms en VB.NET Framework 4.0 con TextBox, Button y GridView para buscar clientes por nombre en SQL Server usando parámetros.
```

---

### Para C#

Incluye:

- Versión de .NET
- Tipo de aplicación
- Librerías permitidas
- Si debe usar ADO.NET, Entity Framework, LINQ, etc.
- Manejo de errores esperado

Buen prompt:

```text
Crea una clase en C# para consultar pedidos desde SQL Server usando ADO.NET, parámetros y using para liberar conexiones.
```

---

## Plantilla rápida

Copia esta estructura y reemplaza los campos:

```text
# Role
Eres un [perfil técnico] especializado en [tecnología/contexto].

# Personality
[tono y estilo de trabajo]

# Goal
[resultado concreto que quiero obtener]

# Success criteria
- [criterio 1]
- [criterio 2]
- [criterio 3]

# Constraints
- [restricción técnica]
- [restricción de seguridad]
- [restricción de compatibilidad]

# Output
- [sección esperada 1]
- [sección esperada 2]
- [sección esperada 3]

# Stop rules
- Si falta [información], pedirla
- Si hay ambigüedad menor, declarar supuestos
- Si no es seguro continuar, explicar por qué
```

## Checklist antes de usar un prompt

Antes de enviar un prompt, revisa:

- ¿La tecnología está clara?
- ¿La versión está clara?
- ¿El resultado esperado está claro?
- ¿Hay restricciones de seguridad?
- ¿El formato de salida está definido?
- ¿El modelo sabe cuándo pedir aclaración?
- ¿Hay ejemplos de entrada/salida?
- ¿Se indica si puede asumir o no?

## Recomendación

Para mejores resultados, combina el esquema con contexto real:

- Código existente.
- Estructura de tablas.
- Mensajes de error.
- Reglas de negocio.
- Restricciones de versión.
- Ejemplo de resultado esperado.

Un prompt bien estructurado reduce respuestas genéricas y mejora la precisión técnica.
