

# Antigen challenge: 

Pick one track: 
- Track 1 (Easiest): 
    Use an existing model (like TAP, AntiFold, ESM embeddings). 
    Generate predictions on GDPa1 and submit them. 
- Track 2 (Harder, but rewarding): 
    Train your own model using GDPa1 with cross-validation. 
    Submit your CV predictions. 


## 5 categories | highest scores so far: 

Hydrophobicity: 0.42 

Self-association: 0.37 

Polyreactivity: 0.32 

Thermo stability: 0.19 

Titer: 0.18 

## Dataset: 

https://huggingface.co/datasets/ginkgo-datapoints/GDPa1 

```
import pandas as pd 

Login using e.g. huggingface-cli login to access this dataset 

df = pd.read_csv("hf://datasets/ginkgo-datapoints/GDPa1/GDPa1_v1.2_20250814.csv") 
```

Docs:  https://huggingface.co/docs/hub/datasets-pandas 


## 🧩 Where to Start Practically 

Learn Python basics if you haven’t already. 

Install scikit-learn → try a simple regression/classification. 

Play with Hugging Face protein models: 

facebook/esm2 (for embeddings). 

Try a mini-project: “Predict hydrophobicity from sequence embeddings.” 

## 📂 Task Division 

### 1. Data & Biology Lead 

- Responsibilities: 
    Understand the 5 developability properties (Hydrophobicity, Self-association, Polyreactivity, Thermostability, Titer). 
    Preprocess datasets (cleaning sequences, formatting labels). 
    Perform exploratory data analysis (EDA): distributions, correlations, simple baseline models. 
    Write documentation for the biological meaning of features (helps in final write-up). 

- Best Fit: 
    Someone with biology / bioinformatics background. 
    Strengths: understanding proteins, interpreting developability. 

 

### 2. Modeling & ML Engineer 

- Responsibilities: 
    Set up embeddings (ESM, ProtBERT, TAP, etc.). 
    Train ML models (ridge regression, neural networks, transformers). 
    Run cross-validation, tune hyperparameters, track performance. 
    Optimize for Spearman correlation on each property. 

- Best Fit: 
    Someone comfortable with Python, scikit-learn, PyTorch/Hugging Face. 
    Strengths: coding, experimenting with ML architectures. 

 

### 3. DevOps & Integration Lead 

- Responsibilities: 
    Set up GitHub/GitLab for version control. 
    Ensure reproducibility (requirements.txt, Dockerfile, training scripts). 
    Handle submission pipeline (convert predictions into required format, test locally). 
    Write clean documentation and automation (so models can be easily rerun). 
    Optional: Build a basic dashboard/GUI for monitoring results. 

- Best Fit: 
    Someone strong in software engineering / DevOps / automation. 
    Strengths: organizing workflow, making sure everything runs smoothly. 

 

 