# Desmosify: Image-Graph Calculator
<img width="1133" height="636" alt="Screenshot 2026-03-18 at 7 23 55 AM" src="https://github.com/user-attachments/assets/442ab869-8d60-4777-8e54-371223712bf7" />

![image](https://github.com/user-attachments/assets/db09ca0b-8887-4b25-8753-52c2f4de225a)
*Sorry there was an error in the design, its not an iOS app :(*

---

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)](https://opencv.org/)
[![Desmos](https://img.shields.io/badge/Desmos-Graphing%20Calculator-006EB6?style=for-the-badge)](https://www.desmos.com/calculator)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)]()

**Transform any image into stunning mathematical art — powered by computer vision and Desmos.**

</div>

---

## 🧠 How It Works

Desmosify bridges the gap between visual art and mathematics. Using OpenCV's edge detection pipeline, it converts images into Desmos-compatible mathematical equations — line by line, curve by curve.

<div align="center">

| Step | Process | Technology |
|------|---------|------------|
| 1️⃣ | Edge Detection | OpenCV Canny Algorithm |
| 2️⃣ | Contour Simplification | Configurable Approximation |
| 3️⃣ | Segment Classification | Line vs. Curve Detection |
| 4️⃣ | Equation Generation | Desmos-formatted Expressions |
| 5️⃣ | Bounds Constraining | Cartesian Coordinate Mapping |

</div>

Each contour in the image is analyzed, categorized, and translated into a corresponding mathematical expression constrained to its original pixel bounds. The result is a clean, code-driven plot in a Cartesian system.

> 💡 **Pro Tip:** For best results, use high-contrast **black-and-white drawings or logos** with minimal background noise.

<div align="center">
<img width="299" alt="Screenshot 2025-05-06 at 11 47 19" src="https://github.com/user-attachments/assets/cbf2773b-3c05-473d-bbbd-40f04c7b7883" />
&nbsp;&nbsp;&nbsp;
<img width="178" alt="Screenshot 2025-05-06 at 11 47 30" src="https://github.com/user-attachments/assets/3af27342-2dde-4543-9be7-5e148287b3f9" />
</div>

---

## 🚀 Getting Started

### Prerequisites

- Python 3.x — [Download here](https://www.python.org/downloads/)
- A black-and-white line drawing or logo (PNG/JPG)

### Installation

```bash
# 1. Clone this repository
git clone https://github.com/gedeonkoh/Desmos-Image-Graphing-Calculator.git
cd Desmos-Image-Graphing-Calculator

# 2. Install dependencies
pip install opencv-python numpy
```

---

## 📖 Step-by-Step Usage

### Step 1 — Prepare Your Image

Place a black-and-white line drawing (e.g., `Hello.png`) on your Desktop. Make sure the image has clear, high-contrast edges for best accuracy.

![image](https://github.com/user-attachments/assets/8ae408f1-6764-42ec-aeea-0041fcf5140e)

### Step 2 — Run the Script

```bash
python desmosify.py
```

The script will process your image and generate an `equations.txt` file in your **Downloads** folder.

### Step 3 — Paste Into Desmos

1. Open `equations.txt` from your Downloads folder
2. Copy **all** contents
3. Paste into the [Desmos Graphing Calculator](https://www.desmos.com/calculator)
4. Wait a moment — your image will materialize as equations ✨

![image](https://github.com/user-attachments/assets/e82720b0-b7da-413b-87c5-b2bbd06fdf04)

---

## ⚙️ Customization Options

Desmosify provides configurable parameters to fine-tune output quality and complexity:

### `INACCURACY_VALUE`

Controls the trade-off between equation detail and file size.

```python
INACCURACY_VALUE = 0.01  # More detailed, more equations
INACCURACY_VALUE = 0.05  # Simpler curves, fewer equations
```

| Value | Detail Level | Number of Equations | Best For |
|-------|-------------|---------------------|----------|
| `0.001 – 0.01` | ⭐⭐⭐⭐⭐ High | Many | Simple logos, clean drawings |
| `0.02 – 0.05` | ⭐⭐⭐ Medium | Moderate | General images |
| `0.1+` | ⭐ Low | Few | Performance testing |

### Y-Axis Flipping
Desmosify automatically inverts the y-axis to align with Desmos' Cartesian coordinate system — no manual adjustment needed.

### Contour Filtering
The script internally filters and prioritizes contours by **complexity and hierarchy**, preserving structural integrity and removing noise automatically.

---

## 🎯 Ideal Use Cases

<div align="center">

| Use Case | Description |
|----------|-------------|
| 📐 **Math Education** | Convert student sketches or teaching materials into live graphing visuals |
| 🏆 **Student Projects** | Perfect for coding competitions, design-based math challenges, and computational art |
| 🎨 **Generative Art** | Translate sketches into plotted equations for art-tech explorations |
| 🔬 **Engineering Diagrams** | Represent schematics and annotations as clean mathematical plots |

</div>

---

## ⚠️ Limitations

Before using Desmosify, keep these constraints in mind:

- ✅ Works best with **clean, black-and-white images**
- ❌ Not suitable for **color images** or **photographs**
- ⚙️ Complex shapes may require fine-tuning of `INACCURACY_VALUE`
- 📦 Very complex images may generate equation files **too large for Desmos** to save

> The image below is an example of an **ideal input** for Desmosify:

<div align="center">

![image](https://github.com/user-attachments/assets/dc6b27b2-831f-48b5-89cf-17553d40a4c8)

</div>

---

## 🛠️ Tech Stack

<div align="center">

| Technology | Role |
|-----------|------|
| ![Python](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white&style=flat-square) | Core scripting and logic |
| ![OpenCV](https://img.shields.io/badge/-OpenCV-5C3EE8?logo=opencv&logoColor=white&style=flat-square) | Edge detection & contour analysis |
| ![NumPy](https://img.shields.io/badge/-NumPy-013243?logo=numpy&logoColor=white&style=flat-square) | Array and coordinate processing |
| ![Desmos](https://img.shields.io/badge/-Desmos-006EB6?style=flat-square) | Mathematical visualization output |

</div>

---

## 📄 License

This project is licensed under the **MIT License** — feel free to use, modify, and distribute with attribution.

---

<div align="center">

Made by [Gedeon Koh](https://beacons.ai/gedeonkoh) · [GitHub](https://github.com/gedeonkoh)

</div>
