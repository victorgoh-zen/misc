# Repo template for local workloads

You can follow below instructions to run files from both locally (for git functionality) and databricks' web UI.

# Usage Instructions

1. Install databricks CLI

`curl -fsSL https://raw.githubusercontent.com/databricks/setup-cli/main/install.sh | sh`

2. Setup local databricks profile (or edit .databrickscfg)

`databricks auth login --configure-cluster --host <host url eg. adb-3409994944177186.6.azuredatabricks.net>`

Once profile is set up, use the following command to specify particular cluster profiles from your .databrickscfg

`databricks auth login https://adb-3409994944177186.6.azuredatabricks.net/ -p default`

3. Install UV 

`curl -LsSf https://astral.sh/uv/install.sh | sh`

4. Initialise pyproject.toml with `$ uv init` or proceed to create virtual environment using existing pyproject.toml via `$ uv venv`

5. `uv add <packages>` as you need or by editing the pyproject.toml, preferably start with the pyproject.toml from this repository for the default cluster

6. `uv sync`

7. Start working on a jupyter notebook with the starting cell as shown in [example](notebooks/example.ipynb)