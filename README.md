# 3D Video Generation with Python and Machine Learning

## Overview
This project demonstrates how to create a 3D video using Python and machine learning techniques in a Kaggle notebook, with the final code and output video shared on GitHub. The project generates a rotating 3D cube animation using `matplotlib` and compiles it into a video using `opencv-python`. Optionally, it supports advanced 3D model generation using the TripoSR model from StabilityAI, though the provided implementation focuses on a simple cube animation for compatibility with Kaggle's free tier.

## Features
- Generates a 3D rotating cube animation using `matplotlib`.
- Compiles frames into a video file (`3d_cube_video.mp4`) using `opencv-python`.
- Runs in a Kaggle notebook environment with minimal setup.
- Includes instructions for pushing the project to GitHub.
- Optional: Supports 3D model generation from 2D images using TripoSR (requires GPU).

## Prerequisites
- **Kaggle Account**: Required to run the notebook. Sign up at [kaggle.com](https://www.kaggle.com).
- **GitHub Account**: For hosting the repository. Sign up at [github.com](https://github.com).
- **Python Libraries**:
  - `matplotlib`, `numpy`, `opencv-python` (pre-installed in Kaggle).
  - `torch`, `torchvision`, and `triposr` (installed via pip in the notebook).
- **Optional**: GPU-enabled Kaggle notebook for TripoSR (requires phone verification).

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/3d-video-project.git
   cd 3d-video-project
   ```

2. **Set Up Kaggle Notebook**:
   - Log in to [Kaggle](https://www.kaggle.com) and create a new notebook (`Code` > `New Notebook`).
   - Copy the contents of `3d_cube_animation.py` from this repository into a Kaggle notebook cell.
   - Install required libraries in a Kaggle cell:
     ```python
     !pip install opencv-python matplotlib numpy torch torchvision
     !pip install git+https://github.com/stability-AI/triposr.git
     ```

3. **Link Kaggle to GitHub**:
   - In the Kaggle notebook, go to `File` > `Link to GitHub` and authorize your GitHub account.
   - Select this repository (`3d-video-project`) to commit the notebook.

## Usage
1. **Run the Notebook**:
   - Open the Kaggle notebook (see [Kaggle Notebook Link](#kaggle-notebook)).
   - Execute all cells to:
     - Generate 100 frames of a rotating 3D cube.
     - Compile frames into `3d_cube_video.mp4` in `/kaggle/working`.
   - Download the video from Kaggle’s “Output” tab.

2. **Optional: Use TripoSR for Advanced 3D Models**:
   - Upload a 2D image to Kaggle (e.g., `/kaggle/input/your-dataset/image.png`).
   - Add the TripoSR code (see notebook comments) to generate a 3D mesh.
   - Note: Requires GPU and additional rendering setup (e.g., `pyrender` or Blender).

3. **Push Video to GitHub**:
   - Download `3d_cube_video.mp4` from Kaggle.
   - Add it to this repository:
     ```bash
     git add 3d_cube_video.mp4
     git commit -m "Add 3D video output"
     git push origin main
     ```

## Files
- `3d_cube_animation.py`: Python script for generating and compiling the 3D video.
- `3d_cube_video.mp4`: Output video of the rotating cube (manually uploaded).
- `README.md`: This file, providing project documentation.

## Kaggle Notebook
- [Link to Kaggle Notebook](https://www.kaggle.com/your-username/your-notebook): Run the code directly in Kaggle.
  *(Replace with the actual notebook URL after making it public in Kaggle’s `Settings` > `Sharing` > `Public`.)*

## Output
- The generated video (`3d_cube_video.mp4`) is available in this repository.
- View it directly on GitHub or download it to watch locally.

## Notes
- **Kaggle Limitations**: Ensure sufficient disk space in Kaggle’s `/kaggle/working` directory. Delete frame files after video compilation to save space.
- **GitHub File Size**: Videos larger than 100MB require Git LFS or external hosting (e.g., Google Drive).
- **Advanced ML**: For TripoSR, refer to [PyImageSearch’s TripoSR tutorial](https://pyimagesearch.com) for setup details.
- **Troubleshooting**: Check Kaggle’s discussion forums or GitHub issues for help with errors.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments
- Built with [Kaggle](https://www.kaggle.com) for notebook execution.
- Uses `matplotlib`, `opencv-python`, and `TripoSR` from StabilityAI.
- Inspired by tutorials from [Analytics Vidhya](https://www.analyticsvidhya.com) and [PyImageSearch](https://pyimagesearch.com).