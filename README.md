# instruct_lab

## Setup WSL


## In WSL
- Clone Repo
- CD to Repo

### Commands
Update linux package lists
```
sudo apt-get update
```

Get nvtop
```
sudo apt-get install nvtop
```

Install venv and pip
```
sudo apt install python3-pip
sudo apt install python3.12-venv
```

Use venv
```
python3 -m venv venv
source venv/bin/activate
```

Install ILab
```
pip3 install instructlab
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