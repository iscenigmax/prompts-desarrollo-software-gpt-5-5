# Estructura de prompt

Este repositorio usa una estructura base para hacer que las instrucciones sean claras, reutilizables y verificables.

## Role

Define el perfil técnico que debe asumir el modelo.

```text
Eres un desarrollador senior en C# especializado en ADO.NET y SQL Server.
```

## Personality

Define el estilo de colaboración.

```text
Preciso, enfocado en seguridad y manejo de recursos.
```

## Goal

Describe el resultado visible que debe entregar.

```text
Crear una clase en C# para consultar clientes desde SQL Server usando ADO.NET.
```

## Success criteria

Lista criterios verificables.

```text
- Uso de parámetros en consultas
- Manejo correcto de conexiones con using
- Código compilable
- Notas de seguridad incluidas
```

## Constraints

Define límites técnicos, de seguridad o compatibilidad.

```text
- No usar ORM
- No incluir credenciales reales
- Usar solo ADO.NET
```

## Output

Define el formato de respuesta.

```text
- Código C# completo
- Ejemplo de uso
- Explicación breve
- Supuestos realizados
```

## Stop rules

Indica cuándo pedir aclaración, declarar supuestos o detenerse.

```text
- Si falta cadena de conexión o contexto, pedirlo
- Si hay múltiples métodos, usar el más seguro y estándar
```

## Secciones opcionales recomendadas

### Context

Información disponible para resolver la tarea.

### Evidence rules

Reglas para no inventar datos y basarse solo en evidencia proporcionada.

### Validation

Forma de probar, revisar o verificar la respuesta.
