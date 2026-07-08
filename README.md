# Detección de ventanas

App de Streamlit para probar 4 modelos entrenados de detección/segmentación de ventanas en fachadas: YOLOv8, YOLOv8-seg, YOLOv11-seg y Detectron2.

## Uso local

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
streamlit run app.py
```

Abre `http://localhost:8501`, sube una o varias imágenes y elige el modelo desde la barra lateral.

## Estructura

```
app.py              # app de Streamlit
models/              # pesos entrenados (versionados con Git LFS)
requirements.txt     # dependencias
```

## Nota sobre Detectron2

Detectron2 no está en PyPI y se instala desde su repositorio de GitHub (ver `requirements.txt`). La compilación puede tardar varios minutos en la primera instalación.
