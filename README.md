# Proyecto: Hábitos de escucha de música online


## Descripción 
### Introducción
En este proyecto, se trabaja con datos reales de la transmisión de música online para explorar y procesar información sobre los hábitos de escucha de los usuarios en dos ciudades: **Springfield** y **Shelbyville**.

### Objetivo general
El propósito de este proyecto es realizar un análisis exploratorio y un procesamiento de datos reales provenientes de una plataforma de transmisión de música online. Mediante este estudio, se pretende evaluar y comparar el comportamiento y las preferencias de consumo musical de los usuarios en dos ciudades específicas: **Springfield** y **Shelbyville**.

### Hipótesis a probar
Para guiar el análisis de los datos, evaluaremos tres hipótesis fundamentales sobre el comportamiento de los usuarios según el día de la semana y su ubicación geográfica:
1. **Actividad por días:** La actividad de los usuarios difiere según el día de la semana y depende directamente de la ciudad.
2. **Preferencias de género los lunes por la mañana:** Los lunes por la mañana, los habitantes de Springfield y Shelbyville escuchan géneros musicales distintos.
3. **Preferencias globales por ciudad:** Los oyentes de Springfield prefieren la música pop, mientras que los de Shelbyville muestran una mayor inclinación hacia el rap.

## Conclusiones generales del proyecto

### 1. Resumen de hallazgos y patrones observados
A lo largo del análisis exploratorio de datos, se identificaron comportamientos de consumo y preferencias musicales muy claros entre ambas ciudades:

* **Disparidad de volumen:** **Springfield** demostró ser el mercado principal de la plataforma, acumulando un total de **42741 reproducciones**, frente a las **18512** registradas en **Shelbyville**.
* **Comportamiento temporal:** A nivel global, la actividad musical se incrementa al iniciar el fin de semana, registrando **21840 reproducciones los viernes** en comparación con las **21354 de los lunes**.
* **Similitud en preferencias:** Sorprendentemente, a pesar de las diferencias geográficas y de volumen, ambas poblaciones comparten un núcleo de gusto musical idéntico. El **Pop, el Dance y el Rock** dominan los primeros puestos de sintonía tanto de manera global como en momentos específicos de la semana.

---

### 2. Problemas detectados y calidad del análisis
Durante la fase de preprocesamiento, se detectaron y resolvieron problemas críticos que ponían en riesgo la validez estadística del estudio:

1. **Encabezados Sucios:** Se eliminaron los espacios y mayúsculas de las columnas (`.lower()`, `.strip()`) y se estandarizó la variable principal a `user_id` bajo el formato *snake_case*.
2. **Valores Ausentes (Nulos):** Los registros vacíos en las variables críticas de segmentación (`artist`, `track` y `genre`) fueron sustituidos de manera uniforme con la etiqueta `'unknown'` para preservar la integridad del volumen de la muestra.
3. **Registros Duplicados:** Se eliminaron **3826 duplicados explícitos** que inflaban artificialmente las métricas. Adicionalmente, se unificaron las variantes ortográficas del género *hiphop* (`'hip'`, `'hop'`, `'hip-hop'`), eliminando duplicados implícitos.

**Impacto:** Estas acciones garantizaron un análisis libre de sesgos, asegurando que las comparativas entre ciudades y los conteos de géneros reflejaran tendencias de consumo reales y unificadas.

---

### 3. Evaluación final de las hipótesis

Para responder a la pregunta central del proyecto sobre si el comportamiento de los usuarios varía según la ciudad y el día de la semana, evaluamos formalmente los resultados de las tres hipótesis de trabajo:

* **Hipótesis 1 (Actividad por días y ciudades): SE CONFIRMA.** Los datos demuestran que el consumo es dinámico y depende de la combinación de ambos factores. Mientras que en **Springfield** la actividad arranca fuerte el lunes (15740) y se eleva hacia el viernes (15,945) impulsada por el ocio del fin de semana; en **Shelbyville** el comportamiento es más plano y uniforme, registrando una actividad laboral muy competitiva el lunes (5,614) frente al viernes (5,895).
* **Hipótesis 2 (Géneros los lunes por la mañana): SE RECHAZA.** La suposición de que escuchaban géneros distintos al iniciar la semana resultó ser falsa. Los resultados del conteo demostraron que tanto en Springfield como en Shelbyville, las primeras horas del lunes están dominadas exactamente por el mismo podio musical: **Pop, Dance y Rock**.
* **Hipótesis 3 (Preferencias globales Pop vs. Rap): SE CONFIRMA PARCIALMENTE.** La suposición se cumplió perfectamente para **Springfield**, donde el Pop es el líder absoluto. Sin embargo, se refutó para **Shelbyville**, ya que su audiencia global también prefiere la música **Pop** por un amplio margen, dejando al Rap en posiciones secundarias.

**Conclusión de cierre:** El comportamiento de los usuarios varía en términos de *cuándo* y *cuánto* escuchan según su ciudad, pero sus gustos en cuanto a *qué* escuchan (los géneros musicales) se mantienen asombrosamente homogéneos y dominados por las tendencias comerciales globales en ambas regiones.


## Tecnologías utilizadas
* Python (Pandas)
* Jupyter Notebook

## Ver el análisis completo
👉 [Haz clic aquí para ver el código y los gráficos interactivos](proyecto_habitos_de_escucha_de_musica_online.ipynb)

