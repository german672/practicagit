# Buenas prácticas

Estas recomendaciones se mantienen dentro del alcance del manual:

* Usa una base de práctica pequeña y controlada.
* Verifica que SQL Server Agent esté iniciado antes de probar el Schedule.
* Usa **Analyze** para comprobar los scripts T-SQL.
* Comprueba la ruta `C:\SQLBackups` antes de ejecutar el respaldo.
* Revisa Activity Monitor y Job History después de una ejecución.
* Conserva la evidencia del archivo `.bak` y de `Bitacora`.
* No publiques contraseñas, secretos ni credenciales reales en GitHub.
* Usa Proxy solo cuando el tipo de Step lo requiera.
* Si no hay suficiente información en Job History, revisa el Error Log.
