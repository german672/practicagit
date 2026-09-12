# Crear los Job Steps

## Step 1 — Respaldo de `PracticaAgente`

En la página **Steps**, seleccionar **New...**

* Nombre: `Respaldo_PracticaAgente`
* Tipo: `Transact-SQL script (T-SQL)`
* Base de datos: `PracticaAgente`

```sql
BACKUP DATABASE PracticaAgente
TO DISK = N'C:\SQLBackups\PracticaAgente.bak'
WITH INIT, NAME = N'Respaldo completo - practica SQL Server Agent';
```

El manual indica utilizar **Analizar** para comprobar la sintaxis.

![Step de respaldo](../.gitbook/assets/09-step1-respaldo.png)

### Opciones avanzadas

* Acción en caso de éxito: **Ir al siguiente paso**.
* Acción en caso de error: **Salir del trabajo e informar el error**.
* Reintentos: `0`.

![Opciones avanzadas](../.gitbook/assets/10-step1-avanzadas.png)

## Step 2 — Registrar en Bitacora

Crear otro Step:

* Nombre: `Registrar_Bitacora`
* Tipo: `Transact-SQL script (T-SQL)`
* Base de datos: `PracticaAgente`

```sql
INSERT INTO dbo.Bitacora (Mensaje)
VALUES (N'Respaldo ejecutado correctamente por SQL Server Agent');
```

Configurar:

* Éxito: dejar el trabajo reportando éxito.
* Fracaso: dejar el trabajo reportando fracaso.

![Segundo Job Step](../.gitbook/assets/12-step2-bitacora.png)

Resultado esperado: la lista contiene ambos Steps en orden.

![Lista de Job Steps](../.gitbook/assets/11-lista-job-steps.jpeg)
