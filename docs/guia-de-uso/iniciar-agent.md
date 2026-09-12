# Iniciar SQL Server Agent

## Paso 1. Abrir SSMS 22

Desde el menú Inicio de Windows, buscar **SQL Server Management Studio 22** y abrirlo.

Resultado esperado: aparece el cuadro de conexión.

![Instalación/apertura de SSMS](../.gitbook/assets/01-ssms-instalacion.png)

## Paso 2. Conectarse al servidor

En el cuadro de conexión:

* **Server name:** `localhost\SQLAGENT`
* **Authentication:** Autenticación de Windows

Después, seleccionar **Conectar**.

![Cuadro de conexión](../.gitbook/assets/02-cuadro-conexion.png)

Resultado esperado: SSMS muestra la instancia en Object Explorer.

## Paso 3. Ubicar SQL Server Agent

Expandir la instancia y localizar **SQL Server Agent** debajo de las carpetas principales.

![Nodo SQL Server Agent](../.gitbook/assets/03-nodo-agent.png)

## Paso 4. Comprobar que Agent está en ejecución

Un icono con flecha verde indica que está iniciado. Si está detenido, hacer clic derecho sobre **SQL Server Agent** y seleccionar **Iniciar**.

![Menú para iniciar Agent](../.gitbook/assets/04-menu-iniciar-agent.png)
