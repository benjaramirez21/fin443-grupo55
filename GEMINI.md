# Instrucciones y Contexto para el Agente de IA - Proyecto FIN443 (Grupo 55)

## 1. Objetivo y Pregunta del Proyecto
Evaluar mediante un backtest fuera de muestra si la incorporación táctica de Cobre y Petróleo en un portafolio de acciones chilenas (IPSA) reduce la caída máxima (MDD) y las pérdidas durante períodos de estrés de mercado sin deteriorar la razón de Sharpe neta de costos.

## 2. Convenciones Financieras y de Cálculo (Obligatorias)
* **Retornos diarios:** Simples ($r_t = P_t / P_{t-1} - 1$), nunca logarítmicos.
* **Limpieza de datos:** Ordenar por fecha ascendente, eliminar fechas duplicadas, ajustar splits y rellenar precios faltantes con el último disponible (LOCF) solo después del primer precio válido de cada activo.
* **Anualización:** Volatilidad muestral $\sigma \times \sqrt{252}$; retorno medio $\bar{r} \times 252$; CAGR usando días calendario $/ 365,25$.
* **Tasa libre de riesgo ($r_f$):** Anual en fracción ($0,05$).
* **Costos de transacción:** Descontar explícitamente la rotación $T_j = \sum_i |w_{i,j} - w_{i,j-1}|$ multiplicada por el costo unitario en el primer día de cada período de rebalanceo.

## 3. Reglas de Reproducibilidad y Validación Crítica
* **Cero look-ahead bias:** Toda señal de estrés de mercado y todo peso de cartera en la fecha $t$ debe calcularse exclusivamente con datos disponibles hasta $t$. Prohibido usar cuantiles o momentos de la muestra completa.
* **Rutas y entorno:** Usar únicamente rutas relativas desde la raíz del repositorio (`datos/`, `codigo/`, `resultados/`), R base reproducible y semilla fija (`set.seed()`).
* **Integridad:** Prohibido inventar datos, referencias bibliográficas o DOIs. Toda cita debe corresponder a un artículo real verificado en Web of Science (Q1/Q2).
