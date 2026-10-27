1. Run command `uv init coffee-cleaning` to scaffold a native project. 
2. In `coffee-cleaning` directory, add libraries with `uv add pandas matplotlib notebook` (they show up in the `pyproject.toml` file this way)
3. Create a new file `coffee_cleaning_analysis.ipynb`
4. With notebook file open, select kernel (Ctrl+shift+p, enter the path to `your-project/.venv/bin/python`)
5. Add the 3 csv file datasets from last week
6. Load the datasets
7. Inspect the data with `.shape` and `.dtypes`