<h1 align="center">⚡ Learn UV Fast</h1>

<p align="center">
  <b>Install, set up a project, manage environments, and ship — all with UV.</b><br>
  <i>Built with ❤️ using Astral’s ultra-fast Python project manager.</i>
</p>

<p align="center">
  <a href="https://astral.sh/uv"><img src="https://img.shields.io/badge/Built%20with-UV-0b3d91?style=for-the-badge&logo=python&logoColor=yellow" alt="Built with UV"></a>
  <a href="https://github.com/astral-sh/uv"><img src="https://img.shields.io/badge/Project-Astral-blue?style=for-the-badge&logo=github"></a>
  <a href="https://python.org"><img src="https://img.shields.io/badge/Python-3.11%2B-green?style=for-the-badge&logo=python&logoColor=white"></a>
</p>


## 🧠 What is UV?

**UV** is a blazing-fast Python package and project manager by [Astral](https://astral.sh).  
It unifies **Python installation**, **virtual environments**, **dependency management**, and **task running** — all in one sleek CLI tool.

### ✨ Features
- ⚡ **Ultra-fast** installs and dependency resolution  
- 🧩 **Manages Python versions and environments together**  
- 🔧 **Drop-in commands** for everyday workflows  
- 🧰 **Cross-platform** (macOS, Linux, Windows)



## 🚀 Installation

### 🐧 macOS & Linux
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
````

### 🪟 Windows (PowerShell)

```powershell
iwr https://astral.sh/uv/install.ps1 -UseBasicParsing | iex
```

### ✅ Verify Installation

```bash
uv --version
```



💡 If `uv` isn’t found, open a new terminal or add UV’s bin path to your `PATH`.



## 🐍 Manage Python Versions

```bash
uv python list               
uv python install 3.12      
uv python run -p 3.12 python --version
```



UV manages Python itself, so no need for `pyenv` or `conda`!

## 🏗️ Start a New Project


mkdir hello-uv && cd hello-uv
uv init


This creates a `pyproject.toml` and initializes your workspace.

uv venv          # create .venv
uv sync          # lock and install dependencies


## 📦 Add Dependencies


uv add requests
uv add fastapi uvicorn


View dependency tree:

uv tree


## ▶️ Run Code & Tools

UV runs commands in the correct virtual environment automatically.


uv run python main.py



### Define Scripts in `pyproject.toml`


[tool.uv.scripts]
start = "python -m hello_uv"


Then run:

uv run start



## 🔒 Locking & Reproducibility

uv lock
uv sync


Export requirements for non-UV tools:


uv export -o requirements.txt



## 🌱 Virtual Environments


uv venv
uv venv --python 3.11



## 🧭 Cheat Sheet

| 🧩 Category | 🔧 Command                      | 📝 Description       |
| ----------- | ------------------------------- | -------------------- |
| **Project** | `uv init`                       | Initialize project   |
|             | `uv add <pkg>`                  | Add dependency       |
|             | `uv sync [--frozen]`            | Sync dependencies    |
| **Python**  | `uv python list`                | List interpreters    |
|             | `uv python install <ver>`       | Install Python       |
| **Env**     | `uv venv`                       | Create virtualenv    |
|             | `uv run <cmd>`                  | Run command in env   |
| **Inspect** | `uv tree`                       | Show dependency tree |
|             | `uv cache clean`                | Clear cache          |
| **Export**  | `uv export -o requirements.txt` | Export requirements  |

---

## 🩺 Troubleshooting

| ⚠️ Issue                | 💡 Solution                                  |
| ----------------------- | -------------------------------------------- |
| `uv: command not found` | Open new shell or add to PATH                |
| SSL / network errors    | Retry with stable connection or proxy config |
| Build failures          | Install compiler tools and Python headers    |








