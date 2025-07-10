# 🧠 Análisis Predictivo de Resultados Saber Pro (2018–2022)

## 🎯 Objetivo del Proyecto

Este proyecto tiene como propósito predecir los resultados en los componentes genéricos de la prueba **Saber Pro** de un estudiante colombiano, a partir de sus características **demográficas y socioeconómicas**, utilizando datos históricos del periodo **2018 a 2022**. El enfoque se centra en responder:

> **¿Qué resultados probablemente obtendrá un estudiante en los componentes genéricos de la prueba Saber Pro de acuerdo a sus características?**

## 🧩 Componentes del Proyecto

### 1. 🔄 Proceso ETL (Extract, Transform, Load)
- **Herramienta**: SQL Server Integration Services (SSIS)
- **Origen**: Archivos planos `.csv` y `.rmp` de RapidMiner
- **Destino**: Azure SQL Database (modelo estrella con tablas `FACT` y `DIM`)
- **Contenedores Docker** para levantar entorno local simulado de Azure SQL

#### Principales scripts del DWH:
- `Scripts Tablas DWH/ESTUDIANTE_Create.sql`
- `Scripts Tablas DWH/FAMI_EDUCACIONMADRE_CREATE.sql`
- `Scripts Tablas DWH/ESTU_PAGOMATRICULABECA_Create.sql`
- ...

### 2. 📊 Visualización de Datos – Power BI
- Dashboards interactivos construidos en **Power BI Desktop**
- Indicadores por región, género, estrato, tipo de financiación, etc.
- Panel predictivo que estima puntajes por estudiante según variables

### 3. 🤖 Modelado Predictivo (RapidMiner)
- Modelos entrenados con técnicas de regresión y clasificación
- Evaluación de desempeño del modelo con métricas como MAE, R², RMSE
- Archivo fuente: `RapidMiner/data/SaberPro_Descriptivo.rmp`

---

## 🛠️ Tecnologías Utilizadas

| Herramienta | Descripción |
|------------|-------------|
| **SQL Server / Azure SQL** | Almacenamiento y procesamiento de datos |
| **SSIS (ETL)** | Transformación de datos con `.dtsx` packages |
| **Docker** | Contenedor para entorno local simulado de Azure |
| **Power BI** | Visualización interactiva de resultados |
| **RapidMiner** | Construcción de modelos de predicción |

---

## 🐳 Docker Setup

```bash
# Construcción del contenedor
docker build -t saberpro-sql .


