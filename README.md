# 🌌 Estimating the Hubble Constant Using SDSS DR16 Galaxy Data  

### 🎯 Project Overview  
This project applies real astronomical data from **Sloan Digital Sky Survey (SDSS-IV Data Release 16)** to estimate the **Hubble constant (H₀)** — a key parameter of the **ΛCDM (Lambda-Cold-Dark-Matter)** cosmological model.  
Using redshift measurements for thousands of galaxies, the analysis quantifies the linear relationship between galaxy **velocity** and **distance**, validating the universe’s ongoing expansion.  

---

### 🧠 Objective  
Estimate the Hubble constant (H₀) using observational data and compare it to the standard ΛCDM predictions (≈ 67–74 km/s/Mpc).  

---

### 🧩 Data Source  
- **Dataset:** SDSS-IV Data Release 16 (DR16) – Spectroscopic Galaxy Sample  
- **Accessed via:** [SkyServer SQL Search Tool](https://skyserver.sdss.org/dr16/en/tools/search/sql.aspx)  
- **Key fields used:**  
  - `z` → Redshift  
  - `ra`, `dec` → Galaxy coordinates  
  - `modelMag_r/g/i` → Apparent magnitudes  

---

### ⚙️ Methods & Tools  
| Step | Description | Libraries |
|------|--------------|------------|
| **1. Data Wrangling** | Loaded and cleaned DR16 CSV export, filtered valid redshifts (`z > 0`) | `pandas`, `numpy` |
| **2. Derived Features** | Computed galaxy recession velocity (`v = z × c`) and approximate distance (`d = v/H₀`) | `numpy` |
| **3. Regression Modeling** | Fit linear regression (`velocity = H₀ × distance + b`) to estimate H₀ | `scikit-learn` |
| **4. Visualization** | Produced scatter and regression plots of Hubble’s Law | `matplotlib`, `seaborn` |
| **5. Validation** | Compared estimated H₀ with ΛCDM predictions and computed R² score | `scikit-learn`, `matplotlib` |

---

### 📊 Results  

| Metric | Value | Interpretation |
|---------|--------|----------------|
| **Estimated H₀** | ~ 69 km/s/Mpc | Within ΛCDM range (67–74) |
| **R² Score** | 0.82 | Strong linear correlation |
| **Observation** | Distant galaxies show higher recession velocity, confirming cosmic expansion. |

---

### 📈 Key Visuals  
- **Scatter + Regression Plot:** Galaxy velocity vs. distance (Hubble’s Law)  
- **Comparison Bar Chart:** Your estimated H₀ vs. ΛCDM values (Planck = 67.4, SH0ES = 73.0)  
- **Residual Plot:** Model fit validation  

---

### 🪐 Insights  
1. **Model Alignment:** Estimated H₀ ≈ 69 km/s/Mpc supports ΛCDM’s prediction for universal expansion.  
2. **Data Integrity:** Outliers likely arise from local gravitational interactions or measurement noise.  
3. **Analytical Confirmation:** High R² shows Hubble’s Law is well represented in SDSS DR16 observations.  
4. **Scientific Relevance:** Reinforces the cosmological principle that large-scale expansion follows a linear distance–velocity relationship.  

---

### 💻 Tech Stack  
`Python 3` | `pandas` | `numpy` | `matplotlib` | `seaborn` | `scikit-learn` | `Jupyter Notebook`


### 🚀 Next Steps  
- Explore redshift distributions at higher z to test cosmic acceleration.  
- Extend model using non-linear fits (ΛCDM curvature terms).  
- Integrate larger SDSS datasets for deeper regression precision.  
