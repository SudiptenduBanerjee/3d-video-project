3D Video Generation from 2D Video

This repository presents a robust Python-based solution, implemented as a Jupyter Notebook, designed to convert conventional 2D video footage into immersive 3D anaglyph videos. This transformation is achieved through a sophisticated pipeline involving per-frame depth estimation, subsequent generation of stereoscopic image pairs, and their final synthesis into an anaglyph format.
Table of Contents

Project Overview

Methodology

Getting Started

Prerequisites

Installation

Usage Guide

Expected Output


Project Overview

This project harnesses advanced deep learning techniques for monocular depth estimation to facilitate the conversion of any standard 2D video input into a 3D anaglyph video. Anaglyph 3D imagery, when viewed through specialized anaglyph glasses (typically red-cyan or red-blue), creates the perception of three-dimensionality. This illusion of depth is meticulously engineered by presenting distinct visual information to each eye.
Methodology

The conversion process is systematically executed through the following key stages:

    Dependency Management: Essential Python libraries, including torch, torchvision, opencv-python-headless, numpy, and timm, are automatically installed to ensure a self-contained execution environment.

    Video Ingestion: The system facilitates the upload of a user-specified 2D video file, supporting common formats such as .mp4 and .avi.

    Frame Discretization: The uploaded video stream is meticulously decomposed into its constituent individual frames. Each frame is then persistently stored as a high-quality image file.

    Depth Estimation via MiDaS: For every extracted frame, the MiDaS (Multi-Dataset Augmented Depth Estimation) model is employed to generate a precise depth map. MiDaS represents a cutting-edge approach in the field of monocular depth estimation, providing highly accurate depth information from a single 2D image.

    Stereoscopic Pair Synthesis: Utilizing the original frame and its corresponding estimated depth map, a stereoscopic image pair (comprising distinct left and right eye views) is computationally generated. This crucial step simulates the natural parallax effect inherent to 3D perception by intelligently displacing pixels based on their calculated depth values.

    Anaglyph Image Composition: The synthesized left and right eye views are subsequently combined to form an anaglyph image. In the context of red-cyan anaglyphs, the red color channel is typically derived from the left eye's image, while the green and blue channels are sourced from the right eye's image, creating the characteristic visual separation.

    Video Reconstruction: All the individually processed anaglyph frames are then sequentially compiled and encoded back into a cohesive video file, preserving the original video's frame rate.

    Output Provision: The final 3D anaglyph video is made available for direct download, enabling immediate access to the transformed content.

Getting Started

To replicate and utilize this code, it is highly recommended to execute the Jupyter Notebook within a Google Colaboratory environment. This platform offers the requisite GPU acceleration and a pre-configured computational setting, streamlining the execution process.
Prerequisites

    A Google Colaboratory account (freely accessible).

    A 2D video file (e.g., .mp4, .avi) intended for 3D conversion.

Installation

Local installation is not a prerequisite when leveraging Google Colab, as the notebook script autonomously manages all necessary dependency installations upon execution.
Usage Guide

    Accessing the Notebook via Google Colab:

        Navigate to the Google Colab platform: colab.research.google.com.

        Upload the 3d-video-generation.ipynb notebook file to your Colab workspace.

    Sequential Cell Execution:

        Step 1: Install dependencies: Execute the initial cell to install all required Python libraries.

        Step 2: Upload video: Run this cell and adhere to the on-screen prompts to upload your desired 2D video file.

        Step 3: Extract frames: Execute this cell to initiate the extraction of individual frames from your uploaded video.

        Step 4: Depth estimation with MiDaS: This cell will load the pre-trained MiDaS model and proceed to generate depth maps for every extracted frame. The execution time for this step is contingent upon the video's duration and the allocated Colab runtime resources.

        Step 5: Create stereoscopic pairs: This cell will generate the distinct left and right eye views for each processed frame.

        Step 6: Create anaglyph images: This cell orchestrates the combination of the stereoscopic pairs into the final anaglyph image format.

        Step 7: Reconstruct video: This cell performs the compilation of all generated anaglyph frames into a new, single 3D video file.

        Step 8: Download the output video: The concluding cell will furnish a direct link for downloading the newly created 3D anaglyph video.

Expected Output

Upon successful execution, the script will produce an output_3d_video.mp4 file, located within the same directory as the notebook. This resultant video, when viewed with appropriate red-cyan anaglyph glasses, will exhibit the intended three-dimensional effect.
Contributing

We welcome and encourage contributions to this project. Should you identify potential enhancements, bug fixes, or new feature implementations, please feel free to open an issue or submit a pull request.
License

This project is distributed under the terms of the MIT License, ensuring open access and flexibility for use and modification.
