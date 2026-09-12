# Requisitos previos

Antes de comenzar, el manual requiere:

* Microsoft SQL Server 2025 Developer.
* SQL Server Management Studio 22.
* SQL Server Agent disponible en la instancia local.
* Instancia de referencia: `localhost\SQLAGENT`.
* Permisos suficientes para utilizar SQL Server Agent y crear el Job de práctica.
* Permiso para crear la carpeta `C:\SQLBackups` en el equipo donde se ejecuta el respaldo.

## Comprobación rápida

| Requisito        | Debe existir                       |
| ---------------- | ---------------------------------- |
| SSMS             | Instalado y disponible             |
| Instancia        | `localhost\SQLAGENT`               |
| Agent            | Visible y ejecutable               |
| Base de práctica | Se crea en el paso correspondiente |
| Carpeta          | `C:\SQLBackups`                    |
