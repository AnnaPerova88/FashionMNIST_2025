# 🧠 Fashion-MNIST Classification with CNN

This solution applies a clean and effective **Convolutional Neural Network (CNN)** architecture to the Fashion-MNIST dataset using TensorFlow/Keras. The goal is to classify grayscale 28×28 images of clothing items into 10 categories (T-shirt, trousers, etc.).

---

## 🏗️ Model Architecture

The model consists of the following layers:

- `Conv2D(32, 3x3)` + ReLU → extracts local features  
- `MaxPooling2D(2x2)` → reduces spatial size  
- `Conv2D(64, 3x3)` + ReLU → deeper feature learning  
- `MaxPooling2D(2x2)`  
- `Flatten()` → prepares data for dense layers  
- `Dense(128)` + ReLU → learning complex combinations  
- `Dropout(0.3)` → regularization to avoid overfitting  
- `Dense(10, softmax)` → output probabilities for 10 classes  

---

## ⚙️ Training Details

- **Loss**: `sparse_categorical_crossentropy`  
- **Optimizer**: `Adam`  
- **Batch Size**: 64  
- **Epochs**: 10  
- **Validation Split**: 10%

---

## 📊 Preprocessing

- Missing values filled with median  
- Pixel values normalized to [0, 1]  
- Input reshaped to (28, 28, 1)  
- No augmentation or pretraining used  

---

## ✅ Results

- **Validation accuracy**: ~0.88  
- Model trains efficiently in under 5 minutes on Kaggle GPU  
- Stable baseline for further tuning (augmentation, batchnorm, pretrained models, etc.)

---

## 📁 Submission

- `submission.csv` includes predicted class labels for the test set  
- Output format: two columns — `Id` and `label`

---

> 🧩 *This baseline CNN provides a reliable foundation for future enhancements such as data augmentation, learning rate scheduling, and ensemble modeling.*

🧠 Классификация Fashion-MNIST с помощью CNN
Это решение реализует чистую и эффективную архитектуру сверточной нейронной сети (CNN) на датасете Fashion-MNIST с использованием TensorFlow/Keras.
Цель — классифицировать изображения одежды размером 28×28 пикселей в 10 категорий (футболка, брюки и др.).

🏗️ Архитектура модели
Модель состоит из следующих слоев:

Conv2D(32, 3x3) + ReLU → извлечение локальных признаков

MaxPooling2D(2x2) → уменьшение пространственных размеров

Conv2D(64, 3x3) + ReLU → более глубокое обучение признаков

MaxPooling2D(2x2)

Flatten() → преобразование тензора в вектор

Dense(128) + ReLU → обучение сложным комбинациям

Dropout(0.3) → регуляризация для предотвращения переобучения

Dense(10, softmax) → выходные вероятности по 10 классам

⚙️ Детали обучения
Функция потерь: sparse_categorical_crossentropy

Оптимизатор: Adam

Размер батча: 64

Эпохи: 10

Валидация: 10% от обучающей выборки

📊 Предобработка данных
Пропущенные значения заполнены медианой

Значения пикселей нормализованы в диапазоне [0, 1]

Входные данные приведены к форме (28, 28, 1)

Аугментация и предобученные модели не использовались

✅ Результаты
Точность на валидации: ~0.88

Модель обучается менее чем за 5 минут на GPU Kaggle

Стабильная базовая версия для будущих улучшений
(аугментация, батч-нормализация, предобученные модели и др.)

📁 Сабмит
submission.csv содержит предсказанные метки классов для тестовой выборки

Формат: два столбца — Id и label
