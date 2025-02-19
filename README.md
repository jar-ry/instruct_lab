# instruct_lab

## Setup WSL


## In WSL
- Clone Repo
- CD to Repo

### Setup Commands
Update linux package lists
```
sudo apt-get update
```

Get nvtop
```
sudo apt-get install nvtop
```

Install Conda
```
curl -L -O "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
bash Miniforge3-$(uname)-$(uname -m).sh
```

CD into Directory
```
cd instruct_lab
```

Use conda
```
conda env create --file=conda.yml
conda activate ilab_env
```

Init ILab
```
ilab init
```

Download model
```
ilab download
```

Serve Model
```
 ilab serve --model-family merlinite --model-path ./models/merlinite-7b-lab-Q4_K_M.gguf
```

## Usage of repo
Since the taxonomy already exists we only need to download the model
```
ilab download
```

## Before tuning the model
Clearly the model has not been trained on the.

AI Principles published by Australia's Department of Industry, Science and Resources
![ai_principles](ai_principles.png)

What the model thinks the principles published by Australia's Department of Industry, Science and Resources
![hallucination_ilab](hallucination_ilab.png)

## Tuning the model
```

```

