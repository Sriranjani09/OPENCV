rerequisites
Make sure you have the following Python libraries installed:

numpy
matplotlib
opencv-python
You can install them using pip:

bash
Copy code
pip install numpy matplotlib opencv-python
Project Structure
xray.jpeg: The input X-ray image used for edge detection.
edge_detection.py: The Python script that applies Sobel and Laplacian filters to the X-ray image and visualizes the results.
Code Overview
The script performs the following steps:

Import Libraries:

numpy: For numerical operations.
matplotlib.pyplot: For displaying images.
cv2 (OpenCV): For image processing.
Load and Display the Image:

The X-ray image (xray.jpeg) is loaded using cv2.imread().
The image is then converted to RGB format for proper visualization using Matplotlib.
Apply Sobel Filters:

sobelX: Detects edges along the x-axis.
sobelY: Detects edges along the y-axis.
The Sobel filters are applied using cv2.Sobel().
Combine Sobel Filters:

The x-axis and y-axis edges are combined using cv2.bitwise_or().
Apply Laplacian Filter:

The Laplacian filter, which detects edges in all directions, is applied using cv2.Laplacian().
Visualize the Results:

The original image, the results of the Sobel filters, the combined Sobel result, and the Laplacian filter result are displayed in a 2x3 grid using Matplotlib.
How to Run
Place the xray.jpeg image in the same directory as the script.
Run the script using Python:
python edge_detection.py
The script will display a 2x3 grid showing the original image, the Sobel X and Y filter results, the combined Sobel result, and the Laplacian result.
Output
The output will be a visual representation of the edge detection process, highlighting the differences captured by the Sobel and Laplacian filters.
