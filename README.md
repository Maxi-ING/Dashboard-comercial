# 📊 Dashboard Comercial y Control de Ventas | Power BI & MySQL

![Power BI](https://shields.io)
![MySQL](https://shields.io)
![Markdown](https://shields.io)

## 📌 Contexto del Proyecto
En el entorno actual del comercio digital (Marketplace), la dispersión de datos transaccionales dificulta la toma de decisiones estratégicas en tiempo real. Este proyecto resuelve la falta de visibilidad comercial mediante el desarrollo de una solución analítica centralizada (Business Intelligence), permitiendo a los directores comerciales monitorear el rendimiento del negocio, identificar categorías líderes y optimizar las operaciones financieras y regionales.

## 🛠️ Solución Desarrollada
Se diseñó e implementó un dashboard interactivo de punta a punta que transforma datos crudos en insights accionables, reduciendo el tiempo de interpretación de reportes para los tomadores de decisiones.

La arquitectura de la solución incluye:
1. **Extracción y Almacenamiento:** Carga, limpieza y optimización del dataset transaccional (*Online Sales Dataset*) dentro de un servidor local **MySQL**.
2. **Modelado de Datos:** Conexión directa desde **Power BI** mediante arquitectura de esquema en estrella, separando la tabla de hechos transaccionales de las dimensiones analíticas.
3. **Modelado Temporal:** Creación e implementación de una tabla maestra de tiempos (`DimCalendario`) optimizada en **DAX** para habilitar análisis cronológicos estables.
4. **Capa de Métricas (DAX):** Desarrollo de cálculos y KPIs comerciales clave centralizados en una tabla exclusiva de medidas.

## 📊 Indicadores Clave de Rendimiento (KPIs) Implementados
* **Ventas Totales:** Medición de ingresos brutos acumulados utilizando la agregación monetaria final de cada orden.
* **Unidades Vendidas:** Control del volumen físico de productos distribuidos en el inventario.
* **Total Pedidos:** Monitoreo operativo del volumen de transacciones únicas procesadas en la plataforma (`DISTINCTCOUNT`).

## ⚙️ Estructura Técnica del Modelo
* **Origen de Datos:** Conexión local a MySQL Server (`localhost`) cargada mediante modo **Import** para un rendimiento óptimo de memoria.
* **Esquema en Estrella:** Relación unidireccional (1:*) desde la dimensión de tiempo hacia la tabla de hechos transaccionales conectada por campos de fecha rígidos.
