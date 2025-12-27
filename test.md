
<h1 align="center">⚡ Learn UV — Fast & Practical</h1>

<p align="center">
  <b>Install Python, manage environments, handle dependencies, and ship projects — all with UV.</b><br>
  <i>A modern Python workflow inspired by tools like npm and pnpm.</i>
  
</p>
<p align="center">
  <a href="https://astral.sh/uv"><img src="https://img.shields.io/badge/Built%20with-UV-0b3d91?style=for-the-badge&logo=python&logoColor=yellow" alt="Built with UV"></a>
  <a href="https://github.com/astral-sh/uv"><img src="https://img.shields.io/badge/Project-Astral-blue?style=for-the-badge&logo=github"></a>
</p>

---

## 🧠 What is UV?

**UV** is a high-performance Python project and package manager built by **Astral**.  
It replaces multiple tools by combining them into **one fast, clean CLI**.

UV handles:
- Python versions
- Virtual environments
- Dependencies
- Lock files
- Running commands

👉 **One tool instead of five.**

---

## 🧠 Analogy: UV vs Traditional Python Tools

### Traditional Python (Old Way)
Like managing a server with many tools:
- `pyenv` → install Python
- `venv` → create environments
- `pip` → install packages
- `pip-tools` → lock dependencies
- `make` / scripts → run commands

⚠️ Powerful, but fragmented.

---

### UV (Modern Way)
Like **npm / pnpm for Python**:
- One CLI
- One config file
- One workflow

> **If you know Node.js package managers, UV will feel familiar immediately.**

---

## 🧠 Vim Analogy (Mental Model)

Think of **UV like Vim**:

- Vim doesn’t try to be flashy
- It focuses on **speed and precision**
- One tool, many workflows
- Extremely fast once you learn it

> **UV is Vim for Python environments**  
> Minimal, fast, and designed for serious developers.

---

## ✨ Why UV?

- ⚡ Extremely fast installs (written in Rust)
- 🧩 Manages Python versions + environments together
- 🔧 Zero-config workflows
- 🧰 Works on macOS, Linux, and Windows

---

## 🚀 Installation

### 🐧 macOS & Linux
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
````

### 🪟 Windows (PowerShell)

```powershell
iwr https://astral.sh/uv/install.ps1 -UseBasicParsing | iex
```

```
### ✅ Verify

```bash             
uv --version
```

💡 If `uv` is not found, open a new terminal or update your `PATH`.

---

## 🐍 Managing Python Versions (Like `nvm`)

```basha
uv python list
uv python install 3.12
uv python run -p 3.12
```

🧠 **Analogy**

* `nvm install 18` → Node
* `uv python install 3.12` → Python

No need for `pyenv` or `conda`.

---

## 🏗️ Start a New Project

```bash
mkdir hello-uv
cd hello-uv
uv init
```

This creates:

* `pyproject.toml`
* A clean project workspace

🧠 **Analogy**

> `npm init` → Node
> `uv init` → Python

---

## 🌱 Virtual Environments (Automatic)

```bash
uv venv
uv sync
```

* `.venv` is created automatically
* Dependencies are installed safely

> You don’t need to activate environments manually —
> **UV handles it for you.**

---

## 📦 Add Dependencies

```bash
uv add requests
uv add fastapi uvicorn
```

🧠 **Node.js analogy**

```bash
npm install express
```

Same idea, cleaner execution.

---

## ▶️ Run Code (Like `npm run`)

```bash
uv run python main.py
```

UV ensures:

* Correct Python version
* Correct environment
* Correct dependencies

No activation required.

---

## 🧾 Define Scripts (Like npm scripts)

In `pyproject.toml`:

```toml
[tool.uv.scripts]
start = "python -m hello_uv"
```

Run it with:

```bash
uv run start
```

🧠 **Analogy**

> `npm run dev`
> `uv run start`

---

## 🔒 Locking & Reproducibility

```bash
uv lock
uv sync
```

* Locks exact dependency versions
* Guarantees same environment everywhere

Export for non-UV users:

```bash
uv export -o requirements.txt
```

---

## 🧭 Cheat Sheet

| Category | Command                   | Purpose             |
| -------- | ------------------------- | ------------------- |
| Project  | `uv init`                 | Initialize project  |
|          | `uv add <pkg>`            | Add dependency      |
|          | `uv sync`                 | Install deps        |
| Python   | `uv python list`          | List versions       |
|          | `uv python install <ver>` | Install Python      |
| Env      | `uv venv`                 | Create venv         |
|          | `uv run <cmd>`            | Run command         |
| Inspect  | `uv tree`                 | Dependency tree     |
|          | `uv cache clean`          | Clean cache         |
| Export   | `uv export`               | Export requirements |

---

## 🩺 Troubleshooting

| Issue                   | Solution                          |
| ----------------------- | --------------------------------- |
| `uv: command not found` | Open new terminal / fix PATH      |
| Network / SSL errors    | Retry or configure proxy          |
| Build errors            | Install compiler & Python headers |

---

## 🎓 Final Teaching One-Liner

> **UV brings Python development to the same modern level as npm did for Node.js.**

---

