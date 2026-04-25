# Guía de uso

## 1. Selecciona el prompt correcto

Busca el archivo que se aproxime a tu tarea real:

- API o backend: `prompts/backend/`
- Refactorización, debugging o tests: `prompts/calidad_codigo/`
- Arquitectura: `prompts/arquitectura/`
- Documentación: `prompts/documentacion/`
- SQL Server: `prompts/sql_server/`
- C#, ADO.NET, VB.NET o Web Forms: `prompts/dotnet/`

## 2. Agrega contexto real

Un buen prompt necesita información concreta:

- Lenguaje y versión.
- Framework.
- Tipo de aplicación.
- Código existente.
- Estructura de tablas.
- Mensajes de error.
- Reglas de negocio.
- Restricciones de seguridad.
- Ejemplo de entrada y salida esperada.

## 3. Revisa el resultado contra los criterios de éxito

No evalúes solo si la respuesta “se ve bien”. Verifica si cumple cada criterio:

- ¿El código compila o es razonablemente ejecutable?
- ¿Respeta la versión indicada?
- ¿Evita credenciales reales?
- ¿Usa parámetros en consultas SQL?
- ¿Incluye pruebas o forma de validación cuando aplica?

## 4. Ajusta y repite

Si la respuesta no es suficiente, agrega más contexto o restricciones. Evita pedir “mejóralo” sin explicar qué falta.
