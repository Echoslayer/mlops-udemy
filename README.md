# mlops-udemy

conda create -p venv python==3.10 -y


pyenv install 3.10
pyenv local 3.10
python -m venv .venv

pip install -r requirements.txt

https://mlflow.org/

[DagsHub: Everything you need to manage multimodal AI](https://dagshub.com/)


pip install dvc 
dvc init
dvc add <FileName>
dvc checkout

dvc stage add -n <StagePipeline> -p <Param> -d <Dependacies> -o <OutputFile> <SrcFilePy>

dvc repro

dvc pull -r origin
dvc push -r origin