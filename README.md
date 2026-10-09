# Vivienda nueva en México

## Pregunta

¿Cómo cambiaron entre 2020 y mayo de 2026 el acceso al crédito para vivienda nueva, sus montos y la oferta habitacional? El notebook compara los indicadores publicados con los que se obtienen de los microdatos, sin cambiar la metodología del análisis.

## Fuentes de datos

Los CSV de financiamientos y oferta se distribuyen en `data/raw/`; la fuente declarada es el [Sistema Nacional de Información e Indicadores de Vivienda (SNIIV)](https://sniiv.sedatu.gob.mx/), sección de datos abiertos. El INPC (`inpc.csv`) corresponde a una exportación del [Banco de Información Económica de INEGI](https://www.inegi.org.mx/app/indicadores/). Consulta y descarga de las copias incluidas: 9 de octubre de 2026. Los 15 archivos se conservan tal como se recibieron; cada uno pesa menos de 50 MB. Para valores de precios de vivienda SHF y costos de construcción publicados por terceros, véanse las referencias y límites indicados en el notebook: esas series no se vuelven a estimar aquí.

## Cómo reproducirlo

Clona `https://github.com/alexmufe/vivienda-nueva-mexico.git`, entra al directorio, crea un entorno de Python e instala `requirements.txt` con `python -m pip install -r requirements.txt`. Ejecuta todas las celdas de [`notebooks/vivienda_nueva.ipynb`](notebooks/vivienda_nueva.ipynb) desde Jupyter/VS Code, o desde la raíz del proyecto con `python -m nbconvert --to notebook --execute --inplace --ExecutePreprocessor.timeout=1800 notebooks/vivienda_nueva.ipynb`. Los datos ya están incluidos y el notebook falla explícitamente si falta un archivo requerido; no necesita credenciales, Drive ni descarga.

## Qué produce

El notebook presenta tablas y gráficas sobre los créditos, el monto promedio, los rangos de ingreso y la oferta, y compara cada indicador publicado con el cálculo. Con las copias incluidas reproduce, entre otras cifras, un monto promedio de $745,199 en 2020 y $1,188,061 en 2026 (+59% nominal), el INPC +37%, el índice de créditos en 88.2 (2020 = 100), la participación del rango de ingreso más bajo de 15.9% a 7.4% y 60,627 frente a 85,718 créditos de vivienda usada en enero-mayo.

## Límites

El corte de 2026 llega a mayo; no equivale a un año completo. Los datos y registros publicados por SNIIV pueden cambiar de versión, y la oferta es un inventario mensual, no un flujo que se deba sumar. El notebook compara las copias versionadas de este repositorio, no reproduce las publicaciones externas de SHF ni las series de costos de construcción que cita la nota. No se incluye un PDF del documento principal.
