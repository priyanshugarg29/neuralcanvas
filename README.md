# NeuralCanvas

**Turn your photos into works of art using Neural Networks.**  
NeuralCanvas is a Streamlit-powered web app that performs **Neural Style Transfer** — blending the content of one image with the style of another, in real time.

---

## Features

- Upload any content image (photo, landscape, etc.)
- Choose from a gallery of artistic styles (e.g., Van Gogh, Monet, abstract)
- Fast, real-time transformation using a pre-trained feedforward neural network
- Adjust style strength with a simple slider
- Download your stylized image instantly
- Built with PyTorch and Streamlit, easy to extend or retrain with your own styles

---

## How It Works

NeuralCanvas uses a **Fast Neural Style Transfer** model based on  
[Johnson et al., *Perceptual Losses for Real-Time Style Transfer* (2016)](https://arxiv.org/abs/1603.08155).

1. A **Transformer Network** learns how to "repaint" images in a specific artistic style.  
2. A fixed **VGG19 network** acts as a teacher, comparing:
   - **Content features** between your photo and the stylized image  
   - **Style features** between the style artwork and the stylized image  
3. The model is trained to minimize these differences, so it can instantly apply that style to any new image in one forward pass.

Intuitively:  
VGG is the art critic,  
the Transformer Network is the artist,  
and your photo is the new canvas.

---

## Project Structure

```
neuralcanvas/
├── app/
│ └── streamlit_app.py # Streamlit web app
├── models/
│ └── fast_style_model.pth # Pre-trained model weights
├── src/
│ ├── model.py # Transformer network
│ ├── utils.py # Image I/O, preprocessing
│ └── train.py # Optional training script
├── assets/ # Example styles, demo images
├── requirements.txt
└── README.md
```

---

## Installation

Clone the repository and install dependencies:

```
bash
git clone https://github.com/<your-username>/neuralcanvas.git
cd neuralcanvas
pip install -r requirements.txt
```

Run the App Locally
```
streamlit run app/streamlit_app.py
```

Then open your browser to `http://localhost:8501`


Upload your photo, choose a style, adjust the slider,
and watch your image transform before your eyes.

## Requirements

Python ≥ 3.9

PyTorch

Streamlit

Pillow

torchvision

numpy

(See requirements.txt for exact versions.)

## Deployment

You can deploy NeuralCanvas easily on Streamlit Cloud:

Push your repo to GitHub.

Visit https://share.streamlit.io


Connect your repo and set the entry point as app/streamlit_app.py.

Your live app will be available at:
https://neuralcanvas.streamlit.app

## Example Output
Content	Style	Result

	

## To train your own style model:

python src/train.py --style_image path/to/style.jpg --dataset path/to/coco/


This will create a new model checkpoint under models/.
Replace it in the app to use your custom style.

## Credits

Fast Neural Style Transfer – Johnson, Alahi & Fei-Fei (2016)

VGG19 feature extractor – Simonyan & Zisserman (2014)

Streamlit UI – https://streamlit.io

## License

MIT License © 2025 Your Name
You are free to use, modify, and share this project with attribution.



