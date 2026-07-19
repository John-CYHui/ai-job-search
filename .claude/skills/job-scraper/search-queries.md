# Search Queries for Job Scraper

## Installed portal CLIs (primary for `/scrape`)

`/scrape` discovers every portal skill under `.agents/skills/*/SKILL.md` and runs its CLI first. Shipped country-agnostic CLIs include `linkedin-search` and `freehire-search`; any skill added with `/add-portal` is included automatically.

The `site:` query templates below are the **WebSearch fallback** — used for portals without a CLI, company career pages, or when a CLI fails.

## Search Sites

Primary (Hong Kong, mainland China, Singapore):
- **linkedin.com/jobs** — covered by `linkedin-search` CLI; fallback `site:` queries listed below
- **jobsdb.com** — Hong Kong's largest general job board; add a CLI with `/add-portal` if desired
- **ctgoodjobs.hk** — HK professional jobs (finance, tech, corporate)
- **zhipin.com** (Boss直聘) — mainland China primary job search app (Beijing / Shanghai / Shenzhen); Chinese CV applies

Secondary (company career pages):
- Direct Google `site:` searches for target companies

## Query Categories

Queries are grouped by priority. Combine with location terms as shown.

---

### Priority 1: AI Engineer / Agent Engineering

Strongest match — most desired career direction.

```
site:linkedin.com/jobs "AI Engineer" "Hong Kong"
site:linkedin.com/jobs "Agent Engineer" OR "Agentic AI" "Hong Kong"
site:linkedin.com/jobs "LLM Engineer" "Hong Kong"
site:linkedin.com/jobs "AI Platform Engineer" "Hong Kong"
site:jobsdb.com "AI Engineer" Hong Kong
site:ctgoodjobs.hk "AI Engineer" Hong Kong
site:linkedin.com/jobs "AI Engineer" Singapore
site:linkedin.com/jobs "LLM Engineer" Singapore
site:zhipin.com "AI工程师" LangGraph OR LangChain OR Agent
site:zhipin.com "大模型工程师" 上海 OR 深圳 OR 北京
site:zhipin.com "智能体工程师" OR "Agent工程师"
```

---

### Priority 2: ML Engineer / GenAI Platform

Multi-agent, GenAI, and MLOps-focused roles.

```
site:linkedin.com/jobs "ML Engineer" LangGraph OR LangChain OR "multi-agent" "Hong Kong"
site:linkedin.com/jobs "MLOps Engineer" "Hong Kong"
site:linkedin.com/jobs "GenAI Engineer" "Hong Kong"
site:jobsdb.com "Machine Learning Engineer" Hong Kong
site:ctgoodjobs.hk "Machine Learning" OR "Deep Learning" Engineer Hong Kong
site:linkedin.com/jobs "ML Engineer" Singapore
site:linkedin.com/jobs "MLOps" Singapore
site:zhipin.com "算法工程师" LLM OR RAG OR Agent 上海 OR 深圳 OR 北京
site:zhipin.com "机器学习工程师" 生成式AI OR 大模型
```

---

### Priority 3: Data Scientist (GenAI / LLM focus)

Broader data scientist roles with a clear AI/LLM angle.

```
site:linkedin.com/jobs "Data Scientist" LLM OR GenAI OR "large language model" "Hong Kong"
site:jobsdb.com "Data Scientist" "Artificial Intelligence" Hong Kong
site:ctgoodjobs.hk "Data Scientist" "Machine Learning" Hong Kong
site:linkedin.com/jobs "Data Scientist" GenAI Singapore
site:zhipin.com "数据科学家" 生成式AI OR LLM 上海 OR 深圳 OR 北京
```

---

### Priority 4: Banking / Finance / Quantitative AI

Target pivot into banking, insurance, or quant/hedge fund applying ML.

```
site:linkedin.com/jobs "AI Engineer" bank OR "financial services" OR fintech "Hong Kong"
site:linkedin.com/jobs "Machine Learning" "investment bank" OR "hedge fund" "Hong Kong"
site:linkedin.com/jobs "Quantitative" "Machine Learning" OR "AI" "Hong Kong"
site:linkedin.com/jobs "Data Scientist" bank OR insurance "Hong Kong"
site:jobsdb.com "Machine Learning" bank OR finance Hong Kong
site:ctgoodjobs.hk "AI" OR "Machine Learning" bank OR "financial services" Hong Kong
site:linkedin.com/jobs "AI Engineer" bank OR fintech Singapore
site:zhipin.com "量化" "机器学习" OR "AI" 上海 OR 深圳
site:zhipin.com "AI工程师" 金融 OR 银行 OR 保险 上海 OR 深圳 OR 北京
```

---

## Location Filter

When evaluating results, verify job location is acceptable:

| Location | Status |
|----------|--------|
| Hong Kong (any district) | ✅ Ideal |
| Singapore | ✅ Acceptable (open to relocate) |
| Shanghai, Shenzhen, Beijing | ✅ Acceptable (Chinese CV applies) |
| Other mainland China cities | 🔶 Flag — raise with user |
| Full remote (international) | 🔶 Flag — raise with user |
| Any other international location | ❌ Skip unless user confirms |

**Always exclude:**
- Outsourcing / IT services companies (Accenture, IBM Global Services, etc. in outsourcing capacity)
- Contract or temporary positions (permanent only)
- Companies with fewer than ~200 employees

---

## Date Filter

Only include jobs posted within the last **14 days**, or with an application deadline that has not yet passed. Flag as "date unknown" if posting date cannot be determined.

---

## Adapting Queries

If the user specifies a focus area with `/scrape [focus]`, select the matching category's queries and generate 2–3 custom queries:

- `/scrape fintech` → Priority 4 queries + custom fintech/quant queries
- `/scrape agent` → Priority 1 queries + custom agentic AI queries
- `/scrape singapore` → All priorities filtered to Singapore
- `/scrape mainland` → All priorities filtered to Shanghai/Shenzhen/Beijing, Chinese-language queries

## CV Language Reminder

- **Hong Kong / Singapore / international roles** → use English CV (`cv/main_<company>_<role>.tex`)
- **Mainland China roles** → use Simplified Chinese CV template
