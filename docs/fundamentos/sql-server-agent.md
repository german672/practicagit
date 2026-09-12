# ¿Qué es SQL Server Agent?

**SQL Server Agent** es el servicio de SQL Server que permite automatizar tareas administrativas mediante **Jobs**.

Un **Job** es una serie de operaciones que SQL Server Agent ejecuta en secuencia. Puede incluir pasos T-SQL, comandos del sistema y otros tipos de acciones. Los Jobs también pueden asociarse a horarios y generar notificaciones.

### Modelo mental

```
SQL Server Agent
      │
      ├── Trabajo(Job)
      │    ├── Paso 1
      │    ├── Paso 2
      │    └── ...
      │
      ├── Programacion
      ├── Historial del trabajo
      ├── Alertas / Operadores
      └── Proxies
```

En la práctica de este manual:

1. El primer paso crea un respaldo de `PracticaAgente`.
2. Si tiene éxito, el segundo paso registra un mensaje en `dbo.Bitacora`.
3. Una programacion permite programar el Job, trabajo.
4. El monitor de actividad, el archivo `.bak`, la tabla y el historial del job sirven como evidencia.
