# ⚙️ Installation and environment setup

## ✅ Prerequisites
- Python 3.10+ recommended.
- Git.
- Local challenge dataset files.
- Enough disk and memory for CSVs and sparse feature matrices.

## 📥 Clone
```bash
git clone https://github.com/Brajesh31/AmazonML-Hackathon.git
cd AmazonML-Hackathon
python -m venv .venv
```

Activate on PowerShell: `.venv\\Scripts\\Activate.ps1`

Activate on Windows CMD: `.venv\\Scripts\\activate.bat`

Activate on macOS/Linux: `source .venv/bin/activate`

## 📦 Install dependencies
```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```
The manifest defines supported version ranges, not an exact lockfile. Capture the installed package versions for each reported experiment. If a dependency changes its API, verify compatibility before updating the environment.

## ▶️ Launch
```bash
jupyter lab
```
Open `AmazonML.ipynb` from the repository root. Replace its developer-specific absolute Windows dataset path with repository-relative `Path("dataset")` paths before execution. See [troubleshooting](troubleshooting.md) for the saved LightGBM compatibility error.
