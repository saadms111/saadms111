<p align="center">
  <img src="assets/banner.svg" alt="Saad Mohammed, open to AI, GenAI, ML, Data and MLOps roles" width="100%">
</p>

<p align="center">
  <a href="mailto:saadmdms03@gmail.com"><img src="https://img.shields.io/badge/Email-saadmdms03%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email: saadmdms03@gmail.com"></a>
  <a href="https://github.com/saadms111/Datamind_router"><img src="https://img.shields.io/badge/project-datamind--router-7c8cff?style=flat-square" alt="datamind-router"></a>
  <a href="https://github.com/saadms111/fraud_risk_platform"><img src="https://img.shields.io/badge/project-fraud--risk--platform-4fd1c5?style=flat-square" alt="fraud-risk-platform"></a>
</p>

## About me

I build machine-learning systems end to end, from the data pipeline to the model to the API that serves it, and I benchmark every one against a baseline.

- Every result comes with its **cost, latency and limitations** next to the accuracy.
- I like problems where **engineering decisions change business outcomes**: dollars of fraud caught, or API spend per 1,000 queries.
- Everything I ship has **tests, reproducible runs and a one-command quickstart**.

## Featured projects

<table>
  <tr>
    <td width="50%" valign="top">
      <a href="https://github.com/saadms111/Datamind_router"><img src="assets/card-datamind.svg" alt="datamind-router" width="100%"></a>
    </td>
    <td width="50%" valign="top">
      <a href="https://github.com/saadms111/fraud_risk_platform"><img src="assets/card-fraud.svg" alt="fraud-risk-platform" width="100%"></a>
    </td>
  </tr>
  <tr>
    <td valign="top">

**[datamind-router](https://github.com/saadms111/Datamind_router)**: a Text-to-SQL agent that answers locally and calls Claude only when it has to.

- **Cascade routing:** a LoRA-tuned Qwen2.5-Coder-1.5B (vLLM) answers first. A confidence threshold on mean token logprob decides when to escalate to Claude.
- **Safe by construction:** sqlglot AST guardrails and a read-only SQLite executor. Only the normalized SQL is executed.
- **Honest benchmarks:** a Spider dev subset, scored for execution accuracy, p95 latency and cost per 1,000 queries, with GPU time priced in.
- Ships a **FastMCP server**, so any MCP client can query the databases.

    </td>
    <td valign="top">

**[fraud-risk-platform](https://github.com/saadms111/fraud_risk_platform)**: streaming card-fraud detection, end to end, on a laptop.

- **Exactly-once bronze layer** on top of at-least-once Kafka, with a DLQ and offset-encoded Parquet files.
- **One feature definition** (a dbt macro) shared by training and the real-time API, with a parity test between them.
- **Dollar-cost threshold:** catches 90.5% of fraud *dollars* under a 3% alert-capacity cap.
- **Champion/challenger gate in MLflow** and **drift-triggered retraining** in Airflow (Evidently + PSI). 73 tests.

    </td>
  </tr>
</table>

<details>
<summary><b>datamind-router: accuracy vs cost</b></summary>
<br>

| Run | Accuracy | Cost / 1k queries | Sent to Claude |
|---|---:|---:|---:|
| Claude only | 96% | $2.31 | 50 / 50 |
| Local, LoRA-tuned | 74% | $0.20 | 0 / 50 |
| **Routed, min-confidence -0.10** | **92%** | **$0.98** | 15 / 50 |
| **Routed, min-confidence -0.05** | **98%** | **$1.51** | 26 / 50 |

<img src="https://raw.githubusercontent.com/saadms111/Datamind_router/HEAD/benchmarks/accuracy_vs_cost.png" alt="Accuracy vs cost" width="80%">

</details>

<details>
<summary><b>fraud-risk-platform: model vs rules on a held-out test week</b></summary>
<br>

| 38,576 txns, 362 frauds | XGBoost champion | Rules baseline |
|---|---:|---:|
| Fraud caught (recall) | **81.2%** | 55.0% |
| Precision of alerts | **41.9%** | 22.8% |
| Fraud dollars caught | **90.5%** | 77.4% |
| Expected loss vs approve-all | **−84.3%** | −67.5% |
| PR-AUC / ROC-AUC | 0.736 / 0.958 | n/a |

</details>

## Tech I work with

**ML & LLMs**<br>
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch">
<img src="https://img.shields.io/badge/XGBoost-1F6FEB?style=for-the-badge" alt="XGBoost">
<img src="https://img.shields.io/badge/Optuna-2C5BB4?style=for-the-badge" alt="Optuna">
<img src="https://img.shields.io/badge/LoRA%20%2F%20PEFT-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="LoRA / PEFT">
<img src="https://img.shields.io/badge/vLLM-30A2FF?style=for-the-badge" alt="vLLM">
<img src="https://img.shields.io/badge/Claude%20API-D97757?style=for-the-badge&logo=anthropic&logoColor=white" alt="Claude API">
<img src="https://img.shields.io/badge/SHAP-8A2BE2?style=for-the-badge" alt="SHAP">

**Data engineering**<br>
<img src="https://img.shields.io/badge/Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white" alt="Kafka">
<img src="https://img.shields.io/badge/dbt-FF694B?style=for-the-badge&logo=dbt&logoColor=white" alt="dbt">
<img src="https://img.shields.io/badge/DuckDB-FFF000?style=for-the-badge&logo=duckdb&logoColor=black" alt="DuckDB">
<img src="https://img.shields.io/badge/Airflow-017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white" alt="Airflow">
<img src="https://img.shields.io/badge/Great%20Expectations-FF6310?style=for-the-badge" alt="Great Expectations">
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">

**MLOps & serving**<br>
<img src="https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white" alt="MLflow">
<img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI">
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
<img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white" alt="Prometheus">
<img src="https://img.shields.io/badge/Evidently-4B0082?style=for-the-badge" alt="Evidently">
<img src="https://img.shields.io/badge/MCP-111111?style=for-the-badge" alt="MCP">

**Languages**<br>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/SQL-336791?style=for-the-badge" alt="SQL">

## How I work

> **Measure against a baseline.** Claude-only for the router and a rules engine for fraud, so every gain has something to be compared to.
>
> **Write down the limitations.** Small samples, synthetic data and latency trade-offs are written up in each README, not hidden.
>
> **Make it reproducible.** One command per pipeline stage, pinned configs and results committed next to the code.

## Let's talk

I'm **open to AI Engineer, GenAI / LLM Engineer, ML Engineer, Data Engineer, MLOps Engineer and Data Scientist roles**.

📫 **[saadmdms03@gmail.com](mailto:saadmdms03@gmail.com)**
