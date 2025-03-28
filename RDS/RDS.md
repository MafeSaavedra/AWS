# 📌 Principios de una Base de Datos  

Para crear aplicaciones **confiables, escalables y mantenibles**, es fundamental seguir estos principios:  

## 🔹 **1️⃣ Confiabilidad**  
✔️ Tolerancia a fallos en **software, hardware y errores humanos**.  
✔️ Garantiza que la base de datos pueda recuperarse de fallos sin pérdida de datos.  

## 🔹 **2️⃣ Escalabilidad**  
✔️ Capacidad de mantener **rendimiento y baja latencia** incluso con grandes volúmenes de datos y usuarios.  
✔️ Permite aumentar la capacidad sin afectar el desempeño.  

## 🔹 **3️⃣ Mantenimiento**  
✔️ **Operatividad sencilla**, fácil evolución y administración eficiente del sistema.  
✔️ Facilita la actualización y optimización sin afectar la disponibilidad.  

---

# 🌐 ¿Qué es una RDS (Relational Database Service)?  

**Amazon RDS** es un servicio de bases de datos en la nube que te permite administrar bases de datos relacionales sin preocuparte por la configuración o mantenimiento.  

💡 **Solo soporta bases de datos relacionales**, como **MySQL, PostgreSQL, MariaDB, SQL Server y Oracle**.  

## 🔹 **Ejemplo práctico**  

Piensa en **RDS** como una base de datos lista para usar. En lugar de instalar y configurar una base de datos en tu computadora o en un servidor físico, **AWS lo hace por ti**.  

### 🔧 **¿Cómo funciona?**  
1️⃣ Eliges el tipo de base de datos que necesitas (**MySQL, PostgreSQL, etc.**).  
2️⃣ AWS se encarga de la instalación, configuración, actualizaciones y backups automáticos.  
3️⃣ Solo te preocupas por usar la base de datos, sin administrar la infraestructura.  

🔹 **Beneficios de Amazon RDS:**  
✔️ Reducción de costos en mantenimiento.  
✔️ Escalabilidad automática.  
✔️ Alta disponibilidad con backups automáticos.  

---

# ⚡ Tipos de Escalabilidad  

## 🔹 **Escalamiento Horizontal**  
Implica agregar múltiples servidores para distribuir la carga de trabajo, permitiendo manejar un mayor tráfico de usuarios.  

✅ **Beneficios:**  
- Ofrece **tolerancia a fallos**, ya que si un servidor falla, los demás continúan operando.  
- Puede **automatizarse** y adaptarse dinámicamente.  
- Tiene una **escalabilidad casi ilimitada**.  

📌 **Ejemplo:**  
Un **e-commerce** que necesita soportar miles de usuarios simultáneos sin afectar el rendimiento.  

---

## 🔹 **Escalamiento Vertical**  
Consiste en aumentar la capacidad de un único servidor mejorando su **CPU, RAM o almacenamiento**.  

✅ **Beneficios:**  
- No requiere cambios en la arquitectura del sistema.  
- Puede ser una opción más sencilla para ciertos casos de uso.  

⚠️ **Limitaciones:**  
- Tiene un **límite físico** en cuanto a la capacidad del hardware.  
- Puede generar **downtime** (tiempo de inactividad) al actualizar el servidor.  

📌 **Ejemplo:**  
Un **sistema bancario** que maneja miles de transacciones por segundo, donde se requiere un alto poder de procesamiento para ejecutar múltiples operaciones en poco tiempo.  

---

## 🔹 **Escalamiento con Sharding**  
Es un tipo de **escalado horizontal**, que permite dividir una base de datos en partes más pequeñas llamadas *shards*.  

✅ **Beneficios:**  
- Reduce la carga en cada servidor y evita cuellos de botella.  
- Si un *shard* falla, el resto de la base de datos sigue funcionando.  

📌 **Ejemplo:**  
Una **red social** que maneja millones de usuarios puede dividir su base de datos en *shards* según la ubicación geográfica.  

---

## 🔹 **Ciclo de Vida de una Transacción**  

Una **transacción** es un conjunto de pasos que deben completarse para garantizar la **integridad de los datos**. Sigue un ciclo de vida estructurado para evitar inconsistencias.  

### 📌 **Fases de una Transacción**  

1️⃣ **Inicio (`BEGIN TRANSACTION`)**  
   🔹 La transacción comienza y el sistema bloquea los recursos necesarios.  

2️⃣ **Ejecución de Operaciones**  
   🔹 Se realizan las operaciones: `INSERT`, `UPDATE`, `DELETE`, `SELECT`.  

3️⃣ **Validación**  
   🔹 Se verifica que los datos sean correctos y cumplan las reglas de integridad.  

4️⃣ **Confirmación o Reversión**  
   ✅ **Commit:** Si todo es correcto, los cambios se guardan permanentemente.  
   ❌ **Rollback:** Si hay un error, se revierte todo y la base de datos regresa a su estado inicial.  

---

## 🔹 **Base de Datos OLTP (Online Transaction Processing)**  
Es un tipo de **base de datos**, optimizada para manejar transacciones en **tiempo real**.  

✅ **Características:**  
- Maneja operaciones rápidas y frecuentes (*inserciones, actualizaciones, eliminaciones*).  
- Se usa en sistemas como bancos, e-commerce y aplicaciones de punto de venta (*POS*).  

📌 **Ejemplo:**  
Cuando compras en línea en un **e-commerce**, este sistema usa una **OLTP** para registrar y actualizar el inventario en tiempo real.  

---
## 🔹 **Base de Datos OLAP (Online Analitycs Processing)**  
Es un tipo de **base de datos**, optimizada para el análisis de grandes volúmenes de datos históricos.

✅ **Características:**  
- Diseñada para consultas complejas y análisis de datos.  
- Se usa en inteligencia de negocios (BI), reportes y minería de datos. 
- Los datos No están Normalizados. 
- Se rigen bajo dos modelos : **estrella y copo de nive**. 
- El almacenamiento se genera por columnas. 

📌 **Ejemplo:**  
Una empresa de **retail** usa una OLAP para analizar las tendencias de ventas de los últimos 5 años y predecir la demanda futura. 

**Amazon Redshift** → Analiza grandes volúmenes de datos para generar reportes y tendencias.  

---

## 🔹 **¿Qué es ACID y cómo se relaciona con una OLTP?**  
ACID es un conjunto de propiedades que garantizan que una base de datos transaccional sea **confiable y segura**. Estas propiedades son esenciales en sistemas que manejan muchas transacciones en tiempo real, como los bancos o e-commerce.  

## 🔹 **Propiedades ACID**  

1️⃣ **Atomicidad**  
👉 Una transacción es **todo o nada**. Si falla, se revierte todo para evitar datos corruptos.  
🔹 *Ejemplo:* Al transferir dinero, si hay un error, el dinero no se descuenta ni se deposita.  

2️⃣ **Consistencia**  
👉 La base de datos siempre mantiene **reglas válidas** y datos correctos.  
🔹 *Ejemplo:* No puedes transferir más dinero del que tienes.  

3️⃣ **Aislamiento**  
👉 Las transacciones ocurren **sin interferirse** entre sí.  
🔹 *Ejemplo:* Si dos personas compran el mismo producto a la vez, la base de datos gestiona cada compra correctamente.  

4️⃣ **Durabilidad**  
👉 Una vez confirmada, una transacción **se guarda permanentemente**, incluso tras un fallo del sistema.  
🔹 *Ejemplo:* Si un banco confirma una transferencia y hay un apagón, el dinero sigue en la cuenta destino.  

---
## 🔹 **Teorema CAP**  

El **teorema CAP** dice que en un sistema distribuido solo puedes garantizar **dos** de estas tres cosas al mismo tiempo:  

1️⃣ **Consistencia (C)** → Todos los datos están actualizados en todos los nodos.  
2️⃣ **Disponibilidad (A)** → Siempre hay respuesta, aunque algunos nodos fallen.  
3️⃣ **Tolerancia a particiones (P)** → El sistema sigue funcionando aunque haya problemas en la red. 

# 🛠️ **¿Qué son los Linters y para qué se usan?**  

Los **linters** son herramientas que analizan el código en busca de errores, malas prácticas y problemas de estilo. Su objetivo es mejorar la calidad y mantenibilidad del código.  

## ✅ **Ventajas de usar un linter:**  
✔️ Mejora la legibilidad del código.  
✔️ Previene errores comunes de sintaxis y lógica.  
✔️ Facilita el trabajo en equipo con reglas de estilo unificadas.  

## 🚀 **Linters más utilizados**  

### 📌 **JavaScript**  
- **ESLint** (el más popular, usado con React y Node.js)  
- **JSHint**  
- **StandardJS**  

### 📌 **React (JavaScript con JSX)**  
- **ESLint con eslint-plugin-react**  
- **Prettier** (usado junto con ESLint para formateo automático)  

### 📌 **Python**  
- **Flake8**  
- **Pylint**  
- **Black** (formateador de código)  
