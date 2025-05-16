# TensorFlow Environment Setup with Conda

## Step-by-Step Instructions

### 1. Create a New Conda Environment

Create a new environment named `tf` with Python 3.10:

    conda create --name tf python=3.10

### 2. Activate the Environment

    conda activate tf

### 3. Install CUDA Toolkit and cuDNN

Install the required versions for GPU support via conda-forge:

    conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1.0

### 4. Upgrade pip

    python.exe -m pip install --upgrade pip

### 5. Install TensorFlow and Dependencies

Install TensorFlow 2.10:

    pip install tensorflow==2.10

Install a specific version of NumPy:

    pip install numpy==1.26.4

### 6. Install Flask and Flask-CORS

    pip install Flask flask-cors

### 7. Install Jupyter Notebook

    conda install anaconda::jupyter

### 8. Install charset-normalizer (from conda-forge)

    conda install -c conda-forge charset-normalizer

# Integrating Backend with Frontend using Ngrok

## Step 1: Download Ngrok

1. Go to the [Ngrok Downloads page](https://ngrok.com/downloads/windows)
2. Download and install the Windows version of Ngrok.

## Step 2: Create a Ngrok Account

1. Visit [Ngrok Sign Up](https://dashboard.ngrok.com/signup)
2. Create a new account and log in.
3. After logging in, copy your **auth token** from the dashboard.

## Step 3: Authenticate Ngrok

Open your terminal (e.g., Command Prompt or PowerShell) and run:

    ngrok config add-authtoken <your_auth_token>

Replace `<your_auth_token>` with the actual token you copied from your Ngrok dashboard.

## Step 4: Start Ngrok Tunnel

Run the following command in terminal:

    ngrok http 5000

Ngrok will generate a **Forwarding URL** (e.g., `https://abc123.ngrok.io`).

## Step 5: Start Your Backend Server

Navigate to your backend project directory and run:

    python app.py

Ensure the backend is running on port **5000**.

## 🔗 Step 6: Use Ngrok URL in Frontend

1. Go to: [https://milkysin.github.io/MachineLearningFrontend/](https://milkysin.github.io/MachineLearningFrontend/)
2. Right-click and select **Inspect**
3. Go to the **Sources** tab.
4. Find and click on **`app.js`**
5. Locate the `fetch` function that contains the backend URL.
6. Replace the old URL with your **Ngrok Forwarding URL**, e.g.:

    ```javascript
    fetch("{REPLACE_HERE}/endpoint", {
        method: "POST",
        headers: {
            "Content-Type": "application/json",
        },
        body: JSON.stringify(data),
    });
    ```
