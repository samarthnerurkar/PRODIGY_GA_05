# 🎨 Neural Style Transfer 

A PyTorch notebook that repaints a photo in the style of a famous painting. The demo turns a kitten photo into a Van Gogh *Starry Night* style image.

![Python](https://img.shields.io/badge/Python-3.x-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-red)
![Colab](https://img.shields.io/badge/Google-Colab-orange)

## ✨ Features

- Upload your own content image
- Style image downloaded automatically (Starry Night), with manual upload as fallback
- Uses pretrained VGG19 features
- Content loss plus Gram-matrix style loss
- Automatically picks GPU or CPU and adjusts image size (512 on GPU, 256 on CPU)
- Side-by-side Content / Style / Stylized Output visualization

## 🛠 Tech Stack

- Python, PyTorch, torchvision (VGG19)
- Pillow, Matplotlib
- Google Colab

## ⚡ Getting Started

1. Open `neuralStyle.ipynb` in Google Colab.
2. Use a GPU runtime for faster results.
3. Run the cell and upload your content image when prompted.
4. Wait for optimization to finish and view the result.

## 🧠 How It Works

- The image is passed through VGG19 layers wrapped with custom loss modules.
- **Content loss:** MSE between feature maps at `conv_4`.
- **Style loss:** MSE between Gram matrices at `conv_1` to `conv_5`.
- The output image is optimized to minimize both losses, so it keeps the shape of the content image and the textures and colors of the style image.

```python
content_layers = ["conv_4"]
style_layers = ["conv_1", "conv_2", "conv_3", "conv_4", "conv_5"]
```

## 🎬 Demo

<img width="1911" height="1055" alt="image" src="https://github.com/user-attachments/assets/2d10a75f-7506-4d08-9ab5-b1c4227c5489" />

## 🔄 Workflow

<img width="780" height="817" alt="image" src="https://github.com/user-attachments/assets/f02e0af9-f877-47f3-8c25-cb9aa0234163" />


## 📚 Style Library

The notebook uses Starry Night. Other style images to try (suggestions):

| Style image | Look you get |
|-------------|--------------|
| The Starry Night (Van Gogh) | Swirling brushstrokes, blue and yellow tones (used in demo) |
| The Great Wave off Kanagawa | Japanese woodblock print, bold outlines |
| Impressionist landscape (Monet) | Soft, blurry color patches |
| Cubist portrait (Picasso) | Angular, fragmented shapes |
| Abstract painting (Kandinsky) | Bright geometric color blocks |

Upload any style image when the download step falls back to manual upload, or change `style_url` in the notebook.

**Content image tips:** use a clear subject with a simple background (pets, portraits, landmarks).

## ⚠️ Notes

- VGG19 weights (about 548 MB) download on first run.
- If the style image download fails, you will be asked to upload one.
- Try different style images for different looks.

## 📄 License

MIT License

## 👤 Author

## 👤 Author

**Samarth Nerurkar**

- GitHub: [@samarthnerurkar](https://github.com/samarthnerurkar)
- LinkedIn: [Samarth Nerurkar](https://www.linkedin.com/in/samarth-nerurkar/)
