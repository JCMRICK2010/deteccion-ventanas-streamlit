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

Detectron2 no está incluido en `requirements.txt` porque no está en PyPI (se compila desde su repo de GitHub) y falla al desplegarse en Streamlit Community Cloud (sin GPU y con límites de build). La app detecta automáticamente si Detectron2 está instalado: si no lo está, simplemente oculta esa opción del selector.

Para usar el modelo Detectron2 en local, instálalo aparte después del resto de dependencias:

```bash
pip install 'git+https://github.com/facebookresearch/detectron2.git'
```
