# Python

# Configuración de Entorno Anaconda + Visual Studio Code desde Cero

Guía paso a paso para instalar **Anaconda**, crear un entorno virtual con **conda** y configurarlo correctamente con **Visual Studio Code** (VS Code) para desarrollar en Python (data science, machine learning, análisis de datos, etc.).

**Última revisión recomendada:** 2025–2026  
**Sistema operativo:** Windows / macOS / Linux

## 1. Instalar Anaconda

1. Descarga Anaconda Individual Edition (gratuita)  
   👉 https://www.anaconda.com/download

2. Elige la versión más reciente (Python 3.11 o 3.12 recomendado)

3. Instalación según tu sistema:

   **Windows**
   - Ejecuta el `.exe`
   - Marca: **“Add Anaconda3 to my PATH environment variable”** (muy recomendado)
   - Elige **“Just Me”**

   **macOS**
   - Abre el `.pkg` y sigue el asistente
   - Cierra y vuelve a abrir Terminal al finalizar

   **Linux**
   
   ```bash
   bash Anaconda3-*-Linux-x86_64.sh

   Acepta licencia → elige yes para inicializar conda

En busqueda escribe: anaconda Prompt

# Crear entorno (elige el nombre y versión que prefieras)

**entorno** es el nombre que le daras al tu entorno, le puedes poner cualquier nombre

en pantalla oscura dentro de anaconda Prompt escribe: conda create --name **entorno** python=3.11 -y


# Activar el entorno
conda activate entorno

# (Opcional) Instalar paquetes comunes de una vez
conda install -y numpy pandas matplotlib seaborn jupyter ipykernel scikit-learn

# O con pip (dentro del entorno activado)
pip install plotly xgboost lightgbm
# Activar el entorno
conda activate data_science

# (Opcional) Instalar paquetes comunes de una vez
conda install -y numpy pandas matplotlib seaborn jupyter ipykernel scikit-learn

# O con pip (dentro del entorno activado)
pip install plotly xgboost lightgbm
