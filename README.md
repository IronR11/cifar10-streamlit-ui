# CIFAR-10 Image Classifier (Streamlit UI)

## Overview

This repository contains the **frontend web application** for a CIFAR-10 image classification project. The UI is built using **Streamlit** and communicates with a **FastAPI backend deployed on Render**.

Users can upload an image and receive real-time predictions from a MobileNetV2-based deep learning model.

---

## Live Application

* **Streamlit App URL:** [https://cifar10-app-ui-645uclhwrasvjwwswszule.streamlit.app/](https://cifar10-app-ui-645uclhwrasvjwwswszule.streamlit.app/)

---

## How It Works

```
User uploads image
        ↓
Streamlit UI
        ↓
FastAPI Backend (Render)
        ↓
MobileNetV2 Model (96×96)
        ↓
Prediction + Confidence
```

---

## Important Design Choice

* The Streamlit app **does NOT load the ML model**
* All preprocessing and inference happen on the backend
* Streamlit acts purely as a UI layer

This follows industry best practices for ML deployment.

---

## Backend API

* **Base URL:** [https://cifar10-fastapi-deploy-1.onrender.com](https://cifar10-fastapi-deploy-1.onrender.com)
* **Prediction Endpoint:** `/predict`

---

## Tech Stack

* Python
* Streamlit
* Requests
* Pillow
* Streamlit Community Cloud

---

## File Structure

```
├── app.py
├── requirements.txt
└── README.md
```

---

## Local Run Instructions

```bash
pip install -r requirements.txt
streamlit run app.py
```

Then open:

```
http://localhost:8501
```

---

## Deployment

This app is deployed on **Streamlit Community Cloud** using GitHub integration.

* Laptop does NOT need to stay on
* App may sleep on free tier
* URL remains permanent unless deleted

---

## Example Use Cases

* ML project demo
* Portfolio showcase
* Client-facing prediction UI

---

## Author

Rishav Nagpal
