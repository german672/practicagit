# Monitoreo y registros

El manual propone cuatro evidencias principales:

1. **Job Activity Monitor:** muestra la actividad y el resultado de la última ejecución.
2. **Bitacora:** confirma que el segundo Step llegó a ejecutarse.
3. **Archivo `.bak`:** confirma que se generó el respaldo.
4. **Job History:** permite revisar ejecuciones, pasos, duración, mensajes y resultado.

También se incluye el **SQL Server Agent Error Log** como apoyo cuando Job History no contiene información suficiente.

## `run_status`

El manual utiliza `sp_help_jobhistory` y señala que:

* `run_status = 1` corresponde a una ejecución exitosa.

Consulta:

```sql
USE msdb;
GO

EXEC dbo.sp_help_jobhistory
    @job_name = N'Job_Mantenimiento_PracticaAgente';
GO
```
