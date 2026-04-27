# Image Captioning Tool with BLIP Model

A simple **image captioning** app that generates natural-language captions for images using Salesforce’s **BLIP (Bootstrapping Language-Image Pretraining)** model.  
This project is set up with a lightweight UI (Gradio) so you can upload an image and instantly get a caption.

---

## Features

- Upload an image and generate an English caption
- Uses Hugging Face `transformers` BLIP captioning model
- Simple web UI powered by **Gradio**
- Runs locally on CPU or GPU (if available)

---

## Demo (Local)

Once running, Gradio will print a local URL in your terminal (typically `http://127.0.0.1:7860`).  
Open it in your browser, upload an image, and generate a caption.

---

## Project Structure (typical)

> Your repo may differ slightly depending on what files you added, but a common layout is:

- `app.py` / `main.py` — Gradio app entry point
- `requirements.txt` — Python dependencies (optional)
- `README.md` — documentation

---

## Setup Instructions

### 1) Create and activate a virtual environment

Open a terminal and make sure you are in your project directory.

```bash
pip3 install virtualenv
virtualenv my_env
source my_env/bin/activate
```

### 2) Install dependencies

Install the required libraries:

```bash
pip install langchain==0.1.11 gradio==4.44.0 transformers==4.38.2 bs4==0.0.2 requests==2.31.0 torch==2.2.1
```

> Notes:
> - `torch` installation can vary depending on your OS/CUDA. If you need GPU support, follow PyTorch’s official install instructions.
> - `langchain`, `bs4`, and `requests` are only necessary if your project code uses them.

---

## Run the App

Run the main script (replace with the correct filename in your repo):

```bash
python app.py
```

or:

```bash
python main.py
```

If everything is set up correctly, you should see Gradio logs and a local URL to open in your browser.

---

## Example Usage

1. Open the Gradio link printed in your terminal  
2. Upload an image (JPG/PNG)  
3. Click the button (e.g., **Generate Caption**)  
4. Copy the generated caption

---

## Troubleshooting

### `ModuleNotFoundError: No module named '...'
Make sure:
- your virtual environment is activated: `source my_env/bin/activate`
- dependencies are installed in that environment

### Torch / CUDA issues
If you see CUDA-related errors, you likely installed a CPU-only Torch build or have mismatched CUDA versions.  
Reinstall Torch using the official selector: https://pytorch.org/get-started/locally/

### Gradio doesn’t open in browser
Copy the local URL printed in the terminal and paste it into your browser.  
If running remotely, set `share=True` in Gradio launch options (if your code supports it).

---

## Acknowledgements

- BLIP model: https://huggingface.co/Salesforce/blip-image-captioning-base  
- Hugging Face Transformers: https://github.com/huggingface/transformers  
- Gradio: https://www.gradio.app/

---
