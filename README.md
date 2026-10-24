# IO Solver 5.0 - Exportación PDF

**Universidad Mariano Gálvez de Guatemala · Investigación de Operaciones · Sección A**

**Integrantes:** José Luis Turcios y Kevin Ernesto Mata Lemus

Esta versión conserva los seis módulos y el chatbot Gemini de IO Solver 4.2. Incorpora **Descargar resultado en PDF** después de cada cálculo; incluye datos, sustituciones, tablas y, cuando corresponde, gráficas. Los PDF se generan en memoria y los visitantes pueden descargarlos desde PC o móvil sin crear una cuenta.

## Cómo ejecutarlo localmente

1. Pon todos los archivos en la misma carpeta.
2. `python -m pip install -r requirements.txt`
3. `python -m streamlit run appTuki.py`

Para habilitar Gemini, configura `GEMINI_API_KEY` en Streamlit **Secrets**, nunca dentro de `appTuki.py` ni en GitHub.

## Cómo actualizar la aplicación publicada

En el repositorio GitHub conectado a Streamlit Community Cloud, reemplaza `appTuki.py`, actualiza `requirements.txt` y conserva `paloma_paraclito.png`. No tienes que crear otra aplicación ni cambiar su URL. Streamlit reinstala dependencias cuando `requirements.txt` cambia. Comprueba el despliegue desde Manage app/Logs.

## Cobertura de exportación

- Respuestas del chatbot IA: pregunta, método seleccionado, explicación, resultado, procedimientos y tablas/gráfica cuando corresponde.
- Modelación, programación lineal, método gráfico: datos, restricciones, valor óptimo y comprobaciones. Los dos últimos incluyen la gráfica.
- Simplex: iteraciones y **todas** las tablas.
- Transporte y asignación: matrices, asignaciones, costos y procedimiento.
- Inventarios: EOQ y punto de reorden con fórmulas sustituidas.
- Centro de aprendizaje: ejemplos resueltos y prácticas verificadas.

**Nota:** Los botones están junto al resultado. Tras cambiar de página o parámetros, vuelve a pulsar Calcular/Resolver para generar un nuevo reporte. Los PDF no se almacenan en el servidor; únicamente se entregan al navegador para su descarga.
