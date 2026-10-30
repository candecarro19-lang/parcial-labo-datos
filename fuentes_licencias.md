# Fuentes y licencia — I1

Gas Turbine CO and NOx Emission Data Set (2019). UCI Machine Learning Repository. DOI10.24432/C5WC95.

- Ficha: https://archive.ics.uci.edu/dataset/551/gas+turbine+co+and+nox+emission+data+set
- Descarga: https://archive.ics.uci.edu/static/public/551/gas+turbine+co+and+nox+emission+data+set.zip
- Licencia: CC BY4.0, https://creativecommons.org/licenses/by/4.0/
- Descarga original del relevamiento:7/9/2026. Verificación de ficha, unidades y licencia:18/9/2026.
- SHA-256 ZIP original:55fdb1acc25f05bd9c77aac285c424e9154ffb0dbf1bbadb56b69a1142231295.

Se usan gt_2011.csv (7.411), gt_2012.csv (7.628) y gt_2013.csv (7.152):22.191 registros. El21.947 del relevamiento era un error aritmético, no un recorte: no se eliminan244 registros para reproducirlo. No hay nulos ni duplicados completos del conjunto original de11 mediciones en esos años. Se conserva cada fila, se excluye CO y se añade ID de origen y año auxiliar.

Partición aleatoria train_size0,7,random_state42; resto dividido test_size0,5,random_state42. CSV ordenados por ID después de separar:15.533/3.329/3.329. Los hashes coinciden con el piloto congelado. No hubo búsqueda de semillas ni remuestreo para mejorar marcas.

La fuente informa orden cronológico sin timestamps. Nuestro protocolo histórico aleatorio no replica la recomendación UCI de desarrollar2011–2013 y probar2014–2015. Puede existir dependencia temporal entre conjuntos. Los años posteriores quedan fuera del examen. La unidad CDP se reproduce según UCI, sin conversiones físicas.

Estabilidad: cinco submuestras del80% sin reemplazo de entrenamiento con semillas42–46; cada ajuste aprende su escala. Se convierten los coeficientes multiplicando coef/escala_submuestra por escala_train para comparar unidades comunes. La selección sigue basada sólo en RMSE de validación. No se usan prueba ni nuevas configuraciones para diagnosticar.

Esquema del proceso adaptado de https://www.energy.gov/hgeo/how-gas-turbine-power-plants-work; el par Mermaid/PNG se conserva y el PNG está embebido. Renderizador: @oai/artifact-tool2.8.59, fromMermaid, perfil claro. No representa un plano ni una ubicación instrumental detallada.

Transformaciones docentes con atribución a la fuente; sin aval del repositorio ni del autor. No se infieren cumplimiento normativo, causalidad o aplicabilidad a otra planta.
