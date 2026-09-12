# Operators y Alerts

## Paso 12 — Crear Operator

En SQL Server Agent → **Operators → New Operator...**

Nombre:

`Operador_PracticaAgente`

Indicar una dirección de correo válida y mantener el operador habilitado.

![Menú de Operator](../.gitbook/assets/24-operator-menu.png)

![Configuración de Operator](../.gitbook/assets/25-operator-general.png)

> Para enviar correos reales, el manual requiere Database Mail configurado.

## Paso 13 — Crear Alert

En **Alerts → New Alert...**

* Name: `Alerta_ErrorGrave_PracticaAgente`
* Type: `SQL Server event alert`
* Database name: `PracticaAgente`
* Severity: `019 - Fatal Error in Resource`

![Menú de Alert](../.gitbook/assets/26-alert-menu.png)

En **Response**:

* marcar `Notify operators`;
* seleccionar `E-mail` para `Operador_PracticaAgente`.

![Respuesta de Alert](../.gitbook/assets/27-alert-response.png)

Resultado esperado: la Alert aparece en Alerts con el Operator como destinatario.
