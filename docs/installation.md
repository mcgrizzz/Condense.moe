## Installation
### 1. Prerequisites
   
**Clone the git repository to a local folder**
``` { .bash .copy }
git clone 'https://github.com/mcgrizzz/Koe.moe'
cd './Koemoe'
```


**Goto the [releases](https://github.com/mcgrizzz/Koemoe/releases) page and download the latest model. Place it into `/koemoe/model` folder that should be empty.**
<div class="admonition folder">
    <p class="admonition-title">koemoe/</p>
    ``` java
    ├── models/
    │   └── [model].pt
    ├── condense.py
    ├── ...
    └── utils.py
    ```
</div>
    
**Download [ffmpeg](https://www.ffmpeg.org/download.html) and install it**

### 2. Continue with Conda or Pip

=== "Conda"
    Download and install **[miniconda](https://docs.anaconda.com/miniconda/)**
    
    In the main directory of `Koemoe` run the following commands
    === "CUDA"
        ``` { .bash .copy }
        conda env create -f 'environment_cuda.yml'
        conda activate 'koemoe'
        ```
    === "CPU"
        ``` { .bash .copy }
        conda env create -f 'environment_cpu.yml'
        conda activate 'koemoe'
        ```
=== "Pip"
    Download and Install [**python 3.8+**](https://www.python.org/downloads/)
    In the main directory of `Koemoe` run the following commands
    === "CUDA"
        ``` { .bash .copy }
        pip install -r 'requirements_cuda.txt'
        ```
    === "CPU"
        ``` { .bash .copy }
        pip install -r 'requirements_cpu.txt'
        ```
    Finally run one more command
       ``` { .bash .copy }
       pip install -r 'requirements_common.txt'
       ```

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
