# Clasificación de Variedades de Papas con CNNs

Este repositorio contiene los notebooks, datasets y el artículo científico relacionados con la clasificación automática de **83 variedades de papas nativas peruanas** usando redes neuronales convolucionales (CNN).

## 📄 Descripción del estudio

El trabajo compara el rendimiento de cuatro arquitecturas CNN:
- **PapaNet** (modelo personalizado)
- **VGG16**
- **SqueezeNet**
- **MobileNetV2**

Todas fueron entrenadas sobre un dataset de imágenes de papas en resolución **128x128 px**, utilizando técnicas de *data augmentation* y optimización avanzada con **AdamW**.

### Resultados destacados:
- **MobileNetV2** alcanzó el mayor accuracy: **91.67%**
- **SqueezeNet** logró **91.16%**, destacando por su eficiencia (solo 0.77M parámetros)
- **PapaNet** mostró buen rendimiento (84.98%) con bajo costo computacional
- **VGG16** obtuvo 85.24%, pero con alta carga de memoria y procesamiento

## 🥔 Dataset

- El dataset incluye **imágenes de 83 variedades nativas peruanas de papa**, capturadas en condiciones controladas de iluminación y fondo.
- Cada variedad contaba inicialmente con **40 a 50 imágenes originales**.
- Se aplicaron transformaciones de *data augmentation* como:
  - Rotaciones controladas (±15°)
  - Ajustes de brillo/contraste (±20%)
  - Volteo horizontal aleatorio
- Esto permitió **ampliar cada clase a 300 imágenes**, mejorando la generalización y el balance del conjunto.
- El dataset está documentado y descrito en detalle en el paper incluido.

## 📁 Contenido del repositorio

- `/notebooks/`: Código en Google Colab para entrenamiento y evaluación
- `/dataset/`: Imágenes preprocesadas y aumentadas de las 83 variedades de papa
- `paper_clasificacion_papas_Deep_Learning.pdf`: Artículo completo del estudio

## ⚙️ Tecnologías utilizadas

- **TensorFlow 2.18.0**
- **GPU T4 (Google Colab)**
- **Python 3.10**
- Técnicas: *Transfer learning*, *BatchNorm*, *Dropout*, *Data Augmentation*

## 🧪 Entrenamiento y evaluación

- División de datos: 70% entrenamiento, 15% validación, 15% prueba
- Métricas: *Accuracy*, *Cross-Entropy Loss*, tiempo por época
- Callbacks: `EarlyStopping`, `ReduceLROnPlateau`, `ModelCheckpoint`

## 🔗 Enlaces

- [Repositorio del Dataset y Código](https://github.com/aprendizajeautomatico-entrega2/2DAENTREGAAPRENDIZAJEAUTOMATICO)

## 📜 Cita

> Torreblanca Paz, S. V., Pachari Lipa, M. A., & Sullcarani Diaz, B. E. (2024). *Evaluación comparativa de arquitecturas CNN en la clasificación de 83 variedades de papas*. Universidad Nacional San Antonio Abad del Cusco.

---

*Este estudio busca contribuir a la valorización tecnológica de cultivos andinos mediante herramientas modernas de visión computacional.*
