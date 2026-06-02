# Image Rotator

## Output Preview

![Rotation modes comparison](rotation_all_modes.gif)

The GIF above shows three rotation strategies side by side: **cut**, **preserve**, and **zoom to content**, generated with the Lanczos (a=4) algorithm.

## Usage

Run the program with:

```bash
python run.py
```

The script will automatically:

- Install Python dependencies from `requirements.txt`
- Compile the C++ extension (using pybind11 and OpenCV)
- Launch the graphical user interface (GUI)

## Features

- **Multiple interpolation methods** – nearest neighbour, bilinear, bicubic (configurable sharpness), and Lanczos (configurable window size)
- **Manual and OpenCV reference implementations** for comparison
- **Real‑time rotation** with three zoom modes: cut corners, preserve whole image, and zoom to maximal inner rectangle
- **Interactive selection** – define a region of interest to compute PSNR locally
- **PSNR analysis** – line plots and boxplots over rotation angles
- **Split‑view comparison** between original and twice‑rotated (-Inverse) image
- **4×2 grid** comparing reference vs manual implementations side‑by‑side

## Requirements
on windows download, extract and put into root folder (C:\opencv\build): https://sourceforge.net/projects/opencvlibrary/

## Compilation
The C++ core is built automatically the first time you run `run.py`.  
On Windows, the script looks for OpenCV in `C:\opencv\build` or uses the `OpenCV_DIR` environment variable.  
On Linux/macOS, `pkg-config opencv4` must be available.