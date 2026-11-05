# Proyecto de Riesgo Crediticio - Fase 1: Diagnóstico y Calidad de Datos (EDA)

Este repositorio documenta la **Fase 1: Diagnóstico y Calidad de Datos (EDA) con Enfoque de Negocio**. El objetivo de esta fase es evaluar la salud financiera de la cartera para tomar decisiones informadas sobre el modelado predictivo. 

## Pilares del Análisis Exploratorio

El flujo de trabajo se estructura en cuatro etapas clave para garantizar la viabilidad de los datos:

* **Integridad de la Información:** Verificación de tipos de datos, nulos y registros duplicados. El procesamiento confirma un conjunto de 25.000 registros sin valores nulos ni registros duplicados.
* **Coherencia Financiera (Reglas de Negocio):** Detección de inconsistencias lógicas en los perfiles financieros. Las validaciones demostraron que la cartera es coherente: cero ingresos o préstamos negativos, Puntaje Crediticio dentro del rango válido de 300-850, y Nivel de Endeudamiento (DTI) contenido en el rango 0-100%.
* **Distribución del Riesgo y Outliers:** Cuantificación de valores atípicos mediante el método de Rango Intercuartílico (IQR) y análisis visual de cómo estas variables impactan en el incumplimiento. 
* **Comportamiento de la Cartera (Desbalance):** Cuantificación de los clientes cumplidores versus los casos de impago para preparar estrategias de remuestreo o ajuste de pesos.

## Hallazgos y Resultados de Outliers (IQR)

Durante la evaluación de dispersión, se cuantificaron los siguientes valores atípicos en las variables clave del negocio:

* **Ingreso Anual:** 976 clientes.
* **Monto del Préstamo:** 157 clientes.
* **Puntaje de Crédito:** 167 clientes.
* **Relación Deuda/Ingreso (DTI):** 663 clientes.

## Variables del Dataset

El análisis se centra en las siguientes métricas de los clientes:

* `Ingreso_Anual` (float64)
* `Monto_Prestamo` (float64)
* `Puntaje_Credito` (float64)
* `Relacion_Deuda_Ingreso` (float64)
* `Riesgo_Impago` (int64) - Variable objetivo

## Uso y Ejecución

Para replicar este análisis, asegúrate de tener instaladas las dependencias de manipulación de datos y visualización (Pandas y Seaborn). Al ejecutar las celdas del Jupyter Notebook, se generarán los logs de calidad de datos en consola y las gráficas comparativas (`boxplot`) que cruzan las variables predictoras contra el indicador de impago.


link presentación: https://canva.link/e361tccfjaq5o64
