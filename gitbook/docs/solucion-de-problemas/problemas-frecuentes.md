# Problemas frecuentes

| Problema                             | Posible causa                                           | Comprobación                                    | Solución                                                   |
| ------------------------------------ | ------------------------------------------------------- | ----------------------------------------------- | ---------------------------------------------------------- |
| SQL Server Agent no aparece          | Falta de permisos                                       | Comprobar si el nodo está oculto para la cuenta | Usar una cuenta autorizada o solicitar permisos en `msdb`. |
| Agent está detenido                  | Servicio no iniciado                                    | Revisar estado en Object Explorer               | SQL Server Agent → Start.                                  |
| Job no se ejecuta a la hora          | Schedule deshabilitado o Agent detenido                 | Revisar Schedule y servicio                     | Habilitar Schedule y asegurar Agent iniciado.              |
| Step 1 falla                         | No existe `C:\SQLBackups` o la cuenta no puede escribir | Revisar carpeta y Job History                   | Crear carpeta y comprobar permisos.                        |
| Error de sintaxis                    | El T-SQL difiere del script                             | Revisar nombres, ruta, comillas y estructura    | Comparar con el script y usar Analyze.                     |
| Job termina Failed                   | Algún Step falló                                        | Revisar Job History                             | Corregir la causa y ejecutar de nuevo.                     |
| Operator no recibe correo            | Database Mail no configurado o dirección inválida       | Revisar Operator y Database Mail                | Configurar Database Mail y validar dirección.              |
| Alert no se dispara                  | El evento no cumple la condición configurada            | Revisar severidad, base y registro              | Comprobar la configuración de la Alert.                    |
| Proxy falla por permisos             | Falta acceso al subsistema o al Proxy                   | Revisar Proxy, subsistema y Principals          | Conceder solo los accesos necesarios.                      |
| History no da información suficiente | El problema puede estar en Agent                        | Revisar Error Log                               | Abrir `Error Logs → View Agent Log`.                       |
