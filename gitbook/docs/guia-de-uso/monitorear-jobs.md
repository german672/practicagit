# Comprobar la ejecución

## Opción A — Job Activity Monitor

Dentro de SQL Server Agent, abrir **Job Activity Monitor**.

Buscar `Job_Mantenimiento_PracticaAgente` y comprobar que el resultado de la última ejecución indique **Correcto**.

![Activity Monitor](../.gitbook/assets/18-activity-monitor.png)

![Detalle de actividad](../.gitbook/assets/19-activity-detalle.png)

## Opción B — Bitacora

Ejecutar:

```sql
SELECT * FROM PracticaAgente.dbo.Bitacora;
```

Debe aparecer al menos una fila con el mensaje de éxito y la fecha/hora.

![Consulta de Bitacora](../.gitbook/assets/21-bitacora-consulta.png)

## Opción C — Archivo de respaldo

Comprobar que exista:

`C:\SQLBackups\PracticaAgente.bak`

La fecha de modificación debe coincidir con la ejecución del Job.

![Archivo de respaldo](../.gitbook/assets/20-backup-generado.png)
