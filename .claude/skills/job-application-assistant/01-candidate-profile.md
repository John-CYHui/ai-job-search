---
framework_version: 1.0.0
---

# Candidate Profile

## Identity
- **Name:** John Hui
- **Location:** Hong Kong S.A.R.
- **Phone:** +852 9794 4075 (English CV) | (+86) 137 6312 6161 (Chinese CVs)
- **Email:** johnsonhcy@gmail.com
- **LinkedIn:** linkedin.com/in/john-hui-51abb2105/
- **GitHub:** [not yet provided]
- **Languages:** Cantonese (native), English (fluent), Mandarin (fluent)
- **Status:** Employed — Associate Data Scientist at OOCL (actively seeking new opportunities)
- **Constraints:** Based in Hong Kong S.A.R. Open to Singapore and mainland China (Shanghai / Shenzhen / Beijing). No other relocation.

## Education

| Degree | Period | Institution | Key Topics |
|--------|--------|-------------|------------|
| MSc, Data Science and Analytics | Sep 2020 – Nov 2022 | The Hong Kong Polytechnic University (QS 54) | Deep Learning, Introduction to AI, Optimization Methods, Statistical Data Mining, High Dimensional Data Analysis, Big Data Computing, Data Structure and Database Design |
| Bachelor's, Engineering | Sep 2013 – Jun 2017 | University of Toronto (QS 29) | Calculus, Statistics, Linear Algebra, Control Theory, Python Programming, Differential Equations, Algorithm and Data Structure |

## Professional Experience

### Associate Data Scientist — Orient Overseas Container Line (OOCL) (Sep 2022 – Present)
Hong Kong S.A.R. | OOCL is a subsidiary of COSCO Shipping (China Ocean Shipping Group)

- Designing multi-agent workflow with LangGraph (ReAct, Reflection, Memory mechanisms) to automate MySQL SRE root cause analysis with auto early-alert discovery and reasoning
- Deployed LSTM log anomaly detection system across 7,000+ CISCO network devices; achieved 82% alarm recall rate, detecting 2+ Level 1 incidents monthly on average
- Built RAG Q&A system for network device logs with LoRA and DPO fine-tuning on Qwen2.5-7B using SRE operational data; deployed with Ollama + AnythingLLM
- Deployed XGBoost microservice for time-series anomaly detection across 750 MySQL databases, 3,300 K8s cluster microservices, and 2,600 OS machines
- Built GPT-3.5 code translation app (XML→Java) for migration of 20,000+ TIBCO scripts; reduced translation time from 16,000h to 600h (70%+ success rate, 63% efficiency gain)
- Built LGBM model for 8-week empty container demand forecasting at global ports; achieved 40% WMAPE via feature engineering and ablation study

**Additional metrics (from Chinese CVs — verify before using in applications):**
- Enterprise Agent Harness SDK (2026): led design of core platform architecture with RuntimePort protocol abstraction, Deferred Tool Registry for 100+ tools (on-demand activation via tool_search), local reverse HTTP proxy for per-agent credential isolation (Bearer / OAuth2 / Keycloak, zero-restart rotation), Config-driven zero-code agent creation (agent.yaml + Pydantic discriminated union types); platform supported 20+ agent projects within 2 months
- Multi-agent AIOps RCA platform (2025–2026): Supervisor-Worker routing, Durable Incident Runtime, distributed tracing (Langfuse/OTLP), Chaos Mesh chaos engineering; P1 incident resolution reduced 7.8h → 6.2h (−20%), 200+ incidents/month; topology-aware MCP toolset covering MySQL, MongoDB, Solace, RabbitMQ, Kafka, API Gateway

### Data Engineer — TCL Corporate Research (HK) Ltd. (Aug 2021 – Sep 2022)
Hong Kong S.A.R.

- Used MILP optimization to model raw material supply/demand for 1,600+ materials across 20+ processing plants; order fulfillment rate +6%, average delay −5.8 days, optimal solution within 30s; model averages 170k+ variables and 10k+ constraints
- Researched integer programming combined with RL; reproduced paper using CPLEX solver + PPO algorithm to improve cutting plane selection
- Contributed to multi-agent AGV project at Huaxing Optoelectronics using spatio-temporal A* algorithm; algorithm performance testing and simulation for 20 vehicles in Gazebo environment

### Engineer II — TDK SAE Magnetics (HK) Ltd. (May 2018 – Jul 2021)
Hong Kong S.A.R.

- Implemented control theory algorithms in C on DSP chips to optimize magnetic head track adhesion accuracy
- Collected and analyzed magnetic head movement trajectory data using Python on ARM Linux; developed hardware drivers

## Independent Projects

- **AIOps Root Cause Analysis on MySQL** (May 2025 – Present): ReAct supervisor agent routing user questions to downstream info-collection agents; metric info collect agent using ReAct for automatic metric data collection; Qwen2.5VL 7B metric analysis agent performing alert summary from charts; MCP server with Prometheus providing data for tool calling
- **AIOps Time Series Anomaly Detection on IT infrastructure** (Sep 2024 – Mar 2025): 170+ features engineered from MySQL, OS, and K8s data; XGBoost anomaly detection model; full data pipeline built with Kafka, S3, Docker, Kubernetes, and API maintenance
- **AIOps Network Device Log Anomaly Detection** (May 2024 – Jun 2025): Drain algorithm for log template extraction; unsupervised LSTM training; FAISS + gte-large-en-v1.5 for vector search and scoring (75–78% precision in production); Qwen2.5-7B fine-tuned with LoRA via Llama Factory; DPO fine-tuning on GPT-4 optimised SRE-style answers; RAG with Ollama + AnythingLLM
- **GPT Code Translation Project** (Apr 2023 – Oct 2023): Logic extraction module from XML structure; JVM syntax validation loop feeding errors back to GPT-3.5; few-shot test case correction module; 16,000h → 600h (70%+ success rate, 63% efficiency improvement)
- **Empty Reefer Container Forecasting** (Sep 2022 – Mar 2023): 35 features built from 3 years of historical data (quantities, sailing schedules, vessel capacity, weekly orders); LGBM; 8:2 train/test split; ablation study selecting 7 optimal feature combinations; 40% WMAPE for 8-week global port forecast
- **MPS Material Planning and Scheduling** (Aug 2021 – Dec 2021): MILP formulation of supply/demand relationships for TCL electronics factories; model averages 170k+ variables and 10k+ constraints

## Technical Skills

### Agent AI / Orchestration
LangGraph, LangChain, ReAct, MCP (Model Context Protocol), A2A, AG-UI, Multi-agent routing, DeepAgents, DeerFlow, FAISS, Redis

### LLM / GenAI
LoRA, SFT, PPO, DPO, RAG, Prompt Engineering, Few-Shot Learning, OpenAI API (GPT-3.5/GPT-4), Hugging Face, Qwen2.5, Llama Factory, Ollama, AnythingLLM

### Machine Learning
XGBoost, LightGBM, Logistic Regression, SVM, Naive Bayes, Scikit-learn

### Deep Learning
CNN, RNN, LSTM, Transformer, PyTorch

### Reinforcement Learning
Q-learning, SARSA, Policy Gradient

### Operations Research
MILP, Branch and Cut, Branch and Bound, CPLEX

### MLOps / Platform Engineering
Docker, Kubernetes, Kafka, S3, Jenkins, FastAPI, Flask, Langfuse/OTLP, Chaos Mesh, CI pipelines, health probes, microservice deployment

### Programming & Data
Python, C, SQL, Pandas, Feature Engineering, Time Series Analysis, Statistical Modelling

## Publications
<!-- None listed in CVs -->

## Awards
<!-- None listed in CVs -->

## Certifications
<!-- None listed in CVs — confirm in follow-up -->

## References
<!-- Not yet provided — add when available -->

More references available upon request.
