# Clasificador de Pingüinos 🐧

Este proyecto predice la especie de un pingüino basado en sus características físicas y su ubicación. La predicción utiliza un modelo de **Random Forest Classifier** entrenado con el conjunto de datos de Palmer Penguins.

## Autor
**Andrés Esteban Ulloa Jaramillo**

---

## Tabla de Contenidos
1. [Descripción del Proyecto](#descripción-del-proyecto)
2. [Características del Dataset](#características-del-dataset)
3. [Exploración de Datos](#exploración-de-datos)
4. [Modelo Predictivo](#modelo-predictivo)
5. [Aplicación Web](#aplicación-web)
6. [Requisitos](#requisitos)
7. [Instrucciones de Ejecución](#instrucciones-de-ejecución)
8. [Estructura del Proyecto](#estructura-del-proyecto)
9. [Contribuciones](#contribuciones)

---

## Descripción del Proyecto

El objetivo principal es predecir si un pingüino pertenece a la especie **Adelie** o **Gentoo**, utilizando características físicas (longitud del pico, profundidad del pico, longitud de la aleta, masa corporal) y la ubicación donde fue observado.

Además de entrenar el modelo, se creó una aplicación web interactiva con **Streamlit** para que los usuarios puedan:
1. Ingresar valores personalizados.
2. Visualizar la predicción de la especie.
3. Observar probabilidades asociadas con la predicción.
4. Explorar visualizaciones de datos y explicaciones sobre el desarrollo del proyecto.

---

## Características del Dataset

El conjunto de datos contiene 7 columnas y 274 registros:

| **Columna**          | **Descripción**                                    |
|-----------------------|---------------------------------------------------|
| `species`            | Especie del pingüino (*Adelie* o *Gentoo*).       |
| `island`             | Isla donde se observó el pingüino.                |
| `bill_length_mm`     | Longitud del pico (mm).                           |
| `bill_depth_mm`      | Profundidad del pico (mm).                        |
| `flipper_length_mm`  | Longitud de la aleta (mm).                        |
| `body_mass_g`        | Masa corporal (gramos).                           |
| `year`               | Año del registro.                                 |

---

## Exploración de Datos

Se realizó un análisis exploratorio (EDA) para entender las características del dataset:
1. **Distribución de variables**:
   - Se observó una clara distinción entre especies basadas en la longitud y profundidad del pico.
2. **Relaciones entre variables**:
   - Variables como `flipper_length_mm` y `body_mass_g` también mostraron diferencias significativas.

---

## Modelo Predictivo

El modelo **Random Forest Classifier** fue evaluado con las siguientes métricas:
- **Métricas de Evaluación**:
  - Precisión: 100%
  - Matriz de Confusión:
    ```
    Predicted
    True   Adelie  Gentoo
    Adelie   30       0
    Gentoo    0      25
    ```

- **Importancia de Características**:
    | Característica       | Importancia |
    |----------------------|-------------|
    | `flipper_length_mm`  | 0.42        |
    | `bill_depth_mm`      | 0.24        |
    | `bill_length_mm`     | 0.20        |
    | `body_mass_g`        | 0.12        |
    | `island`             | 0.01        |


---

## Aplicación Web

La aplicación web permite:
1. Ingresar datos personalizados.
2. Observar predicciones.
3. Ver probabilidades en barras de progreso y un gráfico dinámico.
4. Explorar explicaciones detalladas del proyecto.


---

## Requisitos

- Python 3.7+
- Librerías necesarias:
  - `streamlit`
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `scikit-learn`

---
