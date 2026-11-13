# 🍎 Fresh-or-Rotten Fruit Quality AI

An AI model that checks a photo of a fruit and predicts whether it is **Fresh** or **Rotten**.

Built with Python, TensorFlow, and Transfer Learning. This project helps reduce food waste by quickly checking fruit quality from a photo.

---

## 🎯 What It Does

- Upload a photo of a fruit
- The AI analyses the photo
- It returns a prediction: **FRESH** or **ROTTEN**
- It also shows a confidence score from 0 to 1

Example:
- Score `0.448` → **FRESH** (below 0.5)
- Score `0.750` → **ROTTEN** (above 0.5)

---

## 🧠 How It Works

1. **Data Collection:** Fruit photos are organised into 2 folders:
   - `data/fresh/` - photos of fresh fruit
   - `data/rotten/` - photos of rotten fruit

2. **Model:** MobileNetV2 (pre-trained on ImageNet)
   - The base layers are frozen to keep what it already knows
   - A new classification head is added on top for Fresh vs Rotten

3. **Training:**
   - Image size: 224 x 224
   - Epochs: 3
   - Optimizer: Adam
   - Loss: Binary Crossentropy

4. **Testing:** The model is tested on a new photo it has not seen before and predicts Fresh or Rotten.

---

## 📁 Project Structure
