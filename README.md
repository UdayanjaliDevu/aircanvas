# Air Canvas Using Hand Gesture Recognition

## Project Overview

This project implements a **computer vision-based virtual drawing application** that allows users to draw on a canvas using **hand gestures detected from a webcam**.

The system uses **MediaPipe hand tracking** to detect finger landmarks and interpret gestures for drawing, selecting colors, and erasing. The goal of this project is to demonstrate **real-time gesture-based interaction using computer vision techniques**.

---

## Features

* Real-time **hand gesture detection**
* **Virtual air drawing** using index finger
* **Color palette selection**
* **Eraser mode** to remove drawings
* **Live webcam canvas overlay**
* **Keyboard controls for clearing and exiting**

---

## Technologies Used

This project is built using the following technologies:

* **Python**
* **OpenCV**
* **MediaPipe**
* **NumPy**

These libraries enable real-time image processing, hand landmark detection, and canvas manipulation.

---

## Gesture Controls

| Gesture                  | Action        |
| ------------------------ | ------------- |
| Index Finger Up          | Draw          |
| Index + Middle Finger Up | Select Color  |
| Eraser Selected          | Erase Drawing |

---

## Keyboard Controls

| Key | Action           |
| --- | ---------------- |
| C   | Clear Canvas     |
| Q   | Quit Application |

---

## How the System Works

### Hand Detection

The application uses **MediaPipe Hands** to detect and track 21 hand landmarks. These landmarks provide information about finger positions, which are used to determine gestures.

### Gesture Recognition

Finger positions are compared to determine whether they are raised or folded.

* **Index finger raised** → Drawing mode
* **Index + middle finger raised** → Color selection mode

### Drawing Mechanism

When drawing mode is active, the program tracks the position of the **index fingertip** and connects consecutive points with lines to create smooth drawing strokes.

### Canvas Overlay

The drawing canvas is stored separately and merged with the webcam frame using OpenCV image processing operations. This allows the drawing to appear on top of the live camera feed.

---

## Usage

Run the Python script to start the application:

```
python air_canvas.py
```

Once the webcam opens, the program will begin detecting hand gestures.

---

## Project Structure

```
aircanvas
│
├── air_canvas.py
├── README.md
└── requirements.txt
```

---

## Future Improvements

Possible improvements for this project include:

* Adjustable brush sizes
* Shape drawing tools
* Save drawings as images
* Multi-hand gesture support
* Gesture-based UI controls

