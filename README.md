# Image Equalizer GUI

A desktop application for enhancing image contrast using histogram equalization, built with Python and Tkinter. The project provides a simple interface to load an image, adjust quantization settings, and compare the original and equalized results visually.

## Overview

This repository contains a graphical tool for experimenting with image enhancement techniques. It uses a histogram-based equalization approach to improve brightness and contrast, making details in low-contrast images easier to interpret.

The interface allows users to:

- Import an image from disk
- View the processed output in a resizable canvas
- Adjust quantization parameters in real time
- Switch between original, equalized, histogram, and comparison views
- Save generated histogram outputs in the `data/` directory

## Features

- Image import and display
- Histogram equalization for contrast enhancement
- Adjustable quantization level
- Side-by-side comparison visualization
- Histogram plotting for analysis
- Clean dark-themed desktop UI
- Built with Python and common scientific imaging libraries

## Tech Stack

- Python 3
- Tkinter / CustomTkinter
- ttkThemes
- NumPy
- Pillow (PIL)
- scikit-image
- Matplotlib
- Pandas

## Repository Structure

```text
image_equalizer_GUI/
├── data/                     # Generated output images and supporting files
├── src/
│   ├── histogram.py          # Histogram-related utilities
│   ├── imageWidget.py        # Canvas/image display widgets
│   ├── interface.py          # Main application entry point
│   ├── menu.py               # UI controls and options menu
│   ├── panels.py             # Interface panels and layout helpers
│   ├── settings.py           # Configuration settings
│   ├── tools.py              # Core image processing functions
│   └── __pycache__/          # Python bytecode cache
├── README.md                 # Project overview and usage instructions
└── .gitignore                # Ignore generated files and local environment state
```

## Installation

1. Clone the repository:

```bash
git clone https://github.com/VelascoRt/image_equalizer_GUI.git
cd image_equalizer_GUI
```

2. Create and activate a virtual environment (optional but recommended):

```bash
python -m venv .venv
source .venv/bin/activate  # Linux/macOS
# .venv\Scripts\activate   # Windows
```

3. Install dependencies:

```bash
pip install numpy pandas pillow matplotlib scikit-image customtkinter ttkthemes
```

## Running the Application

From the repository root, start the GUI with:

```bash
python src/interface.py
```

Or run it from the `src` directory:

```bash
cd src
python interface.py
```

## How It Works

The application reads an image, converts it to grayscale when needed, applies quantization, and uses a histogram equalization procedure to redistribute intensity values. The processing pipeline includes:

- Image loading
- Intensity normalization
- Histogram computation
- Cumulative probability transformation
- Result rendering in the GUI

This makes it useful for improving contrast in images that are too dark, washed out, or difficult to interpret visually.

## Usage Notes

- Use the interface controls to select the image view mode.
- Change the quantization value to tune the equalization strength.
- Compare the original image with the equalized output to evaluate the enhancement.
- Generated histogram visualizations are stored under the `data/` folder.

## License

This project does not currently include a license file. If you plan to reuse or distribute it, consider adding an explicit open-source license.

## Contributing

Contributions are welcome. If you want to improve the GUI, optimize the processing logic, or add new image tools, feel free to open a pull request with a clear description of the changes.

## Author

VelascoRt
