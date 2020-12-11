# ShirtStore
MOD10_LAK

## Los objetivos de este programa son:

- Probar una aplicación ASP.NET Core MVC.
- Agregar el manejo de excepciones para los diferentes ambientes. 
- Agregar el registro a una aplicación ASP.NET Core MVC.


Se desarrolla una aplicación ASP.NET Core MVC en un entorno de prueba.
En este ejemplo, crea un proyecto de prueba MSTest y se agregará a la solución. La aplicación 
web ASP.NET Core MVC se agrega a su lista de dependencias y ya se puede probar el modelo Shirt. 

*Etapas en el desarrollo del ejemplo* 

Las principales tareas han sido:

*Primera etapa*

Tareas:
1. Añadir un proyecto de pruebas
2. Escribir una prueba para un modelo
3. Ejecutar la prueba de la unidad - debería fallar
4. Implementar la clase modelo para que la prueba pase
5. Ejecutar la prueba de la unidad - tiene éxito


*Segunda etapa*

Después de crear un proyecto de prueba y probar el modelo, se prueba el controlador.
Para ello, se crea una interfaz de repositorio como una dependencia para que el controlador pueda acceder a los datos. 
Para probar el controlador, se creará un falso repositorio como sustituto, y se le proporcionará al controlador a través de su constructor.

Tareas:
1. Crear un repositorio de interfaz
2. Implementar el repositorio de la interfaz utilizando un repositorio falso
3. Pasar el falso depósito al constructor de un controlador
4. Escribir una prueba para un controlador
5. Ejecutar la prueba de la unidad - debería fallar
6. Implementar la clase de controlador para que la prueba pase
7. Ejecutar la prueba de la unidad - tiene éxito

*Tercera etapa*

Después de que el modelo y el controlador hayan sido probados, se añade una clase de repositorio para que la aplicación pueda ejecutarse. 
En este ejemplo se implementa un repositorio ShirtRepository, que obtendrá datos de una base de datos y actualiza una base de datos. 
El repositorio ShirtRepository se registrará en el método ConfigureService.

Tareas:
1. Implementar el repositorio de la interfaz en una clase de repositorio
2. Registrar el depósito como un servicio
3. Ejecute la aplicación MVC


*Cuarta etapa*

Se añade manejo de excepciones a la aplicación web. Si se produce un error mientras se ejecuta la aplicación, se implementan dos casos de uso: 
- En el caso de que la aplicación se esté ejecutando en un entorno de desarrollo y se produzca un error, el usuario verá una página de error detallada con información sobre dónde encontrar el error. 
- En el caso de que la aplicación se esté ejecutando en un entorno de producción, se mostrará una página personalizada no informativa en la que se indicará que se ha producido un error. Es necesario agregar el manejo de excepciones a cada uno de los casos de uso.

Tareas:
1. Agregar el manejo de excepciones en Startup.cs
2. Crear una excepción temporal para probar
3. Ejecutar la aplicación en el entorno de desarrollo
4. Ejecutar la aplicación en el entorno de producción
5. Eliminar la excepción temporal


*Quinta etapa*

Se utiliza la biblioteca Serilog para registrar los sucesos en la aplicación ASP.NET Core MVC, mientras que se configura el registro por separado utilizando los archivos appsettings.json a los diferentes entornos.
Cualquier registro de trazas en desarrollo se muestra en consola, mientras que cualquier registro a nivel de aviso en producción se escribirá en su archivo dedicado.
Esto también requeriría inyectar el ILogger el controlador, por lo que sería necesario actualizar la prueba del controlador.

Tareas:
1. Añadir el registro a la aplicación MVC
2. Pruebe el controlador usando un marco de burla
3. Ejecutar la prueba de la unidad
4. Ejecutar la aplicación en el entorno de desarrollo
5. Ejecutar la aplicación en el entorno de producción
