## Proyecto-programador-ispc-2022
proyecto de materia programador


### 3. Introducción a las BD: 
BD: Sistema integrado por un conjunto de programas o aplicaciones que permite guardar un conjunto de información almacenada, que nos permite consultar, insertar, modificar y borrar esa información en forma sistematizada (automatizada/digitalizada).  Una base de datos no implica solamente guardar información, también debe garantizar la integridad de los datos.
SGBD o DBMS (siglas en inglés): Software específico o grupo de programas que permiten crear y administrar BD y además actúa como intermediario entre usuario, aplicaciones y BD. Sirve para definir, construir y manipular una BD. Mantiene la integridad de los datos y permite tanto almacenarlos como posteriormente acceder a ellos de forma rápida y estructurada.


### 4. Sistemas Gestores de Base de Datos:

**3.1 Recursos humanos de las bases de datos.**  
Intervienen muchas personas en el desarrollo y manipulación de una base de datos: 
Informáticos: directivos/as, analistas, administradores/as de las bases de datos, desarrolladores/as o programadores/as y equipo de mantenimiento. 
Usuarios: expertos/as, habituales, ocasionales. 

El Administrador de la Base de Datos DBA: será el encargado de crear los usuarios que se conectarán a la BD. En la administración de una BD siempre hay que procurar que haya el menor número de administradores, a ser posible una sola persona. El objetivo principal de un DBA es garantizar que la BD cumple los fines previstos por la organización y efectuar tareas de explotación como vigilar el trabajo diario colaborando en la información y resolución de las dudas de los usuarios de la BD. 

**3.2 Estructura multicapa.**
El proceso que realiza un SGBD está en realidad formado por varias capas que actúan como interfaces entre el usuario y los datos: 
- Facilidades de usuario  
- Capa de acceso a datos 
- Diccionario de datos 
- Núcleo 
- Sistema operativo   
Este modelo toma como objeto principal al usuario habitual de la base de datos y modela el funcionamiento de la base de datos en una sucesión de capas cuya finalidad es ocultar y proteger la parte interna de las bases de datos. 

**3.3 Funcionamiento del SGBD.**
En esta arquitectura describe los datos a tres niveles de abstracción. En realidad, los únicos datos que existen están a nivel físico almacenados en discos u otros dispositivos. Los SGBD basados en esta arquitectura permiten que cada grupo de usuarios haga referencia a su propio esquema externo. El SGBD debe de transformar cualquier petición de usuario (esquema externo) a una petición expresada en términos de esquema conceptual, para finalmente ser una petición expresada en el esquema interno que se procesará sobre la BD almacenada. El proceso de transformar peticiones y resultados de un nivel a otro se denomina correspondencia o transformación, el SGBD es capaz de interpretar una solicitud de datos. 

**3.4 Formas de ejecución de un SGBD.**  
SGBDs monocapa: El Sistema Gestor se instala en una máquina y los usuarios acceden directamente a esa máquina y ese Sistema Gestor. En estos sistemas no se accede de forma remota a la base de datos.   
SGBDs bicapa: Estructura clásica, la base de datos y su SGBD están en un servidor al cual acceden los clientes. El cliente posee software que permite al usuario enviar instrucciones al SGBD en el servidor y recibir los resultados de estas instrucciones. Para ello el software cliente y el servidor deben utilizar software de comunicaciones en red.   
SGBD de tres o más capas: Es una estructura de tipo cliente/servidor, pero en la que hay al menos una capa intermedia entre las dos. Esa capa se suele encargar de procesar las peticiones y enviarlas al SGBD con el que se comunica.   
