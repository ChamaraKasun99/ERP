# Enterprise Sales & Profit + Inventory Intelligence (MySQL + SQL Server + PostgreSQL)

You get **two advanced portfolio projects** in one repo:

## Project 1 — Enterprise Sales & Profit Intelligence
**Goal:** one version of truth across Sales (MySQL), Finance (SQL Server), and CRM/Marketing (Postgres).  
**Outputs:** GM%, CLV, churn-risk, discount vs profit, MoM/YoY trends, top profitable customers.

## Project 2 — Inventory Optimization System
**Goal:** prevent overstock/understock with data-driven reorder automation.  
**Outputs:** reorder suggestions, safety stock logic, slow/fast movers, supplier KPIs.

---

## Run locally (free)
### 1) Start services
```bash
docker compose up -d
```

### 2) Create Python env
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
```

### 3) Copy env file
```bash
cp .env.example .env
```
> If you're on Windows, create `.env` manually by copying `.env.example`.

### 4) Seed databases (sample data included)
```bash
python scripts/seed_all.py
```

### 5) Build the unified analytics warehouse (Postgres)
```bash
python scripts/build_warehouse.py
```

### 6) BI (optional, free)
Metabase runs at: http://localhost:3000  
Connect it to the **warehouse** Postgres: `localhost:5432`, db `warehouse`, user `postgres`, pass `postgres`.

---

## GitHub Pages (to showcase)
1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Source: `Deploy from a branch`
4. Branch: `main`, folder: `/docs`
5. Your portfolio documentation page will be live.

---

## What to highlight in your CV
- Multi-RDBMS integration (MySQL + SQL Server + Postgres)
- Warehouse + marts design (star schema)
- Advanced SQL (CTEs, window functions, views, indexing)
- Inventory logic (reorder points + safety stock + alerts)
