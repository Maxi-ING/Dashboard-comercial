# Dashboard comercial | Explorar el informe

**El PBIX permite recorrer el dashboard con los datos ya importados.** Para actualizarlo desde tu equipo, restaura la tabla de ventas en MySQL y ajusta el origen del informe.

## Abrir el dashboard

1. Descarga `Dashboard comercial.pbix` y ábrelo en Power BI Desktop.
2. Explora los gráficos y utiliza el filtro de región.
3. Con todas las regiones, los indicadores publicados son **80.567,85 de ventas, 518 unidades y 240 pedidos**. La tarjeta de ventas muestra el importe redondeado como 80,57 mil.

La vista de referencia está en `dashboardvista.png`.

## Actualizar desde MySQL

1. Prepara una base de trabajo llamada `control_ventas`.
2. Importa `dbventas2024.sql` en esa base. El archivo recrea la tabla `ventas_raw`: utiliza una base de prueba, porque reemplaza una tabla existente con ese nombre.
3. En Power BI, abre **Transformar datos** y configura el paso de origen para tu servidor y base MySQL.
4. Configura las credenciales localmente y actualiza el informe.

El origen documentado es MySQL local, en modo Import. La tabla de ventas del modelo se llama `control_ventas ventas_raw`; el calendario es `calc_calendario` y los indicadores están en `_medidas`.

## Alcance de los datos

La carga contiene 240 registros, del 1 de enero al 27 de agosto de 2024. Cada registro identifica un pedido. Los importes del SQL coinciden con los indicadores de la captura; esta comprobación no ejecuta el motor DAX.
