# 🪖 AI Enabled Smart Helmet for Drowsiness and Accident Detection

### An AI-powered rider safety prototype using TinyML, Edge Impulse, and Python

This project explores the application of artificial intelligence and sensor-based monitoring to improve motorcycle rider safety. It combines machine learning-based accident detection, simulated drowsiness monitoring, and an interactive emergency alert system.

The current implementation is a **software-based prototype developed in Google Colab**, using a trained Edge Impulse model and synthetic accelerometer data.

## 🚀 Key Features

* **AI-Based Accident Detection:** Classifies accelerometer readings as normal riding or accident conditions using a trained machine learning model.
* **Drowsiness Monitoring:** Simulates prolonged eye closure and triggers an alert when a predefined threshold is exceeded.
* **Interactive Dashboard:** Allows users to demonstrate normal riding, drowsiness, and accident scenarios.
* **Emergency Alert System:** Simulates an emergency notification following accident detection.
* **Alert Cancellation:** Provides an "I'm Safe" option to cancel a simulated emergency alert.

## 🛠️ Technologies Used

| Technology   | Purpose                             |
| ------------ | ----------------------------------- |
| Python       | Data processing and simulation      |
| Edge Impulse | Machine learning model development  |
| TinyML       | Lightweight sensor-based inference  |
| Google Colab | Development and testing environment |
| NumPy        | Numerical computations              |
| ipywidgets   | Interactive simulation dashboard    |

## 🧠 Machine Learning Approach

The accident detection model was developed using Edge Impulse and synthetic three-axis accelerometer data.

**Model configuration:**

* Input: X, Y, and Z accelerometer readings
* Sampling frequency: 10 Hz
* Window size: 2 seconds
* Input window: 20 readings × 3 axes
* Classification labels: `normal` and `accident`

The trained model processes accelerometer data and predicts whether the input represents normal riding or an accident scenario.

Drowsiness monitoring is implemented separately using a rule-based simulation of prolonged eye closure.

## 📊 Model Evaluation

The accident detection model achieved:

**97.14% classification accuracy (34/35 samples)**

This result was obtained using a held-out synthetic test dataset.

An example accident test sample produced:

* Accident probability: **99.61%**
* Normal probability: **0.39%**

These results demonstrate the model's performance in the simulated environment. They do not establish its accuracy on real motorcycle sensor data.

## ⚙️ How the Simulation Works

1. Synthetic accelerometer readings represent normal riding and accident conditions.
2. The trained Edge Impulse model processes the accelerometer input.
3. The system displays the predicted classification.
4. A separate rule-based simulation monitors prolonged eye closure.
5. When an accident or drowsiness condition is detected, the dashboard activates a simulated warning.
6. The emergency alert interface allows the user to cancel an alert using the **I'm Safe** button.

## 💻 Running the Project

1. Open `AI_Enabled_Smart_Helmet.ipynb` in Google Colab.
2. Install the required Python dependencies using the notebook's setup cells.
3. Upload the exported Edge Impulse Linux x86_64 `.eim` model when prompted.
4. Upload any required test samples.
5. Run the notebook cells in order.
6. Use the interactive dashboard to demonstrate the available scenarios.

**Note:** The exported `.eim` model is a separate dependency and is not embedded in the notebook.

## 🔍 Current Limitations

* Training and evaluation data are synthetic.
* The prototype has not been validated using real motorcycle riding data.
* Drowsiness detection is simulated rather than measured using a physical eye-blink sensor.
* Emergency alerts and buzzer responses are simulated in software.
* Hardware integration with ESP32 and physical sensors remains future work.

## 🔮 Future Enhancements

* Integration with an ESP32-based smart helmet prototype
* Real-time accelerometer and eye-blink sensor monitoring
* GPS-based accident location tracking
* GSM or internet-based emergency notifications
* Real-world dataset collection and model validation
* Improved accident detection through additional sensor inputs

## 🎯 Project Objective

To demonstrate how machine learning and sensor-based monitoring can contribute to the development of intelligent motorcycle rider safety systems.

---

**Project Type:** Artificial Intelligence · Machine Learning · TinyML · Rider Safety

**Status:** Software prototype / simulation

