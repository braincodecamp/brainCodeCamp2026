# brainCodeCamp

This repository contains the source code for the Brain Code Camp learning website. It is built using Jupyter Book (version 1, as opposed to the latest version).

## Build Instructions 

### Option 1: Pixi (Recommended)

    # install pixi https://pixi.sh/latest/getting-started/
    pixi install
    pixi run clean
    pixi run build

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
Then, go to a web browser and open http://localhost:8080.

### Option 2: VS Code Live Server
1. Change directory in VS Code to `_build/html`
   ```bash
   cd _build/html
   code .
   ```
2. Right click `index.html` and select **Open with Live Server**


# Firebase Deployment Guide

This guide describes how to deploy the Jupyter Book website to Firebase Hosting.

## Prerequisites

1.  **Firebase CLI**: Install it globally using npm:
    ```bash
    npm install -g firebase-tools
    ```
2.  **Firebase Account**: Sign up at [firebase.google.com](https://firebase.google.com/).

## Step 1: Create a Firebase Project

1.  Go to the [Firebase Console](https://console.firebase.google.com/).
2.  Click **Add project** and name it `course2026-braincodecamp` (or your preferred ID).
3.  Once created, go to the lower left part of the sidebar, there will be a small arrow. Click it to expand the menu. Then click **Hosting & Serveless > Hosting**.
4.  Follow the wizard until you see the Hosting dashboard.

## Step 2: Initialize Firebase Locally

In your terminal, run the following commands:

1.  **Login to Firebase**:
    ```bash
    firebase login
    ```
2.  **Initialize Hosting**:
    ```bash
    firebase init hosting
    ```
    - Select **"Use an existing project"** and choose your project.
    - Public directory: `_build/html` (The `firebase.json` is already configured for this).
    - Configure as a single-page app: **n**.
    - Set up automatic builds and deploys with GitHub: **n**.

## Step 3: Build and Deploy

Now you can use the `pixi` tasks to manage your site:

1.  **Clean the Build** (Optional):
    ```bash
    pixi run clean
    ```
2.  **Build the Book**:
    ```bash
    pixi run build
    ```
3.  **Deploy to Firebase**:
    ```bash
    pixi run deploy
    ```

The website will be live at `https://course2026-braincodecamp.web.app`.
