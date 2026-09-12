# 1. Base y Bitacora

Ejecuta:

```sql
CREATE DATABASE PracticaAgente;
GO

USE PracticaAgente;
GO

CREATE TABLE dbo.Bitacora (
    Id INT IDENTITY (1,1) PRIMARY KEY,
    Mensaje NVARCHAR(200) NOT NULL,
    FechaHora DATETIME2 NOT NULL DEFAULT SYSDATETIME()
);
GO
```

Después crea la carpeta:

`C:\SQLBackups`

**Evidencia:** base creada, tabla `dbo.Bitacora` visible y carpeta disponible.
