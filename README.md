# ISPC 2026 
## Laboratorio de Análisis Agropecuario: Estrategia de fidelización y análisis de demanda

Proyecto integrador de la **Tecnicatura en Inteligencia Artificial — ISPC**, orientado al análisis de datos de un laboratorio de análisis agropecuario para mejorar la fidelización de clientes y la previsibilidad de la demanda.

**Espacios curriculares**
-Ciencia de datos
-Analista de datos
-Proyecto integrador

Entrega EVIDENCIA 1 - CIENCIA DE DATOS

## 1. Descripción del problema

El problema se centra en la fuga de clientes y la falta de previsibilidad de la demanda en un Laboratorio de Análisis Agropecuario. A pesar de contar con registros históricos, la entidad opera de forma reactiva.

Esto gener una baja capacidad para tomar decisiones basadas en datos, generando impactos negativos:

Impacto Económico: Pérdida de ingresos por clientes que dejan de enviar muestras sin ser detectados (Churn). Falta de visibilidad sobre la cartera activa
Impacto Operativo: Incapacidad de planificar la capacidad del laboratorio (insumos, personal) ante picos estacionales de cultivos como el maní o la soja. Problemas para planificar recursos y mano de obra.

Objetivo de Ciencia de Datos: Transformar registros transaccionales en un modelo de segmentación de clientes y análisis de series temporales para fidelización y optimización de recursos.

## 2. Identificación de Fuentes de Datos
Para este proyecto, la fuente es una Base de Datos Operativa (SQL/Estructurada) interna de la empresa, de la cuál se dispone. Los datos se encuentran disponibles desde Junio de 2020 con un bache en los años 2023 y 2024 por una pérdida de la BD original. Retoman la continuidad en Marzo de 2025.

Entidades principales identificadas en el Dataset:
Clientes: ID, Razón Social,CUIT.
Muestras: ID de muestra, Fecha de ingreso, Especie de cultivo (Maní, Soja, Maíz, etc.), Tipo de análisis solicitado (Germinación, Pureza, Vigor).
Transacciones: costo por muestra, bonificación aplicada, forma de pago.

## 3. Primer Análisis del Dataset (Exploratory Data Analysis - EDA)

En esta etapa inicial para la materia, debemos proponer las métricas que vamos a calcular para "entender" los datos:

A. Análisis de Calidad y Limpieza
Datos Faltantes: Identificar nulos en campos críticos como "Especie" o "Fecha".
Consistencia Temporal: Verificar que el rango de fechas sea continuo para no tener "huecos" en el análisis de estacionalidad.

B. Estadísticas Descriptivas (KPIs Iniciales)
Volumen Total: ¿Cuántas análisis realiza el laboratorio por año/mes? 
Pareto de Cultivos: Determinar qué especies representan el 80% del volumen.
Concentración de Clientes: ¿Depende el laboratorio de pocos clientes grandes o de muchos pequeños? 
Fidelización de clientes: clientes fidelizados vs detractores.

C. Análisis de Estacionalidad (Time Series)
Visualización de los "picos" de trabajo. Estacionalidad en la demanda.

D. Evolución de precios en el tiempo, ingresos mensuales/anuales

## Objetivo general

Desarrollar una solución analítica que permita transformar los datos históricos del laboratorio en información útil para la toma de decisiones.

## Objetivos específicos

- Identificar clientes activos, inactivos y en riesgo de abandono.
- Analizar la evolución histórica del volumen de muestras.
- Detectar patrones de estacionalidad y picos de demanda.
- Segmentar clientes por tipo y comportamiento.
- Construir un dashboard con indicadores clave para distintos usuarios del laboratorio.

## Problema a resolver

El laboratorio posee una base de datos operativa con registros de:
- clientes,
- muestras,
- especies analizadas,
- fechas de ingreso,
- tipos de análisis.

Sin embargo, esa información no se utiliza de manera estratégica para:
- detectar fuga de clientes,
- analizar estabilidad de la demanda,
- anticipar cuellos de botella,
- mejorar la comunicación y fidelización.

## Solución propuesta

Se propone desarrollar un **Dashboard de Inteligencia de Clientes y Demanda**, que permita visualizar indicadores relevantes para la gestión del laboratorio.

### Alcance inicial
- Clientes activos, inactivos y en riesgo de abandono.
- Volumen de muestras por mes y por año.
- Análisis por especie de cultivo.
- Análisis por tipo de estudio.
- Estacionalidad de la demanda.
- Promedio de muestras por cliente.
- Segmentación por tipo de cliente.
- Resumen ejecutivo de KPIs.

## Tecnologías y herramientas

- **Python**
- **Pandas**
- **Google Colab**
- **Matplotlib / Plotly**
- **Google Drive**
- **GitHub Projects**
- **Base de datos operativa del laboratorio**

## Variables principales del proyecto

- Fecha de ingreso
- Especie de cultivo
- Tipo de análisis
- ID de cliente
- Tipo de cliente
- Cantidad / volumen
- Ubicación / localidad

## Historias de usuario iniciales

HISTORIAS DE USUARIO REFINADAS

HU-01 · Identificación de clientes frecuentes Como responsable del laboratorio, quiero visualizar un listado de clientes con su volumen de muestras enviadas en un período de tiempo, para identificar a los clientes más frecuentes, priorizar acciones de seguimiento y tomar decisiones comerciales informadas.

HU-02 · Reporte de cultivos por especie y período Como coordinador de Relaciones Institucionales, quiero visualizar un reporte de muestras analizadas agrupadas por especie y período, para identificar las especies con mayor demanda y orientar campañas de comunicación dirigidas a los productores.

HU-03 · Evolución mensual y estacionalidad del volumen de muestras Como analista del laboratorio, quiero visualizar la evolución mensual del volumen de muestras recibidas e identificar patrones de estacionalidad cuando el histórico lo permita, para detectar tendencias en el tiempo y anticipar picos de demanda que ayuden a optimizar la asignación de insumos y personal.

HU-04 · Identificación de clientes inactivos por patrón de envío Como responsable de marketing, quiero identificar a los clientes que no han enviado muestras durante un período superior al ciclo habitual de su cultivo principal, o superior a 90 días cuando ese dato no está disponible, para diseñar acciones de recuperación oportunas y contextualmente relevantes según el perfil productivo de cada cliente.

HU-05 (Épica) · Resumen Ejecutivo Estratégico — Dashboard Institucional HU-05.1 · Indicadores de volumen y facturación mensual Como director institucional, quiero visualizar gráficos mensuales de muestras analizadas e ingresos devengados, para monitorear el nivel de actividad y la facturación del laboratorio.

HU-05.2 · Análisis de crecimiento interanual (YoY) Como director institucional, quiero ver el porcentaje de variación anual del volumen de muestras y de los ingresos, para evaluar el ritmo de crecimiento del laboratorio comparado con el año anterior.

HU-05.3 · Reporte de eficiencia en tiempos de respuesta Como director institucional, quiero consultar el tiempo promedio de entrega de resultados agrupado por especie y tipo de análisis, para medir la eficiencia del laboratorio y garantizar el cumplimiento de los acuerdos de nivel de servicio.

HU-06 · Segmentación estratégica de clientes (Modelo RFM) Como responsable comercial, quiero clasificar la cartera de clientes mediante un modelo que combine Recencia, Frecuencia y Valor Monetario (RFM) durante el ciclo 25/26, para priorizar las acciones de recupero en función del impacto económico real y diseñar estrategias de retención proactivas antes de que los clientes de alto valor abandonen el laboratorio.

## Organización del equipo

- **Sabrina Maldonado**— Project Manager
- **Nahuel Espiga** — QA (solo participa en la materia Proyecto integrador)
- **Julieta Strada** — Business Analyst
- **Cristian Albarracín** — Dev / Data Scientist
- **Juan Calero** — Dev / Data Scientist
- **Isaías Sudañez** — Dev / Data Scientist

## Plan de trabajo

### Fase 1 — Kick-off
Definición del problema, roles, historias de usuario, carpeta compartida y board Kanban.

### Fase 2 — Exploración de datos
Análisis exploratorio, limpieza, normalización y primeras visualizaciones.

### Fase 3 — Producto intermedio
Construcción de un prototipo del dashboard y validación inicial.

### Fase 4 — Entrega final
Presentación de dashboard funcional, documentación técnica y cierre del proyecto.

## Repositorio

Este repositorio contiene los archivos, avances y entregables técnicos vinculados al proyecto integrador.

## Estado del proyecto

En desarrollo.

## Integrantes

- Cristian Albarracín
- Juan Calero
- Sabrina Maldonado
- Julieta Strada
- Isaías Sudañez

## Docente
**Carlos Charletti**
**Dianela Accietto**
**Pratta Nahuel**
**Salomon Yamil**

LINK A COLAB https://colab.research.google.com/drive/1GdEe4CbxwAsWUt4NmB0V_fLcWaEGSv1A?usp=sharing

