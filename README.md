# Regression analysis

report.ipynb compares OLS, WLS, GLSAR, and Ridge on simulated data.
The first 80% of rows form the training set; the remaining 20% form the test set.
Keep the original row order.

## Data

Google Drive download link: [Click This Link](https://drive.google.com/drive/folders/1ZRIr3VRAD7rCLDqHQKQWTnSYfK_cby2W?usp=sharing).

Download raw_data_simulasi.txt and place it beside report.ipynb.
The file contains 1,500,000 rows with tab-separated columns X1–X30 and Y.
It is about 443 MB and is excluded from Git. The data must be available before
running the notebook.

## Run

Use Python 3.12 and create a virtual environment:

    python -m venv .venv

Activate it with the following PowerShell command:

    .venv\Scripts\Activate.ps1

On macOS/Linux, use:

    source .venv/bin/activate

Install the dependencies and register the notebook kernel:

    python -m pip install -r requirements.txt
    python -m pip install ipykernel
    python -m ipykernel install --user --name regression-report --display-name "Regression report"

Open report.ipynb in a notebook editor, select **Regression report**, and run all
cells from top to bottom. For the JupyterLab interface, also install jupyterlab
and launch it with:

    python -m jupyterlab

The notebook reads packages from the selected environment. It does not require
any .analysis-* folder. Analysis package versions are pinned in requirements.txt;
notebook interface packages are installed separately.

## Files to publish

Publish report.ipynb, requirements.txt, README.md, and .gitignore.
The notebook includes the executed results, charts, and numerical checks.
Raw data, local environments, and generated HTML/PDF exports are excluded.
