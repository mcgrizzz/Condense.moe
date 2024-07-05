## Installation
1. Clone the git repository to a local folder
``` { .bash .copy }
git clone https://github.com/mcgrizzz/Koe.moe
cd ./Koe.moe
```
2. Download [ffmpeg](https://www.ffmpeg.org/download.html) and install it
=== "Conda"
    1. Download and install [miniconda](https://docs.anaconda.com/miniconda/)
    === "CUDA"
        ``` { .bash .copy }
        conda env create -f "environment_cuda.yml"
        conda activate koemoe
        ```
    === "CPU"
        ``` { .bash .copy }
        conda env create -f "environment_cpu.yml"
        conda activate koemoe
        ```
=== "Pip"
    1. Download and Install [**python 3.8+**](https://www.python.org/downloads/)
=== "Manual"
    1. Download and Install [**python 3.8+**](https://www.python.org/downloads/)
    2. Install

## FAQ
??? question "Which do I install: CUDA or CPU?"
    ``` mermaid
    graph LR
    A(Do you have an Nvidia GPU?)-- YES -->B(CUDA);
    A-- NO -->C(CPU);
    ```
??? question "Why use Conda?"
    Conda will create a self-contained environment for all of project requirements that is separate from the rest of your system. For example you can have python 3.8 installed on your system but in the conda environment it can be any other version.
    The downside to this approach is you must be in the conda environment (```conda activate koemoe```) in order to run the program
