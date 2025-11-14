# Data Analysis Project — Talent Flow (Rotación de Personal)

## 🛠️ Tecnologías Utilizadas

<div align="center">

<table>
  <tr>
    <td align="center">
      <kbd>
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="42" />
        <br><b>Python</b>
      </kbd>
    </td>
    <td align="center">
      <kbd>
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" width="42" />
        <br><b>Pandas</b>
      </kbd>
    </td>
    <td align="center">
      <kbd>
        <img src="https://upload.wikimedia.org/wikipedia/commons/d/d0/Google_Colaboratory_SVG_Logo.svg" width="70" />
        <br><b>Google Colab</b>
      </kbd>
    </td>
    <td align="center">
      <kbd>
        <img src="https://cdn.worldvectorlogo.com/logos/seaborn-1.svg" width="42" />
        <br><b>Seaborn</b>
      </kbd>
    </td>
    <td align="center">
      <kbd>
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/84/Matplotlib_icon.svg/1200px-Matplotlib_icon.svg.png" width="42" />
        <br><b>Matplotlib</b>
      </kbd>
    </td>

  </tr>
</table>

</div>

**Estado:** En desarrollo 🚧

---

## 📌 1. Descripción del Proyecto

Este proyecto realiza un **Análisis Exploratorio de Datos (EDA)** sobre un dataset de personas en una organización, con el fin de identificar patrones y factores asociados a la **rotación de personal**, así como dinámicas internas relacionadas con satisfacción, antigüedad e ingresos.

---

## 🎯 2. Objetivos

### ✔ Objetivo General
Analizar el comportamiento laboral de los empleados para identificar factores clave relacionados con la rotación y el bienestar organizacional.

### ✔ Objetivos Específicos
- Limpiar y validar los datos.
- Crear nuevas variables a partir de columnas numéricas y fechas.
- Analizar la rotación general y por categorías.
- Realizar análisis univariados, bivariados y multivariados.
- Generar conclusiones basadas en evidencia.

---

## 🧩 3. Dataset

**Archivo:** `PFDA_people_analytics.csv`

## 📊 Variables Principales del Dataset

| **Variable**              | **Descripción** |
|---------------------------|-----------------|
| **Age**                   | Edad del empleado en años. |
| **Attrition**             | Indica si el empleado dejó la empresa (Yes/No). |
| **Gender**                | Género del empleado. |
| **JobRole**               | Cargo o rol del empleado dentro de la organización. |
| **DistanceFromHome**      | Distancia entre el hogar y el trabajo (en km). |
| **MonthlyIncome**         | Ingreso mensual del empleado. |
| **YearsAtCompany**        | Años que lleva trabajando en la empresa. |
| **YearsSinceLastPromotion** | Años desde la última promoción. |
| **EnvironmentSatisfaction** | Nivel de satisfacción con el entorno laboral (1–4). |
| **OverTime**              | Indica si trabaja horas extra (Yes/No). |

## 🧩 Variables Derivadas

| **Variable Nueva**        | **Descripción** |
|---------------------------|-----------------|
| **AgeGroup**             | Agrupación por rangos de edad usando `pd.cut`. |
| **IncomeCategory**       | Clasificación del salario en categorías. |
| **TenureGroup**          | Segmentos basados en antigüedad en la empresa. |
| **Month / Year**         | Variables generadas a partir de columnas de fecha usando `.dt`. |

---

## 📊 4. Análisis Realizados

### 🔹 Limpieza y Preparación
- Corrección de tipos de datos.  
- Imputación de valores faltantes.  
- Estandarización de categorías.  
- Creación de variables derivadas.

### 🔹 Análisis Univariado
- Histogramas: edad, salarios, distancia, antigüedad.  
- Conteo de rotación general.  
- Distribuciones de satisfacción laboral.

### 🔹 Análisis Bivariado
- Rotación por edad.  
- Rotación por ingreso.  
- Satisfacción vs. antigüedad.  
- Relación ingreso–distancia.  
- Rotación por departamento.

### 🔹 Insights Destacados (ejemplos)
- Mayor rotación entre empleados con baja antigüedad (0–2 años).  
- Empleados con horas extras presentan mayor tendencia a renunciar.  
- La satisfacción del entorno tiene relación inversa con la rotación.  

---

## 📈 5. Visualizaciones

Ejemplo de código utilizado:

```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.countplot(data=df, x='Attrition')
plt.title('Distribución de Rotación')
plt.show()
```

Principales gráficos utilizados:

- 📉 Histogramas  
- 📦 Boxplots  
- 🔢 Countplots  
- 🔥 Heatmaps de correlación  
- 🎯 Scatterplots  
- 📊 Barras comparativas  
- 🧩 Pairplots  

---

## 📝 6. Estructura del Proyecto
```
📁 proyecto-people-analytics/
│── README.md  
│── requirements.txt  
│── PFDA_people_analytics.csv  
│── eda_people_analytics.ipynb  
│── /img/
│     ├── distribucion_rotacion.png
│     ├── correlacion_heatmap.png
│     └── histogramas.png
```

## 🔍 7. Metodología

1. **Exploración inicial del dataset**  
   - Revisión de dimensiones, tipos de datos y detección de valores faltantes.
   - Identificación de las variables más relevantes para el análisis.

2. **Limpieza y preparación de datos**  
   - Conversión de tipos de datos incorrectos.
   - Imputación de valores nulos.
   - Normalización y estandarización de categorías.

3. **Creación de variables derivadas**  
   - Segmentación de edad, ingresos y antigüedad mediante `pd.cut`.
   - Creación de columnas temporales usando `.dt` (mes, año, etc.).
   - Generación de categorías para facilitar análisis comparativos.

4. **Análisis univariado**  
   - Identificación de la distribución de variables clave.
   - Uso de histogramas, countplots y estadísticas descriptivas.

5. **Análisis bivariado y multivariado**  
   - Evaluación de la relación entre variables laborales, demográficas y de satisfacción.
   - Uso de scatterplots, boxplots, heatmaps y tablas cruzadas.

6. **Identificación de insights clave**  
   - Interpretación de patrones relevantes.
   - Detección de factores asociados a la rotación de personal.

---

## 📚 8. Conclusiones

El análisis permitió identificar patrones relevantes sobre los factores asociados a la rotación de personal dentro de la organización. Entre los hallazgos más significativos se encuentran:

- **El tiempo dentro de la empresa es el predictor estructural más fuerte de la rotación**, destacando el rango de 0–2 años como el de mayor vulnerabilidad.
- La **satisfacción con el entorno laboral** muestra una correlación inversa con la rotación, indicando la necesidad de fortalecer políticas de bienestar interno.
- La variable **OverTime** actúa como un potencial indicador de sobrecarga o burnout, correlacionándose con mayor salida de personal.
- Se detectan **diferencias sistemáticas por JobRole**, lo que sugiere la presencia de dinámicas internas específicas según el tipo de trabajo.
- Los análisis multivariados muestran que la **rotación es multifactorial**, resultado de interacciones entre antigüedad, satisfacción, carga laboral y nivel salarial.
- Los hallazgos proporcionan un marco sólido para la toma de decisiones en **retención de talento**, **recursos humanos basados en datos** y **optimización de condiciones laborales**.


