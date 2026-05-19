QA API Testing Project – ReqRes API

📌 Descripción del Proyecto

Proyecto de pruebas manuales enfocado en validación de APIs REST utilizando Postman y la API pública de ReqRes.

Durante este proyecto se realizaron pruebas funcionales sobre distintos endpoints para validar:

Métodos HTTP (GET y POST)
Status codes
Estructura JSON
Manejo de errores
Validación de datos
Comportamiento de respuestas de la API

El objetivo fue simular escenarios reales de pruebas QA sobre servicios backend.

🛠 Herramientas utilizadas
Postman
ReqRes API
JSON
HTTP Methods
GitHub
📂 Casos de prueba realizados
✅ GET – Obtener lista de usuarios
Endpoint:
GET https://reqres.in/api/users?page=2
Validaciones realizadas:
Status code 200 OK
Tiempo de respuesta aceptable
Validación de estructura JSON
Verificación de usuarios retornados
Resultado:

✅ Prueba exitosa

✅ POST – Crear usuario
Endpoint:
POST https://reqres.in/api/users
Body:
{
  "name": "Sergio",
  "job": "QA Tester"
}
Validaciones realizadas:
Status code 201 Created
Validación de ID generado
Validación de fecha de creación
Verificación de datos enviados
Resultado:

✅ Usuario creado correctamente

⚠️ POST – Envío de Body vacío
Endpoint:
POST https://reqres.in/api/users
Body:
{}
Validaciones realizadas:
Comportamiento de la API con body vacío
Validación de respuesta del servidor
Resultado observado:

⚠️ La API permite crear registros sin validar campos obligatorios.

Impacto:

Puede generar registros incompletos y afectar integridad de datos.

⚠️ POST – Tipos de datos inválidos
Endpoint:
POST https://reqres.in/api/users
Body:
{
  "name": 12345,
  "job": true
}
Resultado esperado:

La API debería rechazar tipos de datos inválidos.

Resultado actual:

La API acepta valores numéricos y booleanos sin validación.

Impacto:

Riesgo de inconsistencias y datos corruptos en el sistema.

🐞 Bugs identificados

ID	Descripción	Severidad
BUG-01	La API permite crear usuarios con body vacío	Media
BUG-02	La API acepta tipos de datos inválidos	Alta
BUG-03	Falta validación estricta de campos obligatorios	Alta

📊 Habilidades aplicadas

Diseño de pruebas API
Validación de respuestas JSON
Análisis de status codes
Detección de defectos
Documentación QA
Uso de Postman
Pensamiento analítico


👨‍💻 Autor

Sergio Andrés Barragán Caro
QA Tester Junior | Manual Testing | API Testing | Postman | Jira
