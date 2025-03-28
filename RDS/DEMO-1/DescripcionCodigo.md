El archivo `rds_postgres` es **AWS CloudFormation** despliega una infraestructura en AWS para alojar una base de datos **PostgreSQL** en una instancia **RDS (Relational Database Service)** dentro de la capa gratuita.

##  Funcionalidades Principales

✅ Define parámetros personalizables (nombre de la base de datos, usuario, almacenamiento, IP permitidas).
✅ Crea una **VPC** con **dos subredes públicas**.
✅ Configura conectividad a Internet mediante un **Internet Gateway** y rutas adecuadas.
✅ Configura seguridad con un **Grupo de Seguridad** para PostgreSQL (puerto 5432).
✅ Despliega una instancia **RDS PostgreSQL** en una instancia `db.t4g.micro` con backups y acceso público.
✅ Define **outputs** con el endpoint y el identificador de la base de datos.

---

# Práctica ACID en SQL  

Este archivo, `practica_acid.sql`, contiene instrucciones SQL diseñadas para practicar los principios de **ACID** en bases de datos. Se ha utilizado **DBeaver** como software editor de bases de datos y **AWS** como servicio de hosting para la base de datos.  

## Objetivo  
El propósito de esta práctica es establecer una conexión con la base de datos en AWS a través de DBeaver y ejecutar consultas que permitan validar la correcta implementación de transacciones bajo los principios de **Atomicidad, Consistencia, Aislamiento y Durabilidad (ACID)**.  

## Evidencia  
A continuación, se muestra una captura de pantalla de la conexión establecida y la consulta realizada en la base de datos:  

![Evidencia de conexión y consulta](DEM0-1/Evidencia/ConexionYConsultaBD.jpg)  

## Requisitos  
Para ejecutar este archivo SQL, se recomienda tener:  
- **DBeaver** o cualquier otro editor SQL compatible.  
- Acceso a una base de datos en **AWS RDS** o similar.  
- Configuración correcta de credenciales y permisos en la base de datos.  

 
