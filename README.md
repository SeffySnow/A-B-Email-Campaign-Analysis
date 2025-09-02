# Marketing Campaign A/B Testing

## 📌 Project Overview
This project analyzes the effectiveness of **digital marketing campaigns** using **A/B testing**.  
The dataset includes campaigns across multiple channels (Email, Social Media, SEO, PPC, Referral) with customer demographics and conversion outcomes.

The focus of this notebook is:
- Comparing **Email campaigns vs other channels**.
- Evaluating **conversion rate (CVR) differences**.
- Checking **statistical significance** with Z-tests and confidence intervals.
- Performing **power analysis** to assess whether the sample size is sufficient.
- Exploring **segment-level uplift** (e.g., CVR difference by gender).

---

## 📂 Dataset
- Source: Kaggle — *Predict Conversion in Digital Marketing Dataset*  
- Main columns used:
  - `CustomerID` → unique user ID  
  - `CampaignChannel` → Email, Social, SEO, PPC, Referral  
  - `CampaignType` → Awareness, Conversion, Retention  
  - `Conversion` → target outcome (1 = converted, 0 = not converted)  
  - Demographic features such as Gender  

---

## 🛠️ Methods

### 1. A/B Testing
- **Email vs Social Media**  
- **Email vs Rest**  
- Two-proportion **Z-tests** with p-values.  
- **Confidence intervals** (Wilson method).  
- **Effect size**: uplift in percentage points.  
- **Power analysis**: Minimum Detectable Effect (MDE) at 2pp threshold.

### 2. Segment-Level Analysis
- Stratified by **Gender**.  
- Checked **Sample Ratio Mismatch (SRM)** using Chi-square tests.  
- Compared CVRs for Email vs PPC by segment.  
- Tested significance with Z-tests and Chi-square tests.

---

## 📊 Results (from notebook)
- **Email vs other channels**: small differences in CVR, not statistically significant at the 2pp MDE.  
- **Power analysis**: current sample size is underpowered — at least ~2,400 users per group are needed to detect a 2pp effect reliably.  
- **Gender segments**: uplift (Email − PPC CVR) varies slightly, but no strong statistically significant effects were found.
