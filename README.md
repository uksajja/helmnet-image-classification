
## Helmnet-Image-Classification


### v1.0.0 — ComputerVison - CNNs Development

ComputerVision
Convolutional Neural Networks

## Skills & Tools
------------------
- EDA
- CNNs
- Filters
- Transfer Learning (VGG16)
- Data Augmentation
- HyperParameter Tuning
- Model Performance Evaluation
- Business Recommendations


## Steps to Run the project:
----------------------------

- Note: On windows, tensorflow does not support GPU, only CPU version is supported.

- For Tensorflow with GPU support:
  - Use docker
  - Switch to Linux
  - Use WSL2

- Local venv environment
  - py -3.12 -m venv .venv
  - source .venv/Scripts/activate  (Git bash)  or .\.venv\Scripts\Activate.ps1 (PowerShell)
  - source .venv/bin/activate (on linux)
  - python -V
  - python -m pip install --upgrade pip setuptools wheel

  - python -m pip install -r requirements.txt
  - open notebook and select the local python .venv as kernel
  - run all the cells

  - deactivate if you want to come out of the virtual environment

- Local conda environemnt
  - conda env create -n .conda -f environment.yaml

  - To activate this environment, use

    - conda activate C:\github\helmnet-image-classification\.conda\tf-cpu

    - # To deactivate an active environment, use

    - conda deactivate

    - open notebook and select the local python env-helmnet-image-classification as kernel
    - run all the cells

- Inside docker
  - docker build -t helmnet-image-classification .
  - docker run --rm -p 8891:8888 -e JUPYTER_TOKEN=my-secret-token helmnet-image-classification
  - Run with gpu
    - check if GPU is available
    - nvidia-smi
    - If avialable,
    - docker run --gpus all --rm -p 8891:8888 -e JUPYTER_TOKEN=my-secret-token helmnet-image-classification
    - open http://localhost:8891/?token=my-secret-token
    - run the notebook
