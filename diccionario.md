# Diccionario — I1: sensores y NOX

Una fila contiene medidas agregadas durante una hora (media o suma según variable) de una turbina de Turquía. CSV UTF-8, coma separadora, punto decimal. Nueve predictores, objetivo NOX y dos auxiliares. Las unidades se conservan como publicadas por UCI.

| Campo | Descripción | Unidad / uso |
|---|---|---|
| AT | Temperatura ambiente | °C; predictor |
| AP | Presión ambiente | mbar; predictor |
| AH | Humedad ambiente | %; predictor |
| AFDP | Diferencia de presión del filtro de aire | mbar; predictor |
| GTEP | Presión de escape de la turbina | mbar; predictor |
| TIT | Temperatura de entrada de la turbina | °C; predictor |
| TAT | Temperatura posterior a la turbina | °C; predictor |
| TEY | Producción energética de la turbina | MWh; predictor |
| CDP | Presión de descarga del compresor | mbar según fuente, sin reinterpretación; predictor |
| NOX | Concentración de óxidos de nitrógeno | mg/m³; objetivo |
| anio | Año del CSV original | Auxiliar de EDA; no predictor |
| id_medicion | Año y posición original del registro | Trazabilidad; no predictor ni timestamp |

La fuente afirma orden cronológico, pero no publica fecha por fila ni garantiza horas consecutivas. No convertir ID en hora del calendario. No se corrige humedad fuera de0–100 ni unidad CDP sin documentación. CO se excluye del paquete estudiantil. particiones.csv contiene ID, año y asignación, sin objetivos.
