# Supervised Learning Credit-Prediction

> Proyecto de aprendizaje supervisado que aplica múltiples algoritmos de clasificación para predecir si un cliente se suscribirá a un crédito bancario, a partir de datos de una campaña de telemarketing.

---

##  Descripción

Este proyecto forma parte del módulo de **Sistemas de Machine Learning** y tiene como objetivo demostrar el uso de algoritmos de aprendizaje supervisado para resolver un problema de clasificación binaria.

A partir de un dataset de una campaña de marketing telefónico bancario, se entrena y evalúa distintos modelos para predecir si un cliente acabará suscribiéndose a un crédito (`yes`/`no`).

---

##  Algoritmos utilizados

- **KNN** (K-Nearest Neighbors)
- **Regresión Logística**
- **Random Forest**

---

## 📁 Estructura del proyecto

```
supervised-learning-credit-prediction/
│
├── data/
│   ├── credit_train.csv       # Dataset de entrenamiento
│   └── credit_test.csv        # Dataset de prueba
│
├── .gitignore                 # Archivos y carpetas ignorados por Git
├── notebook.ipynb             # Notebook principal con todo el análisis
├── requirements.txt           # Dependencias del proyecto
└── README.md
```

---

## ⚙️ Instalación y uso

### 1. Clona el repositorio

```bash
git clone https://github.com/tresssco/supervised-learning-credit-prediction.git
cd supervised-learning-credit-prediction
```

### 2. Crea un entorno virtual (opcional pero recomendado)

```bash
python -m venv venv
source venv/bin/activate        # Linux/Mac
venv\Scripts\activate           # Windows
```

### 3. Instala las dependencias

```bash
pip install -r requirements.txt
```

### 4. Ejecuta el notebook

```bash
jupyter notebook notebook.ipynb
```

---

##  Resultados

|Las métricas mostradas corresponden a la clase positiva (`y = 1`, es decir, cliente que sí se suscribe al crédito), que es la clase de interés en este problema.

| Algoritmo           | Accuracy | Precisión | Recall | F1-Score |
|---------------------|----------|-----------|--------|----------|
| KNN                 | 90%      | 64%       | 33%    | 44%      |
| Regresión Logística | 86%      | 44%       | 90%    | 59%      |
| Random Forest       | 90%      | 53%       | 81%    | 64%      |

###  Análisis comparativo

Los tres modelos alcanzan una accuracy similar (~86–90%), pero se comportan de forma muy distinta al predecir la clase positiva:

- **KNN** obtiene la mayor precisión (64%) pero un recall muy bajo (33%), lo que significa que deja escapar a muchos clientes potenciales. No es ideal para este problema.
- **Regresión Logística** consigue el recall más alto (90%), detectando casi todos los clientes interesados, pero a costa de una precisión baja (44%) — genera muchos falsos positivos.
- **Random Forest** ofrece el mejor equilibrio entre precisión y recall, reflejado en el **F1-Score más alto (64%)**. Es el modelo más robusto para este problema, ya que maximiza la detección de clientes reales sin disparar los falsos positivos.

>  **Modelo recomendado: Random Forest**, por su mejor F1-Score en la clase positiva y su comportamiento equilibrado en precisión y recall.

---

##  Etapas del proyecto

1. **Importación de datos**
2. **Análisis numérico y visual (EDA)**
3. **Preprocesado**
4. **Entrenamiento de modelos**
5. **Evaluación y métricas**
6. **Comparativa final de algoritmos**

---

##  Tecnologías

- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook

---

## 👤 Autor

**Jorge Escolano González**  
IES de Teis — Vigo  
Módulo: Machine Learning
