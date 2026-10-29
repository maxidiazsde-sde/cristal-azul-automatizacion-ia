# Esquema de base de datos — Airtable

Crear una base llamada **Cristal Azul — Gestión Comercial** con estas tablas.

## Tabla 1: Clientes
- `Nombre` — texto de una línea
- `Email` — email
- `Teléfono` — texto (opcional)
- `Empresa` — texto (opcional)
- `Solicitudes` — vínculo a la tabla Solicitudes

## Tabla 2: Solicitudes
- `ID Solicitud` — texto (usar identificador único recibido/generado)
- `Cliente` — vínculo a Clientes
- `Servicio` — selección: Limpieza de vidrios en altura; Limpieza comercial; Otro
- `Ubicación` — texto
- `Mensaje original` — texto largo
- `Origen` — texto
- `Estado` — selección: Pendiente; Datos incompletos; En análisis IA; Esperando aprobación; Aprobado; Rechazado; Enviado; Error
- `Fecha de recepción` — fecha/hora
- `Propuesta IA` — texto largo
- `Aprobado por` — texto
- `Fecha de aprobación` — fecha/hora
- `ID de envío` — texto
- `Error` — texto largo
- `Cliente relacionado` — vínculo a Clientes

## Tabla 3: Registro de errores
- `ID Error` — texto
- `Fecha` — fecha/hora
- `Etapa` — texto
- `ID Solicitud` — texto o vínculo a Solicitudes
- `Mensaje de error` — texto largo
- `Estado de resolución` — selección: Pendiente; Revisado; Resuelto

## Relaciones
- Una persona de Clientes puede estar vinculada a muchas Solicitudes.
- Cada Solicitud puede tener registros de error asociados.
- En n8n se debe gestionar la creación o actualización de registros para evitar clientes duplicados.

## Privacidad
Usa datos ficticios en las pruebas. El enlace compartido debe tener permisos de solo lectura y no exponer información de clientes reales.
