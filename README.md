# 09MIAR_TFM

Implementación de modelos LLM de código abierto para la generación de descripciones detalladas y usos de medicamentos en un vademécum digital.

### Resumen

Este proyecto tiene como objetivo el desarrollo de un vademécum digital mediante la aplicación de modelos de lenguaje de gran tamaño (LLMs, por sus siglas en inglés) open source, adaptados específicamente para el dominio de la medicina y la farmacología. Los modelos seleccionados, **BioGPT**, **LlamaCare**, y **ClinicalT5**, se entrenaron y ajustaron para generar descripciones detalladas medicamentos, así como para responder a consultas relacionadas con sus usos, dosificación, efectos secundarios, contraindicaciones, y otras advertencias relevantes.

La metodología empleada en este proyecto se fundamenta en el uso de la arquitectura Transformer, la cual se caracteriza por su capacidad para procesar secuencias de texto de manera eficiente, permitiendo que los modelos comprendan y generen lenguaje natural de manera precisa. La selección de los modelos se basa en sus diferentes enfoques arquitectónicos:
- **ClinicalT5**, con su estructura encoder-decoder, se utiliza para tareas que requieren un análisis detallado del contexto antes de generar la respuesta.
- **BioGPT** y **LlamaCare**, que emplean un decodificador puro, son más adecuados para la generación rápida de texto a partir de una entrada inicial, proporcionando respuestas detalladas y específicas de manera ágil.

El desarrollo del vademécum digital se ha realizado con el fin de mejorar el acceso a información médica de calidad, optimizando la forma en que se generan y presentan las descripciones de los medicamentos. Este enfoque permite que profesionales de la salud y pacientes obtengan respuestas confiables y adaptadas a sus necesidades, mejorando la experiencia de consulta de medicamentos y su comprensión.

### Estructura del Proyecto
- **openFDA.json**: Archivo que contiene la estructura de los medicamentos almacenados en los repositorios de OpenFDA, incluyendo una base de datos detallada utilizada para realizar el ajuste fino (fine-tuning) de los modelos LLM seleccionados. Estos datos incluyen información relevante sobre indicaciones, dosificación, efectos secundarios, y advertencias de uso, fundamentales para entrenar los modelos en la generación precisa y coherente de descripciones médicas.
- **load_dataset.ipynb**: Notebook utilizado para descargar, preprocesar y preparar el dataset. Incluye la limpieza, estructuración y transformación de la información de medicamentos, dejándola lista para el ajuste fino de los modelos LLM seleccionados.
- **train_model_gpt**: Fine-tuning del modelo BioGPT, especializado en la generación de texto, utilizando su arquitectura decoder para un procesamiento eficiente del texto.
- **train_model_llama**: Notebook, utilizado para realizar el fine-tunning del modelo LLamaCare, empleando técnicas de optimización de memoria y entrenamiento por instrucciones para mejorar su rendimiento en la generación de texto.
- **train_model_t5**: Fine-tuning del modelo ClinicalT5, optimizando la generación de descripciones detalladas mediante su arquitectura encoder-decoder.

### Requisitos

- Python 3.10+
- PyTorch
- Transformers (Hugging Face)
- Jupyter Notebook
- WandB (Weights & Biases) para monitoreo de entrenamientos

### Instalación

1. Clona este repositorio:
   ```bash
   git clone https://github.com/ljham/drugs-generative.git
   cd drugs-generative

