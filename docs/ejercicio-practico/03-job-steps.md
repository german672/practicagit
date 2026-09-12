# 3. Job Steps

## Step 1

```sql
BACKUP DATABASE PracticaAgente
TO DISK = N'C:\SQLBackups\PracticaAgente.bak'
WITH INIT, NAME = N'Respaldo completo - practica SQL Server Agent';
```

Éxito → siguiente paso.

Error → salir del Job e informar error.

Reintentos → `0`.

## Step 2

```sql
INSERT INTO dbo.Bitacora (Mensaje)
VALUES (N'Respaldo ejecutado correctamente por SQL Server Agent');
```

Éxito → terminar reportando éxito.

Fracaso → terminar reportando fracaso.

**Evidencia:** ambos Steps aparecen en el orden correcto.
