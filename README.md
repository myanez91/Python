# Python

# Configuración de Entorno Anaconda + Visual Studio Code desde Cero

Guía paso a paso para instalar **Anaconda**, crear un entorno virtual con **conda** y configurarlo correctamente con **Visual Studio Code** (VS Code) para desarrollar en Python (data science, machine learning, análisis de datos, etc.).

**Última revisión recomendada:** 2025–2026  
**Sistema operativo:** Windows / macOS / Linux

## 1. Instalar Anaconda

1.1 Descarga Anaconda Individual Edition (gratuita)  
   👉 https://www.anaconda.com/download

1.2 Elige la versión más reciente (Python 3.11 o 3.12 recomendado)

1.3 Instalación según tu sistema:

   **Windows**
   - Ejecuta el `.exe`
   - Marca: **“Add Anaconda3 to my PATH environment variable”** (muy recomendado)
   - Elige **“Just Me”**

   **macOS**
   - Abre el `.pkg` y sigue el asistente
   - Cierra y vuelve a abrir Terminal al finalizar

En busqueda escribe: anaconda Prompt

# 2. **Crear entorno (elige el nombre y versión que prefieras)**

**entorno** es el nombre que le daras al tu entorno, le puedes poner cualquier nombre

en pantalla oscura dentro de anaconda Prompt escribe: conda create --name **entorno** python=3.11 -y

### Activar el entorno
conda activate entorno

### (Opcional) Instalar paquetes comunes de una vez
conda install -y numpy pandas matplotlib seaborn jupyter ipykernel scikit-learn

### O con pip (dentro del entorno activado)
pip install plotly xgboost lightgbm

### Activar el entorno
conda activate entorno

### (Opcional) Instalar paquetes comunes de una vez
conda install -y numpy pandas matplotlib seaborn jupyter ipykernel scikit-learn

### O con pip (dentro del entorno activado)
pip install plotly xgboost lightgbm

# 3. Instalar Visual Studio Code

3.1 Descarga VS Code

👉 https://code.visualstudio.com/
Instala (en Windows marca “Add to PATH”)

# 4. Conectar VS Code con el entorno conda

Abre VS Code
Instala extensiones esenciales:
Python          → Microsoft
Jupyter         → Microsoft (para notebooks)
Pylance         → Microsoft (mejor autocompletado)
Atajo: Ctrl+Shift+X → busca e instala
Selecciona el intérprete correcto:
Presiona Ctrl + Shift + P (o Cmd + Shift + P en Mac)
Escribe: Python: Select Interpreter
Elige el que diga algo como:textdata_science (Python 3.11.x)  ~/.conda/envs/data_science/bin/pythono la ruta equivalente en Windows

(Opcional pero muy útil para Jupyter en VS Code)
Dentro del entorno activado, registra el kernel:Bashpython -m ipykernel install --user --name data_science --display-name "Data Science (3.11)"

5. Prueba rápida que todo funciona
Crea un archivo test.py en VS Code:
Pythonimport sys
import numpy as np
import pandas as pd

print("¡Entorno funcionando!")
print("Python:", sys.version.split()[0])
print("NumPy:  ", np.__version__)
print("Pandas: ", pd.__version__)

df = pd.DataFrame({"A": [1, 2, 3], "B": [10, 20, 30]})
print(df)
Ejecuta:

Clic en el triángulo verde (arriba derecha)
o
Ctrl+Shift+P → Python: Run Python File in Terminal

Deberías ver la salida sin errores.
Resumen de comandos más usados (copia y pega)
Bash# Entornos
conda env list
conda create -n mi_entorno python=3.11 -y
conda activate mi_entorno
conda deactivate

# Paquetes
conda install numpy pandas matplotlib -y
pip install seaborn plotly

# Actualizar
conda update -n base conda -y
conda update --all -y

# Jupyter kernel (para VS Code / JupyterLab)
python -m ipykernel install --user --name mi_entorno --display-name "Mi Entorno"
