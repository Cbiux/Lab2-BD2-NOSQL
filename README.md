# Lab2-BD2-NOSQL
Evaluar y comparar el rendimiento de dos sistemas de bases de datos no relacionales (NoSQL) para las principales operaciones CRUD (Create, Read, Update, Delete), así como documentar de forma clara y detallada el proceso de instalación, preparación del ambiente de desarrollo y los resultados obtenidos.

Instalación de las Bases de Datos
    MongoDB
1.Descarga e instalación:
Se descargó desde su sitio oficial y se instaló utilizando un gestor de paquetes (apt para Linux o choco para Windows).

2.Verificación:
-Se confirmó el funcionamiento del servicio.
-Uso de MongoDB Compass para la administración visual de datos.

3.Creación de la base:
-Base de datos: TransaccionesDB.
-Colección: Transacciones.

    Cassandra
1.Descarga e instalación:
-Instalación siguiendo las instrucciones oficiales.
-Ejecución del servidor desde la consola con el comando adecuado.

2.Configuración inicial:
-Keyspace: TransaccionesDB.
-Creación de la tabla Transacciones con los campos principales (e.g., IdTransaccion, Usuario, Monto).


-----------------------------------------------------------------------

Instalación de Herramientas de Ejecución
Node.js
1.Proceso de instalación:
-Descarga desde Node.js (versión LTS recomendada).
-Ejecución del instalador con la opción "Add to PATH" habilitada.
-Verificación de instalación con:
    -node -v: muestra la versión de Node.js.
    -npm -v: muestra la versión del gestor de paquetes npm.

2.Ejecución del servidor:
-Creación de un archivo JS con lógica de servidor.
-Uso del comando node {ubicacionArchivo/nombreArchivo} para ejecutar el servidor.

Autocannon
1.Instalación:
-Instalación global con npm install -g autocannon.
-Verificación con autocannon -v.
2.Configuración para pruebas:
-Simulación de múltiples conexiones simultáneas y pruebas CRUD en las bases de datos.

-----------------------------------------------------------------------

Implementación de Pruebas
1.Diseño experimental:
-Uso de Autocannon para evaluar las rutas configuradas.
-Pruebas realizadas en escenarios controlados con 10,000 registros en formato JSON.

2.Pruebas específicas:
-Inserción: Se evaluó la latencia, las solicitudes por segundo y la estabilidad.
-Lectura, actualización y eliminación: Se siguió un enfoque similar, destacando métricas clave como bytes transferidos por segundo.

-----------------------------------------------------------------------

    Pasos Detallados para Reproducir
Preparación del Ambiente de Pruebas
-Configurar rutas de servidor accesibles en http://localhost:3000.
-Crear scripts en Node.js para operaciones CRUD.
-Cargar registros JSON con herramientas como Postman.
-Automatizar pruebas con Autocannon.

-----------------------------------------------------------------------

    Información Adicional para el Usuario
1.Uso de Postman:
-Descargar desde su sitio oficial.
-Crear y enviar solicitudes HTTP a las rutas configuradas.

2.Uso de Autocannon:
-Configuración de parámetros como duración, conexiones y métodos HTTP.
-Generación de estadísticas detalladas para comparar rendimiento.