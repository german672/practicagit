# 7. Historial

Interfaz:

**Job → View History / Ver Historial**

T-SQL:

```sql
USE msdb;
GO

EXEC dbo.sp_help_jobhistory
    @job_name = N'Job_Mantenimiento_PracticaAgente';
GO
```

Buscar:

* `run_status`
* `run_date`
* `run_time`
* `message`

Para la práctica, `run_status = 1` indica éxito.
