# Anime Face GAN Model

This project implements a **Generative Adversarial Network (GAN)** for generating anime-style faces using PyTorch. The model is trained on the **Anime Face dataset** from Kaggle and utilizes **Vision Transformer (ViT)** for image processing.

## 📌 Features
- **Anime Face Image Generation** using a deep learning model.
- **Dataset Preprocessing**: Resizes images to 224x224 for compatibility.
- **Training & Evaluation**: Implements GAN-based image generation.
- **Colab Integration**: Supports training in Google Colab with Google Drive.

## 📁 Dataset
The project uses the **Anime Face Dataset** from Kaggle:  
[🔗 Anime Face Dataset](https://www.kaggle.com/datasets/splcher/animefacedataset)  

## 🛠 Installation & Setup

1. **Clone the Repository**  
   ```sh
   git clone https://github.com/Kanhaiya1610/AnimeGANTrainer.git
   cd AnimeGANTrainer
   ```

2. **Install Dependencies**  
   ```sh
   pip install -r requirements.txt
   ```

3. **Download Dataset** (Using Kaggle API in Colab)  
   ```sh
   !pip install kaggle
   !mkdir -p ~/.kaggle
   !echo '{"username":"<your_kaggle_username>","key":"<your_kaggle_key>"}' > ~/.kaggle/kaggle.json
   !chmod 600 ~/.kaggle/kaggle.json
   #for google_colab first mount gdrive & replace <./data> to <./content/drive> 
   !kaggle datasets download -d splcher/animefacedataset -p ./data #<./content/drive/>
   !unzip ./data/animefacedataset.zip -d ./data/anime_dataset #<./content/drive/anime_dataset>
   ```

## 🚀 Running the Model
Run the Jupyter Notebook step by step in **Google Colab**:
```sh
jupyter notebook AnimeFace_GAN_Model.ipynb
```

Or execute the Python script:
```sh
# After copying whole code into a file named train.py
python train.py
```

## ⚙️ Training Parameters
- **Image Size**: 224x224  
- **Batch Size**: 32  
- **Epochs**: Recommended to start small (e.g., 100) and increase  
- **Optimizer**: Adam  

## 🖼 Output Examples
After training, the model generates **anime-style faces** similar to those in the dataset & you can't find exact in the dataset if tried to cross-check.

## 🏗 Future Improvements
- Enhance model architecture (e.g., using StyleGAN).  
- Implement hyperparameter tuning for better quality.  
- Add GUI for generating images interactively.  

## 📜 License
This project is open-source under the **MIT License**.
