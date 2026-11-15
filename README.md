# SnapClass AI Attendance Landing Page

SnapClass is a responsive promotional website for an AI-powered classroom attendance product. This repository contains the landing page and its Flask server; the attendance application itself is a separate service linked from the page.

## What the landing page includes

- Product introduction and links to the attendance application
- Feature highlights for face-based attendance, sequential voice identification, and QR-based enrollment
- Teacher and student workflow sections
- Technology overview and product screenshots
- Responsive styling and scroll-reveal effects

## Technology

- Python and Flask serve the page.
- HTML templates are in `templates/`.
- CSS, JavaScript, fonts, logos, and screenshots are in `static/`.
- `requirements.txt` lists the Python dependencies.
- `vercel.json` configures deployment as a Vercel Python application.

  ## Run locally

You need Python installed. From the project root, create and activate a virtual environment, install dependencies, and start the Flask server.

## Windows PowerShell

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python app.py
```

If PowerShell blocks virtual-environment activation, run this in the same terminal and activate again:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\.venv\Scripts\Activate.ps1
```

Open [http://127.0.0.1:5002](http://127.0.0.1:5002) in your browser. Stop the server with **Ctrl+C**.

### macOS or Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python app.py
```

Then open [http://127.0.0.1:5002](http://127.0.0.1:5002).

## Deploy to Vercel

1. Push this repository to GitHub.
2. In Vercel, choose **Add New → Project** and import the GitHub repository.
3. Use the repository root (`./`) as the Root Directory.
4. Vercel can detect the Flask application. If asked to choose a framework, select **Flask** (or **Other** if Flask is not offered).
5. Leave build and output directory overrides empty; `vercel.json` defines the Python app and route.
6. Deploy. Subsequent pushes to the connected branch trigger new deployments.
