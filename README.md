# Estrategia de fidelización y análisis de demanda en un Laboratorio de Análisis Agropecuario

Proyecto de Ciencia de Datos orientado a detectar fuga de clientes, analizar patrones de demanda y mejorar la planificación operativa de un laboratorio agropecuario.

## Contexto

El laboratorio cuenta con registros históricos de clientes, muestras y transacciones, pero actualmente opera de manera reactiva. Esto dificulta anticipar:

- pérdida de clientes,
- picos de demanda,
- necesidades de capacidad operativa,
- planificación de insumos y personal.

## Objetivo

Aplicar técnicas de ciencia de datos para convertir datos operativos en información accionable, con foco en:

- **segmentación de clientes**,
- **detección de churn**,
- **análisis de estacionalidad**,
- **optimización de recursos**.

## Dataset

La fuente de información es una base de datos SQL interna y estructurada.

### Variables principales

**Clientes**
- ID cliente
- Razón social
- Tipo de cliente

**Muestras**
- ID muestra
- Fecha de ingreso
- Especie de cultivo
- Tipo de análisis

**Transacciones**
- Facturación histórica
- Volumen por período
- Forma de pago

## Análisis propuesto

### Calidad de datos
- Detección de nulos
- Validación temporal
- Revisión de consistencia

### EDA
- Volumen total de muestras
- Pareto de cultivos
- Concentración de clientes
- Distribución por tipo de análisis

### Series temporales
- Identificación de picos de demanda
- Estacionalidad por cultivo
- Evolución mensual/anual

### Fidelización
- Identificación de clientes activos e inactivos
- Detección de riesgo de abandono
- Segmentación para acciones comerciales

## Preguntas clave

- ¿Qué clientes podrían dejar de operar con el laboratorio?
- ¿Qué cultivos concentran la mayor demanda?
- ¿Qué meses requieren mayor capacidad operativa?
- ¿Cómo anticipar mejor la demanda futura?

## Herramientas posibles

- Python
- SQL
- Pandas
- Matplotlib / Seaborn
- Jupyter Notebook
- Power BI

## Equipo

- Cristian Albarracín
- Juan Calero
- Sabrina Maldonado
- Julieta Strada
- Isaías Sudañez
- Nahuel Espiga

## Institución

**Tecnicatura en Inteligencia Artificial — ISPC**  
**Docente:** Carlos Charletti

## Estado

En desarrollo.
