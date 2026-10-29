# Evolución de precios de medicamentos e inflación

Trabajo Práctico Grupal de **Laboratorio de Métodos Cuantitativos Aplicados a la Gestión**, Facultad de Ciencias Económicas, Universidad de Buenos Aires.

## Pregunta de investigación

¿Cómo evolucionó el precio de venta al público de los medicamentos registrados por una farmacia entre septiembre de 2025 y septiembre de 2026, y cómo se compara esa variación con la inflación del mismo período?

## Datos

El análisis utiliza registros de una farmacia entre el **1 de septiembre de 2025 y el 30 de septiembre de 2026**.

- Archivo de origen: `Dataset_farmacia.csv`.
- Dimensiones verificadas: **41.880 filas y 33 columnas**.
- Precio por unidad o producto: `PUBLICO VENTA`.
- Identificador de producto: `TROQUEL`. Se verificó que cada código corresponde a una descripción `DESCRIPX` y viceversa.
- El CSV utiliza `;` como separador y codificación `cp1252`. Los datos se cargan inicialmente como texto.

El archivo debe incluirse en el repositorio o acompañarse con instrucciones para obtenerlo. En Google Colab, el código de carga espera encontrarlo en `/content/Dataset_farmacia.csv`.

## Método de comparación

Para reducir el efecto de cambios en la mezcla de productos vendidos, se seleccionaron los **298 códigos `TROQUEL` presentes en los 13 meses**. Se calculó el precio unitario promedio de cada producto en cada mes y se expresó su evolución como un índice individual, con septiembre de 2025 como base 100. Luego se promediaron los índices de los productos, asignando el mismo peso a cada uno.

El resultado describe la evolución de esos 298 productos y no necesariamente la de todo el surtido de la farmacia. La comparación de inflación utiliza el IPC nacional, nivel general, publicado por el INDEC.

## Resultado preliminar

Entre septiembre de 2025 y septiembre de 2026, el índice promedio de los 298 productos aumentó **29,13%**. En el mismo período, la variación interanual del IPC nacional fue **33,40%**. Por lo tanto, la variación de los productos analizados quedó **4,27 puntos porcentuales por debajo** de la inflación general.

Fuente: [INDEC, Índice de precios al consumidor, septiembre de 2026](https://www.indec.gob.ar/uploads/informesdeprensa/ipc_10_268C45A9444C.pdf).

## Estado del trabajo

- [x] Carga del dataset y exploración inicial.
- [x] Conversión de fecha y precio unitario para el análisis.
- [x] Identificación de productos presentes en los 13 meses.
- [x] Cálculo de la variación del conjunto y comparación con el IPC.
- [x] Primer gráfico de evolución mensual del índice, con exportación a PNG.
- [ ] Completar e interpretar los otros dos gráficos requeridos.
- [ ] Completar y ejecutar el notebook en Google Colab y exportarlo como `.ipynb`.
- [ ] Redactar el informe académico en PDF, de 3 a 5 páginas.
- [ ] Preparar la presentación obligatoria, de 6 a 10 diapositivas.
- [ ] Documentar en el notebook las celdas asistidas por IA y los prompts utilizados.

## Ejecución

El análisis se desarrolla en **Python y Google Colab**, con las librerías `pandas`, `numpy` y `matplotlib`.

1. Subir `Dataset_farmacia.csv` al almacenamiento de la sesión de Colab.
2. Ejecutar las celdas del notebook en orden.
3. Descargar y guardar el notebook ejecutado en formato `.ipynb`.

La ruta `/content/Dataset_farmacia.csv` corresponde a Google Colab, no a una carpeta de la computadora local.

## Entregables

El repositorio grupal debe contener, como mínimo:

- El notebook ejecutado en formato `.ipynb`.
- El informe académico en PDF.
- El dataset o instrucciones para obtenerlo.
- La presentación o un enlace para consultarla.

## 📊 Presentación online

[Ver presentación interactiva](https://fjmv89.github.io/Trabajo-Practico-Grupal/presentacion.html)

