# Cristal Azul — Ecosistema de Automatización IA para Consultas y Presupuestos

Proyecto final de automatización: recepción de consultas comerciales, validación de datos, registro en base de datos, análisis asistido por IA, aprobación humana y respuesta por correo.

> **Estado del repositorio:** estructura inicial/documentación preparada. La integración completa debe configurarse y probarse con las cuentas reales antes de presentarse como un sistema operativo.

## Arquitectura prevista

1. **Entrada:** webhook de n8n recibe una solicitud.
2. **Validación:** comprueba campos obligatorios y deriva los datos incompletos a una respuesta controlada.
3. **Base de datos:** Airtable registra clientes, solicitudes, propuestas y errores.
4. **IA:** OpenAI clasifica la consulta y prepara un borrador, sin inventar precios ni prometer disponibilidad.
5. **Aprobación humana:** una persona revisa el borrador antes de contactar al cliente.
6. **Salida:** Gmail envía el mensaje aprobado y se registra el resultado.
7. **Resiliencia:** manejo de errores, estados y control de duplicados.

## Tecnologías

- n8n: orquestación
- Airtable: base de datos
- OpenAI API: procesamiento de lenguaje natural
- Gmail: canal de salida

## Estructura

- `workflow/`: exportación JSON inicial de n8n.
- `database/`: esquema de tablas y campos para Airtable.
- `prompts/`: prompt estructurado de IA.
- `docs/`: documentación y diagrama PDF.
- `tests/`: casos de prueba y resultados a completar.
- `evidencias/`: capturas reales del flujo y ejecuciones.
- `demo/`: guion del video de 3 minutos.

## Configuración pendiente antes de la entrega

- [ ] Crear las tablas en Airtable según `database/esquema_airtable.md`.
- [ ] Conectar Airtable, OpenAI y Gmail en n8n usando credenciales seguras.
- [ ] Completar el flujo con nodos de base de datos, IA, aprobación y correo.
- [ ] Configurar el manejo de errores y la prevención de duplicados.
- [ ] Ejecutar las pruebas cinco veces como mínimo, incluyendo datos incompletos.
- [ ] Añadir capturas reales en `evidencias/`.
- [ ] Añadir el enlace de solo lectura real de Airtable en `database/ENLACE_BASE_DE_DATOS.md`.
- [ ] Exportar desde n8n el JSON final ya probado y reemplazar el archivo inicial.
- [ ] Grabar el video demo y agregar el enlace en `demo/VIDEO_DEMO.md`.

## Seguridad

No guardes API keys, contraseñas, tokens, credenciales ni datos personales reales en este repositorio. Configura las credenciales desde el gestor de credenciales de n8n. Revisa las capturas para ocultar datos sensibles.

## Cómo publicar en GitHub

1. En GitHub, crea un repositorio llamado `cristal-azul-automatizacion-ia`.
2. Elegí visibilidad pública solo si no contiene secretos ni datos personales.
3. Subí el contenido de esta carpeta conservando la estructura.
4. Actualizá los pendientes de este README únicamente después de completar y verificar cada uno.
