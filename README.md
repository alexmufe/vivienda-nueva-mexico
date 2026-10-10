# Vivienda nueva en México

¿Quién dejó de poder estrenar casa en México y por qué? El análisis compara los créditos de vivienda nueva, su monto, la distribución por ingreso y la oferta registrada.

## Hallazgos principales

Entre 2020 y 2026, el crédito promedio subió de $745 mil a $1.188 millones (+59%), mientras el INPC aumentó 37%; el índice de créditos otorgados quedó en 88.2 y la participación del rango de ingreso más bajo bajó de 15.9% a 7.4%. Los créditos para vivienda usada pasaron de 60,627 a 85,718 entre enero y mayo.

![Gráfica 1. El crédito para estrenar casa creció más rápido que la inflación, y se otorgan menos](docs/figuras/grafica_1_credito_inflacion.png)

[Documento completo](docs/Vivienda_nueva_AlejandroMunoz.md)

## Fuentes de datos

[SNIIV](https://sniiv.sedatu.gob.mx/Reporte/Datos_abiertos), [INPC de INEGI](https://www.inegi.org.mx/temas/inpc/), [SHF](https://www.gob.mx/shf) y [CEICO-CMIC](https://www.cmic.org.mx/ceico/). Los datos incluidos se consultaron el 9 de octubre de 2026.

## Límites de los datos

El promedio del crédito no es el precio de la vivienda: también depende del enganche, la institución y el perfil de quien califica. La caída del crédito al rango de ingreso más bajo puede reflejar menor acceso o cambios en el registro del ingreso; la clasificación de la oferta cambia en 2024 y limita las comparaciones por segmento.

## Código

[Notebook](notebooks/vivienda_nueva.ipynb)
Los datos están incluidos; el notebook corre con las dependencias fijadas en `requirements.txt`.
`python -m nbconvert --to notebook --execute --inplace --ExecutePreprocessor.timeout=1800 notebooks/vivienda_nueva.ipynb`
