# Tong Chang

Data science student at the University of Macau. I work on the full analysis chain:
framing a question the data can actually answer, preparing it honestly, modelling it, and
being explicit about what the result does not tell you.

GitHub: [github.com/Tong-Chang](https://github.com/Tong-Chang) · Email: mc63803@um.edu.mo

## Technical skills

- **Languages:** Python, SQL
- **Data handling:** pandas, NumPy, data wrangling, missing-value treatment
- **Modelling:** scikit-learn, linear and polynomial regression, Ridge regularisation,
  pipelines, train/test evaluation
- **Visualisation:** matplotlib, seaborn, exploratory data analysis
- **Tools:** Jupyter Notebook, Git and GitHub, GitHub Pages

## Project showcase

### House Sales in King County, USA — what actually drives price?

**Research question.** How accurately can a house's sale price in King County be predicted
from its structural attributes and location, and which attributes carry the most signal?

![Above-ground living area vs sale price](images/fig2_price_vs_sqft_above.png)

*Above-ground living area against sale price with a fitted regression line. The upward
slope confirms a positive relationship; the widening spread at larger areas shows size
alone becomes a weaker predictor as houses get bigger.*

**Findings.** Living area is the strongest single predictor of price (r = 0.702) and alone
explains about half the variance (R² = 0.493). Neighbourhood quality beats room count —
the living area of the 15 nearest neighbours (r = 0.585) predicts price far better than
bedroom count (r = 0.309). Raw geography misleads a linear model: longitude contributes
almost nothing (r = 0.022) and zipcode as a plain number is negative (r = −0.053). Adding
2nd-degree polynomial terms gives the largest gain, lifting R² on held-out data from
0.648 to 0.700.

**Limitation.** The best headline figure (R² = 0.751) is in-sample and therefore optimistic;
only the two Ridge models were tested on held-out data, using a single fixed split with no
cross-validation. The data also covers one county over twelve months in 2014–2015.

- **Repository:** [github.com/Tong-Chang/.data-science-project](https://github.com/Tong-Chang/.data-science-project)
- **Status:** Completed
