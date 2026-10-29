# Plan de pruebas

Registrar fecha, número de ejecución, resultado real y captura asociada. No marcar una prueba como aprobada si no se ejecutó.

| N.º | Escenario | Resultado esperado | Resultado real |
|---|---|---|---|
| 1 | Solicitud completa ficticia | Se valida y registra; IA genera borrador; queda esperando aprobación | Pendiente |
| 2 | Falta el email | Se rechaza el procesamiento comercial o se solicita el dato faltante; no se envía correo | Pendiente |
| 3 | Falta ubicación | IA indica que hace falta información; aprobación requerida | Pendiente |
| 4 | Error simulado de API IA | Error registrado; no se envía correo al cliente | Pendiente |
| 5 | Repetición del mismo ID de solicitud | No se genera un segundo envío; se identifica como duplicado | Pendiente |
| 6 | Borrador rechazado por humano | Estado Rechazado; no se contacta al cliente | Pendiente |
| 7 | Borrador aprobado | Gmail envía solo tras aprobación y se registra el resultado | Pendiente |

## Evidencia mínima
Para cada prueba, guardar captura del nodo/ejecución y anotar el resultado. Ocultar emails reales, tokens, claves y datos personales.
