# Structura inicial del proyecto
📦 emotion_detection_project/
├── 📂 data/                        # Todos los datos del proyecto
│   ├── 📂 raw/                     # Datos crudos (originales)
│   ├── 📂 processed/               # Datos procesados
│   │   ├── 📂 train/               # Estructura que ya mostramos
│   │   └── 📂 val/                 
│   └── 📂 external/                # Datos de terceros
│
├── 📂 models/                      # Modelos entrenados
│   ├── 📄 best_model.h5            # Modelo con mejor performance
│   └── 📄 checkpoint/              # Checkpoints durante entrenamiento
│
├── 📂 notebooks/                   # Jupyter/Colab notebooks
│   ├── 📄 1_data_exploration.ipynb
│   ├── 📄 2_model_training.ipynb
│   └── 📄 3_evaluation.ipynb
│
├── 📂 src/                         # Código fuente
│   ├── 📄 data_preprocessing.py    # Scripts para preparar datos
│   ├── 📄 model.py                 # Arquitectura del modelo
│   ├── 📄 train.py                 # Lógica de entrenamiento
│   └── 📄 predict.py               # Para hacer predicciones
│
├── 📂 reports/                     # Resultados y análisis
│   ├── 📂 figures/                 # Gráficos y visualizaciones
│   └── 📄 results.md               # Métricas finales
│
├── 📄 requirements.txt             # Dependencias
├── 📄 config.yaml                  # Configuraciones
└── 📄 README.md                    # Documentación