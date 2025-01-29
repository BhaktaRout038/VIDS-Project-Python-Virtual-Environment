# VIDS Project Python Virtual Environment Installation Guide

## Step-by-Step Setup

### 1. Create a Virtual Environment

Run the following command to create a virtual environment:

```sh
python -m venv venv
```

### 2. Activate the Virtual Environment

For Windows:

```sh
venv\Scripts\activate
```

For macOS/Linux:

```sh
source venv/bin/activate
```

### 3. Upgrade Pip

Ensure your package manager is up to date:

```sh
python -m pip install --upgrade pip
```

### 4. Upgrade Setuptools and Wheel

Ensure other package management tools are updated:

```sh
pip install --upgrade setuptools wheel
```

### 5. Install OpenCV

Install OpenCV separately:

```sh
pip install opencv-contrib-python
```

### 6. Install Ultralytics

```sh
pip install ultralytics
```

### 7. Install PostgreSQL Adapter

```sh
pip install psycopg2
```

### 8. Install PyTorch with CUDA 12.1

Check if PyTorch is installed:

```sh
pip show torch
```

If installed, uninstall existing PyTorch packages:

```sh
pip uninstall torch torchvision torchaudio -y
```

Then install the correct version:

```sh
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
```

Refer to [this guide](https://github.com/BhaktaRout038/How-to-Install-NVIDIA-GPU-For-object-detection-Cuda-Toolkit-And-cuDNN) for more details on NVIDIA GPU setup.

## below step just for the information

### 9. Installing `dlib`

If you encounter issues while installing `dlib`, follow these steps:

#### a. Install Microsoft Build Tools (Windows only)

Download and install **Microsoft Build Tools for Visual Studio** from:
[https://visualstudio.microsoft.com/downloads/](https://visualstudio.microsoft.com/downloads/)


#### b. Install Required Packages

```sh
pip install cmake wheel setuptools
```

#### c. Install `dlib` Without Cache

```sh
pip install --no-cache-dir dlib
```

### 10. Additional Notes

- If you are using a virtual environment, ensure it is activated before running the installation commands.
- If installation issues persist, consider using a compatible Python version (**3.8+ recommended**).
- For GPU support, ensure CUDA and cuDNN are installed and properly configured.

### 11. Final Setup Steps

Clean temporary files:

```sh
del /q /s %TEMP%
```

Install dependencies from `requirements.txt`:

```sh
pip install -r requirements.txt
```

### 12. Troubleshooting

If you still encounter issues, check the error messages and refer to:

- [dlib GitHub Repository](https://github.com/davisking/dlib)
- [OpenCV Documentation](https://opencv.org/)
- [Python Package Index (PyPI)](https://pypi.org/)

---

This README provides essential installation steps and troubleshooting tips for dependencies used in this project. If additional issues arise, update the document with new solutions. Happy coding!

