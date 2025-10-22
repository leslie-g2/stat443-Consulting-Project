```markdown
# Gas Turbine NOx Reduction – STAT 443 Consulting Project

## Project Goal
Consulting project for STAT-443 Professional Statistics.  
We are working with **turbine sensor data from an energy provider in Turkey** to:
- Analyze **NOx (nitrogen oxides) emissions** and **CO (carbon monoxide)**.  
- Identify operational variables that drive NOx.  
- Provide recommendations for reducing NOx emissions while keeping CO under control.  
- Deliver a final **report + documented code (R/Python)** by December.  

---

## Requirements / Objectives
1. **Data Exploration (EDA)**
   - Check distributions, trends, and outliers for all variables.  
   - Plot NOx and CO against turbine variables (TIT, CDP, TEY, etc.).  

2. **Data Cleaning**
   - Handle missing values or sensor errors.  
   - Remove outliers (spikes beyond physical turbine ranges).  

3. **Feature Engineering**
   - Create load bands from TEY.  
   - Derive temperature deltas (TIT–TAT, TIT–TK2).  
   - Add interaction terms (CDP × TIT, AT × AH).  

4. **Modeling**
   - Build predictive models for NOx (Linear Regression, Random Forest, etc.).  
   - Compare results and feature importance.  
   - Test “what-if” scenarios (lower TIT, change load band).  

5. **Recommendations**
   - Operational changes to lower NOx.  
   - Trade-off analysis between NOx and CO.  
   - Sensitivity to ambient conditions (temperature, humidity).  

---

## Repository Structure
```

Gas-Turbine-NOX-Reduction/
│
├── hee-jae/          # individual work folder
├── leah/             # individual work folder
├── leslie/           # individual work folder
├── sean/             # individual work folder
├── viraj/            # individual work folder

├── TurbineGroup2.csv # dataset
└── README.md         # this file

````

Each member works in their **own folder**. Shared code or reports go in the root consulting notebook (`STAT-443.ipynb`).  

---

## Setup
- Python 3.x  
- Packages: `pandas`, `numpy`, `matplotlib`, `scikit-learn`  
- (Optional) R setup if needed for final deliverable.  

````markdown
## Git Workflow (Direct to Main)

Since each member works only inside their own folder, you can push directly to `main`.

1. **Check repo status**
   ```bash
   git status
````

2. **Stage your changes**

   ```bash
   git add .
   git status   # confirm files are staged
   ```

3. **Commit (short message, straight to the point)**

   ```bash
   git commit -m "feat(<name>): add/update analysis"
   ```

   Examples:

   * `feat(hee-jae): add NOx vs TEY plots`
   * `feat(sean): update regression model`
   * `chore(viraj): clean CO outliers`

4. **Push directly to main**

   ```bash
   git push origin main
   ```

---

## Notes

* Always keep work **inside your folder**.
* Do not touch files in other teammates’ folders.
* Use short commit messages: `feat`, `fix`, or `chore` + your name + action.

```