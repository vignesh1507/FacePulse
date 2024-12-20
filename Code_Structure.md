# **Code Structure:**

### **Import Libraries:**

- **streamlit**: Used for building the web app interface.
- **opencv-python**: Used for capturing images from the webcam and performing image processing.
- **numpy**: Required for image processing with OpenCV.
- **pyngrok**: Used for connecting the app to the web (particularly useful in Colab or local environments).
- **face-recognition**: Library for face detection and recognition.
- **pillow**: Used for handling image processing, like saving captured frames. 

---

## **App Structure:**

### **App Title and Menu:**

- `st.title("FacePulse: Facial Recognition Attendance System")`: Displays the app title.
- `menu = ["Register", "Train", "Attendance", "About"]`: A sidebar with 4 options (Register, Train, Attendance, About).
- Depending on the user’s selection, different functionality is displayed.

### **Register New User:**

- The user can enter their ID and Name to register.
- When **"Take Images"** is clicked, it triggers the webcam, captures 10 images, and saves them locally. These images are stored to be used for training the facial recognition model.

### **Train the Model:**

- After registering users, this section allows the app to train a facial recognition model. 
- It uses the captured images to learn and recognize each registered face.
- Clicking **"Train Images"** triggers the training process, which involves scanning the directory of saved images, encoding the face data, and preparing it for recognition.

### **Take Attendance:**

- The **"Attendance"** section uses the webcam to detect faces and compare them with the trained model to recognize users.
- When a user’s face is recognized, their attendance is recorded, and a success message is displayed.

### **About Section:**

- Provides a brief description of the **FacePulse** system and how it works.
