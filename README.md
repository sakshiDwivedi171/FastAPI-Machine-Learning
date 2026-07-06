# FastAPI - 

A small FastAPI project that demonstrates serving a machine learning model and simple patient data management. This repository includes the FastAPI app (`main.py`) and a sample `patient.json` data file.

## Features
- FastAPI application entrypoint: `main.py`
- Example patient dataset: `patient.json`
- Development server using `uvicorn`

## Prerequisites
- Python 3.8+ (use the Windows `py` launcher if `python` is not on PATH)
- `pip` for installing packages

## Setup (recommended)
From the project root (`fastAPI_1`) run:

```powershell
py -m venv myenv
.\myenv\Scripts\Activate
pip install -r requirements.txt
```

If you do not have a `requirements.txt`, install the core packages:

```powershell
pip install fastapi uvicorn pydantic-core
```

Note: The repository originally placed `patient.json` inside the `myenv` folder. Keep project data files outside the virtual environment (move `myenv\patient.json` to the project root `patient.json`) so they are not removed if the environment is recreated.

## Run the app
From the project root with the virtual environment activated:

```powershell
uvicorn main:app --reload
```

If `uvicorn` is not found, run via the Python module:

```powershell
py -m uvicorn main:app --reload
```

Open http://127.0.0.1:8000 in your browser (or check `/docs` for the automatic API docs).

## Project structure

- `main.py` - FastAPI application entrypoint
- `patient.json` - Example patient data (move to repo root if currently inside `myenv`)
- `myenv/` - Python virtual environment (ignored by `.gitignore`)
- `.gitignore` - Git ignore rules

## Git / Collaboration
If you need to push this repository to GitHub (first time):

```powershell
git init
git remote add origin https://github.com/<your-username>/<repo>.git
git branch -M main
git add README.md main.py patient.json
git commit -m "Initial project files"
git push -u origin main
```

If your push is rejected because the remote has commits, fetch and rebase first:

```powershell
git fetch origin
git pull --rebase origin main
git push origin main
```

## Contributing
Open an issue or create a pull request. Please keep model/data files small and add a `requirements.txt` when you add new dependencies.

## License
Choose a license for your project (for example MIT) and add a `LICENSE` file if you plan to share the repository publicly.

---
If you'd like, I can also:
- move `patient.json` out of `myenv` for you,
- create `requirements.txt` from the currently installed packages, or
- commit the README and push the change to your GitHub remote.
