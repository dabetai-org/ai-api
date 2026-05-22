# dabetai — AI Inference API

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11-3776AB?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/FastAPI-0.95-009688?logo=fastapi&logoColor=white" alt="FastAPI">
  <img src="https://img.shields.io/badge/scikit_learn-1.3-F7931E?logo=scikitlearn&logoColor=white" alt="scikit-learn">
  <img src="https://img.shields.io/badge/PyTorch-2.x-EE4C2C?logo=pytorch&logoColor=white" alt="PyTorch">
  <img src="https://img.shields.io/badge/MongoDB-7.0-47A248?logo=mongodb&logoColor=white" alt="MongoDB">
</p>

<p align="center">
  <em>Dedicated REST API for AI model inference — processing real-time biometric data to deliver risk predictions for diabetes complications.</em>
</p>

<p align="center">
  <a href="https://github.com/dabetai-org/ai-api">Repository</a>
  ·
  <a href="https://github.com/dabetai-org/ai-api/issues">Report Bug</a>
  ·
  <a href="https://chrisssp.vercel.app/assets/docs/papers/Prevenci%C3%B3n-de-Riesgos-de-la-Diabetes-Mediante-una-Plataforma-Inteligente-de-Monitorizaci%C3%B3n-y-Predicci%C3%B3n-de-Complicaciones-con-Inteligencia-Artificial.pdf">Research Paper</a>
</p>

<p align="center">
  <a href="README.md">🇬🇧 English</a> · <a href="README.es.md">🇪🇸 Español</a>
</p>

---

## About dabetai

**dabetai** is a comprehensive preventive ecosystem for diabetes that predicts complications like retinopathy, nephropathy, neuropathy, and diabetic foot before they become irreversible.

This repository contains the **AI Inference API** — a dedicated FastAPI service that exposes trained machine learning models through REST endpoints for real-time risk prediction of:

- Diabetic Retinopathy
- Diabetic Nephropathy
- Diabetic Neuropathy
- Diabetic Foot

### Ecosystem

| Component | Repository | Stack |
|-----------|-----------|-------|
| **AI Inference API** (this) | [dabetai-org/ai-api](https://github.com/dabetai-org/ai-api) | FastAPI, Python 3.11, MongoDB |
| **Mobile App** | [dabetai-org/mobile-app](https://github.com/dabetai-org/mobile-app) | React Native 0.79, Expo 53, Tailwind CSS |
| **Web Portal** | [dabetai-org/web-app](https://github.com/dabetai-org/web-app) | Angular 19, Tailwind CSS |
| **Core API** | [dabetai-org/api](https://github.com/dabetai-org/api) | NestJS 11, PostgreSQL, Prisma |
| **AI Models** | [dabetai-org/ai-models](https://github.com/dabetai-org/ai-models) | Python, scikit-learn, XGBoost, PyTorch |
| **Landing** | [dabetai-org/landing](https://github.com/dabetai-org/landing) | Astro, Tailwind CSS |

## Features

- **Fast Predictions** — REST endpoints for real-time risk scoring
- **Multiple Models** — scikit-learn and PyTorch based predictions
- **Complication Coverage** — Retinopathy, Nephropathy, Neuropathy, Diabetic Foot
- **JSON Responses** — Risk metrics and probability scores
- **Model Validation** — Endpoints for testing and validation

## Quick Start

### Prerequisites

- Python 3.11+
- pip

### Setup

```bash
git clone https://github.com/dabetai-org/ai-api.git
cd ai-api
python -m venv env
source env/bin/activate  # Linux/macOS
pip install -r requirements.txt
```

Run the server:

```bash
uvicorn main:app --reload
```

The API will be available at `http://localhost:8000`

## Architecture

```
┌──────────────────────────────────────────────┐
│            AI Inference API                   │
│               FastAPI                         │
│                                               │
│  ┌─────────┐  ┌─────────┐  ┌──────────────┐ │
│  │  Risk   │  │  Model  │  │  Health      │ │
│  │ Predict │  │  Loader │  │  Check       │ │
│  └────┬────┘  └────┬────┘  └──────┬───────┘ │
│       │            │               │         │
│  ┌────▼────────────▼───────────────▼──────┐  │
│  │         ML Model Registry              │  │
│  │    scikit-learn / PyTorch / XGBoost    │  │
│  └────────────────┬───────────────────────┘  │
└───────────────────┼─────────────────────────┘
                    │ Internal
          ┌─────────┴─────────┐
          ▼                   ▼
┌──────────────┐    ┌──────────────┐
│  MongoDB     │    │  Core API    │
│  (Features)  │    │  (NestJS)    │
└──────────────┘    └──────────────┘
```

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/v1/predict/retinopathy` | Retinopathy risk prediction |
| POST | `/api/v1/predict/nephropathy` | Nephropathy risk prediction |
| POST | `/api/v1/predict/neuropathy` | Neuropathy risk prediction |
| POST | `/api/v1/predict/diabetic-foot` | Diabetic foot risk prediction |
| GET | `/health` | Health check |

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for branch naming, commit conventions, and PR workflow.

## License

This project is licensed under the GNU General Public License v3.0 — see the [LICENSE](LICENSE) file for details.

## Acknowledgments

**Authors:**
- Cardenas Cabal Fermín
- Ortiz Pérez Alejandro — alex03ortizperez@gmail.com
- Serrano Puertos Jorge Christian — christian.serrano.puertos@gmail.com

**Advisors:**
- Guarneros Nolasco Luis Rolando
- Cruz Ramos Nancy Aracely

**Academic Support:**
- Universidad Tecnológica del Centro de Veracruz
