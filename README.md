This is a very basic Sign language detecting model. We are detecting hand signs with Python, Mediapipe, Opencv and Scikit Learn. The reference youtube tutorial is at [https://youtu.be/MJCSjXepaAM?feature=shared ]


## **1. Project Title & Description**

* **Name:** *Talk With My Hand – Real-Time ASL Recognition using MediaPipe & SVM*
* Short intro on what it does and why you built it.

---

## **2. Demo**

<img width="811" height="654" alt="image" src="https://github.com/user-attachments/assets/af209143-42d1-4c86-8bc4-040ae239fbef" />

<img width="812" height="643" alt="image" src="https://github.com/user-attachments/assets/458efee4-e96f-42db-8ae1-1f7fc79cb638" />

<img width="805" height="645" alt="image" src="https://github.com/user-attachments/assets/362c170c-e709-4885-ab60-7bcc21295716" />




## **3. Features**

* Real-time webcam-based recognition
* Detects ASL gestures (A, B, L)
* Lightweight (runs on CPU)
* Modular structure: dataset creation, model training, and inference separated
* Easy to extend to new gestures

---

## **4. Tech Stack**

* **Language:** Python
* **Libraries:**

  * `opencv-python` – video capture & display
  * `mediapipe` – hand landmark detection
  * `scikit-learn` – SVM model training
  * `numpy` – array operations
  * `pickle` – model saving/loading

---

## **5. Dataset**

* Custom dataset with 42-feature vectors (x,y for each of 21 landmarks)
* Folder structure:

```
Dataset/
    A/
    B/
    L/
```

* Instructions for creating dataset with `create_dataset.py`

---

## **6. Installation**

* Clone the repo:

```bash
git clone https://github.com/Nishtha-Parashar/Talk-with-my-hand.git
cd Talk-with-my-hand
```

* Create & activate virtual environment:

```powershell
python -m venv virtual
.\virtual\Scripts\Activate.ps1
```

* Install dependencies:

```bash
pip install -r requirements.txt
```

---

## **7. Usage**

* **Step 1:** Create dataset:

```bash
python create_dataset.py
```

* **Step 2:** Train model:

```bash
python train_classifier.py
```

* **Step 3:** Run live inference:

```bash
python inference_classifier.py
```

* Press `q` to quit webcam feed.

---

## **8. How It Works**

1. Capture webcam frame using OpenCV
2. Detect 21 hand landmarks using MediaPipe
3. Normalize coordinates and store as a feature vector
4. Train Support Vector Machine (SVM) model on features
5. Predict sign in real time and display result on video feed

---

## **9. Results**

* Accuracy: \~95–98% for 3 classes
* Runs in real time on CPU

