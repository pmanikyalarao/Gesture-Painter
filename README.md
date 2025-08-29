## Gesture Painter 🎨

A real-time, interactive drawing application that lets you paint on a digital canvas using hand gestures detected by your webcam. This project uses computer vision to track your finger movements and translate them into a creative and intuitive drawing experience.

### Features

* **Real-Time Drawing:** Use your index finger to draw directly on the canvas.
* **Intuitive Controls:** Raise your index finger to start drawing and lower it to stop.
* **Dynamic Color Selection:** Choose from a palette of four colors (Red, Green, Blue, and Yellow) by moving your fingers over the on-screen color boxes.
* **Clear Canvas Function:** Easily erase everything and start fresh by using the "Clear" button.
* **Powered by MediaPipe:** Utilizes **MediaPipe's Hand Landmarks** model for accurate and efficient hand tracking.

---

### Technologies Used

* **Python:** The core programming language.
* **OpenCV (`cv2`):** Used for video capture, image processing, and displaying the user interface.
* **NumPy:** Essential for handling and manipulating image data as arrays.
* **MediaPipe:** The powerful framework for real-time hand detection and landmark recognition.

---

### Getting Started

Follow these steps to set up and run the project on your local machine.

#### Prerequisites

* Python 3.x
* `pip` (Python package installer)
* **Jupyter Notebook** or **JupyterLab** to run the `.ipynb` file.

#### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/pmanikyalarao/Gesture-Painter.git
    cd Gesture-Painter
    ```

2.  **Install the required libraries:**
    ```bash
    pip install opencv-python numpy mediapipe jupyter
    ```

3.  **Launch Jupyter:**
    ```bash
    jupyter notebook
    ```
    This will open a new browser tab with the Jupyter interface.

#### Usage

1.  In the Jupyter browser tab, navigate to and open the **`painter.ipynb`** file.

2.  Run the notebook cells one by one or click `Cell -> Run All` to execute the entire code.

3.  A window showing your webcam feed and a separate "paint" canvas will appear.

4.  **To Draw:** Raise your index finger and move it in the air. A line will be drawn on the canvas. To stop drawing, simply lower your finger.

5.  **To Change Color:** Place your finger over one of the colored boxes at the top of the screen (Red, Green, or Yellow) on the `Camera` window.

6.  **To Clear:** Move your finger over the "Clear" box. The entire canvas will be erased.

7.  **To Exit:** Press the `q` key on your keyboard while a display window is active.

---

### How It Works

The application uses your webcam to capture video frames. MediaPipe processes each frame to identify the landmarks of your hand, specifically the tip of your index finger.  The real-time coordinates of your fingertip are then used to draw a continuous line on a separate canvas.

The on-screen buttons (for color change and clearing the canvas) work by checking if your fingertip coordinates fall within the defined rectangle boundaries of those buttons.

---
