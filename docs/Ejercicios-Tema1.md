# Tema 1: Arquitecturas de software para la nube

## Ejercicio 1: Buscar una aplicación de ejemplo, preferiblemente propia, y deducir qué patrón es el que usa. ¿Qué habría que hacer para evolucionar a un patrón tipo microservicios?

La Tienda utiliza una arquitectura basada en ASP.NET Core microservicios. Las solicitudes HTTP de los clientes a la aplicación web de la tienda para que pueden acceder a los microservicios se enrutan a través de una puerta de enlace API, que es una implementación de Backens-For-Frontends. Las puertas de enlace API mejoran la seguridad y desacoplan los servicios backend de los clientes individuales.
La Tienda incluye las siguientes características
- Catálogo de servicios
- Cesta de Compra
- Gestión de Usuarios
- Gestión de Pedidos
- Pagos
Cada una de las características anteriores se administra con un microservicio distinto. Cada microservicio es autónomo, se puede implementar de forma independiente y es responsable de sus propios datos.


## Ejercicio 2: En la aplicación que se ha usado como ejemplo en el ejercicio anterior, ¿podría usar diferentes lenguajes? ¿Qué almacenes de datos serían los más convenientes?


Esta arquitectura permite que cada microservicio implemente el almacén de datos que esté mejor optimizado para su carga de trabajo, necesidades de almacenamiento y patrones de lectura-escritura. Las opciones dealmacenamiento de datos incluyen relacional, documento y valor-clave.
El servicio de catálogos por ejemplo, almacena sus datos en una base de datos SQL Server en Linux. El servicio de cesta de compra utiliza una cache de Redis para almacenamiento. No existe un único almacén de datos con el que interactúen todos los servicios. En cambio, la comunicación entre servicios se produce según sea necesario, ya sea a través de llamadas API síncronas o de forma asíncrona a través de mensajería. Este aislamiento de datos le da a cada servicio la autonomía para aplicar de forma independiente las actualizaciones del esquema de datos, sin romper otros servicios en el entorno de producción.



