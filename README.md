# Skyrmion U-Net workshop repository

[![Binder](https://img.shields.io/badge/JupyterHub-Ready-orange?logo=jupyter)](https://plg.physlab.uni-due.de:80/hub/login?next=%2Fhub%2F)

This badge above is the JupyterHub badge for the JupyterLab instance at the University of Duisburg. To run the Jupyter Notebooks online, click on the Jupyter Hub badge and enter the username and password that will be provided during the PhD focus session hands-on workshop. The JupyterHub will be accessible during that period.

This repository is intended to help users get started with the Skyrmion U-Net through tutorials and to facilitate its use. It is also used in the [MA 35: PhD Focus Session: Using Artificial Intelligence Tools in Magnetism](https://www.dpg-verhandlungen.de/year/2025/conference/regensburg/part/ma/session/35/contribution/5) . The organizers of this session and the creators of this repository are Kilian Leutner, Robin Msiska, Kübra Kalkan, Thomas B. Winkler, and Jan Maskill. For any questions regarding this repository, please contact Kilian Leutner at kileutne@students.uni-mainz.de.

## Getting Started on Your Own Device

If you have not yet downloaded this repository, you can do so in two ways. If you have `git` installed on your device, you can use the command:

```
git clone https://github.com/kfjml/AI-Magnetism-Session-Regensburg-2025
```

If you do not have `git`, go to the main page of the GitHub repository, click the green `Code` button at the top of the page, and then select `Download ZIP`. After downloading, unzip the archive and open a command line. Navigate to the unzipped folder.

To run the reposiotry, we will install `pixi`, which is highly recommended because it ensures compatibility across multiple platforms. The package installation via Pixi supports Linux 64-bit, macOS 64-bit (Intel), macOS ARM 64-bit (Apple Silicon), Windows 64-bit, and Linux AArch64. Windows ARM 64 is not supported. To use Pixi on Windows ARM 64, please install it via WSL (Windows Subsystem for Linux) and then install Pixi and the required packages within WSL, as this will work. To install `pixi`, follow the instructions at [https://pixi.sh/latest/](https://pixi.sh/latest/). It is easy to install on Windows, Linux, and macOS via the command line. Once installed, open the command line (if it is not already open) and navigate to the downloaded repository folder (`AI-Magnetism-Session-Regensburg-2025`). To install the default environment for CPU, run:

```
pixi install
```

This installation process only affects the repository folder, and all required packages will be stored in a subfolder named `./pixi/`. After installation, start Jupyter Notebook by running:

```
pixi run jupyter notebook
```

This command will start Jupyter Notebook and output a localhost address, which you can open in your web browser to access Jupyter Notebook. Depending on your platform, the notebook may open automatically.

### Run repository on GPU

If you want to ensure that the environment runs on the GPU (if your device has a GPU), additional CUDA/cuDNN libraries will be installed by running:

```
pixi install --manifest-path gpu_pixi_environment/pixi.toml
```

After installation, start the Jupyter Notebook with:

```
pixi run --manifest-path gpu_pixi_environment/pixi.toml jupyter notebook
```

### Run repository with Anaconda

If you prefer to set up the environment and necessary packages using Anaconda, you can follow [these instructions](./using-conda.md).

## Getting Started in Online Notebooks

If you want to run the Jupyter Notebooks online, click on the **Jupyter Hub** badge at the top of the page and type in the username and password. 

If the JupyterLab instance at the University of Duisburg **is not working at all**, click on the badge of the corresponding Jupyter Notebook in the table below this paragraph to open it in **Google Colab**. Please only run the notebooks online on servers during the hands-on live tutorial if you are unable to manage a local installation and cannot use the Jupyter Hub instance from the University of Duisburg. **Google Colab** allows you to run notebooks for only about 2 hours before disconnecting. For more details, check [here](./google-colab.md).

| Description | Jupyter Notebook | Google Colab |
|---|---|---|
| Training and Prediction Tutorial | `1_training_and_prediction_tutorial.ipynb` |  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kfjml/AI-Magnetism-Session-Regensburg-2025/blob/main/Prediction_tutorial.ipynb) | 
| Pretrained Models Prediction Tutorial | `2_pretrained_models_prediction_tutorial.ipynb` |  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kfjml/AI-Magnetism-Session-Regensburg-2025/blob/main/Training_tutorial.ipynb) | 
| Prediction and Analysis Editor GUI  | `3_prediction_analysis_editor_gui.ipynb`  |  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kfjml/AI-Magnetism-Session-Regensburg-2025/blob/main/Editor.ipynb) | 


## Manual installation

For a manual installation in anaconda, see: [Manual setup](./manual-setup.md).

## Acknowledgements

The dataset included in this repository is extracted from the Zenodo repository (v2.0) by Winkler et al.: [https://doi.org/10.5281/zenodo.10997175](https://doi.org/10.5281/zenodo.10997175). The authors of this repository, which also includes the authors of the Zenodo repository, are Kilian Leutner, Thomas Brian Winkler, Isaac Labrie-Boulay, Alena Romanova, Hans Fangohr, Mathias Kläui, Raphael Gruber, Fabian Kammerbauer, Klaus Raab, Jakub Zazvorka, Elizabeth Martin Jefremovas, and Robert Frömter.
