Esta plantilla de **AWS CloudFormation** despliega una infraestructura en AWS para alojar una base de datos **PostgreSQL** en una instancia **RDS (Relational Database Service)** dentro de la capa gratuita.  

## 📍 Funcionalidades Principales

✅ Define parámetros personalizables (nombre de la base de datos, usuario, almacenamiento, IP permitidas).  
✅ Crea una **VPC** con **dos subredes públicas**.  
✅ Configura conectividad a Internet mediante un **Internet Gateway** y rutas adecuadas.  
✅ Configura seguridad con un **Grupo de Seguridad** para PostgreSQL (puerto 5432).  
✅ Despliega una instancia **RDS PostgreSQL** en una instancia `db.t4g.micro` con backups y acceso público.  
✅ Define **outputs** con el endpoint y el identificador de la base de datos.  

---