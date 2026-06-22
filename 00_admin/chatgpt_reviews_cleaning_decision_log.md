# Chatgpt_reviews — Data Cleaning Decision Log

**Purpose:** Document inspection-based decisions before applying transformations, so the cleaned dataset is reproducible and defensible.

- **Dataset:** <chatgpt_reviews.csv / https://www.kaggle.com/datasets/ashishkumarak/chatgpt-reviews-daily-updated / Downloaded: 20.06.2026>
- **Owner:** <you>
- **Date started:** <2026-06-22>
- **Last updated:** <2026-06-22> The data owner asserts that it is daily updated
- **Scope:** Setup & Cleaning (Stage 0–1)
  

- **Definition of Done (DoD):**
  - Consistent names (snake_case)
  - Types confirmed (safe coercions only)
  - Obvious invalids handled (with rationale)
  - Missingness summarized + policy per column
  - Duplicates assessed (row + candidate keys)
  - Staged artifact saved under `/processed`
  - This decision log updated and shipped

---

## 0. Project Structure & Reproducibility
- **Project root strategy:** (e.g., `Path.cwd().parent`)
- **Folders ensured:** `/01_data/raw`, `/01_data/processed`, `/02_notebooks`, etc.
- **Artifact naming convention:** `YYYY-MM-DD_stageN_keyword.ext`
- **Environment notes:** (optional: python version, env.yml/requirements.txt)

---

## 1. Observation Summary (Baseline Facts)
### 1.1 Dataset Snapshot
- **Rows x Cols:** Shape: 1,089,749 rows × 8 columns
Top 3 rows (quick peek):
- **Column list:** ['reviewId', 'userName', 'content', 'score', 'thumbsUpCount',
       'reviewCreatedVersion', 'at', 'appVersion']
- **Dtypes summary:** 
appVersion                str
at                        str
content                   str
reviewCreatedVersion      str
reviewId                  str
score                   int64
thumbsUpCount           int64
userName                  str
dtype: object

- **Head/tail anomalies:** none

### 1.2 Missingness Overview
appVersion              0.072350
reviewCreatedVersion    0.072350
content                 0.000016
userName                0.000002
score                   0.000000
reviewId                0.000000
thumbsUpCount           0.000000
at                      0.000000
Name: missing_rate, dtype: float64

appVersion              78843
reviewCreatedVersion    78843
content                    17
userName                    2
score                       0
reviewId                    0
thumbsUpCount               0
at                          0
dtype: int64

Notes about missingness: 
- 7% of missing values. Defer decision as to what to do with them.
- missing rows regarding content and user name can be dropped given how small they are.


### 1.3 Duplicates & Candidate Keys
- **Row duplicates:** <count>
- **Candidate key(s):** <none / list>
- **Duplicate policy:** <keep / drop / investigate>

---

## 2. Column Inventory (Roles)
- **Target(s):** <...>
- **Identifiers:** <...>
- **Categoricals:** <...>
- **Numerics:** <...>
- **Booleans:** <...>
- **High-missing columns:** <...>

---

## 3. Decisions (Document Before Acting)

### 3.1 Naming & Schema Normalization
- **Decision:** <e.g., normalize to snake_case>
- **Rationale:** <1 line>
- **Evidence:** <optional>
- **Action:** <planned code step>

### 3.2 Structural Drops (Zero Ambiguity)
| Column | Observation | Decision | Rationale | Evidence |
|---|---|---|---|---|
| | | | | |

### 3.3 Semantic Redundancy / Deterministic Equivalence
> Validate before dropping (equality checks / crosstabs / derived-rule checks).

| Candidate | Hypothesis (Same info?) | Validation Method | Result | Decision | Notes |
|---|---|---|---|---|---|
| | | | | | |

### 3.4 Type Sanity & Boolean Coherence (Confirm, Don’t Over-transform)
| Column | Expected Concept | Current dtype | OK? | Notes / Deferred fixes |
|---|---|---|---|---|
| | | | | |

### 3.5 Validity Rules (Invalid vs Extreme-but-Plausible)
| Column | Invalid Definition | Handling | Rationale | Evidence |
|---|---|---|---|---|
| | | | | |

### 3.6 Missingness Policy (No Heavy Imputation Yet)
| Column | Missing Count | Policy (Drop rows / Keep missing / Drop col / Defer impute) | Rationale |
|---|---:|---|---|
| | | | |

---

## 4. Transformation Plan (Approved Actions Only)
- [ ] Action 1: <...>
- [ ] Action 2: <...>
- [ ] Action 3: <...>

---

## 5. Execution Notes (What Was Actually Applied)
### 5.1 Changes Applied
- <bullet list of applied changes>

### 5.2 Artifacts Saved
| Date | Stage | Artifact | Notes |
|---|---|---|---|
| <YYYY-MM-DD> | <stageN> | <path> | <what changed> |

---

## 6. Deferred Items (Explicit Backlog)
- <e.g., Age imputation deferred to Modeling Stage>
- <e.g., Feature engineering deferred to Stage 6>

---

## 7. Quick Reproduction Steps
1. <Open repo / set env>
2. <Run notebook/script>
3. <Confirm outputs in /processed>
