# brainCodeCamp

This repository contains the source code for the Brain Code Camp learning website. It is built using Jupyter Book (version 1, as opposed to the latest version).

## Build Instructions 

### Option 1: Pixi (Recommended)

    # install pixi https://pixi.sh/latest/getting-started/
    pixi install
    pixi shell
    jupyter-book clean .
    jupyter-book build .

### Option 2: Pip (Using virtual environment is highly recommended)

    # using python >=3.10
    pip install jupyter-book==1.0.3
    jupyter-book clean .
    jupyter-book build .

## Test Locally

### Option 1: Using Pixi (Recommended)
From the project root, run:
```bash
pixi run serve
```

### Option 2: VS Code Live Server
1. Change directory in VS Code to `_build/html`
   ```bash
   cd _build/html
   code .
   ```
2. Right click `index.html` and select **Open with Live Server**
