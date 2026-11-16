# ⚙️ Installation

**Prerequisites:** Python 3.10+, Git, local challenge CSVs, sufficient memory/disk.

```bash
git clone https://github.com/Brajesh31/AmazonML-Hackathon.git
cd AmazonML-Hackathon
python -m venv .venv
```

Activate with `.venv\\Scripts\\Activate.ps1` (PowerShell), `.venv\\Scripts\\activate.bat` (CMD), or `source .venv/bin/activate` (macOS/Linux).

Install libraries referenced by the current notebook:

```bash
python -m pip install --upgrade pip
python -m pip install pandas numpy scikit-learn scipy lightgbm tqdm requests jupyter
jupyter lab
```

There is no pinned lockfile. Open `AmazonML.ipynb` from the repository root and replace its developer-specific absolute data path with a relative `Path("dataset")` path before running.
