# 💻 Bases de Datos NoSQL

Una **base de datos NoSQL** es un tipo de base de datos que no utiliza las tradicionales **tablas** como las bases de datos SQL. Organiza los datos de forma más flexible, ideal para manejar grandes cantidades de información o datos sin un formato fijo.
## Ejemplo 
- MongoDb

♦️🔗## Características:
- **UUIDs:** Identificadores únicos para los datos, garantizando que sean distintos.
- **Sin Autoincremento:** No se usa un valor que se incremente automáticamente como en  SQL.
- **Escalabilidad Horizontal:** Permite agregar más servidores para manejar más datos y tráfico.

♦️🔗## MongoDB y el Operador `$lookup`:
En **MongoDB**, no se usan joins tradicionales, pero se puede combinar datos de dos colecciones usando el operador **`$lookup`**, lo que es similar a un join en SQL.

---

# ** 🟢 DynamoDB**

**DynamoDB** es una base de datos NoSQL gestionada por Amazon Web Services (AWS), diseñada para almacenar datos de manera rápida, escalable y de baja latencia.

## ➡️**Características**

- **Escalado Horizontal**: Se adapta automáticamente a la carga de trabajo, manejando grandes volúmenes de datos sin necesidad de intervención manual.
  
- **Clave Primaria Única**: Cada elemento en DynamoDB se identifica de forma única mediante una clave primaria (Primary Key). Esta clave puede ser una clave de partición o una combinación de clave de partición y clave de ordenación

- **Latencia Predecible**: Responde con tiempos de acceso constantes, incluso con grandes cantidades de datos.

- **Operaciones Atómicas**: Garantiza la consistencia de los datos mediante operaciones indivisibles.

- **Alta Disponibilidad**: Replicación automática en múltiples zonas de disponibilidad para asegurar la durabilidad y accesibilidad.

- **Índices Secundarios**: Permite crear índices para realizar consultas más flexibles y rápidas.

-- **Consultas HTTP**: En DynamoDB, las consultas a través de HTTP se realizan mediante la AWS SDK o directamente usando la API de Amazon DynamoDB sobre el protocolo HTTP.

---

## ✍🏼**Operaciones de Lectura**
-**GetItem **: Lectura por clave primaria. Conocer PK y SK

-**Query**: Lectura con búsqueda por clave primaria y opcionalmente clave de ordenación. 

-**Scan**: Lectura completa de la tabla. (Es muy lento)

---


## **📈 Access Patern**
Un access pattern es cómo y con qué frecuencia accederás a los datos en una base de datos. Es esencial para diseñar una base de datos eficiente, especialmente en sistemas NoSQL como DynamoDB, ya que ayuda a estructurar los datos de manera que optimices su rendimiento y consultas.

## 💻PartiQL 

PartiQL  es un lenguaje de consulta desarrollado por AWS que permite realizar operaciones de lectura y escritura en bases de datos de Amazon Web Services (AWS), como Amazon DynamoDB, Amazon S3 y Amazon Redshift, utilizando una sintaxis SQL estándar.
