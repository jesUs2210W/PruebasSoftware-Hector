# PruebasSoftware
Ejemplos de pruebas de software: unitarias, integración y API.

## Pruebas agregadas para el examen

- **Unitaria:** `ClienteService.ObtenerPorId` devuelve el cliente esperado y verifica con Moq que `IClienteRepository.ObtenerPorId` se llamó exactamente una vez.
- **Integración:** consulta un identificador inexistente usando el repositorio real y SQLite; el resultado esperado es `null`.
- **API:** consulta un cliente existente y espera `200 OK`; consulta un identificador inexistente y espera `404 Not Found`.

## Ejecutar todas las pruebas

El proyecto está configurado para .NET 8. Desde la carpeta principal, ejecutar:

```bash
dotnet test .\ClienteApp.Tests\ClienteApp.Tests.csproj
```

Para crear las evidencias, abre una terminal en la carpeta del proyecto, ejecuta el comando y toma una captura donde se vea el resumen final con las pruebas aprobadas. También puedes ejecutar desde Visual Studio: **Prueba > Ejecutar todas las pruebas** y capturar el Explorador de pruebas con el resultado.

## Publicar en GitHub

Sube esta carpeta a un repositorio personal nuevo. En GitHub, crea un repositorio vacío y luego, desde esta carpeta, ejecuta los comandos que GitHub muestra para subir un repositorio existente. No subas archivos de base de datos locales ni contraseñas.
