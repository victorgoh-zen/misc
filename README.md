# Repo for random workloads

Run files locally or via databricks UI

# Usage Instructions

1. Install databricks CLI

`curl -fsSL https://raw.githubusercontent.com/databricks/setup-cli/main/install.sh | sh`

2. Setup local databricks profile (or edit .databrickscfg)

`$ databricks auth login --configure-cluster --host <host url eg. adb-3409994944177186.6.azuredatabricks.net>`

Once profile is set up, use the following command to specify particular cluster profiles

`$ databricks auth login https://adb-3409994944177186.6.azuredatabricks.net/ -p default`

3. Install UV 

`$ curl -LsSf https://astral.sh/uv/install.sh | sh`

4. initialise pyproject.toml with `$ uv init` or proceed to create virtual environment using existing pyproject.toml via `$ uv venv`

5. `$ uv add <packages>` as you need or edit the pyproject.toml
6. `$ uv sync`