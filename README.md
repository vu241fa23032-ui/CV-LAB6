# Bit-Plane Slicing in Image Processing

This script demonstrates bit-plane slicing in Computer Vision using Python. It extracts and visualizes the individual bit planes of an 8-bit grayscale image, from the Least Significant Bit (LSB) to the Most Significant Bit (MSB).

## Prerequisites

Ensure you have the required Python libraries installed:

    pip install opencv-python matplotlib numpy

## How to Use

1. Update the image path in the script. It currently reads from `/content/drive/MyDrive/womancat.webp`. Change this to your local image path:
       
       img = cv2.imread('path/to/your/image.webp', cv2.IMREAD_GRAYSCALE)
       
2. Run the script in your terminal or Python environment.
### Note: You can directly open the `.ipynb` file in Colab or Jupyter Notebook.

## How it Works

1. **Image Loading**: The image is loaded directly in grayscale mode.
2. **Bitwise Operations**: A loop iterates through the 8 bits (0 to 7). For each bit `i`, the image is bitwise right-shifted by `i` and logically AND-ed with `1` to extract the exact bit plane.
3. **Scaling**: The extracted bit values (0 or 1) are multiplied by 255 to map them to valid visible pixel values for grayscale rendering.
4. **Visualization**: Matplotlib is used to plot the original image alongside all 8 individual bit planes in a grid format, demonstrating how higher bit planes contain the most visual information.
