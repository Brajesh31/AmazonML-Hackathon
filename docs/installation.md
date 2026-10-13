# Installation

Create a virtual environment with Python 3.10 or newer, then install the libraries used by the committed notebook:

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate
python -m pip install pandas numpy scikit-learn scipy lightgbm tqdm requests jupyter
```

Open `AmazonML.ipynb` from the repository root. Replace its absolute dataset paths with relative paths before execution. Keep large image downloads outside the repository.
