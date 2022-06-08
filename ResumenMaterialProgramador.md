## Proyecto-programador-ispc-2022
proyecto de materia programador


### 3. Introducción a las BD: 
**BD:** Sistema integrado por un conjunto de programas o aplicaciones que permite guardar un conjunto de información almacenada, que nos permite consultar, insertar, modificar y borrar esa información en forma sistematizada (automatizada/digitalizada).  Una base de datos no implica solamente guardar información, también debe garantizar la integridad de los datos.

**SGBD o DBMS** (siglas en inglés)**:** Software específico o grupo de programas que permiten crear y administrar BD y además actúa como intermediario entre usuario, aplicaciones y BD. Sirve para definir, construir y manipular una BD. Mantiene la integridad de los datos y permite tanto almacenarlos como posteriormente acceder a ellos de forma rápida y estructurada. EJEMPLOS: MySQL, MariaDB, Microsoft SQL Server, OracleDatabase, mongoDB.

Cuando surgen las BD modelo relacional se estandariza la estructura (ISO y ANSI). Las 3 partes o modelos que componen SGBD:
    -Interno o físico: Datos físicos, archivos RAW (Archivos de lectura y escritura en 0 y 1). Es mitad software y mitad hardware.
    -Conceptual: Se define la estructura de la BBDD, de la aplicación o sistema desarrollado.
    -Externo: Conecta al usuario o aplicación c la base de datos a través de una interfaz gráfica por ejemplo. Es el "Panel de control". Ej: Workbeanch(MySQL),                   Enterprise y SQLDeveloper(Oracle).


### 4. Sistemas Gestores de Base de Datos:

**3.1 Recursos humanos de las bases de datos.**  
Intervienen muchas personas en el desarrollo y manipulación de una base de datos:   
-Informáticos: directivos/as, analistas, administradores/as de las bases de datos, desarrolladores/as o programadores/as y equipo de mantenimiento.   
-Usuarios: expertos/as, habituales, ocasionales. 

El Administrador de la Base de Datos DBA: será el encargado de crear los usuarios que se conectarán a la BD. En la administración de una BD siempre hay que procurar que haya el menor número de administradores, a ser posible una sola persona. El objetivo principal de un DBA es garantizar que la BD cumple los fines previstos por la organización y efectuar tareas de explotación como vigilar el trabajo diario colaborando en la información y resolución de las dudas de los usuarios de la BD. 

**3.2 Estructura multicapa.**
El proceso que realiza un SGBD está en realidad formado por varias capas que actúan como interfaces entre el usuario y los datos: facilidades de usuario, capa de acceso a datos,diccionario de datos,núcleo y sistema operativo.   
Este modelo toma como objeto principal al usuario habitual de la base de datos y modela el funcionamiento de la base de datos en una sucesión de capas cuya finalidad es ocultar y proteger la parte interna de las bases de datos. 

**3.3 Funcionamiento del SGBD.**
En esta arquitectura describe los datos a tres niveles de abstracción. En realidad, los únicos datos que existen están a nivel físico almacenados en discos u otros dispositivos. Los SGBD basados en esta arquitectura permiten que cada grupo de usuarios haga referencia a su propio esquema externo. El SGBD debe de transformar cualquier petición de usuario (esquema externo) a una petición expresada en términos de esquema conceptual, para finalmente ser una petición expresada en el esquema interno que se procesará sobre la BD almacenada. El proceso de transformar peticiones y resultados de un nivel a otro se denomina correspondencia o transformación, el SGBD es capaz de interpretar una solicitud de datos. 

**3.4 Formas de ejecución de un SGBD.**  
-SGBDs monocapa: El Sistema Gestor se instala en una máquina y los usuarios acceden directamente a esa máquina y ese Sistema Gestor. En estos sistemas no se accede de forma remota a la base de datos.   
-SGBDs bicapa: Estructura clásica, la base de datos y su SGBD están en un servidor al cual acceden los clientes. El cliente posee software que permite al usuario enviar instrucciones al SGBD en el servidor y recibir los resultados de estas instrucciones. Para ello el software cliente y el servidor deben utilizar software de comunicaciones en red.   
-SGBD de tres o más capas: Es una estructura de tipo cliente/servidor, pero en la que hay al menos una capa intermedia entre las dos. Esa capa se suele encargar de procesar las peticiones y enviarlas al SGBD con el que se comunica.   

**4. Tipos de Sistemas Gestores de Bases de Datos**  

En la práctica, al definir las bases de datos desde el mundo real hasta llegar a los datos físicos se pasa por los distintos SGBD está en que proporcionan diferentes modelos lógicos.
El modelo conceptual es independiente del DBMS que se vaya a utilizar. El lógico depende de un tipo de SGBD en particular. El modelo lógico está más cerca del modelo físico, el que utiliza internamente el ordenador. El modelo conceptual es el más cercano al usuario, el lógico es el encargado de establecer el paso entre el modelo conceptual y el modelo físico del sistema.  

**4.1 Modelo jerárquico.**
Era utilizado por los primeros SGBD, desde que IBM lo definió para su IMS en 1970. La información se organiza con una jerarquía en la que la relación entre las entidades de este modelo siempre es del tipo padre / hijo. De esta forma hay una serie de nodos que contendrán atributos y que se relacionarán con nodos hijos de forma que puede haber más de un hijo para el mismo padre (pero un hijo sólo tiene un padre). Los datos de este modelo se almacenan en estructuras lógicas llamadas segmentos. Los segmentos se relacionan entre sí utilizando arcos. La forma visual de este modelo es de árbol invertido, en la parte superior están los padres y en la inferior los hijos.   

**4.2 Modelo en red (Codasyl).**
Es un modelo que ha tenido una gran aceptación. En especial se hizo popular la forma definida por Codasyl a principios de los 70 que se ha convertido en el modelo en red más utilizado. El modelo en red organiza la información en registros (también llamados nodos) y enlaces. En los registros se almacenan los datos, mientras que los enlaces permiten relacionar estos datos. Las bases de datos en red son parecidas a las jerárquicas sólo que en ellas puede haber más de un padre.   

**4.3 Modelo relacional.** 
En este modelo los datos se organizan en tablas cuyos datos se relacionan.   

**4.4 Modelo de bases de datos orientadas a objetos.**
La programación orientada a objetos permite cohesionar datos y procedimientos, haciendo que se diseñen estructuras que poseen datos (atributos) en las que se definen los procedimientos (operaciones) que pueden realizar con los datos. En las bases orientadas a objetos se utiliza esta misma idea. A través de este concepto se intenta que estas bases de datos consigan arreglar las limitaciones de las relacionales.   

**4.5 Bases de datos objeto-relacionales.**
Tratan de ser un híbrido entre el modelo relacional y el orientado a objetos. En las bases de datos objeto relacionales se intenta conseguir una compatibilidad relacional dando la posibilidad de integrar mejoras de la orientación a objetos. Estas bases de datos se basan en el estándar SQL 99. En ese estándar se añade a las bases relacionales la posibilidad de almacenar procedimientos de usuario, triggers, tipos definidos por el usuario, consultas recursivas.  

**4.6 Bases de datos NoSQL.** 
Se agrupan las bases de datos pensadas para grabar los datos de manera veloz para así poder atender a miles de peticiones. La idea es que los datos apenas necesitan validarse y relacionarse y lo importante es la disponibilidad de la propia base de datos. El nombre NoSQL, hace referencia a que este modelo de bases de datos rompe con el lenguaje SQL (el lenguaje de las bases de datos relacionales, las bases de datos dominantes hasta la actualidad) para poder manipular los datos con lenguajes de otro tipo.  
