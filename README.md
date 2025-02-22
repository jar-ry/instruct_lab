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
ilab config init
```

Download model
```
ilab model download -rp --filename merlinite-7b-lab-Q4_K_M.gguf
```

Serve Model
```
 ilab serve --model-family merlinite --model-path ~/.cache/instructlab/models/merlinite-7b-lab-GGUF/merlinite-7b-lab-Q4_K_M.gguf
```

## Usage of repo
Since the taxonomy already exists we only need to download the model
```
ilab model download -rp --filename merlinite-7b-lab-Q4_K_M.gguf
```

## Before tuning the model
Clearly the model has not been trained on the.

AI Principles published by Australia's Department of Industry, Science and Resources
![ai_principles](ai_principles.png)

What the model thinks the principles published by Australia's Department of Industry, Science and Resources
![hallucination_ilab](hallucination_ilab.png)

## Tuning the model
```
cp -r taxonomy_new/knowledge/ai ~/.local/share/instructlab/taxonomy/knowledge

ilab data generate --model ~/.cache/instructlab/models/merlinite-7b-lab-GGUF/merlinite-7b-lab-Q4_K_M.gguf  --pipeline simple
```

