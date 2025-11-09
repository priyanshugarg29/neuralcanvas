# neuralcanvas

neuralcanvas/
├─ app/                      # Streamlit app code
│  └─ streamlit_app.py
├─ models/                   # pre-trained model weights (or training scripts)
│  └─ fast_style_model.pth
├─ src/
│  ├─ model.py               # feedforward transformer network
│  ├─ utils.py               # image transforms, interpolation, caching
│  └─ train.py               # training pipeline (optional)
├─ assets/                   # UI images, sample styles & content
├─ requirements.txt
├─ README.md
└─ .github/workflows/        # CI (optional)
