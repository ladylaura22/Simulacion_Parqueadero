# Simulación de Pago de Parqueadero 🅿️

**Aplicación de Teoría de Colas en un Sistema de Pago de Parqueadero**

## 📋 Descripción del Proyecto

Este proyecto implementa una **simulación de un sistema de pago de parqueadero** utilizando la **teoría de colas (Queueing Theory)** como fundamento matemático. El objetivo es analizar y optimizar el comportamiento de las colas de vehículos en los sistemas de pago, evaluando métricas de desempeño como tiempo de espera, utilización del servicio y capacidad del sistema.

La simulación está desarrollada en **Jupyter Notebooks**, permitiendo una visualización interactiva de los resultados y facilidades para el análisis exploratorio de datos.

### Conceptos Aplicados

- **Teoría de Colas**: Modelos matemáticos para analizar sistemas de espera
- **Procesos Estocásticos**: Llegada aleatoria de vehículos y tiempos de servicio variables
- **Simulación de Eventos Discretos**: Modelamiento del sistema en tiempo discreto
- **Análisis de Rendimiento**: Evaluación de KPIs del sistema de pago

## 👥 Integrantes del Proyecto

| Integrante |
|-----------|
| Lady Laura Olmos Contreras |
| Jorge Andrés Hernández Campos |
| Juan Felipe Parra |

## 🎓 Contexto Académico

- **Tipo**: Actividad del Curso de Simulación
- **Institución**: IU Digital
- **Fecha**: Junio 2026

## 🚀 Características Principales

- ✅ Modelamiento de llegada de vehículos (distribución Poisson)
- ✅ Simulación de tiempos de servicio (distribución exponencial)
- ✅ Implementación de modelo de cola M/M/c (c servidores)
- ✅ Cálculo de métricas de rendimiento
- ✅ Visualización interactiva de resultados
- ✅ Análisis comparativo de diferentes configuraciones
- ✅ Notebooks ejecutables con análisis paso a paso

## 📊 Métricas Analizadas

- **Tiempo promedio en cola (Wq)**: Tiempo medio que espera un vehículo antes de ser atendido
- **Tiempo promedio en el sistema (W)**: Tiempo total que invierte un vehículo en el sistema
- **Número promedio de vehículos en cola (Lq)**: Cantidad media de vehículos esperando
- **Número promedio de vehículos en el sistema (L)**: Cantidad media de vehículos en todo el sistema
- **Utilización del servidor (ρ)**: Porcentaje de tiempo que el sistema está ocupado
- **Probabilidad de espera (Pw)**: Probabilidad de que un vehículo tenga que esperar

## 🛠️ Requisitos Técnicos

### Software
- Python 3.8 o superior
- Jupyter Notebook o JupyterLab

### Librerías Necesarias
- `numpy` - Cálculos numéricos
- `pandas` - Manipulación de datos
- `matplotlib` - Visualización de gráficos
- `seaborn` - Visualización estadística avanzada
- `scipy` - Funciones científicas
- `sympy` - Cálculos simbólicos

## 📦 Instalación

### 1. Clonar el repositorio
```bash
git clone https://github.com/ladylaura22/Simulacion_Parqueadero.git
cd Simulacion_Parqueadero
```

### 2. Crear un entorno virtual (recomendado)
```bash
python -m venv env
source env/bin/activate  # En Windows: env\Scripts\activate
```

### 3. Instalar dependencias
```bash
pip install -r requirements.txt
```

### 4. Ejecutar Jupyter
```bash
jupyter notebook
```

## 📁 Estructura del Proyecto

```
Simulacion_Parqueadero/
├── README.md                              # Este archivo
├── requirements.txt                       # Dependencias del proyecto
├── notebooks/
│   ├── 01_Introduccion_Teoria_Colas.ipynb        # Fundamentos teóricos
│   ├── 02_Modelo_MM1.ipynb                       # Modelo M/M/1 (un servidor)
│   ├── 03_Modelo_MMc.ipynb                       # Modelo M/M/c (múltiples servidores)
│   ├── 04_Simulacion_Eventos_Discretos.ipynb    # Implementación de la simulación
│   ├── 05_Analisis_Resultados.ipynb              # Análisis y visualizaciones
│   └── 06_Optimizacion_Sistema.ipynb             # Optimización del número de servidores
└── datos/
    └── resultados/                       # Archivos con resultados de simulaciones
```

## 🧮 Teoría de Colas Aplicada

### Modelo M/M/c

- **Arribos**: Proceso de Poisson (M)
- **Servicio**: Exponencial (M)
- **Servidores**: c (número de cajas de pago)

### Parámetros Clave

- **λ (lambda)**: Tasa media de llegada de vehículos por unidad de tiempo (vehículos/hora)
- **μ (mu)**: Tasa media de servicio por servidor (vehículos/hora)
- **c**: Número de servidores (cajas de pago)
- **ρ (rho)**: Factor de utilización = λ / (c·μ)

### Fórmulas Principales

#### Para el modelo M/M/1:
- **W** = 1/(μ - λ)
- **Wq** = λ/(μ(μ - λ))
- **L** = λ/(μ - λ)
- **Lq** = λ²/(μ(μ - λ))

#### Para el modelo M/M/c:
Se utilizan fórmulas de Erlang C y probabilidades de Poisson truncadas.

## 📈 Resultados Esperados

La simulación permite:
- Determinar el número óptimo de servidores (cajas de pago)
- Estimar costos operacionales vs satisfacción del cliente
- Evaluar el impacto de cambios en tasas de llegada
- Optimizar la experiencia del cliente reduciendo tiempos de espera
- Realizar análisis de sensibilidad

## 💻 Ejemplo de Uso

Dentro de cualquier notebook, puedes ejecutar simulaciones como:

```python
import numpy as np
from scipy.stats import poisson, expon

# Parámetros de la simulación
lambda_arrival = 2.0  # vehículos por hora
mu_service = 1.5      # vehículos atendidos por hora
num_servers = 2       # número de cajas de pago

# Generar eventos y simular
# (ver notebooks para implementación completa)
```

## 📚 Referencias Bibliográficas

- Gross, D., & Harris, C. M. (1998). *Fundamentals of Queueing Theory*. John Wiley & Sons.
- Ross, S. M. (2013). *Simulation* (5th ed.). Academic Press.
- Kelton, W. D., Sadowski, R. P., & Sturrock, D. T. (2014). *Simulation with Arena*. McGraw-Hill.
- Law, A. M. (2015). *Simulation Modeling and Analysis* (5th ed.). McGraw-Hill.

## 🔗 Enlaces Útiles

- [Teoría de Colas - Wikipedia](https://es.wikipedia.org/wiki/Teor%C3%ADa_de_colas)
- [Documentación NumPy](https://numpy.org/)
- [Documentación Pandas](https://pandas.pydata.org/)
- [Documentación Matplotlib](https://matplotlib.org/)
- [Jupyter Notebook Guía](https://jupyter.org/)

## 📝 Notas Importantes

- Los notebooks están diseñados para ejecutarse de forma secuencial
- Se recomienda revisar primero el notebook de introducción antes de pasar a los modelos
- Los resultados pueden variar debido a la naturaleza aleatoria de la simulación
- Para cambiar parámetros, edita las celdas de configuración en cada notebook

## 📄 Licencia

Este proyecto es parte de una actividad académica del curso de Simulación.

## 💬 Contacto y Contribuciones

Para consultas o sugerencias sobre el proyecto, contacta a los integrantes del equipo.

---

**Última actualización**: Junio 2026  
**Lenguaje**: Jupyter Notebook (Python)
