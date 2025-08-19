# Telecom X - Análisis de Evasión de Clientes (Customer Churn)

## 📋 Descripción del Proyecto

Este proyecto realiza un análisis completo de **customer churn** (evasión de clientes) para la empresa ficticia **Telecom X**, que enfrenta una alta tasa de cancelaciones. El objetivo es identificar patrones y factores que contribuyen a la pérdida de clientes mediante un análisis exploratorio de datos estructurado.

## 🎯 Objetivos

- **Objetivo Principal**: Identificar los factores que influyen en la decisión de los clientes de abandonar Telecom X
- **Objetivo Secundario**: Proporcionar insights accionables para el equipo de Ciencia de Datos
- **Objetivo Técnico**: Implementar una metodología ETL robusta para el procesamiento de datos

## 🛠️ Metodología ETL

El proyecto sigue una metodología **ETL (Extract, Transform, Load)** estructurada:

### 1. **Extracción**
- Carga de datos desde API JSON pública
- Conversión a DataFrame de Pandas
- Verificación de integridad de datos

### 2. **Transformación**
- Exploración de estructura y tipos de datos
- Limpieza de inconsistencias y valores ausentes
- Normalización de columnas y creación de variables derivadas
- Creación de columna **"Cuentas_Diarias"** basada en facturación mensual
- Estandarización opcional (conversión Yes/No a 1/0)

### 3. **Carga y Análisis**
- Análisis descriptivo completo
- Visualización de distribuciones de evasión
- Análisis por variables categóricas y numéricas
- Generación de insights y recomendaciones

## 📊 Fuente de Datos

- **API**: https://raw.githubusercontent.com/ingridcristh/challenge2-data-science-LATAM/main/TelecomX_Data.json
- **Formato**: JSON
- **Registros**: 7,267 clientes
- **Variables**: Información demográfica, servicios contratados, datos de facturación y estado de evasión

## 🔧 Tecnologías Utilizadas

- **Python 3.12.4+**
- **Pandas**: Manipulación y análisis de datos
- **NumPy**: Operaciones numéricas
- **Matplotlib**: Visualizaciones estáticas
- **Seaborn**: Gráficos estadísticos avanzados
- **Requests**: Consumo de API
- **Jupyter Notebook**: Entorno de desarrollo interactivo

## 📁 Estructura del Proyecto

```
telecom_churn_analysis/
│
├── TelecomX_LATAM_parte2.ipynb    # Notebook principal con análisis completo
└── README.md                        # Documentación del proyecto
```

## 🚀 Instalación y Uso

### Prerrequisitos
```bash
python >=  3.12.4
pip
```

### Instalación
```bash
# Clonar o descargar el proyecto
cd telecom_churn_analysis

# Instalar dependencias
pip install -r requirements.txt

# Ejecutar Jupyter Notebook
jupyter notebook TelecomX_Churn_Analysis.ipynb
```

### Ejecución
1. Abrir el notebook `TelecomX_LATAM_parte2.ipynb`
2. Ejecutar todas las celdas secuencialmente
3. Los datos se cargarán automáticamente desde la API
4. Las visualizaciones se generarán en línea

## 📈 Principales Hallazgos

### Tasa de Evasión General
- **26.5%** de los clientes abandonan el servicio

### Factores de Alto Riesgo
- **Contratos mes a mes**: Mayor tasa de evasión
- **Servicio de Fibra Óptica**: Asociado con mayor abandono
- **Pago con Cheque Electrónico**: Método de pago problemático
- **Clientes nuevos**: Mayor riesgo durante primeros meses
- **Sin servicios adicionales**: Falta de "adherencia" al servicio

### Variables Críticas
1. **Tenure** (antigüedad): Correlación negativa con churn
2. **MonthlyCharges**: Cargos altos aumentan probabilidad de abandono
3. **Servicios adicionales**: Su ausencia incrementa el riesgo

## 💡 Recomendaciones

### Acciones Inmediatas
- Programa de retención para clientes nuevos (primeros 6 meses)
- Revisión de estructura de precios para fibra óptica
- Incentivos para contratos de largo plazo

### Estrategias a Mediano Plazo
- Bundling de servicios (paquetes integrados)
- Mejora en métodos de pago
- Segmentación de clientes por perfil de riesgo

## 📊 Visualizaciones Incluidas

- Distribución de evasión (barras y pastel)
- Análisis por variables categóricas (barras apiladas)
- Distribuciones de variables numéricas (histogramas)
- Análisis de boxplots por grupos
- Matriz de correlación (heatmap)

## 🔍 Análisis de Calidad de Datos

- **Valores ausentes**: Identificados y tratados apropiadamente
- **Duplicados**: Verificación de registros únicos
- **Tipos de datos**: Conversión y normalización
- **Consistencia**: Estandarización de formatos



## 📄 Licencia

Este proyecto es de uso educativo y de demostración para análisis de datos.


