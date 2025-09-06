# MLOps Assignment 3: The MLOps Workflow

This project demonstrates a simple MLOps workflow with **Git best practices**, **model versioning**, and **release management**.

## Project Structure
```
mlops-assignment3/
│-- train.py           # Training script for a simple ML model
│-- requirements.txt   # Python dependencies
│-- .gitignore         # Files to ignore in Git
│-- README.md          # Project instructions
```

## Steps to Reproduce

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/mlops-assignment3.git
cd mlops-assignment3
```

### 2. Create a virtual environment and install dependencies
```bash
python -m venv .venv
source .venv/bin/activate    # On Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Run the training script
```bash
python train.py
```
This will generate a `model.pkl` file (ignored by Git).

### 4. Make code changes and commit
Edit `train.py` (e.g., change hyperparameters), then:
```bash
git add train.py
git commit -m "feat: Update hyperparameters for better performance"
```

### 5. Create a version tag and push
```bash
git tag -a v1.0.0 -m "Release v1.0.0"
git push origin main
git push origin v1.0.0
```

### 6. Create deployment branch
```bash
git checkout -b deployment/v1.0.0
git push origin deployment/v1.0.0
```

## Deliverables Checklist
- [x] `train.py` and `requirements.txt` committed
- [x] `model.pkl` ignored by Git
- [x] `v1.0.0` tag created and pushed
- [x] `deployment/v1.0.0` branch created

## Tools Used
- Python 3.x
- scikit-learn
- Git / GitHub
