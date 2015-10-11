---
title       : Bases de Datos 
subtitle    : Introducción a los sistemas de bases de datos
author      : Kevin Pérez - Ing de Sistemas - Estadístico
job         : Departamento de Matemáticas y Estadística - Universidad de Córdoba
logo        : unicordoba3.png
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax, bootstrap, quiz, shiny, interactive]            
mode        : selfcontained # {standalone, draft}
ext_widgets : {rCharts: [libraries/nvd3]}
knit        : slidify::knit2slides
---

## Contenido

> * Introducción a las bases de datos
    + Concepto y origen de las BD y los SGBD
    + Evolución de los SGBD
    + Objetivos y funcionalidad de los SGBD
    + Modelos de BD

---

## Introducción 

> + Las bases de datos son el método preferido para el almacenamiento estructurado de datos. Desde las grandes aplicaciones multiusuario, hasta los teléfonos móviles y las agendas electrónicas utilizan tecnología de bases de datos para asegurar la integridad de los datos y facilitar la labor tanto de usuarios como de los programadores que las desarrollaron.

> + Desde la realización del primer modelo de datos, pasando por la administración del sistema gestor, hasta llegar al desarrollo de la aplicación, los conceptos y la tecnología asociados son muchos y muy heterogéneos. Sin embargo, es imprescindible conocer los aspectos clave de cada uno de estos temas para tener éxito en cualquier proyecto que implique trabajar con bases de datos.


---


## Origen de las bases de datos 

> + Las aplicaciones informáticas de los **años sesenta** acostumbraban a darse totalmente
por lotes (batch) y estaban pensadas para una tarea muy específica relacionada con muy pocas entidades tipo.

> + Cada aplicación (una o varias cadenas de programas) utilizaba ficheros de movimientos para actualizar (creando una copia nueva) y/o para consultar uno o
dos ficheros maestros o, excepcionalmente, más de dos.

> + A medida que se fueron introduciendo las líneas de comunicación, los terminales y los discos, se fueron escribiendo programas que permitían a varios usuarios consultar los mismos ficheros on-line y de forma simultánea. Más adelante fue surgiendo la necesidad de hacer las actualizaciones también on-line.



---


## Origen de las bases de datos

> + A medida que se integraban las aplicaciones, se tuvieron que **interrelacionar**
sus ficheros y fue necesario eliminar la **redundancia**.

> + El acceso on-line y la utilización eficiente de las interrelaciones exigían estructuras físicas que diesen un acceso rápido, como por ejemplo los índices, las
multilistas, las técnicas de hashing, etc.

> + Estos conjuntos de ficheros interrelacionados, con estructuras complejas y
compartidos por varios procesos de forma simultánea (unos on-line y otros por
lotes), recibieron al principio el nombre de _**Data Banks**_, y después, a inicios de
los años setenta, el de _**Data Bases**_. Aquí los denominamos bases de datos _**(BD)**_.



---


## Origen de las BD y SGDB

> + El software de gestión de ficheros era demasiado elemental para dar satisfacción a todas estas necesidades. Por ejemplo, el tratamiento de las interrelaciones no estaba previsto, no era posible que varios usuarios actualizaran datos simultáneamente, etc.

> + La utilización de estos conjuntos de ficheros por parte de los programas de aplicación era excesivamente compleja, de modo que, especialmente durante la segunda mitad de los años setenta, fue saliendo al mercado oftware más sofisticado: _**los Data Base Management Systems**_, que aquí denominamos sistemas de gestión de _**BD**_ _**(SGBD)**_.


---

## Definición de Base de Datos 

Una base de datos es un conjunto estructurado de datos que representa entidades y sus interrelaciones. La representación será única e integrada, a pesar de que debe permitir utilizaciones varias y simultáneas

---

## Los años sesenta y setenta: sistemas centralizados

Los SGBD de los años sesenta y setenta (IMS de IBM, IDS de Bull, DMS de Univac, etc.) eran sistemas totalmente centralizados, como corresponde a los sistemas operativos de aquellos años, y al hardware para el que estaban hechos: un gran ordenador para toda la empresa y una red de terminales sin inteligencia ni memoria.


---

## Los años ochenta: SGBD relacionales

> + Los _**ordenadores minis**_, en primer lugar, y después los ordenadores micros,
extendieron la informática a prácticamente todas las empresas e instituciones.

> + La aparición de los SGBD _relacionales_ supone un avance importante
para facilitar la programación de aplicaciones con BD y para conseguir
que los programas sean independientes de los aspectos físicos de la BD.

> + Todos estos factores hacen que se extienda el uso de los SGBD. La estandarización, en el año 1986, del lenguaje _**SQL**_ produjo una auténtica explosión de los SGBD relacionales.


---


## Los años noventa: distribución, C/S y 4GL

> + Al acabar la década de los ochenta, los SGBD relacionales ya se utilizaban prácticamente en todas las empresas. A pesar de todo, hasta la mitad de los noventa, cuando se ha necesitado un rendimiento elevado se han seguido utilizando los SGBD prerrelacionales.

> + La necesidad de tener una visión global de la empresa y de interrelacionar diferentes aplicaciones que utilizan BD diferentes, junto con la facilidad que dan las redes para la intercomunicación entre ordenadores, ha conducido a los SGBD actuales, que permiten que un programa pueda trabajar con diferentes BD como si se tratase de una sola. Es lo que se conoce como base de datos distribuida.

> + La tecnología que se utiliza habitualmente para distribuir datos es la que
se conoce como entorno (o arquitectura) cliente/servidor (C/S). Todos los SGBD relacionales del mercado han sido adaptados a este entorno.

---


## Los años noventa: distribución, C/S y 4GL

> + El éxito de las BD, incluso en sistemas personales, ha llevado a la aparición de
los Fourth Generation Languages (4GL), lenguajes muy fáciles y potentes, es pecializados en el desarrollo de aplicaciones fundamentadas en BD. Proporcionan muchas facilidades en el momento de definir, generalmente de forma visual, diálogos para introducir, modificar y consultar datos en entornos C/S.

---

## Tendencias actuales

> + Hoy día, los SGBD relacionales están en plena transformación para
adaptarse a tres tecnologías de éxito reciente, fuertemente relacionadas:
la multimedia, la de orientación a objetos (OO) e Internet y la web.

> + Los tipos de datos que se pueden definir en los SGBD relacionales de los años
ochenta y noventa son muy limitados. La incorporación de tecnologías multimedia _**imagen y sonido**_ en los SI hace necesario que los SGBD relacionales acepten atributos de estos tipos.

> + En los SI se inicia también la adopción tímida de momento, de la OO. La utilización de lenguajes como C++ o Java requiere que los SGBD relacionales se
adapten a ellos con interfaces adecuadas.

> + La rápida adopción de la web a los SI hace que los SGBD incorporen recursos
para ser servidores de páginas web, como por ejemplo la inclusión de SQL en
guiones HTML, SQL incorporado en Java, etc.


---


## Tendencias actuales 


> + Durante estos últimos años se ha empezado a extender un tipo de aplicación
de las BD denominado _**Data Warehouse**_, o almacén de datos, que también
produce algunos cambios en los SGBD relacionales del mercado.

> + A lo largo de los años que han trabajado con BD de distintas aplicaciones, las
empresas han ido acumulando gran cantidad de datos de todo tipo. Si estos datos se analizan convenientemente pueden dar información valiosa 

> + Los datos de este gran almacén, el Data Warehouse, se obtienen por una replicación más o menos elaborada de las que hay en las BD que se utilizan en el trabajo cotidiano de la empresa. Estos almacenes de datos se utilizan exclusivamente para hacer consultas, de forma especial para que lleven a cabo estudios los analistas
financieros, los analistas de mercado, etc.

---

## Modelos de bases de datos 

> + Una BD es una representación de la realidad (de la parte de la realidad que nos interesa en nuestro SI). Dicho de otro modo, una BD se puede considerar un modelo de la realidad. El componente fundamental utilizado para modelar en un SGBD relacional son las tablas (denominadas relaciones en el mundo teórico). Sin embargo, en otros tipos de SGBD se utilizan otros componentes.

> + El conjunto de componentes o herramientas conceptuales que un SGBD proporciona para modelar recibe el nombre de modelo de BD. Los cuatro modelos de BD más utilizados en los SI son el modelo relacional, el modelo jerárquico, el modelo en red y el modelo relacional con objetos.

---

## Modelos de bases de datos 

Todo modelo de BD nos proporciona tres tipos de herramientas:

> 1. _**Estructuras**_ de datos con las que se puede construir la BD: tablas, árboles, etc.

> 2. Diferentes tipos de _**restricciones (o reglas) de integridad**_ que el SGBD tendrá que hacer cumplir a los datos: dominios, claves, etc.

> 3. Una serie de _**operaciones**_ para trabajar con los datos. Un ejemplo de ello,
en el modelo relacional, es la operación SELECT, que sirve para seleccionar (o
leer) las filas que cumplen alguna condición. Un ejemplo de operación típica
del modelo jerárquico y del modelo en red podría ser la que nos dice si un determinado 
registro tiene “hijos” o no.

---

## Evolución de los modelos de BD

> + De los cuatro modelos de BD que hemos citado, el que apareció primero, a
principios de los años sesenta, fue el modelo jerárquico. Sus estructuras son
registros interrelacionados en forma de árboles. El SGBD clásico de este modelo
es el IMS/DL1 de IBM.

> + A principios de los setenta surgieron SGBD basados en un modelo en red.
Como en el modelo jerárquico, hay registros e interrelaciones, pero un registro
ya no está limitado a ser “hijo” de un solo registro tipo.

> + Durante los años ochenta apareció una gran cantidad de SGBD basados en el
_**modelo relacional**_ propuesto en 1969 por E.F. Codd, de IBM, y prácticamente
Introducción a las bases de datos todos utilizaban como lenguaje nativo el SQL. 
El modelo relacional se basa en el concepto matemático de relación, que aquí podemos considerar de momento equivalente al término tabla (formada por filas y columnas).

---

## Evolución de los modelos de BD

<img class=center src="/home/kevin/Imágenes/Modelos BD.png" height=600 width=500>

---

## Lenguajes y usuarios

Para comunicarse con el SGBD, el usuario, ya sea un programa de aplicación
o un usuario directo, se vale de un lenguaje. Hay muchos lenguajes diferentes,
según el tipo de usuarios para los que están pensados y el tipo de cosas que los
usuarios deben poder expresar con ellos:

a). Habrá usuarios informáticos muy expertos que querrán escribir procesos 
complejos y que necesitarán lenguajes complejos.

b). Sin embargo, habrá usuarios finales no informáticos, ocasionales (esporádicos), que sólo harán consultas. Estos usuarios necesitarán un lenguaje muy sencillo, aunque dé un rendimiento bajo en tiempo de respuesta.

También podrá haber usuarios finales no informáticos, dedicados o especializados. Son usuarios cotidianos o, incluso, dedicados exclusivamente a trabajar con la BD.


---

## Lenguajes y usuarios

> + Hay lenguajes especializados en la escritura de esquemas; es decir, en la
descripción de la BD. Se conocen genéricamente como _**DDL**_ o _data definition language_. 
Incluso hay lenguajes específicos para esquemas internos, lenguajes para esquemas conceptuales y lenguajes para esquemas externos.

> + Otros lenguajes están especializados en la utilización de la BD (consultas y mantenimiento). Se conocen como _**DML**_ o data management language. Sin embargo, lo más frecuente es que el mismo lenguaje disponga de construcciones para las dos funciones, DDL y DML.

---

## Lenguajes y usuarios

> + El _**lenguaje SQL**_, que es el más utilizado en las BD relacionales, tiene verbos –ins-
trucciones– de tres tipos diferentes:

> 1. _**Verbos del tipo DML**_; por ejemplo, `SELECT` para hacer consultas, e `INSERT`,
`UPDATE` y `DELETE` para hacer el mantenimiento de los datos.

> 2. _**Verbos del tipo DDL**_; por ejemplo, `CREATE TABLE` para definir las tablas,
sus columnas y las restricciones.

> 3. Además, SQL tiene _**verbos de control del entorno**_, como por ejemplo
`COMMIT` y `ROLLBACK` para delimitar transacciones.

---

## Lenguajes y usuarios

En cuanto a los aspectos _**DML**_, podemos diferenciar dos tipos de lenguajes:

a) Lenguajes muy declarativos (o implícitos), con los que se especifica qué se
quiere hacer sin explicar cómo se debe hacer.

b). Lenguajes más explícitos o _**procedimentales**_, que nos exigen conocer más
cuestiones del funcionamiento del SGBD para detallar paso a paso cómo se deben 
realizar las operaciones (lo que se denomina _navegar_ por la BD).

Como es obvio, los _**aspectos DDL**_ (las descripciones de los datos) son siempre
declarativos por su propia naturaleza.

---

## Contenido

> * Introducción a las bases de datos
    + Concepto y origen de las BD y los SGBD
    + Evolución de los SGBD
    + Objetivos y funcionalidad de los SGBD
    + Modelos de BD
    + Modelo Entidad-relación

---

## Modelo Entidad-Relación

El Modelo Entidad-Relación, como cualquier modelo de datos, tiene sus estructuras
propias que son conocidas como Diagramas Entidad-Relación.

De hecho, para describir el esquema conceptual de la base de datos del mundo objeto de
estudio se construye su Diagrama Entidad-Relación.

---

## Elementos del Modelo Entidad-Relación 

Los elementos componentes del Modelo Entidad-Relación son los siguientes:

- Entidades
- Atributos 
- Relaciones 

Cada uno de estos elementos tiene asociado un modo gráfico de representación o símbolo
específico, que lo distingue del resto de elementos. En los apartados siguientes
describiremos cada uno de estos elementos, sus características y simbología.

---

## Entidades 

Una entidad es un objeto real o abstracto de interés en una organización y acerca del
cual se puede y se quiere obtener una determinada información; personas, cosas, lugares,
etc., son ejemplos de entidades. La entidad se representa gráficamente por medio de un
rectángulo y en el interior del mismo se escribe el identificador de la entidad.

<img class=center src="/home/kevin/Imágenes/entidades.png" height=350 width=600>

Reglas que debe cumplir una entidad:

- Tiene que tener existencia propia.
- Cada ocurrencia de un tipo de entidad debe poder distinguirse de las demás.
- Todas las ocurrencias de un tipo de entidad deben tener los mismos tipos de características (atributos)

---

## Atributos 

> + Un atributo es una propiedad o característica asociada a una determinada entidad y, por
tanto, común a todas las ocurrencias de esa entidad; nombre, cantidad, categoría
profesional, edad, cargo, etc., son ejemplos de atributos. El atributo se representa
gráficamente por medio de una elipse y en el interior de la misma se escribe el
identificador del atributo.

> + Asociado al concepto de atributo surge el concepto de dominio. Un **dominio** es el conjunto de valores permitidos para un atributo. Por ejemplo, si tenemos el atributo COLOR el
dominio sobre el que se define podría ser: (NARANJA, BLANCO, AZUL y NEGRO).

> + De acuerdo con lo dicho anteriormente podríamos dar la siguiente definición formal de
atributo:

---

## Atributos 

Función que a una entidad le asigna un dominio. $$ A:E \to F(v) $$ 

Donde:

- A: Atributo 
- E: Tipo de entidad 
- V: Conjunto de valores (dominio)
- F: Función 

---

## Atributos 

En función de sus características respecto de la entidad que definen se distinguen dos
tipos de atributos :

- Atributo Identificador Principal (AIP): Distingue unívocamente una ocurrencia de
entidad del resto de ocurrencias.
- Atributo Descriptor: Caracteriza una ocurrencia pero no la distingue del resto de
ocurrencias de entidad.

De entre todos los atributos de un tipo de entidad debemos elegir uno o varios que
identifiquen unívocamente cada una de las ocurrencias de ese tipo de entidad. Este
atributo o conjunto de atributos se denomina **ATRIBUTO IDENTIFICADOR PRINCIPAL
(AIP)**, y los atributos que lo componen deben ser mínimos en el sentido de que la
eliminación de cualquiera de ellos le hará a perder su carácter identificador.

---

## Atributos 

Puede ocurrir que exista más de un conjunto de atributos que verifiquen la condición de
ser identificador unívoco y mínimo de cada ocurrencia del tipo de entidad, por lo que denominaremos a cada uno de ellos **ATRIBUTO IDENTIFICADOR CANDIDATO (AIC)**. Elegiremos uno como AIP y el resto serán **ATRIBUTOS IDENTIFICADORES ALTERNATIVOS (AIA)**

Representación gráfica de atributos


<img class=center src="/home/kevin/Imágenes/atributos.png" height=250 width=400>


---

## Relaciones 

Una relación es básicamente una asociación entre entidades y se caracterizará por unas determinadas restricciones que determinarán las entidades que pueden o no participar de dicha relación: PROVEEDOR suministra PRODUCTO , PERSONA ha nacido en PAÍS , EMPLEADO trabaja en DEPARTAMENTO , etc., son ejemplos de relación. La relación se representa gráficamente por medio de un rombo y en el interior del mismo se escribe la etiqueta que identifica la relación

<img class=center src="/home/kevin/Imágenes/relacion.png" height=250 width=400>


---


## Relaciones 

> + Asociado al concepto de relación surge el concepto de ocurrencia de relación. Una ocurrencia de relación es la asociación concreta de ocurrencias de entidad de diferentes entidades. Por ejemplo, si tenemos las entidades EMPLEADO y DEPARTAMENTO , y la relación trabaja en, una ocurrencia de interrelación será: MARTA GARCÍA trabaja en el DEPARTAMENTO DE DIRECCIÓN.

> + Una relación queda caracterizada por tres propiedades:

> - **Nombre**: Como todo objeto en el modelo E-R las relaciones deben tener un nombre que las identifique unívocamente.
> - **Grado**: Número de tipos de entidad sobre las que se realiza la asociación. La
interrelación del ejemplo anterior será binaria, es decir, su grado seria dos.
> - **Tipo de correspondencia**: Número máximo de ocurrencias de cada tipo de entidad que
pueden intervenir en una ocurrencia del tipo de relación. 

> + Las relaciones pueden tener atributos propios. En el ejemplo que venimos manejando, si interesase conocer desde qué fecha trabaja un empleado en un determinado departamento, dicho atributo fecha seria una propiedad de la relación “Trabaja en”.

---

## Representación Gráfica del Modelo E-R 

El Modelo E-R, como ya sabemos, permite representar gráficamente el esquema
conceptual de la base de datos que en cada momento estemos definiendo mediante lo que
hemos denominado Diagrama Entidad-Relación (E/R). De hecho, ya conocemos cómo
se representan cada uno de los elementos del modelo.

<img class=center src="/home/kevin/Imágenes/modeloer.png" height=250 width=600>


---

## Representación Gráfica del Modelo E-R 

Sin embargo, para poder realizar el Diagrama E-R todavía debemos definir una serie de
aspectos:

- Para representar la pertenencia de un atributo a una entidad o interrelación se une el
símbolo del atributo correspondiente mediante un arco.

- Para reflejar la asociación existente entre dos o más entidades mediante una
interrelación se unen los símbolos de dichas entidades al símbolo de la interrelación
correspondiente mediante arcos.

Ahora estamos en condiciones de representar mediante un diagrama E-R el esquema
conceptual de una base de datos.

---

## Modelo relacional 

> + Consiste en la conversión de las entidades en tablas, donde una tabla esta compuesta por columnas llamadas campos que toman los mismos nombres de los atributos de la entidad, por las filas llamadas _tuplas_ o _registros_ que son los datos guardados en la tabla.

> + Toda tabla tiene un nombre igual al nombre de la tabla o la relación que la define. Para convertir el modelo E-R en el modelo relacional se siguen ciertas reglas.

---

## Modelo relacional 

El **modelo relacional** es un modelo de datos y, como tal, tiene en cuenta los tres aspectos siguientes de los datos:

> 1. La **estructura**, que debe permitir representar la información que nos interesa del mundo real

> 2. La **manipulación**, a la que da apoyo mediante las operaciones de actualización y consulta de los datos.

> 3. La **integridad**, que es facilitada mediante el establecimiento de reglas de integridad; es decir, condiciones que los datos deben cumplir.

---

## Modelo relacional 

> + El principal objetivo del modelo de datos relacional es facilitar que la base de datos sea percibida o vista por el usuario como una estructura lógica que consiste en un conjunto de relaciones y no como una estructura física de implementación. Esto ayuda a conseguir un alto grado de independencia de los datos.

> + Un objetivo adicional del modelo es conseguir que esta estructura lógica con la que se percibe la base de datos sea simple y uniforme. Con el fin de proporcionar simplicidad y uniformidad, toda la información se representa de una única manera: mediante valores explícitos que contienen las relaciones (no se utilizan conceptos como por ejemplo apuntadores entre las relaciones).

---

## Modelo relacional 

En primer lugar, presentaremos el concepto de relación de manera informal. Se puede obtener una buena idea intuitiva de lo que es una relación si la visualizamos como una tabla o un fichero. En la figura se muestra la visualización tabular de una relación que contiene datos de empleados.

<img class=center src="/home/kevin/Imágenes/modeloR.png" height=150 width=600>

---

## Clave candidata, clave primaria y clave alternativa de las relaciones

Toda la información que contiene una base de datos debe poderse identificar de alguna forma. En el caso particular de las bases de datos que siguen el modelo relacional, para identificar los datos que la base de datos contiene, se pueden utilizar las claves candidatas de las relaciones. A continuación definimos qué se entiende por clave candidata, clave primaria y clave alternativa de una relación, será necesario definir el concepto de superclave.

Una superclave de una relación de esquema **R(A 1 , A 2 , ..., A n )** es un subconjunto de los atributos del esquema tal que no puede haber dos tuplas en la extensión de la relación que tengan la misma combinación de valores para los atributos del subconjunto.

---

## Clave candidata, clave primaria y clave alternativa de las relaciones

> + Una **clave candidata** de una relación es una superclave C de la relación que cumple que ningún subconjunto propio de C es superclave.

> + Habitualmente, una de las **claves candidatas** de una relación se designa clave primaria de la relación. La clave primaria es la clave candidata cuyos valores se utilizarán para identificar las tuplas de la relación.

> + Las **claves candidatas** no elegidas como primaria se denominan claves alternativas.

---

## Claves foráneas de las relaciones

Una **clave foránea** de una relación R es un subconjunto de atributos del esquema de la relación, que denominamos CF y que cumple las siguientes condiciones:

 1. Existe una relación S (S no debe ser necesariamente diferente de R) que tiene por clave primaria CP.

 2. Se cumple que, para toda tupla t de la extensión de R, los valores para CF de t son valores nulos o bien valores que coinciden con los valores para CP de alguna tupla s de S.

Y entonces, se dice que la clave foránea CF referencia la clave primaria CP de la relación S, y también que la clave foránea CF referencia la relación S.

---

## Teoría de la Normalización

El modelo relacional tiene asociada una teoría que no puede ser separada del modelo: la
teoría de la normalización de relaciones (...) tiene por objeto eliminar los comportamientos
anormales de las relaciones durante las actualizaciones. También permite eliminar datos
redundantes y facilita la comprensión de las relaciones semánticas entre los datos.

Concepción de esquemas relacionales.

+ Concepción de esquemas relacionales.
+ Problemas derivados de una mala percepción del mundo real:
    - redundancias
    - incoherencias durante las actualizaciones
    - proliferación de valores nulos
    
Una relación que no represente verdaderas entidades o asociaciones entre entidades
parece que sufrirá la presencia de datos redundantes y de incoherencias potenciales.

---

## La aproximación por descomposición

...parte de una relación compuesta de todos los atributos denominada ‘relación universal’,
para descomponerla en subrelaciones que no padecen las anomalías anteriormente citadas.
Es un proceso de depuración sucesiva que debe lograr aislar unas entidades y unas
asociaciones del mundo real.

---

## Operaciones básicas sobre relaciones:

Aunque el estudio de la componente dinámica del Modelo Relacional es materia del
siguiente tema, necesitamos conocer dos operaciones básicas sobre relaciones: La
descomposición mediante proyección y la reunión de dos relaciones.

+ Proyección

    - La proyección de una relación sobre un subconjunto de sus atributos es una relación
      definida sobre ellos, eliminando las filas repetidas. El resultado es un subconjunto                                 vertical de la relación a la que se aplica el operador.
+ Descomposición:
    
    - Sustitución de la relación $ R(A 1 , A 2 ... A n ) $ por una serie de relaciones $ R1, R2, ...Rn $ obtenidas mediante proyecciones de R y tales que la relación resultante de las reuniones $ R1 * R2 * ... * Rn $ tiene el mismo esquema que R.

---

## Formas Normales

La teoría de la normalización consiste en obtener esquemas relacionales que cumplan unas
determinadas condiciones y se centra en las denominadas formas normales. Se dice que un
esquema de relación está en una determinada forma normal si satisface un conjunto
determinado de restricciones.

---

