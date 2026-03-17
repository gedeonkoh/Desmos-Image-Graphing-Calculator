# Desmosify: Image-Graph Calculator
<img width="1133" height="636" alt="Screenshot 2026-03-18 at 7 23 55 AM" src="https://github.com/user-attachments/assets/442ab869-8d60-4777-8e54-371223712bf7" />

![image](https://github.com/user-attachments/assets/db09ca0b-8887-4b25-8753-52c2f4de225a)
__________________________
How It Works
1. Desmosify operates through a combination of computer vision and geometric approximation. The workflow starts with edge detection via OpenCV’s Canny algorithm, isolating the most prominent lines and features in the image. It then simplifies these contours with a configurable approximation parameter, effectively reducing noise while maintaining essential structure. From there, it categorizes each segment as either a line or curve and generates a corresponding mathematical expression, formatted for Desmos and constrained to its original bounds.
2. This process makes it easy to represent art, annotations, or schematics as a clean, code-driven plot in a Cartesian system. For best results, the source image should be a high-contrast, black-and-white drawing or logo with minimal noise.

<img width="299" alt="Screenshot 2025-05-06 at 11 47 19" src="https://github.com/user-attachments/assets/cbf2773b-3c05-473d-bbbd-40f04c7b7883" />
<img width="178" alt="Screenshot 2025-05-06 at 11 47 30" src="https://github.com/user-attachments/assets/3af27342-2dde-4543-9be7-5e148287b3f9" />

__________________________

(Setup Instructions) To use Desmosify, follow these steps:
1. Install Python: Ensure Python 3.x is installed on your machine. You can download it from python.org.
2. Install Dependencies: Open a terminal or command prompt and run:
    pip install opencv-python numpy
3. Prepare Your Image:
    Place a black-and-white line drawing (e.g., Hello.png) on your Desktop.
    Modify the image path in the script if you’re using a different name or location.
   
![image](https://github.com/user-attachments/assets/8ae408f1-6764-42ec-aeea-0041fcf5140e)

5. Run the Script:
    Execute the Python script (python desmosify.py) using your terminal or preferred IDE.
    The program will then process the image and create a file called equations.txt in your Downloads folder.
6. Paste Into Desmos:
`  Open the file, copy the contents, and paste them into the Desmos Graphing Calculator.
    Your image will now appear in equation form after a while.

![image](https://github.com/user-attachments/assets/e82720b0-b7da-413b-87c5-b2bbd06fdf04)


(Customization Options) Desmosify includes configurable parameters that allow you to adjust output fidelity and control complexity, such as:

INACCURACY_VALUE: 
This parameter determines how simplified or detailed the final equations will be.
1. Smaller values retain more curve detail but generate more expressions.
2. Larger values simplify the curves and reduce the number of equations.

Y-Axis Flipping: 
1, Desmosify automatically flips the y-axis to match Desmos' Cartesian layout.

Contour Filtering:
1. Internally, the script filters and prioritizes contours by complexity and hierarchy to preserve structural integrity.

(Ideal Use Cases) Desmosify is well-suited for a variety of applications:
1. Mathematics Education: Teachers can turn student sketches or teaching materials into live graphing visuals.
2. Student Projects: Great for coding competitions, design-based math challenges, and computational art showcases.
3. Art-Tech Explorations: Artists and designers can explore generative design by translating sketches into plotted equations.

(Limitations) While Desmosify is powerful, it’s best used under the following constraints:
1. Works best with clean, black-and-white images.
2. Not ideal for color images or photographs.
3. Complex shapes may require fine-tuning of the INACCURACY_VALUE to balance performance and precision.
4. Complex images might make the equation file too large to be saved on desmos. The image below is one ideal image to use "Desmosify" in. 

![image](https://github.com/user-attachments/assets/dc6b27b2-831f-48b5-89cf-17553d40a4c8)
