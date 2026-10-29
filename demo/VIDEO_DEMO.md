# Guion del video demo — 3 minutos

**0:00–0:25 | Presentación**
“Este proyecto se llama Cristal Azul y automatiza la gestión de consultas para un negocio de limpieza de vidrios en altura.”

**0:25–0:55 | Entrada**
Mostrar el webhook de n8n y explicar qué datos recibe. Usar una solicitud completamente ficticia.

**0:55–1:25 | Base de datos**
Mostrar Airtable y las tablas Clientes, Solicitudes y Registro de errores. Explicar los estados y las relaciones.

**1:25–1:55 | IA**
Mostrar el nodo de OpenAI y el prompt dinámico. Explicar que el modelo prepara un borrador, no inventa precios y no envía nada por sí solo.

**1:55–2:25 | Aprobación humana y salida**
Mostrar el mecanismo real de aprobación y, si se probó, el envío de Gmail solo después de aprobar. No mostrar credenciales ni información personal.

**2:25–2:50 | Manejo de errores**
Mostrar una prueba de datos incompletos y/o una falla controlada, junto con el registro del error.

**2:50–3:00 | Cierre**
“Este flujo integra orquestación, base de datos, IA y canal de salida, con validación humana y controles de resiliencia.”

## Antes de grabar
- Reemplazar cualquier paso aún no construido.
- Mostrar solo resultados reales.
- Ocultar claves API, tokens, direcciones privadas y datos de clientes.
