# Eye Disease Detection using Deep Learning

This project detects various eye diseases using a deep learning model trained on a custom image dataset and deployed through a simple web interface using Flask.

---

## 🧠 Project Summary
- **Model**: MobileNetV2 (or similar CNN)
- **Input**: Eye image (.jpg, .png)
- **Output**: Predicted disease class (14 total)
- **Interface**: Flask + HTML Form UI

---

## 🏷️ Disease Categories Detected
- Bulging Eyes
- Central Serous Chorioretinopathy
- Crossed Eyes
- Disc Edema
- Macular Scar
- Myopia
- Pterygium
- Retinal Detachment
- Retinitis Pigmentosa
- Uveitis
- Cataract
- Diabetic Retinopathy
- Glaucoma
- Normal (Healthy Eye)

---

## 📁 Project Structure
```
EyeCare/
├── app.py                 # Flask backend (model loading & prediction)
├── form.html              # Frontend upload form
├── eye_disease_model.h5   # Trained model (not committed)
├── static/img.jpg         # Background image (optional)
├── templates/form.html    # Flask looks for templates here
├── README.md              # Project documentation
```

---

## 💾 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/EyeCare.git
cd EyeCare
```

### 2. Create a Virtual Environment
```bash
python -m venv venv
venv\Scripts\activate   # On Windows
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Add Your Trained Model
Place your trained `.h5` model in the project directory. Update the path in `app.py`:
```python
model = load_model('eye_disease_model.h5')
```

---

## 🚀 Running the Application
```bash
python app.py
```
Visit `http://127.0.0.1:5000` in your browser.

---

## 🌐 Web Interface Overview
- Built using **Flask** & HTML.
- Simple upload form to submit eye image.
- Prediction is displayed after model inference.

---

## ⚙️ Prediction Workflow
1. User uploads image.
2. Image resized to 224x224 and normalized.
3. Model infers class probabilities.
4. Top class is mapped to a readable label.
5. Result is returned to the frontend via JSON.

---

## 🧪 Example Labels Output
```json
"The patient is suffering from Uveitis"
"The patient have no problem normal_eye"
```

---

## 📦 Dependencies
- TensorFlow
- Flask
- NumPy
- Pillow (PIL)
- Pandas (optional)

To generate `requirements.txt`:
```bash
pip freeze > requirements.txt
```

---

## 🎯 Future Improvements
- Add Grad-CAM visualizations to highlight disease regions.
- Deploy on cloud (Render, Heroku, etc.)
- Improve frontend styling and UX.
- Expand dataset and classes.

---

## 👨‍💻 Author
**Sai Narendra Panga**  
🔗 [LinkedIn](https://www.linkedin.com/in/sainarendrapanga/)  
📧 saipanga678@gmail.com

---

## 📄 License
This project is open-source and available under the MIT License.



