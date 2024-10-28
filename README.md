# DataProject: Dashboard & Análisis de Datos

<p align="center">
    <img src="https://github.com/mck21/StudentPerformaceAnalysis/blob/main/img/header.png" />    
</p>

<div align="center">
    <img src="https://img.shields.io/badge/google%20sheets-%2342B883.svg?style=for-the-badge&logo=googlesheets&logoColor=white" alt="Google Sheets">
    <img src="https://img.shields.io/badge/kaggle-%2320BEFF.svg?style=for-the-badge&logo=kaggle&logoColor=white" alt="Kaggle">
</div>
<br>

Este repositorio contiene un análisis del [dataset de Kaggle](https://www.kaggle.com/datasets/lainguyn123/student-performance-factors/data) que examina varios factores que podrían influir en el rendimiento académico de los estudiantes.<br><br>

> [!IMPORTANT]
Aquí puedes acceder al [análisis en Google Sheets](https://docs.google.com/spreadsheets/d/1xaC4Uw8iyd0s6YDOQmCVE0gIYyCW9urNs5iH_Bp2bMw/edit?usp=sharing) (enlace con acceso para cualquier persona)

## 1. Exploratory Data Analysis (EDA)

### 1.1. Comprensión General de los Datos

El conjunto de datos muestra varios factores que podrían influir en el rendimiento académico de los estudiantes, siendo la variable objetivo es **Exam_Score** (puntuación del examen). Las columnas del dataset que vamos a analizar son:
- **Student_ID (ID_Estudiante)**: Integer - Identificador único del estudiante.
- **Hours_Studied (Horas_Estudio)**: Integer - Cantidad de horas dedicadas al estudio.
- **Attendance (Asistencia)**: Integer - Porcentaje de asistencia a clases.
- **Parental_Involvement (Implicación_Parental)**: String - Nivel de implicación de los padres en la educación del estudiante.
- **Access_to_Resources (Acceso_a_Recursos)**: String - Grado de acceso a recursos de estudio y apoyo.
- **Extracurricular_Activities (Actividades_Extracurriculares)**: String - Participación en actividades fuera del currículo académico.
- **Sleep_Hours (Horas_Sueño)**: Integer - Promedio de horas de sueño diarias del estudiante.
- **Previous_Scores (Puntuaciones_Anteriores)**: Integer - Puntuaciones obtenidos en evaluaciones previas.
- **Motivation_Level (Nivel_Motivación)**: String - Nivel de motivación del estudiante.
- **Internet_Access (Acceso_Internet)**: String - Indica si el estudiante tiene acceso a Internet.
- **Tutoring_Sessions (Sesiones_Tutoría)**: Integer - Número de sesiones de tutoría recibidas.
- **Family_Income (Ingresos_Familiares)**: String - Nivel de ingresos familiares.
- **Teacher_Quality (Calidad_Profesorado)**: String - Percepción de la calidad del profesorado.
- **School_Type (Tipo_Escuela)**: String - Tipo de institución educativa (pública o privada).
- **Peer_Influence (Influencia_De_Compañeros)**: String - Influencia de los compañeros en el rendimiento académico.
- **Physical_Activity (Actividad_Física)**: Integer - Cantidad de horas dedicadas a actividades físicas semanales.
- **Learning_Disabilities (Discapacidades_Aprendizaje)**: String - Indica si el estudiante tiene alguna discapacidad de aprendizaje.
- **Parental_Education_Level (Nivel_Educación_Parental)**: String - Nivel educativo alcanzado por los padres.
- **Distance_from_Home (Distancia_de_Casa)**: String - Proximidad de la escuela con respecto al hogar del estudiante.
- **Gender (Género)**: String - Género del estudiante.
- **Exam_Score (Puntuación_Examen)**: Integer - Calificación obtenida en el examen final.


### 1.2. Transformación y Limpieza

- **Eliminar duplicados**
  <p align="center">
    <img src="https://github.com/mck21/StudentPerformaceAnalysis/blob/main/img/duplicados.png" />
  </p>
  
- **Tratar los valores nulos**
  <p align="center">
   <img src="https://github.com/mck21/StudentPerformaceAnalysis/blob/main/img/null_values.png" />
  </p>
  Cambiamos las celdas vacías por “Unknown” en las columnas **Teacher_Quality**, **Parental_Education_Level** y **Distance_from_Home**.

- **Corregir/borrar datos erróneos o formatos incorrectos** (no se encontraron errores significativos).

### 1.3. Patrones y Outliers

- **Tablas dinámicas**: Se utilizaron para observar la relación entre las puntuaciones del examen y el resto de factores.
- **Gráficos**: BarCharts, LineCharts, AreaChart, DonutChart.
- **Formato condicional**: Se aplicó formato condicional para resaltar los valores en la nota de los exámenes.
  <p align="center">
   <img src="https://github.com/mck21/StudentPerformaceAnalysis/blob/main/img/formaro_condicional.png" />
  </p>

## 2. Dashboard

Se ha creado un dashboard interactivo que permite filtrar los datos según género, tipo de escuela, influencia de los compañeros y distancia a la escuela.

<p align="center">
  <img src="https://github.com/mck21/StudentPerformaceAnalysis/blob/main/img/dashboard.png" />
</p>

## 3. Conclusiones e Interpretación de Resultados
Con los resultados puestos en gráficos en el dashboard podemos ver mejor los patrones y tendencias de este conjunto de 6607 estudiantes.
 - Vemos que todas las gráficas referidas a la variable objetivo (nota del examen) tienen cierta correlación.
 - Hasta valores de la nota cerca de 77, las gráficas siguen una tendencia ascendente, mientras que por encima de este valor empiezan a verse irregularidades en la tendencia.
 - En cuanto a la media de horas estudiadas, podemos apreciar que los estudiantes con notas más altas no precisan dedicar tantas horas como los estudiantes de notas más bajas. Esto se puede deber a la calidad del estudio; no por invertir más tiempo significa que el alumno aprenda más.
 - La media de horas de sueño es ligeramente más baja de cara a los alumnos con mejor nota. Esto se puede atribuir a factores como el estrés o, en casos independientes, a las horas invertidas en el estudio.
 - Los valores bajos de asistencia acarrean peores notas entre los estudiantes; sin embargo, según los resultados, con una asistencia de entre el 70% y el 80% de las clases sería suficiente para algunos alumnos que han obtenido una nota de entre 80 y 93.
 - En cuanto a las clases particulares, apreciamos que a más clases tomadas por el alumno, mejor nota obtiene, siendo lo normal tomar entre 1 y 3 clases. El alumno que ha obtenido mejor nota ha tomado 5 clases particulares.
 - Apreciamos hasta dos puntos de diferencia en la nota media global entre los alumnos cuyos padres presentan alto nivel de implicación (68.09) y bajo nivel de implicación (66.36).
 - Analizando la nota previa respecto a la de este examen, apreciamos una tendencia ascendente, lo que significa que la mayoría de estudiantes han mejorado su rendimiento.
 - También vemos una tendencia ascendente en la nota media a medida que más horas de ejercicio físico realizan los estudiantes. Una mejor salud implica un mejor rendimiento.
 - Por último, podemos ver hasta 1.1 puntos de diferencia en la media global entre los alumnos que presentan discapacidades para aprender y los que no.
