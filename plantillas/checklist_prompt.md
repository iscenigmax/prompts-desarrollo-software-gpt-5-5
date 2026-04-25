# Checklist para crear prompts de desarrollo de software

## Contexto técnico

- [ ] Lenguaje definido
- [ ] Framework definido
- [ ] Versión definida
- [ ] Tipo de aplicación definido
- [ ] Base de datos definida si aplica
- [ ] Librerías permitidas o prohibidas definidas

## Resultado esperado

- [ ] Se indica exactamente qué debe entregar el modelo
- [ ] Se define si se necesita código completo, fragmento o explicación
- [ ] Se especifica si debe incluir ejemplos de uso
- [ ] Se especifica si debe incluir pruebas

## Seguridad

- [ ] No se permite SQL concatenado con entradas de usuario
- [ ] Se piden parámetros para consultas SQL
- [ ] Se pide manejo de errores
- [ ] Se evita exponer secretos, cadenas de conexión reales o credenciales
- [ ] Se aclaran efectos secundarios si hay cambios de datos

## Calidad

- [ ] Se piden nombres claros
- [ ] Se evita sobre-ingeniería
- [ ] Se pide compatibilidad con la versión indicada
- [ ] Se piden comentarios solo cuando aportan valor
- [ ] Se piden supuestos explícitos

## Stop rules

- [ ] El modelo sabe cuándo pedir más información
- [ ] El modelo sabe cuándo declarar supuestos
- [ ] El modelo sabe cuándo abstenerse
- [ ] El modelo sabe cuándo detenerse
