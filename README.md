# 💻 widads | Desarrollador Web & Especialista en Bases de Datos

## 🌿 Sobre mí
Hola, soy widads. Actualmente estoy cursando el ciclo formativo de **Desarrollo de Aplicaciones Web (DAW)**. Dentro del ecosistema del desarrollo de software, mi verdadera pasión se encuentra en el **diseño, optimización y gestión de Bases de Datos Relacionales**. Me encanta estructurar la información de manera eficiente y exprimir el potencial del lenguaje SQL para resolver problemas complejos de lógica de negocio.

* 🔍 **Mi enfoque:** Modelado de datos, optimización de consultas y automatización en el lado del servidor.
* 🛠️ **Filosofía de trabajo:** "Un código limpio está bien, pero una base de datos bien estructurada es el motor de cualquier aplicación exitosa."

---

## 🛠️ Tecnologías y Herramientas

### 🗄️ Gestión de Datos (Mi Especialidad)
![SQL](https://img.shields.io/badge/SQL-00758F?style=for-the-badge&logo=mysql&logoColor=white)
![PL/SQL](https://img.shields.io/badge/PL--SQL-F80000?style=for-the-badge&logo=oracle&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

### 💻 Programación y Frontend
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

### 🌐 Sistemas, Redes y Marcas Avanzadas
* **Lenguajes de marcas:** Gestión de datos estructurados XML mediante consultas con `XPath`, `XQuery` y transformaciones con `XSLT`.
* **Sistemas y Virtualización:** Administración de entornos `Linux` y `Windows Server` sobre máquinas virtuales (VirtualBox/VMware) y redes básicas.
* **Control de Versiones:** Uso de terminal de comandos con Git y despliegue en GitHub.

---

## 📁 Proyectos Destacados
Aquí tienes algunos de los laboratorios y proyectos prácticos que he diseñado durante mi formación:

1. **E-Commerce Database Design:** Diseño conceptual (Entidad-Relación) y lógico de una base de datos para una tienda online, implementando restricciones avanzadas, índices de rendimiento y triggers de auditoría en `SQL` y `PL/SQL`.
2. **Procesador de Datos XML:** Desarrollo de scripts de extracción de datos utilizando `XPath` y plantillas de transformación `XSLT` para convertir catálogos XML en páginas web estructuradas.
3. **Sistema de Gestión (Java POO):** Aplicación de consola en Java orientada a objetos para la administración interna de registros de usuarios y stock de productos.
4. **Calculadora Web Interactiva:** Frontend dinámico utilizando `HTML5`, `CSS3` y lógica de control mediante manipulación del DOM con `JavaScript`.

Para gestionar y levantar estos entornos de desarrollo en mi máquina local o servidor, utilizo la terminal de comandos de Linux mediante herramientas como `cd` o `ls`.

### 📊 Ejemplo de Código: Optimización SQL
Los perfiles de datos siempre muestran código real. Aquí tienes un ejemplo de cómo realizo una consulta optimizada combinando tablas mediante un `INNER JOIN` y aplicando filtros específicos:

```sql
-- Consulta para obtener las ventas totales de clientes VIP
SELECT 
    c.nombre AS cliente, 
    COUNT(p.id_pedido) AS total_pedidos, 
    SUM(p.importe_total) AS facturacion_acumulada
FROM clientes c
INNER JOIN pedidos p ON c.id_cliente = p.id_cliente
WHERE c.tipo_cuenta = 'VIP'
GROUP BY c.id_cliente, c.nombre
HAVING SUM(p.importe_total) > 500
ORDER BY facturacion_acumulada DESC;
