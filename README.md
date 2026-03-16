# 🦭 MARIADB DESDE CERO - GUÍA COMPLETA

**MariaDB desde Cero** es un sitio educativo completo diseñado para enseñar MariaDB desde los fundamentos hasta conceptos avanzados, con explicaciones claras, ejemplos prácticos y código listo para usar.

> *"MariaDB es la alternativa completamente libre a MySQL, creada por el fundador original de MySQL."*

---

## 🎯 ¿Qué es este Proyecto?

Este proyecto proporciona un recurso educativo gratuito para aprender MariaDB, incluyendo:

- **Documentación completa** de cada tema
- **Ejemplos de código** listos para ejecutar
- **Ejercicios prácticos** para reforzar el aprendizaje
- **Sitio web educativo** con navegación intuitiva

---

## 📚 Contenido del Curso

### Módulo 1: Fundamentos

1. **Introducción**
   - Historia de MariaDB
   - Diferencias con MySQL
   - Ecosistema y comunidad

2. **Instalación**
   - Instalación en Linux (Ubuntu, CentOS)
   - Instalación en Windows
   - Configuración inicial
   - Seguridad básica

3. **Conceptos básicos**
   - Creación de bases de datos
   - Tipos de datos
   - Operaciones CRUD
   - Restricciones

### Módulo 2: Intermedio

4. **Ejemplos prácticos**
   - Consultas SELECT avanzadas
   - JOINs múltiples
   - Vistas y subconsultas
   - Stored procedures

5. **Buenas prácticas**
   - Optimización de consultas
   - Indexación estratégica
   - EXPLAIN y profiling
   - Normalización

### Módulo 3: Avanzado

6. **Casos reales**
   - Galera Cluster
   - Replicación multi-master
   - Backup estratégico
   - Monitoreo

7. **Proyecto final**
   - Implementación empresarial completa
   - Alta disponibilidad

---

## 🗂️ Estructura del Proyecto

```
Practica-Nro10/
├── index.html          # Página principal
├── css/
│   └── styles.css      # Estilos del sitio
├── js/
│   └── main.js         # JavaScript del sitio
└── README.md
```

---

## 🚀 Cómo Usar este Proyecto

### Opción 1: Navegar el Sitio Web

1. Abre `index.html` en tu navegador
2. Navega por las secciones del curso
3. Haz clic en los temas para ver la documentación detallada

### Opción 2: Ejecutar los Ejemplos SQL

1. Abre MySQL Client o HeidiSQL
2. Conéctate a tu instancia de MariaDB
3. Ejecuta los scripts SQL de ejemplo

### Requisitos

- **MariaDB 10.5** o superior
- **MySQL Client** o **HeidiSQL**
- Navegador web moderno (Chrome, Firefox, Edge)

---

## 📝 Ejemplos Rápidos

### Crear Base de Datos

```sql
CREATE DATABASE IF NOT EXISTS empresa;
USE empresa;
```

### Crear Tabla

```sql
CREATE TABLE empleados (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100) NOT NULL,
    email VARCHAR(255) UNIQUE,
    salario DECIMAL(10,2),
    fecha_ingreso DATE,
    INDEX idx_nombre (nombre)
) ENGINE=InnoDB;
```

### Consulta con JOIN

```sql
SELECT e.nombre, d.nombre AS departamento
FROM empleados e
INNER JOIN departamentos d ON e.depto_id = d.id
WHERE e.salario > 50000
ORDER BY e.salario DESC;
```

### Temporal Table

```sql
CREATE TABLE productos (
    id INT PRIMARY KEY,
    nombre VARCHAR(100),
    precio DECIMAL(10,2),
    SYSTEM VERSIONING
);
```

---

## 🎓 Metodología de Aprendizaje

### 1. Leer la Teoría
Cada tema comienza con una explicación clara del concepto.

### 2. Ver Ejemplos
Los ejemplos de código muestran la aplicación práctica.

### 3. Practicar
Los ejercicios te permiten aplicar lo aprendido.

### 4. Experimentar
Modifica los ejemplos para entender cómo funcionan.

---

## 🔧 Comandos Esenciales

### Gestión de Bases de Datos

```sql
-- Listar bases de datos
SHOW DATABASES;

-- Usar una base de datos
USE nombre_base_datos;

-- Eliminar base de datos
DROP DATABASE IF EXISTS nombre_base_datos;
```

### Gestión de Tablas

```sql
-- Listar tablas
SHOW TABLES;

-- Ver estructura de tabla
DESCRIBE nombre_tabla;

-- Ver engines disponibles
SHOW ENGINES;
```

### Consultas Comunes

```sql
-- Contar registros
SELECT COUNT(*) FROM nombre_tabla;

-- Ver primeros registros
SELECT * FROM nombre_tabla LIMIT 10;

-- Analizar consulta
EXPLAIN SELECT * FROM nombre_tabla WHERE id = 1;
```

---

## 📖 Recursos Adicionales

### Documentación Oficial

- [MariaDB Documentation](https://mariadb.com/docs/)
- [MariaDB Knowledge Base](https://mariadb.com/kb/en/)
- [MariaDB Blog](https://mariadb.com/resources/blog/)

### Herramientas Recomendadas

- **HeidiSQL** - Cliente gratuito para Windows
- **DBeaver** - Cliente universal multiplataforma
- **MariaDB CLI** - Línea de comandos oficial

### Comunidades

- [MariaDB Community](https://mariadb.org/community/)
- [Stack Overflow - MariaDB](https://stackoverflow.com/questions/tagged/mariadb)
- [Reddit r/MariaDB](https://www.reddit.com/r/MariaDB/)

---

## 💡 Consejos para Principiantes

1. **Aprovecha la compatibilidad**: Si conoces MySQL, ya conoces MariaDB.
2. **Explora nuevos engines**: Aria, ColumnStore ofrecen ventajas únicas.
3. **Usa System Versioning**: Para tracking histórico de datos.
4. **Considera Galera**: Para alta disponibilidad.
5. **Monitorea el rendimiento**: Usa slow query log.

---

## ⚠️ Mejores Prácticas

### Seguridad

- Cambia la contraseña root inmediatamente
- Usa usuarios con privilegios mínimos necesarios
- Habilita el slow query log

### Rendimiento

- Ajusta innodb_buffer_pool_size
- Usa thread pool para muchas conexiones
- Indexa columnas de búsqueda

### Código

- Usa nombres descriptivos
- Documenta stored procedures
- Versiona tus esquemas

---

## 🧪 Ejercicios Prácticos

### Nivel Básico

1. Instala MariaDB en tu sistema
2. Crea una base de datos `Biblioteca`
3. Crea tablas con relaciones
4. Inserta datos de prueba

### Nivel Intermedio

1. Crea vistas para reportes
2. Implementa stored procedures
3. Configura backup automático

### Nivel Avanzado

1. Configura replicación
2. Implementa Galera Cluster
3. Optimiza consultas lentas

---

## 👨‍💻 Desarrollado por Isaac Esteban Haro Torres

**Ingeniero en Sistemas · Full Stack · Automatización · Data**

- 📧 Email: zackharo1@gmail.com
- 📱 WhatsApp: 098805517
- 💻 GitHub: https://github.com/ieharo1
- 🌐 Portafolio: https://ieharo1.github.io/portafolio-isaac.haro/

---

© 2026 Isaac Esteban Haro Torres - Todos los derechos reservados.
