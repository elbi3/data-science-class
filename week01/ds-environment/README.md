# Assignment: Creating and Documenting a Modern Python Project with `uv`
## questions
1. Why is it important to isolate different data science projects from each other instead of installing all Python packages globally on your machine?

In the field of Data Science, it is important that we be able to reproduce the same results. Project isolation removes many additional variables. It allows us to draw conclusions about datasets in a tightly-controlled environment that is independent from other work products, experiments, and research. There are times when a project may require different or unexpected versions of particular libraries and tools. We rely on dependency declaration and isolation.

2. In this modern setup, you did not have to write a `requirements.txt` file or run an activation script (like source bin/activate). Explain how `uv` tracks and handles your environment packages automatically.
The tool `uv` is a package manager. It creates a virtual environment for you and creates a `.venv` if you don't have it. It takes advantage of "global cache" so that the user can avoid re-downloading. The command `uv add` automatically updates dependencies in `pyproject.toml` and generates the `uv.lock` record for reproducibiliy.

3. Open the `pyproject.toml` file. What is the purpose of this file in a collaborative environment? If you shared your project folder with a colleague, how does this file help them?
This file contains "top-level dependencies". It allows another person to reproduce the project's environment so they may run the same program and get the same results. It typically defines the build backend and its dependencies, stores the project's metadata, and provides configuration for dev tooling. It is spiritually a replacement for `setup.py`.

4. Look at the `uv.lock` file that was generated. How does a lockfile differ from your `pyproject.toml file`, and why is a lockfile critical for absolute data science reproducibility?
The `uv.lock` file saves the project's state so that a user can have 100% reproducibility. It is similar to the `package-lock.json` habit in `npm` handling with Node & JavaScript. the `.toml` file is where we define direct dependencies. You can manually edit this. The `uv.lock` is more specific than the `.toml` file. It pins the exact dependenies as well as their sub-dependencies. This file is managed by `uv`.

5. `uv` is significantly faster than traditional package managers due to its global cache. Why are tool speed and workflow efficiency important when managing code environments in a professional engineering environment?
`uv` is fast because it is written in Rust. Tool and workflow efficiency are important because an optimal workflow can create more room for the developer to do more work. In an ideal situation the developer can spend more time doing analysis with fast setup and avoid putting a lot of time into their tooling and environment. It's too bad that OpenAI acquired Astral though, it makes tools like `uv` less agnostic. Some have noticed trends where certain software solutions get a lot of attention when a particular LLM is preoccupied with it (I noticed this with Hono, an Express.js alternative). OpenAI might end up being the driving force behind "what's relevant" in Python tooling, instead of community users.

## references
https://pydevtools.com/handbook/reference/pyproject.toml/
https://pydevtools.com/handbook/explanation/uv-complete-guide/