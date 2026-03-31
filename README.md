# Road-Crack-Deection

Smart Road Crack Detection
This project is an automated, image-based system designed to detect and assess road surface cracks using classical computer vision techniques. Developed for a Computer Vision course during the Winter Semester 2025–2026, it provides a consistent and objective alternative to manual road inspections.

Project Overview
The system identifies crack regions in road surface photographs, highlights them visually, and classifies damage severity without requiring deep learning or GPU computation. It is designed to be lightweight, transparent, and computationally efficient.

Technical Pipeline
The detection process consists of a sequential multi-stage pipeline:

Preprocessing: Converts images to grayscale, applies Contrast Limited Adaptive Histogram Equalization (CLAHE) for enhancement, and uses a Gaussian Blur to remove noise.

Feature Extraction: Combines Canny Edge Detection and Adaptive Thresholding via a bitwise OR operation to capture both fine edges and broader dark regions.

Refinement: Utilizes morphological operations, such as closing and opening, to bridge gaps in crack lines and eliminate isolated noise pixels.

Analysis: Detects contours and filters them by area to calculate the total crack coverage percentage.

Severity Classification
The system categorizes road damage based on the total crack area relative to the image size:

Low: Less than 1% crack area; indicates minor surface cracks.

Medium: 1% to 5% crack area; indicates moderate damage where maintenance is recommended.

High: Greater than 5% crack area; indicates severe cracking requiring immediate repair.

Features
Visual Pipeline: Displays all intermediate processing stages, including grayscale, blurred, edges, and thresholding results.

Batch Processing: Supports loading and processing individual images or entire folders.

Interpretability: Every step of the pipeline is based on fundamental computer vision concepts, making the results easy to understand and tune.

Tech Stack
Language: Python 3.8+

Libraries: OpenCV, NumPy, Matplotlib

Installation and Usage
Clone the repository and navigate to the project folder.

Install dependencies using the provided requirements file.

Run the main script to process images in the data directory and generate severity reports and visual outputs.
