# Vivienda nueva en México

## Pregunta

¿Quién dejó de poder estrenar casa en México y por qué? El análisis compara los créditos de vivienda nueva, su monto promedio, la distribución por ingreso y la oferta registrada.

## Fuentes de datos

Los registros de financiamientos y oferta provienen de los [datos abiertos del SNIIV](https://sniiv.sedatu.gob.mx/Reporte/Datos_abiertos); `inpc.csv` es la serie del [INPC de INEGI](https://www.inegi.org.mx/temas/inpc/). Las copias de los 15 archivos incluidos se consultaron el 9 de octubre de 2026 y se guardan en `data/raw/`; todos pesan menos de 50 MB. Los precios por segmento de vivienda se citan a partir de los boletines de [SHF](https://www.gob.mx/shf), y los costos de construcción a partir de [CEICO-CMIC](https://www.cmic.org.mx/ceico/); esas series externas no se calculan en este notebook.

## Cómo reproducirlo

Clona `https://github.com/alexmufe/vivienda-nueva-mexico.git`, instala las versiones fijadas con `python -m pip install -r requirements.txt` y ejecuta todas las celdas de [`notebooks/vivienda_nueva.ipynb`](notebooks/vivienda_nueva.ipynb). También puedes correr desde la raíz `python -m nbconvert --to notebook --execute --inplace --ExecutePreprocessor.timeout=1800 notebooks/vivienda_nueva.ipynb`. Los datos ya están incluidos; no se requiere descarga externa.

## Qué produce

El crédito promedio pasó de $745 mil en 2020 a $1.188 millones en 2026 (+59%), frente a un aumento de 37% del INPC; descontada la inflación, el monto aumentó 16%. El índice de créditos otorgados quedó en 88.2 (2020 = 100). La participación del rango de ingreso más bajo bajó de 15.9% en 2020 a 7.4% en 2026, después de llegar a 17.5% en 2022. Los créditos para vivienda usada subieron de 60,627 a 85,718 entre enero y mayo. El notebook muestra las comparaciones y genera la [gráfica del crédito e inflación](docs/figuras/grafica_1_credito_inflacion.png).

## Límites

El monto promedio del crédito no es el precio de la vivienda: también depende del enganche, de la institución y de quién califica. La caída de los créditos al rango de ingreso más bajo puede reflejar menor acceso o cambios en el registro del ingreso. El ejercicio describe el acceso a vivienda nueva, no una escasez general: el documento estima que 96% del déficit habitacional corresponde a viviendas existentes con carencias y 4% a necesidad de vivienda nueva. La serie de oferta cambia de clasificación en 2024; para la comparación por segmento, el documento empieza en 2025. Haría falta observar precios de venta por segmento frente al ingreso de los hogares para determinar a quién le alcanza.

**Documento completo:** [Análisis sobre vivienda nueva](docs/Vivienda_nueva_AlejandroMunoz.md).
