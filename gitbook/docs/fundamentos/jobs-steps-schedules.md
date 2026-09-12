# Jobs, Steps y Schedules

## Job

El Job de la práctica se llama:

`Job_Mantenimiento_PracticaAgente`

Está compuesto por dos pasos.

## Step 1 — Respaldo

Nombre:

`Respaldo_PracticaAgente`

Tipo:

`Transact-SQL script (T-SQL)`

Base de datos:

`PracticaAgente`

Comando:

```sql
BACKUP DATABASE PracticaAgente
TO DISK = N'C:\SQLBackups\PracticaAgente.bak'
WITH INIT, NAME = N'Respaldo completo - practica SQL Server Agent';
```

## Step 2 — Bitácora

Nombre:

`Registrar_Bitacora`

Comando:

```sql
INSERT INTO dbo.Bitacora (Mensaje)
VALUES (N'Respaldo ejecutado correctamente por SQL Server Agent');
```

## Flujo entre pasos

El Step 1 debe:

* continuar al siguiente paso cuando tiene éxito;
* salir del Job e informar el error cuando falla;
* usar 0 reintentos en esta práctica.

El Step 2 termina reportando éxito o fracaso según corresponda.
