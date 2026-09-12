# Conceptos básicos

| Concepto             | Explicación                                                                                                                                                               |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SQL Server Agent     | Servicio encargado de ejecutar y automatizar Jobs en una instancia de SQL Server.                                                                                         |
| Job                  | Trabajo automatizado compuesto por una o más acciones que Agent ejecuta en secuencia.                                                                                     |
| Job Step             | Paso individual de un Job. En esta práctica, cada paso ejecuta una instrucción T-SQL.                                                                                     |
| Schedule             | Programación que determina cuándo y con qué frecuencia debe ejecutarse un Job.                                                                                            |
| Job History          | Historial que registra ejecuciones del Job y de sus pasos, incluyendo resultado, fecha, hora, duración y mensajes.                                                        |
| Job Activity Monitor | Ventana de SSMS que permite consultar la actividad actual de los Jobs y, según los permisos, iniciar, detener, habilitar, deshabilitar y revisar propiedades o historial. |
| T-SQL                | Transact-SQL, el lenguaje de SQL Server utilizado en los comandos de los pasos de esta práctica.                                                                          |
| msdb                 | Base de datos del sistema que contiene, entre otros elementos, información utilizada por SQL Server Agent, como Jobs e historial.                                         |
| Alert                | Regla de SQL Server Agent que reacciona ante determinados eventos o niveles de gravedad y puede generar una respuesta.                                                    |
| Operator             | Destinatario de notificaciones de SQL Server Agent, por ejemplo, mediante correo electrónico.                                                                             |
| Proxy                | Mecanismo que permite que determinados tipos de Job Step se ejecuten bajo el contexto de una credencial.                                                                  |
