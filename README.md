# credit-risk-vintage-analysis

Implementación de un modelo de Análisis de Cosechas (Vintage Analysis) para detectar variaciones en el apetito de riesgo, optimizando la detección temprana de deterioro de cartera.

Proceso de Construcción Técnica:


1.	Extracción y Limpieza: Consolidación de bases históricas de colocación (originación) y bases de comportamiento mensual (pagos/mora).

2\.	Cálculo de MOB (Months on Books): Creación de la métrica de maduración mediante la diferencia de fechas: MOB = (Mes Reporte – Mes Originación).

3\.	Definición del Evento de Mora: Clasificación de cuentas en mora (ej. +30 días) para calcular el numerador de la tasa.

4\.	Matriz de Pivotaje: Transformación de datos transaccionales a una estructura de cohorte (Filas: Mes Origen | Columnas: MOB | Valores: % Mora Acumulada).

5\.	Cálculo Acumulado: Implementación de lógica para que el % de mora refleje el deterioro total desde el nacimiento de la cosecha hasta el mes analizado.


Conclusión


Basado en la matriz de Vintage préstamos personales mora +30 días, se extraen los siguientes puntos críticos:


Aceleración de la Mora Temprana: Las cosechas de 08-2025 y 09-2025 muestran niveles de mora del 6.3% en el Mes 1, duplicando o triplicando el comportamiento de las cosechas de 2024 (que solían iniciar en 0%).


Deterioro Exponencial: La cosecha de agosto 2025 alcanza un 18.8% de mora en solo 3 meses (MOB 3). Comparado con la cosecha de agosto 2024 (que tenía 0% en el mismo periodo), indica un cambio drástico en el perfil de riesgo del cliente captado.


Quiebre de Tendencia: Se observa que a partir de julio 2025, todas las cohortes rompen la estabilidad histórica. Esto sugiere que el modelo de admisión actual no está filtrando correctamente el riesgo ante un posible cambio en el entorno macroeconómico o una relajación excesiva de las políticas de crédito.



