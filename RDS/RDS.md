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

## 🔹 **Escalamiento Sharding**  
Es un tipo de **escalado horizontal**, que permite dividir una base de datos en partes más pequeñas llamadas shards

✅ **Beneficios:**  
- Reduce la carga en cada servidor y evita cuellos de botella.
- Si un shard falla el resto de bases de datos sigue funcionando

📌 **Ejemplo:**  
Un ** Red Social** que maneja miles de usuarios puede dividir la bases de datos en shards según la ubicación geográfica.

---

## 🔹 **Base de Datos OLTP (Online Transaction Processing)**  
Es un tipo de **Base de datos**, optimizada para manejar transacciones en **tiempo real**.

✅ **Caracteristicas:**  
- Maneja operaciones rápidas y frecuentes (inserciones, actualizaciones, eliminaciones.
- Se usa en sistemas como bancos, e-commerce, aplicaciones de punto de venta (POS).

📌 **Ejemplo:**  
Cuando compras en linea, el un **e-commerce**, dicho aplicativo, usa una OLTP, para registrar y actualizar el inventario.

---

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
