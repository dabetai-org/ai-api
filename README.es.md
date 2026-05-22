# dabetai — API de Inferencia IA

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11-3776AB?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/FastAPI-0.95-009688?logo=fastapi&logoColor=white" alt="FastAPI">
  <img src="https://img.shields.io/badge/scikit_learn-1.3-F7931E?logo=scikitlearn&logoColor=white" alt="scikit-learn">
  <img src="https://img.shields.io/badge/PyTorch-2.x-EE4C2C?logo=pytorch&logoColor=white" alt="PyTorch">
  <img src="https://img.shields.io/badge/MongoDB-7.0-47A248?logo=mongodb&logoColor=white" alt="MongoDB">
</p>

<p align="center">
  <em>API REST dedicada para inferencia de modelos IA — procesa datos biométricos en tiempo real para entregar predicciones de riesgo de complicaciones diabéticas.</em>
</p>

<p align="center">
  <a href="https://github.com/dabetai-org/ai-api">Repositorio</a>
  ·
  <a href="https://github.com/dabetai-org/ai-api/issues">Reportar Bug</a>
  ·
  <a href="https://chrisssp.vercel.app/assets/docs/papers/Prevenci%C3%B3n-de-Riesgos-de-la-Diabetes-Mediante-una-Plataforma-Inteligente-de-Monitorizaci%C3%B3n-y-Predicci%C3%B3n-de-Complicaciones-con-Inteligencia-Artificial.pdf">Artículo de Investigación</a>
</p>

<p align="center">
  <a href="README.md">🇬🇧 English</a> · <a href="README.es.md">🇪🇸 Español</a>
</p>

---

## Acerca de dabetai

**dabetai** es un ecosistema preventivo integral para la diabetes que predice complicaciones como retinopatía, nefropatía, neuropatía y pie diabético antes de que sean irreversibles.

Este repositorio contiene la **API de Inferencia IA** — un servicio FastAPI dedicado que expone modelos de machine learning entrenados a través de endpoints REST para predicción de riesgo en tiempo real de:

- Retinopatía diabética
- Nefropatía diabética
- Neuropatía diabética
- Pie diabético

### Ecosistema

| Componente | Repositorio | Stack |
|-----------|-----------|-------|
| **API de Inferencia IA** (este) | [dabetai-org/ai-api](https://github.com/dabetai-org/ai-api) | FastAPI, Python 3.11, MongoDB |
| **App Móvil** | [dabetai-org/mobile-app](https://github.com/dabetai-org/mobile-app) | React Native 0.79, Expo 53, Tailwind CSS |
| **Portal Web** | [dabetai-org/web-app](https://github.com/dabetai-org/web-app) | Angular 19, Tailwind CSS |
| **Core API** | [dabetai-org/api](https://github.com/dabetai-org/api) | NestJS 11, PostgreSQL, Prisma |
| **Modelos IA** | [dabetai-org/ai-models](https://github.com/dabetai-org/ai-models) | Python, scikit-learn, XGBoost, PyTorch |
| **Landing** | [dabetai-org/landing](https://github.com/dabetai-org/landing) | Astro, Tailwind CSS |

## Funcionalidades

- **Predicciones Rápidas** — Endpoints REST para puntuación de riesgo en tiempo real
- **Múltiples Modelos** — Predicciones basadas en scikit-learn y PyTorch
- **Cobertura de Complicaciones** — Retinopatía, Nefropatía, Neuropatía, Pie Diabético
- **Respuestas JSON** — Métricas de riesgo y probabilidades
- **Validación de Modelos** — Endpoints para pruebas y validación

## Inicio rápido

### Prerrequisitos

- Python 3.11+
- pip

### Instalación

```bash
git clone https://github.com/dabetai-org/ai-api.git
cd ai-api
python -m venv env
source env/bin/activate  # Linux/macOS
pip install -r requirements.txt
```

Ejecuta el servidor:

```bash
uvicorn main:app --reload
```

La API estará disponible en `http://localhost:8000`

## Endpoints de la API

| Método | Endpoint | Descripción |
|--------|----------|-------------|
| POST | `/api/v1/predict/retinopathy` | Predicción de riesgo de retinopatía |
| POST | `/api/v1/predict/nephropathy` | Predicción de riesgo de nefropatía |
| POST | `/api/v1/predict/neuropathy` | Predicción de riesgo de neuropatía |
| POST | `/api/v1/predict/diabetic-foot` | Predicción de riesgo de pie diabético |
| GET | `/health` | Health check |

## Contribuciones

Por favor lee [CONTRIBUTING.md](CONTRIBUTING.md) para nuestras convenciones de ramas, commits y flujo de PRs.

## Licencia

Este proyecto está licenciado bajo GNU General Public License v3.0 — consulta el archivo [LICENSE](LICENSE) para más detalles.

## Reconocimientos

**Autores:**
- Cardenas Cabal Fermín
- Ortiz Pérez Alejandro — alex03ortizperez@gmail.com
- Serrano Puertos Jorge Christian — christian.serrano.puertos@gmail.com

**Asesores:**
- Guarneros Nolasco Luis Rolando
- Cruz Ramos Nancy Aracely

**Apoyo Académico:**
- Universidad Tecnológica del Centro de Veracruz
