# Proyecto FIN443 - Grupo 55
**Universidad Adolfo Ibáñez - Magíster en Finanzas 2026**

## 1. Pregunta de Investigación
¿Permite la inclusión del cobre y el petróleo como commodities tácticos en una cartera de acciones locales (IPSA/Chile) reducir la caída máxima (Maximum Drawdown) y las pérdidas en períodos de estrés de mercado, sin deteriorar el Sharpe?

## 2. Datos
* **Activos:** Acciones locales chilenas (IPSA) y series de precios de Cobre y Petróleo (WTI/Brent).
* **Ubicación:** Carpeta `datos/` (archivos crudos sin edición manual).

## 3. Estructura del Repositorio
* `datos/`: Series de precios originales.
* `codigo/`: Scripts en R numerados para lectura, limpieza, señales tácticas y backtesting.
* `resultados/`: Tablas de métricas (`CSV`) y figuras generadas automáticamente.

## 4. Cómo ejecutar el proyecto
Desde la terminal en la raíz del proyecto, ejecutar:
`Rscript codigo/00_ejecutar_todo.R`
