# 🖼️ End-to-End Image Understanding System

🚀 **[Live Demo](https://huggingface.co/spaces/swagatadutta26/ai-image-analysis)** — Try it yourself

An AI pipeline that performs **multi-task image analysis** using three 
pre-trained deep learning models — ViT, DETR, and BLIP — integrated 
via HuggingFace Transformers.

## 🔍 What It Does

Given any input image, the system automatically produces:

| Task | Model Used | Output |
|------|-----------|--------|
| Image Classification | ViT (google/vit-base-patch16-224) | Top-5 labels with confidence scores |
| Object Detection | DETR (facebook/detr-resnet-50) | Detected objects above 60% threshold |
| Image Captioning | BLIP (Salesforce/blip-image-captioning-base) | Natural language description |
| Scene Analysis | Rule-based (keyword matching) | Indoor / Outdoor / Mixed |

## 📸 Sample Output

**Input:** Varanasi Ghat at dusk

**Output:**
- 📝 Caption: *"boats are docked in the water at dusk"*
- 🎯 Detected Objects: boat, person, umbrella
- 🌅 Scene Type: Outdoor
- 🏷️ Top Classifications: dock/dockage (29.59%), lakeside (22.37%), boathouse (8.01%)

![Input Image](screenshots/input_1.png)
![Output Analysis](screenshots/output_1.png)

**More examples:**

![Input Image](screenshots/input_2.png)
![Output Analysis](screenshots/output_2.png)

![Input Image](screenshots/input_3.png)
![Output Analysis](screenshots/output_3.png)

![Input Image](screenshots/input_4.png)
![Output Analysis](screenshots/output_4.png)

## 🛠️ Tech Stack

- Python, PyTorch
- HuggingFace Transformers
- ViT, DETR, BLIP
- PIL, Matplotlib
- Streamlit (deployment)
- Google Colab (GPU/CPU dynamic detection)

## 🚀 Try It Yourself

**Option 1 — Live Web App (recommended):**
[Open the deployed app](https://huggingface.co/spaces/swagatadutta26/ai-image-analysis) — upload any image directly in your browser, no setup required.

**Option 2 — Run the notebook:**
1. Open the notebook in Google Colab
2. Run all cells in order
3. Upload any image when prompted
4. View the full analysis output

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Qpf9TxBj7HXJ1qOslIoMStc8uZa23zRH?usp=sharing)

## ⚠️ Known Limitations

- Scene analysis is rule-based (keyword matching), not model-driven
- Object detection limited to COCO dataset's 80 classes
- Runs on CPU if GPU unavailable — slower inference

## 📁 Repository Structure
