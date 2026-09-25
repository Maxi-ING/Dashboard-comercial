# Dashboard Comercial y Control de Ventas | Power BI & MySQL


## Contexto del Proyecto
En el entorno actual del comercio digital (Marketplace), la dispersión de datos transaccionales dificulta el seguimiento y análisis del rendimiento comercial. Este proyecto resuelve la falta de visibilidad comercial mediante el desarrollo de una solución analítica centralizada (Business Intelligence), permitiendo a los directores comerciales monitorear el rendimiento del negocio, identificar categorías líderes y optimizar las operaciones financieras y regionales.

## Solución Desarrollada
Se diseñó e implementó un dashboard interactivo de punta a punta que transforma datos crudos en insights accionables, reduciendo el tiempo de interpretación de reportes para los tomadores de decisiones.

La arquitectura de la solución incluye:
1. **Extracción y Almacenamiento:** Carga, limpieza y optimización del dataset transaccional (*Online Sales Dataset*) dentro de un servidor local **MySQL**.
2. **Modelado de Datos:** Conexión directa desde **Power BI** en modo **Import**, con una tabla de ventas, una tabla calendario para el análisis temporal y una tabla de medidas.
3. **Modelado Temporal:** Creación e implementación de la tabla calendario `calc_calendario` en **DAX** para habilitar análisis cronológicos estables.
4. **Capa de Métricas (DAX):** Desarrollo de cálculos y KPIs comerciales clave centralizados en una tabla exclusiva de medidas.

## Indicadores Clave de Rendimiento (KPIs) Implementados
* **Ventas Totales:** Medición de ingresos brutos acumulados utilizando la agregación monetaria final de cada orden.
* **Unidades Vendidas:** Control del volumen físico de productos distribuidos en el inventario.
* **Total Pedidos:** Monitoreo operativo del volumen de transacciones únicas procesadas en la plataforma (`DISTINCTCOUNT`).

## Estructura Técnica del Modelo
* **Origen de datos:** Tabla `ventas_raw` de una base MySQL local (`localhost`), cargada en Power BI mediante modo **Import**. Los cambios en la fuente se reflejan después de actualizar el modelo.
* **Tablas del modelo:** `control_ventas ventas_raw` contiene las transacciones; `calc_calendario` organiza el análisis por fecha; `_medidas` reúne los indicadores DAX.
