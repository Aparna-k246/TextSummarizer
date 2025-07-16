# 🧾 TextSummarizer — End-to-End NLP Project with MLOps + APIs + Hugging Face 🤗

A complete end-to-end **Text Summarization** ML pipeline using 🧠 Transformer models (Pegasus), 🧰 MLOps principles, and 🛰️ API deployment.

---

## 🚀 Features

- 📦 Data Ingestion (local/file-based)
- 🔧 Data Transformation (tokenization, formatting)
- 🧠 Model Training (Pegasus from Hugging Face 🤗)
- 🧪 Model Evaluation (BLEU/Rouge)
- 🛠️ Training + Prediction Pipelines
- 🌐 REST API with FastAPI
- 🐳 Dockerized
- ☁️ Workflow Automation (CI/CD ready)
- 📊 Frontend-ready structure

---

## 🔄 Workflows

CI/CD & automation enabled via GitHub Actions:

```bash
.github/workflows/
└── main.yaml  # 🔁 Auto tests + linting
```

---

## ⚙️ Configuration Files

```bash
config/
├── config.yaml         # ✅ Central project config (paths, dirs)
params.yaml             # ⚙️ Hyperparameters (epochs, batch_size, etc.)
```

---

## 📦 Configuration Entity & Manager

- `ModelTrainerConfig`, `DataIngestionConfig`, etc. defined in 🧠 `textSummarizer.entity`
- `ConfigurationManager` reads YAML and prepares configs dynamically

---

## 🧩 Components

Modularized under `textSummarizer/components/`:

- 📥 `data_ingestion.py`
- 🧽 `data_transformation.py`
- 🤖 `model_trainer.py`
- 📈 `model_evaluation.py`

---

## 🧬 Training & Prediction Pipelines

```bash
src/textSummarizer/pipeline/
├── stage_1_data_ingestion_pipeline.py
├── stage_2_data_transformation_pipeline.py
├── stage_3_model_trainer_pipeline.py
├── stage_4_model_evaluation.py
├── prediction_pipeline.py
```

---

## 🌐 Frontend & API Support

- `main.py` — Main FastAPI app
- `app.py` — Entry point for web interface
- API endpoints:
  - 🏋️ `/train` → triggers training pipeline
  - 🔮 `/predict` → summary prediction
  - 📂 `/batch_predict` → batch inference

---

## 🤗 Powered by Hugging Face Transformers

This project uses the 🤗 [Hugging Face Transformers](https://huggingface.co/docs/transformers/index) library with:

- `AutoModelForSeq2SeqLM` – loads Pegasus
- `AutoTokenizer` – tokenizer for Pegasus
- 📦 Model checkpoint: `google/pegasus-cnn_dailymail`

---

## 📁 Folder Structure

```bash
.
├── .github/
│   └── workflows/
│       └── main.yaml
├── config/
│   └── config.yaml
├── src/textSummarizer/
│   ├── components/
│   ├── config/
│   ├── constants/
│   ├── entity/
│   ├── logging/
│   ├── pipeline/
│   ├── utils/
├── research/                         # 📊 Jupyter notebooks
├── app.py                            # 🌐 FastAPI UI
├── main.py                           # 🚀 FastAPI runner
├── params.yaml
├── requirements.txt
├── Dockerfile
└── README.md
```

---

## 🧪 How to Run

1. 🔨 Install dependencies:

```bash
pip install -r requirements.txt
```

2. 🚀 Train the model:

```bash
python main.py
```

3. 🌐 Run the API locally:

```bash
uvicorn app:app --reload
```

4. 🐳 (Optional) Run with Docker:

```bash
docker build -t textsummarizer .
docker run -p 8080:8080 textsummarizer
```

---

## 🧑‍💼 For Recruiters

This project demonstrates real-world end-to-end skills:

✅ Clean modular code with separation of concerns  
✅ MLOps principles (configs, pipelines, automation)  
✅ Hugging Face 🤗 integration for production NLP  
✅ FastAPI backend with custom endpoints  
✅ Docker support for containerized deployment  
✅ CI-ready structure for scalable development  
✅ Project structure that reflects production readiness  

Please feel free to reach out for walkthroughs or codebase clarity!

---

## 📌 To-Do

- [ ] Add Streamlit frontend
- [ ] Add monitoring/alerts (Prometheus/Grafana)
- [ ] Add model versioning with MLflow

---

## 📄 License

[MIT License](LICENSE)

---

## ✨ Star this repo if it helped you!
