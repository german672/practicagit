# FAQ

## ¿El Job debe ejecutarse a las 22:00?

No necesariamente. El manual indica 22:00 como ejemplo y permite elegir la hora que se prefiera para la demostración.

## ¿Puedo ejecutar el Job manualmente?

Sí. El procedimiento usa **Start Job at Step...** y permite comenzar desde `Respaldo_PracticaAgente`.

## ¿Cómo sé que funcionó?

Comprueba Activity Monitor, `dbo.Bitacora`, el archivo `.bak` y Job History.

## ¿Qué significa `run_status = 1`?

En el contexto de la consulta mostrada por el manual, significa que la ejecución terminó con éxito.

## ¿Necesito Proxy para este ejercicio?

No para los dos Steps T-SQL principales. El manual incluye Proxy como función complementaria para pasos de tipo CmdExec.

## ¿Necesito Database Mail?

Solo si quieres que el Operator reciba notificaciones reales por correo.
