# opencv-document-scanner
This "Document Scanner" project utilizes OpenCV to preprocess an image, detect the document's contours, reorder them, apply a perspective transform, and crop the result. It handles grayscale conversion, blurring, edge detection, contour finding, and warping, providing a clean, scanned-like output of the document.
This project demonstrates a Document Scanner built using OpenCV in C++. It provides a complete solution for scanning documents, processing them, and obtaining a neatly cropped and perspective-corrected image. The implementation involves pre-processing, contour detection, perspective warping, and cropping.

Key Features
Pre-Processing: Converts the original image to grayscale, applies Gaussian blur for noise reduction, and uses Canny edge detection to highlight the document's edges. Morphological dilation further enhances these edges for contour detection.

Contour Detection: Identifies the largest contour that resembles a document shape (4-sided polygon) and selects it as the target. This ensures only the relevant document area is extracted.

Reordering Points: The corner points of the detected document are reordered to ensure they follow the correct sequence for perspective transformation.

Perspective Warp: Applies a perspective warp to transform the detected document area into a bird's-eye view, giving the appearance of a scanned document.

Cropping: The final image is cropped to remove any unwanted borders, producing a clean and sharp scanned output.

How It Works
The program reads an input image of a document.
Through pre-processing, the edges of the document are detected, and contours are used to identify the document's boundaries.
Using the identified points, a perspective transformation warps the image, resulting in a flat, scan-like appearance.
Technologies Used
OpenCV: Image processing and computer vision operations.
C++: Core programming language for implementation.
Requirements
OpenCV library installed.
C++ compiler.
How to Run
Place your document image in the "Resources" folder.
Compile and run the program.
The output will display the original, warped, and cropped images.
This project serves as a great introduction to computer vision concepts such as image processing, contour detection, and perspective transformation.
