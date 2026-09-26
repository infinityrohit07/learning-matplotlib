# Learning Matplotlib

A small, notebook-based learning folder for practicing data visualization in Python. The notebooks progress from general visualization notes to Matplotlib concepts, line plots, and bar charts.

## What's in this folder

- `01_data-visualisation-notes.ipynb` — introductory data visualization notes.
- `02_matplotlib-notes.ipynb` — notes and examples for Matplotlib.
- `03_lineplot.ipynb` — line plot examples and practice.
- `04_barcharts.ipynb` — bar chart examples and practice.
- `requirement.txt` — the Python packages needed to run the notebooks: NumPy, pandas, Matplotlib, and Jupyter.
- `.gitignore` — excludes the local virtual environment and Python/Jupyter cache files from Git.

## What you need

1. Install Python 3.11 or newer from [python.org](https://www.python.org/downloads/). On Windows, enable **Add Python to PATH** in the installer.
2. Open a terminal (PowerShell on Windows, Terminal on macOS/Linux) and change directory to this folder.
3. Create a virtual environment and activate it:

   **Windows PowerShell**
   ```powershell
   python -m venv venv
   .\venv\Scripts\Activate.ps1
   ```

   If PowerShell blocks activation scripts, you can activate from Command Prompt instead with `venv\Scripts\activate.bat`, or use the current PowerShell session-only option `Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass` and run the activation command again.

   **macOS / Linux**
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

4. Install the packages listed in the provided file (its name is singular: `requirement.txt`):

   ```bash
   python -m pip install --upgrade pip
   python -m pip install -r requirement.txt
   ```

5. Start Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

   Your browser will open the Jupyter file list. Choose a notebook to begin. Run cells from top to bottom with **Shift+Enter**. When finished, stop the notebook server with **Ctrl+C** in the terminal and confirm if prompted.

## Using the virtual environment

A virtual environment is a separate Python setup for this folder. Packages installed while it is active stay with this project instead of changing your system-wide Python installation or interfering with packages used by another project. This also makes it easier to reproduce the setup: create a fresh environment and install the packages from `requirement.txt`.

Activate the environment whenever you work on these notebooks. The terminal prompt usually shows `(.venv)` when it is active. To leave it, run:

```bash
deactivate
```

The `venv/` directory is a local environment created on one machine. Virtual environments are generally not portable between machines, so create your own by following the steps above rather than relying on a copied environment folder. It is ignored by Git.

## Troubleshooting

- If `python` or `py` is not recognized, install Python and reopen the terminal. On macOS/Linux, use `python3` where needed.
- If Jupyter cannot find a package, make sure the virtual environment is active and rerun `python -m pip install -r requirement.txt`.
- If notebook cells use the wrong Python, select the environment's Python kernel in Jupyter. You can register it with `python -m ipykernel install --user --name learning-matplotlib --display-name "Python (learning-matplotlib)"` while the environment is active.
