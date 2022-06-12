## Proyecto-programador-ispc-2022
 proyecto de materia programador


### Historia y evolución de los SGBD II
Década de los 80 – SGBD Relacionales:
En los '80 se desarrolló SQL (lenguaje de consulta de estructura), un lenguaje que permite consultar y hacer modificaciones (dentro de una base de datos) de forma relativamente sencilla.
Permitía analizar gran cantidad de datos y especificar varios tipos de operaciones con una misma información.
Imponiéndose frente a los SGBD (sistemas gestores de base de datos) anteriores como IMS de IBM, IDS de Bull y DMS de Univac, entre otros, que eran totalmente centralizados y demasiado complejos e inflexibles, cuya utilización requería un personal muy cualificado.
SQL comenzó a ser el modelo estándar de las industrias con su base de datos bajo un sistema de tablas (filas y columnas) ya que su nivel de programación era sencillo y su nivel relativamente bajo. El sistema de bases de datos relacionales fue un éxito comercial y como también lo fue la venta de ordenadores estimulando el mercado de las BD.
El dominio de Oracle en el mercado fue casi total hasta la aparición de SQL Server de Microsoft. Posteriormente durante los '90 fueron apareciendo nuevos sistemas de SGBD Relacionales como PostgreSQL, My SQL y Firebird gestando así las BD orientadas a objetos.

Década de los 90: Distribución, C/S y 4GL:
A finales de los '80 y principios de los '90 el sector empresarial se encontró con que debido a la gran cantidad de BD y SGBD surge la necesidad de tener una visión global que Permitir interrelacionar las diferentes aplicaciones y las distintas BD

### Pude MODIFICAR TXT

Continuará…


### 3. Introducción a las BD: 
**BD:** 

Sistema integrado por un conjunto de programas o aplicaciones que permite guardar un conjunto de información almacenada, que nos permite consultar, insertar, modificar y borrar esa información en forma sistematizada (automatizada/digitalizada).  Una base de datos no implica solamente guardar información, también debe garantizar la integridad de los datos.

**SGBD o DBMS** (siglas en inglés)**:** 

Software específico o grupo de programas que permiten crear y administrar BD y además actúa como intermediario entre usuario, aplicaciones y BD. Sirve para definir, construir y manipular una BD. Mantiene la integridad de los datos y permite tanto almacenarlos como posteriormente acceder a ellos de forma rápida y estructurada. EJEMPLOS: MySQL, MariaDB, Microsoft SQL Server, OracleDatabase, mongoDB.  

Cuando surgen las BD modelo relacional se estandariza la estructura (ISO y ANSI). Las 3 partes o modelos que componen SGBD:


    -Interno o físico: Datos físicos, archivos RAW (Archivos de lectura y escritura en 0 y 1). Es mitad software y mitad hardware.
    
    -Conceptual: Se define la estructura de la BBDD, de la aplicación o sistema desarrollado.
    
    -Externo: Conecta al usuario o aplicación c la base de datos a través de una interfaz gráfica por ejemplo. Es el "Panel de control". Ej: Workbeanch(MySQL), Enterprise y SQLDeveloper(Oracle).


### 4. Sistemas Gestores de Base de Datos:

**1.1 Sistemas de Información orientados a procesos.**

Éstos consistían en un conjunto de programas que definían y trabajaban sus propios datos. Los datos se
almacenan en archivos y los programas manejan esos archivos para obtener la información. Si la
estructura de los datos de los archivos cambia, todos los programas que los manejan se deben
modificar.
La definición de los datos se encuentra codificada dentro de los programas de
aplicación en lugar de almacenarse de forma independiente, y además el control del acceso y la
manipulación de los datos vienen impuesto por los programas de aplicación.

La única ventaja, es que los procesos son independientes por lo que la modificación de uno no
afectaba al resto. 

Inconvenientes de un sistema de gestión de archivos:

- Redundancia e inconsistencia de los datos: se produce porque los archivos son creados por
distintos programas y van cambiando a lo largo del tiempo, es decir, pueden tener distintos
formatos y los datos pueden estar duplicados en varios sitios.

- Dependencia de los datos física-lógica: Cualquier cambio en esa estructura implica al programador identificar, modificar y probar todos los
programas que manipulan esos archivos.

- Dificultad para tener acceso a los datos: Cada vez que se necesite una consulta que no fue prevista en el inicio implica la necesidad de codificar el programa
de aplicación necesario. 

- Separación y aislamiento de los datos: Al estar repartidos en varios archivos, y tener
diferentes formatos, es difícil escribir nuevos programas que aseguren la manipulación de los datos
correctos.

- Dificultad para el acceso concurrente: En un sistema de gestión de archivos es
complicado que los usuarios actualicen los datos simultáneamente.

- Dependencia de la estructura del archivo con el lenguaje de programación: pues la
estructura se define dentro de los programas. Esto implica que los formatos de los archivos sean
incompatibles.

- Problemas en la seguridad de los datos: Ya que cada aplicación se crea independientemente; es por tanto muy difícil establecer criterios de
seguridad uniformes. 

- Problemas de integridad de datos (datos inconsistentes): El mismo dato puede tener valores distintos según qué aplicación
acceda a él.


**1.2 Sistemas de Información orientados a los datos. Bases de Datos.** 

En esos sistemas los datos se almacenan en una única estructura lógica que es utilizable por las aplicaciones. 
A través de esa estructura se accede a los datos que son comunes a todas las aplicaciones.
Cuando una aplicación modifica un dato, dicho dato la modificación será visible para el resto de
aplicaciones. 

Ventajas

- Independencia de los datos y los programas y procesos. Esto permite modificar los datos
sin modificar el código de las aplicaciones.

- Menor redundancia. No hace falta tanta repetición de datos. Sólo se indica la forma en la que se
relacionan los datos.

- Integridad de los datos. Mayor dificultad de perder los datos o de realizar incoherencias con
ellos.

- Mayor seguridad en los datos. Al permitir limitar el acceso a los usuarios. Cada tipo de usuario
podrá acceder a unas cosas.

- Datos más documentados. Gracias a los metadatos que permiten describir la información de la
base de datos.

- Acceso a los datos más eficiente. La organización de los datos produce un resultado más
óptimo en rendimiento.

- Menor espacio de almacenamiento. Gracias a una mejor estructuración de los datos.

- Acceso simultáneo a los datos. Es más fácil controlar el acceso de usuarios de forma
concurrente. 


Desventajas

- Instalación costosa. El control y administración de bases de datos requiere de un software y
hardware poderoso.

- Requiere personal cualificado. Debido a la dificultad de manejo de este tipo de sistemas.

- Implantación larga y difícil. Debido a los puntos anteriores. La adaptación del personal es
mucho más complicada y lleva bastante tiempo.

- Ausencia de estándares reales. Lo cual significa una excesiva dependencia hacia los sistemas
comerciales del mercado. 



**2. Arquitectura de los Sistemas Gestores de Bases de Datos**

Un SGBD es el software que permite a los usuarios procesar, describir, administrar y recuperar los datos almacenados en una base de datos. 
Entre las herramientas que proporciona están:

- Herramientas para la creación y especificación de los datos: Especificación de la estructura, el tipo de los datos, las restricciones y relaciones
entre ellos mediante lenguajes de definición de datos. Toda esta información se almacena en el
diccionario de datos.

- Herramientas para administrar y crear la estructura física: requerida en las unidades de
almacenamiento.

- Herramientas para la manipulación de los datos: de las bases de datos, para añadir,
modificar, suprimir o consultar datos.

- Herramientas de recuperación: en caso de desastre.

- Herramientas para la creación de copias de seguridad: para restablecer la información en
caso de fallos en el sistema.

- Herramientas para la gestión de la comunicación: de la base de datos.

- Herramientas para la creación de aplicaciones: que utilicen esquemas externos de los datos.

- Herramientas de instalación: de la base de datos.

- Herramientas para la exportación e importación: de datos. 


**2.1 Niveles de abstracción de una base de datos.** 

Nivel externo o de visión: es el más cercano a los usuarios, se describen varios
esquemas externos o vistas de usuarios. Cada esquema describe la parte de la BD que interesa a un
grupo de usuarios.
Los esquemas externos los realizan las programadoras.
El conjunto de todas las vistas de usuario es lo que se denomina esquema externo
global. 

-Nivel interno o físico: Esta es la forma en la que realmente están almacenados los datos.  Describe la estructura física de la BD mediante un esquema interno. Este
esquema se especifica con un modelo físico y describe los detalles de cómo se almacenan físicamente los datos: los archivos que contienen la información, su organización, 
los métodos de acceso a los registros, los tipos de registros, la longitud, los campos que los componen, etcétera.
Esta visión sólo la requiere el administrador.

-Nivel conceptual: Ese nivel se sitúa entre el físico y el externo. Se trata de un esquema teórico de los datos en el que figuran organizados en estructuras reconocibles
del mundo real y en el que también aparece la forma de relacionarse los datos. Este esquema es el paso que permite modelar un problema real a su forma correspondiente en el ordenador.



**3. Componentes de los Sistemas Gestores de Bases de Datos** 

Lenguajes de los SGBD

  -Lenguaje de definición de datos (LDD o DDL): se utiliza para especificar el esquema de la BD, las
vistas de los usuarios y las estructuras de almacenamiento.
Es el que define el esquema conceptual y el esquema interno. Lo utilizan los diseñadores y los
administradores de la BD. 

Permite definir las tres estructuras de la base de datos
(relacionadas con los tres niveles de abstracción).

• Estructura interna
• Estructura conceptual
• Estructura externa 

La función de definición sirve pues para crear, eliminar o modificar metadatos.

Mediante ese lenguaje:
• Se definen las estructuras de datos
• Se definen las relaciones entre los datos
• Se definen las reglas que han de cumplir los datos

  -Lenguaje de manipulación de datos (LMD o DML): se utilizan para leer y actualizar los datos de la
BD. Es el utilizado por los usuarios para realizar consultas, inserciones, eliminaciones y modificaciones.
Los hay procedurales, en los que el usuario será normalmente un programador y especifica las
operaciones de acceso a los datos llamando a los procedimientos necesarios. Estos lenguajes acceden a
un registro y lo procesan.
Las sentencias de un DML procedural están embebidas en un lenguaje de alto nivel llamado anfitrión.
Las BD jerárquicas y en red utilizan estos DML procedurales.
Mediante ese lenguaje se puede:
• Añadir datos
• Eliminar datos
• Modificar datos
• Buscar datos
Actualmente se suele distinguir aparte la función de buscar datos en la base de datos (función de
consulta). Para lo cual se proporciona un lenguaje de consulta de datos o DQL.

  -Lenguaje de control de datos (LCD o DCL): Mediante esta función los administradores poseen
mecanismos para proteger los datos; de modo que se permite a cada usuario ver ciertos datos y otros
no; o bien usar ciertos recursos concretos de la base de datos y prohibir otros. El lenguaje que implementa
esta función es el lenguaje de control de datos o DCL.

  -No procedurales son los lenguajes declarativos. En muchos SGBD se pueden introducir
interactivamente instrucciones del LMD desde un terminal, también pueden ir embebidas en un lenguaje
de programación de alto nivel. Estos lenguajes permiten especificar los datos a obtener en una consulta,
o los datos a modificar, mediante sentencias sencillas.

**3.1 Recursos humanos de las bases de datos**

*Informáticos*
Lógicamente son los profesionales que definen y preparan la base de datos.

- Directivos/as. Organizadores y coordinadores del proyecto a desarrollar y máximos responsables
del mismo.

- Analistas. Son los encargados de controlar el desarrollo de la base de datos aprobada por la
dirección. Normalmente son además los diseñadores de la base de datos y los directores de la programación de la misma.

- Administradores de las bases de datos. Encargados de crear el esquema interno de la
base de datos, que incluye la planificación de copia de seguridad, gestión de usuarios y permisos y
creación de los objetos de la base de datos.

- Desarrolladores o programadores. Encargados de la realización de las aplicaciones de
usuario de la base de datos.

- Equipo de mantenimiento. Encargados de dar soporte a los usuarios en el trabajo diario.

*Usuarios*

- Expertos. Utilizan el lenguaje de manipulación de datos (DML) para acceder a la base de
datos.

- Habituales. Utilizan las aplicaciones creadas por los desarrolladores para consultar y actualizar los
datos.

- Ocasionales. Son usuarios que utilizan un acceso mínimo a la base de datos a través de una
aplicación que permite consultar ciertos datos.


*El Administrador de la Base de Datos DBA*  

Será el encargado de crear los usuarios que se conectarán a la BD. En la administración de una BD siempre hay que procurar que haya el menor número de administradores, a ser posible una sola persona.  
El objetivo principal de un DBA es garantizar que la BD cumple los fines previstos por la organización y efectuar tareas de explotación como vigilar el trabajo diario colaborando en la información y resolución de las dudas de los usuarios de la BD. 

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

### 5. Diseño de Base de Datos Relacionales:

3.4 **Diseño Físico**

El objetivo del diseño fisico es implementar el diseño de una base de datos en un SGBD.

Se establecen índices que son estructura de datos que facilitan el acceso o la consulta de datos. Y se organizan en base a campos relacionados.

Los indices poseen dos campos:

- valor de la clave 
- Dirección Fisica del registro

El lado negativo es que el índice debe actualizarse cuando una tabla sufra una modificación.

Por último, pueden llevar valores nulos o no y pueden indicar elementos que no so repetidos.

3.5 **Restricciones de Integridad.**

Este tipo de restricciones ayudan a cuidar la consistencia semántica de los datos.

Los tipos de restricciones de integridad en una base de datos se pueden resumir en:

-Claves
-Cardinalidad de la relación
-Restrcciones de los dominios
-Integridad referencial
-Participación total
-Dependencia funcionales
-Otras restricciones

Para esto se utilizan los siguientes mecanismos:

-Declaracion de claves
-Declaracion de integridad referencial
-Declaracion de tipo de cardinalidad
-Disparadores (Triggers)

3.5.1 **Restricciones de los dominios.**

En esta restriccione se establece un dominio de valores posibles.

No solo permite verificar los valores introducidos sino que aseguramos que la consulta tenga sentido por medio de comparaciones.

* Restricciones de existencia

Esta se utiliza para evitar la aparicion de valores nules. Y para la definicion de la tabla se utilizaría NOT NULL.

- Restrcciones de unicidad

Esta restriccion evita la aparicion de valores duplicados en las columnas.

3.5.2 **Restriccines de integridad referencial**

   La integridad referencial permite asegurar que un valor que aparece en una relación para un conjunto de atributos determinado aparezca también en otra relación para ese mismo conjunto de atributos.

Este tipo de restricciones se denota simplificadamente:

Relación1.(Atributo1-1,...,Atributo1-N) ⊆
Relación2.(Atributo2-1,...,Atributo2-N)

De forma que si quedan tuplas colgantes la actualización se rechace como error o se aplica en cascada similar al borrado.

3.5.3 **Dependencias Funcionales**

Es una propiedad semantica que determina el diseñador, y determina un conjunto de atributos a partir de otr conjunto de atributos.

Esto evita la redundancia de valores no deseables. La dependencis funcionales se denotan de la siguiente forma:

Conunto de atributos que determinan ---> Conjunto de atributos determinados.

3.5.4 **Disparadores**

Los disparadores son mecanismos útiles para implementar restricciones de integridad, alertar a los usuarios o para realizar de manera automática ciertas tareas cuando se 
cumplen determinadas condiciones.

Un ejemplo sería indicar cuándo se ha alcanzado un stock minimo de un producto el cual se debera reponer.


3.6 **Normalización**

Es un proceso de análisis y diseño que se utiliza para evitar redundancia de datos  y las anomalías que estan producen.

Un esquema de relación puede estar en distintas formas normales dependiendo del grado de descomposición que se haya realidado.

3.6.1 **Redundancia de datos**

El objetivo del diseño de la base de datos es agrupar atributos en relaciones de forma que reduzca la redundancia de datos y así el espacio de almacenamiento requeridoa.

3.6.2 **Anomalías de actualizacíón**

Pueden ser de tres tipos

* Anomalias de inserción: Se produce cuando se incerta una nueva fila sin respetar las dependencias funcionales. O cuando cuando se imposibilita
añadir nuevos datos para una dependencia funcional sin que existan antecedentes
para ella.

* Anomalías de modificación: Se produce cuando se modifican columnas con datos redundantes en un sólo subconjunto de filas con el mismo dato.

*Anomalías de eliminación: Se produce cuando se eliminan todas las filas en las que aparecen los datos redundante. Por lo que se pierde los datos de la dependencia funcional.

3.6.3 **Formas normales y normalización**

Se refiere a la mejor forma normal de diseñar un esquema relacional indicando así el grado hasta el que se ha normalizado. Se deben cumplir dos propiedades.

* La propiedad de preservación de dependencias.

* La propiedad de la posibilidad de reproducir la información de la tabla original.

las formas normales más habituales son:

-Primera (1FN)
-Segunda (2FN)
-Tercera (3FN)
Boyce/Codd (FNBC)

3.6.4 **Primera forma normal**

Se estabece que los dominios de los atributos sólo pueden ser atómicos, para evitar atributos multivalorados, compuestos y sus combinaciones.

Para esto es factible eliminar atributos, crear nuevas relaciones, ampliar la clave de la relación.

3.6.5 **Segunda forma normal**

Se dice que una relación esta en segunda forma normal si cada atributo que no forma parte de la clave primaria depende funcional y completamente de cada clave.

El procedimiento de normalización es crear tantas nuevas relacines como  dependencias funcionales no sean completas.

3.6.6 **Tercera forma normal**

Se basa en el concepto de dependencia funcinal transitiva. Un esquema en tercera forma normal si satisface la segunda forma normal y ninuno de los atributos que no froman parte de una clave candidata depende transitivamente
de la clave primaria.

El procedimiento para normalizar esta relación consiste en descomponerla en los atributos definidos por la dependencia funcional.

3.6.7 **Forma normal de Bpyce-Codd**

Esta forma se propuso como una forma más simple que la tercera forma normal, pero en realidad es más estricta porque cada relación en FNBC está en 3FN. Sin embargo
esto último no se cumple a la inversa.

3.6.8 **Desnormalización para el rendimiento**

El proceso de tomar un esquema normalizado y hacerlo no normalizado se denomina desnormalización, y los diseñadores lo utilizan para ajustar el rendimiento de los 
sistemas para dar soporte a las operaciones críticas en el tiempo.

3.7 **Normativa de denominación**

Es una colección de reglas que permite asignar nombres a identificadores y objetos. El objetivo es que los nombres que se elijan identifiquen de forma lo más clara 
posible el significado del elemento al que se refiere el nombre.

3.7.1 **Identificadores**

Se construyen de números y letras. Y se utilizan las siguientres relgas:

* Separar cada palabra por un caracter de subrayado. Ejemplo, Nombre_del_paciente.

*Separar cada palabra ponendo la primera letra de cada una en mayúscula. Ejemplo, NombreDelPaciente.

3.7.2 **Tablas**

Las tablas representan entidades y sus nombres deberían describir las entidades que representan.

Las reglas son:

* Seleccionar nombres de tablas basados en los nombres posibles para las entidades involucradas.

* Usar sustantivos.

* Asegurarse de que tengan un sentido intuitivo.

* Algunas tablas no representan entidades sino su relación, pero puede utilizarse el nombre de las dos tablas asociadas para describirla.

3.7.3 **Restricciones**

 Las restricciones se pueden denominar de forma autoinperativas. Hay que utilizar una abreviatura de dos letras para identificar la naturaleza de la restricción.

* CP para clave principal.

* IR para integridad referencial.

* CO para la de comprobación.

* UN para la de unicidad.

Cuando están involucradas dos tablas hay que hacer que el segundo elemento del nombre sea la tabla con la clave externa y que el tercer elemento sea la tabla donde reside 
la clave principal.

Ejemplo, CO_Médicos_FormatoCódigo.

3.7.4 **Controles**

Cada tipo de control se debería denominar con una indicación del tipo control, anteponiendo a un nombre descriptor un prefijo que indique el tipo.

3.7.5 **Variables.**

Cada variable se debería denominar con una indicación del tipo variable, anteponiendo a un nombre descriptor un prefijo que indique el tipo.

3.7.6 **Objetos de la base de datos**

Cada objeto se debería denominar con una indicación del tipo de objeto, anteponiendo a un nombre descriptor un prefijo que indique el tipo.
