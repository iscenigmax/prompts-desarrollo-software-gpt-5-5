# Prompts para desarrollo de software con GPT-5.5

Colección de prompts estructurados para usar ChatGPT/GPT-5.5 en tareas de desarrollo de software: backend, SQL Server, .NET, debugging, refactorización, arquitectura, testing y documentación técnica.

## Objetivo

Este repositorio ayuda a convertir solicitudes vagas de programación en prompts técnicos claros, reutilizables y verificables.

La estructura base de cada prompt es:

```text
# Role
# Personality
# Goal
# Success criteria
# Constraints
# Output
# Stop rules
```

## Por qué esta estructura funciona

GPT-5.5 está diseñado para tareas complejas de trabajo real, especialmente programación, debugging, análisis, creación de documentos y flujos donde el modelo debe planear, usar herramientas, verificar y continuar hasta completar una tarea.

Por eso, los prompts de este repositorio priorizan:

- Resultado esperado.
- Criterios de éxito verificables.
- Restricciones técnicas y de seguridad.
- Formato de salida claro.
- Reglas para pedir contexto, declarar supuestos o detenerse.

Fuentes oficiales:

- OpenAI: Introducing GPT-5.5: https://openai.com/index/introducing-gpt-5-5/
- OpenAI API: Prompt guidance for GPT-5.5: https://developers.openai.com/api/docs/guides/prompt-guidance?model=gpt-5.5

## Estructura del repositorio

```text
.
├── README.md
├── LICENSE
├── CHANGELOG.md
├── CONTRIBUTING.md
├── docs/
│   ├── guia_uso.md
│   ├── buenas_practicas_gpt_5_5.md
│   ├── estructura_prompt.md
│   ├── presentacion_repositorio.md
│   └── README_original.md
├── prompts/
│   ├── backend/
│   ├── calidad_codigo/
│   ├── arquitectura/
│   ├── documentacion/
│   ├── sql_server/
│   └── dotnet/
├── plantillas/
│   ├── plantilla_prompt.md
│   ├── plantilla_prompt_gpt_5_5.md
│   └── checklist_prompt.md
└── ejemplos/
    └── prompts_completos.md
```

## Índice de prompts

### Backend

- [`prompts/backend/01_api_rest_node.md`](prompts/backend/01_api_rest_node.md)

### Calidad de código

- [`prompts/calidad_codigo/01_refactorizacion_codigo.md`](prompts/calidad_codigo/01_refactorizacion_codigo.md)
- [`prompts/calidad_codigo/02_debugging_errores.md`](prompts/calidad_codigo/02_debugging_errores.md)
- [`prompts/calidad_codigo/03_tests_unitarios.md`](prompts/calidad_codigo/03_tests_unitarios.md)

### Arquitectura

- [`prompts/arquitectura/01_arquitectura_software.md`](prompts/arquitectura/01_arquitectura_software.md)

### Documentación

- [`prompts/documentacion/01_documentacion_tecnica.md`](prompts/documentacion/01_documentacion_tecnica.md)

### SQL Server

- [`prompts/sql_server/01_consultas.md`](prompts/sql_server/01_consultas.md)
- [`prompts/sql_server/02_procedimientos_almacenados.md`](prompts/sql_server/02_procedimientos_almacenados.md)
- [`prompts/sql_server/03_vistas.md`](prompts/sql_server/03_vistas.md)

### .NET y legacy

- [`prompts/dotnet/01_vbnet_framework_40_windows_forms.md`](prompts/dotnet/01_vbnet_framework_40_windows_forms.md)
- [`prompts/dotnet/02_csharp_general.md`](prompts/dotnet/02_csharp_general.md)
- [`prompts/dotnet/03_csharp_adonet_sql_server.md`](prompts/dotnet/03_csharp_adonet_sql_server.md)
- [`prompts/dotnet/04_vbnet_framework_40_aspnet_webforms.md`](prompts/dotnet/04_vbnet_framework_40_aspnet_webforms.md)

## Cómo usar un prompt

1. Elige el prompt según la tarea.
2. Copia el contenido.
3. Agrega el contexto real: código, error, tablas, versión, reglas de negocio o salida esperada.
4. Ejecuta el prompt en ChatGPT.
5. Revisa si cumple los criterios de éxito.
6. Ajusta restricciones o contexto si la respuesta es incompleta.

## Ejemplo rápido

```text
Quiero crear una consulta SQL Server para obtener ventas por cliente entre fechas.

Usa el prompt:
prompts/sql_server/01_consultas.md

Contexto:
Tablas:
- Ventas(IdVenta, IdCliente, Fecha, Total)
- Clientes(IdCliente, Nombre)

Resultado esperado:
- Total vendido por cliente
- Filtro por rango de fechas
- Ordenado por total descendente
```

## Buenas prácticas

- Define lenguaje, framework y versión.
- Incluye entradas y salidas esperadas.
- Declara restricciones de seguridad.
- No incluyas credenciales reales.
- Pide validación o pruebas cuando aplique.
- Usa reglas de detención para evitar respuestas inventadas.

## Licencia

MIT. Consulta [`LICENSE`](LICENSE).
