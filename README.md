# SISTEMA-ANALITICO-DE-COMERCIO-COLOMBIANO-INTEGRADO-CON-INVENTARIO-Y-FACTURACION-ETL-WAREHOUSE
Sistema analítico del comercio colombiano basado en procesos ETL y Data Warehouse. Integra datos empresariales, macroeconómicos y geográficos para analizar ventas, identificar patrones regionales y apoyar la toma de decisiones en PYMES.

# Sistema Analítico de Comercio Colombiano

## Descripción

Este proyecto desarrolla un sistema de analítica de datos enfocado en el comercio colombiano, integrando información empresarial, macroeconómica y geográfica mediante un proceso ETL.

El objetivo es construir un **Data Warehouse** que permita analizar el comportamiento de las ventas, identificar patrones económicos y apoyar la toma de decisiones en pequeñas y medianas empresas (PYMES).

---

## Objetivos

* Integrar múltiples fuentes de datos (EMICRON, CIIU, DIVIPOLA, IPC, PIB)
* Diseñar un modelo dimensional tipo estrella
* Analizar la distribución de ventas y su comportamiento
* Evaluar la relación entre variables macroeconómicas y ventas
* Generar indicadores clave (KPIs)

---

## Fuentes de datos

* **EMICRON**: Información de micronegocios 
* **CIIU**: Clasificación de actividades económicas
* **DIVIPOLA**: División territorial de Colombia
* **IPC**: Índice de precios al consumidor
* **PIB**: Producto Interno Bruto por departamento
* **EMPRESAS**: Información empresarial

---

## Proceso ETL

### 1. Extracción

* Carga de múltiples datasets en formatos CSV y XLSX

### 2. Transformación

* Limpieza de datos
* Estandarización de variables
* Eliminación de duplicados
* Tratamiento de valores nulos
* Transformaciones logarítmicas
* Feature engineering (KPIs)

### 3. Carga

* Integración en modelo estrella
* Construcción de tabla de hechos (*fact_emicron*)
* Creación de dimensiones (tiempo, geografía, sector)

---

## Modelo de datos

Se implementó un esquema tipo **estrella**, donde:

* **Tabla de hechos**: ventas, ingresos, productividad
* **Dimensiones**:

  * Geográfica (departamento)
  * Económica (CIIU)
  * Temporal (año, mes)
  * Macroeconómica (PIB, IPC)

---

## Principales hallazgos

* Distribución de ventas altamente sesgada (asimetría positiva)
* Alta concentración de ingresos en pocas empresas
* Fuerte desigualdad regional
* Baja correlación entre ventas y PIB
* Presencia significativa de outliers

---

## Tecnologías utilizadas

* Python / R
* Pandas / dplyr
* SQL
* Excel
* Modelado de datos

---

## Posibles mejoras

* Implementación de modelos predictivos (Machine Learning)
* Desarrollo de dashboards (Power BI / Tableau)
* Inclusión de variables como informalidad o acceso a crédito
* Automatización del pipeline ETL

---

## Autor

**Raúl Ernesto Díaz Cuchala**

Proyecto académico – ETL y Ciencia de Datos
Universidad Autónoma de Occidente

---

## 📎 Licencia

Uso académico

