# ShirtStore
MOD10_LAK

## Los objetivos de este programa son:

- Probar una aplicación ASP.NET Core MVC.
- Agregar el manejo de excepciones para los diferentes ambientes. 
- Agregar el registro a una aplicación ASP.NET Core MVC.


Se requiere desarrollar una aplicación ASP.NET Core MVC en un entorno de prueba.
En este ejercicio, creará un proyecto de prueba MSTest y lo agregará a la solución, agregará la aplicación 
web ASP.NET Core MVC a su lista de dependencias y luego probará el modelo Shirt. 

El ejercicio se ha desarrollado en tres etapas.

*Primera etapa:* Las principales tareas han sido:

1. Añadir un proyecto de pruebas
2. Escribir una prueba para un modelo
3. Ejecutar la prueba de la unidad - debería fallar
4. Implementar la clase modelo para que la prueba pase
5. Ejecutar la prueba de la unidad - tiene éxito


Después de crear un proyecto de prueba y probar el modelo, se prueba el controlador.
Para ello, se crea una interfaz de repositorio como una dependencia para que el controlador pueda acceder a los datos. 
Para probar el controlador, se creará un falso repositorio como sustituto, y se le proporcionará al controlador a través de su constructor.

Las principales tareas de este ejercicio son las siguientes:

1. Crear un repositorio de interfaz
2. Implementar el repositorio de la interfaz utilizando un repositorio falso
3. Pasar el falso depósito al constructor de un controlador
4. Escribir una prueba para un controlador
5. Ejecutar la prueba de la unidad - debería fallar
6. Implementar la clase de controlador para que la prueba pase
7. Ejecutar la prueba de la unidad - tiene éxito

Escenario

Después de que el modelo y el controlador hayan sido probados, se le ha pedido que añada una clase de repositorio para que la aplicación pueda ejecutarse. En este ejercicio, implementará un repositorio ShirtRepository, que obtendrá datos de una base de datos y actualizará una base de datos. El repositorio ShirtRepository se registrará en el método ConfigureService.

Las principales tareas de este ejercicio son las siguientes:

1. Implementar el repositorio de la interfaz en una clase de repositorio
2. Registrar el depósito como un servicio
3. Ejecute la aplicación MVC


Escenario

Se le ha pedido que añada el manejo de excepciones a la aplicación web. Si se produce un error mientras se ejecuta la aplicación, deben implementarse dos casos de uso: En el caso de que la aplicación se esté ejecutando en un entorno de desarrollo y se produzca un error, el usuario vería una página de error detallada con información sobre dónde encontrar el error. En el caso de que la aplicación se esté ejecutando en un entorno de producción, se mostraría una página personalizada no informativa en la que se indicaría que se ha producido un error. Es necesario agregar el manejo de excepciones a cada uno de los casos de uso.

Las principales tareas de este ejercicio son las siguientes:

1. Agregar el manejo de excepciones en Startup.cs
2. Crear una excepción temporal para probar
3. Ejecutar la aplicación en el entorno de desarrollo
4. Ejecutar la aplicación en el entorno de producción
5. Eliminar la excepción temporal


Scenario

You are required to provide logging to the ASP.NET Core MVC application by using the Serilog library, while configuring the logging separately by using appsettings.json files to the different environments.
Any trace log level logs in development would be displayed to the console, while any warning level logs in production would be written to its dedicated file.
This would also require injecting the ILogger to the controller, thus would require to update the controller’s test.

The main tasks for this exercise are as follows:

1. Add logging to the MVC application
2. Test the controller by using a mocking framework
3. Run the unit test
4. Run the application in the development environment
5. Run the application in the production environment
