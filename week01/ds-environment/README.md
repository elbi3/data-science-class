Assignment: Creating and Documenting a Modern Python Project with `uv`

1. Why is it important to isolate different data science projects from each other instead of installing all Python packages globally on your machine?

2. In this modern setup, you did not have to write a requirements.txt file or run an activation script (like source bin/activate). Explain how `uv` tracks and handles your environment packages automatically.

3. Open the `pyproject.toml` file. What is the purpose of this file in a collaborative environment? If you shared your project folder with a colleague, how does this file help them?

4. Look at the `uv.lock` file that was generated. How does a lockfile differ from your pyproject.toml file, and why is a lockfile critical for absolute data science reproducibility?

5. `uv` is significantly faster than traditional package managers due to its global cache. Why are tool speed and workflow efficiency important when managing code environments in a professional engineering environment?