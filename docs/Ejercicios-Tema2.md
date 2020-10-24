# Tema 2: Desarrollo basado en pruebas

## Ejercicio 1: Instalar alguno de los entornos virtuales de node.js (o de cualquier otro lenguaje con el que se esté familiarizado) y, con ellos, instalar la última versión existente, la versión minor más actual de la 4.x y lo mismo para la 0.11 o alguna impar (de desarrollo).

Al emplear .Net Core 3.1 SDK (Software Development Kit) en la realización de mi proyecto, no necesito instalar un entorno virtual. Sin embargo, si explicaré algunos detalles que tuve en cuenta para el manejo de las herramientas empleadas por este framework.
.Net Core SDK me permite desarrollar APIs Web, interfaces de usuario y otras aplicaciones basadas en la nube. Incluye un paquete especial de NuGet, mecanismo compatible con Microsoft para compartir código, que define cómo se crean, alojan y consumen los paquetes para .NET, y proporciona las herramientas para cada uno de esos roles, además, contiene una aplicación de consola.

Características:
- .Net es gratis. No hay tarifas ni costos de licencia, incluso para uso comercial.
- .Net es de código abierto y multiplataforma, con herramientas de desarrollo gratuitas para Windows, Linux, macOS.
- .NET es compatible con Microsoft. Microsoft envía versiones oficiales que se crean y prueban en servidores mantenidos por Microsoft en Azure y son compatibles como cualquier producto de Microsoft.

Entonces, Para probar que se encuentra instalado, ingresando el comando:

![UniTradicional](./img/UniTradicional2.png)

Instalando las herramientas:

``` $ dotnet ef ``` 
(Entity Framework) Core Puede ser instalada como una herramienta global o local. En este caso fue instalada como una herramienta global.

Actualizar las herramientas globales a la última versión

Instalar una versión específica agregando al siguiente comando 

``` $ --version <VERSION>  ``` Ejecutar el siguiente comando para verificar que EF Core CLI tools fue instalada correctamente:

La ubicación predeterminada de los archivos binarios de las herramientas instaladas depende del sistema operativo:

```
OS -Linux/macOS   Path-$HOME/.dotnet/tools
OS -Windows          Path-%USERPROFILE%\.dotnet\tools

```
Usar múltiples entornos en ASP.NET Core
ASP.NET Core configura el comportamiento de la aplicación según el entorno de ejecución mediante una variable de entorno.

Para determinar el entorno de ejecución, ASP.NET Core lee las siguientes variables de entorno:
- DOTNET_ENVIRONMENT
- ASPNETCORE_ENVIRONMENT cuando se llama a ConfigureWebHostDefaults. Las plantillas de aplicación web ASP.NET Core predeterminadas llaman a ConfigureWebHostDefaults. El valor ASPNETCORE_ENVIRONMENT anula DOTNET_ENVIRONMENT.

IHostEnvironment.EnvironmentName se puede establecer en cualquier valor, pero el framework proporciona los siguientes valores:
- Development: el archivo launchSettings.json establece ASPNETCORE_ENVIRONMENT en Desarrollo en la máquina local.
- Staging
- Production : el valor predeterminado si no se han establecido DOTNET_ENVIRONMENT y ASPNETCORE_ENVIRONMENT

Referencia documentación empleada:

[Enlace](https://docs.microsoft.com/en-us/ef/core/miscellaneous/cli/dotnet)

[Enlace](https://docs.microsoft.com/es-es/aspnet/core/fundamentals/environments?view=aspnetcore-3.1)


## Ejercicio 2: Crear una descripción del módulo usando package.json. En caso de que se trate de otro lenguaje, usar el método correspondiente.

## Ejercicio 3: Descargar el repositorio de ejemplo anterior, instalar las herramientas necesarias (principalmente Scala y sbt) y ejecutar el ejemplo desde sbt. Alternativamente, buscar otros marcos para REST en Scala tales como Finatra o Scalatra y probar los ejemplos que se incluyan en el repositorio.

## Ejercicio 4: Para la aplicación que se está haciendo, escribir una serie de aserciones y probar que efectivamente no fallan. Añadir tests para una nueva funcionalidad, probar que falla y escribir el código para que no lo haga. A continuación, ejecutarlos desde mocha (u otro módulo de test de alto nivel), usando descripciones del test y del grupo de test de forma correcta. Si hasta ahora no has subido el código que has venido realizando a GitHub, es el momento de hacerlo, porque lo vamos a necesitar un poco más adelante.

## Ejercicio 5: Ejercicio: Haced los dos primeros pasos antes de pasar al tercero.

