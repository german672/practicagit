# Diagnóstico

Cuando el Job falla, sigue este orden:

1. **Job Activity Monitor:** confirma si está ejecutándose y su resultado.
2. **Job History:** identifica el Step que falló y el mensaje.
3. **Ruta del respaldo:** comprueba que `C:\SQLBackups` exista y sea accesible.
4. **T-SQL:** compara exactamente el comando usado con el script de la práctica.
5. **Agent:** confirma que el servicio esté iniciado.
6. **Error Log:** si History no es suficiente, revisa el Agent Log.
7. **Proxy:** solo si el Step involucrado utiliza un subsistema que depende de Proxy.

## Regla práctica

No cambies varios elementos al mismo tiempo. Comprueba primero el punto que corresponde al mensaje de error observado.
