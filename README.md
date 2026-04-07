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

* **EMICRON**: Información de micronegocios en formato CSV.
* Link: https://microdatos.dane.gov.co/index.php/catalog/875/get-microdata
* **CIIU**: Clasificación de actividades económicas en formato CSV.
* Link: https://www.datos.gov.co/Comercio-Industria-y-Turismo/CODIGOS-CIIU-POR-MUNICIPIO/3vbk-w3sc/about_data
* **DIVIPOLA**: División territorial de Colombia en formato CSV.
* Link: https://www.datos.gov.co/Mapas-Nacionales/DIVIPOLA-C-digos-municipios/gdxc-w37w/about_data
* **IPC**: Índice de precios al consumidor en formato xlsx.
* Link: https://www.dane.gov.co/index.php/estadisticas-por-tema/precios-y-costos/indice-de-precios-al-consumidor-ipc
* **PIB**: Producto Interno Bruto por departamento en formato xlsx.
* Link: https://www.dane.gov.co/index.php/estadisticas-por-tema/cuentas-nacionales/cuentas-nacionales-departamentales
* **EMPRESAS**: Información empresarial en formato CSV.
* Link: https://www.datos.gov.co/Comercio-Industria-y-Turismo/Base-de-datos-NIT-y-Actividad-Econ-mica/cas9-r54x/about_data

* Las bases de datos se pueden encontrar listas para simular y los resultados de los datasets finales en el repositorio Zenodo con el identificador.
* Link: https://doi.org/10.5281/zenodo.19448823

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

## USO Y RESTRICCIONES DE LOS DATOS
Los datasets utilizados en este proyecto provienen de fuentes públicas como el Departamento Administrativo Nacional de Estadística (DANE) y el portal de Datos Abiertos Colombia. Estos datos se publican bajo esquemas de datos abiertos que permiten su acceso, reutilización y transformación para fines académicos, investigativos o de desarrollo. Sin embargo, su uso requiere citar adecuadamente la fuente original y respetar las condiciones de licencia abierta. Adicional, el usuario es responsable del uso adecuado de la información y de las interpretaciones derivadas del análisis. En el caso de los datos publicados por el DANE, estos cumplen con el principio de reserva estadística, por lo que la información se encuentra anonimizada y no permite identificar individuos o empresas específicas

