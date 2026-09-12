# Alerts, Operators y Proxies

Estas funciones aparecen en el manual como componentes complementarios.

## Operator

Nombre usado:

`Operador_PracticaAgente`

Debe tener una dirección de correo válida si se desea enviar notificaciones por correo.

> Para recibir correos reales, el manual indica que es necesario tener **Database Mail** configurado en la instancia.

## Alert

Nombre:

`Alerta_ErrorGrave_PracticaAgente`

Configuración del manual:

* Type: `SQL Server event alert`
* Database name: `PracticaAgente`
* Severity: `019 - Fatal Error in Resource`

En **Response** se marca `Notify operators` y se selecciona `E-mail` para `Operador_PracticaAgente`.

## Proxy

El manual muestra un Proxy para pasos de tipo **CmdExec**, asociado a una Credential.

El ejemplo de credencial contiene una contraseña ilustrativa. **No debe publicarse una contraseña real en GitHub.** Sustitúyela por una cuenta y secreto seguros si vas a ejecutar esa parte.

```sql
USE master;
GO

CREATE CREDENTIAL CredencialPracticaAgente
  WITH IDENTITY = N'NOMBRE_EQUIPO\usuario_practica',
  SECRET = N'<CONTRASEÑA_NO_PUBLICAR>';
GO

USE msdb;
GO

EXEC dbo.sp_add_proxy
  @proxy_name = N'Proxy_PracticaAgente',
  @credential_name = N'CredencialPracticaAgente',
  @description = N'Proxy de practica para pasos de tipo CmdExec';
GO

EXEC dbo.sp_grant_proxy_to_subsystem
  @proxy_name = N'Proxy_PracticaAgente',
  @subsystem_name = N'CmdExec';
GO
```

> Los dos Steps principales de esta práctica son T-SQL. El Proxy se documenta porque forma parte del manual, pero no es necesario para ejecutar esos dos Steps.
