# PROYECTO-SPRINT-8

🛺 Análisis Exploratorio de Datos de Taxis y Evaluación de Hipótesis sobre Clima
Este proyecto analiza los datos de viajes en taxi en la ciudad de Chicago para:

Identificar las empresas de taxi con mayor volumen de viajes.

Determinar los barrios con mayor número promedio de finalizaciones de viaje.

Evaluar si las condiciones climáticas afectan la duración de los viajes desde el Loop hasta el Aeropuerto Internacional O'Hare.

📁 Archivos Utilizados
project_sql_result_01.csv: Datos agregados por empresa de taxis y número total de viajes.

project_sql_result_04.csv: Promedio de viajes por barrio de destino.

project_sql_result_07.csv: Detalles de viajes realizados los sábados con y sin lluvia, incluyendo duración, fecha y condiciones climáticas.

📊 Análisis Exploratorio
Se exploraron dos aspectos clave:

Empresas de taxis: Las más grandes dominan en cantidad de viajes. Esto puede estar relacionado con su cobertura geográfica, presencia digital, precios y calidad del servicio.

Barrios con más viajes: Las zonas con mayor actividad turística, comercial o conectividad (como aeropuertos o estaciones) presentan el mayor número de llegadas.

Se utilizaron gráficos de barras con matplotlib y seaborn para visualizar estos patrones.

🧪 Prueba de Hipótesis
Hipótesis:

H₀: La duración promedio de los viajes desde el Loop hasta O'Hare es la misma los sábados lluviosos y los sábados sin lluvia.

H₁: La duración promedio de los viajes desde el Loop hasta O'Hare cambia los sábados lluviosos.

Se aplicó una prueba t de muestras independientes (scipy.stats.ttest_ind) con equal_var=False debido a posibles varianzas distintas.

📌 Resultados
El valor p obtenido se interpreta con un nivel de significancia de α = 0.05.

Si p < 0.05, se concluye que el clima sí afecta la duración de los viajes.

Si p ≥ 0.05, no hay evidencia suficiente para afirmar que el clima tenga un efecto significativo.
