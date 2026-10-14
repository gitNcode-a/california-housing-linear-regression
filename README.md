# California Housing — Linear Regression

A learning project that predicts an area's median house value using census information. Each row represents a census block group, not an individual house.

## Dataset
California Housing Prices by Cam Nugent, based on the 1990 California census.

Source: https://www.kaggle.com/datasets/camnugent/california-housing-prices

## What this project covers
- Inspecting data, missing values and unusual observations.
- Exploring distributions and relationships.
- Creating a rooms-per-household feature.
- Splitting training, validation and test data.
- Filling missing numeric values using training medians.
- Encoding ocean proximity categories.
- Training and evaluating linear regression.
- Investigating residuals and negative predictions.
- Building a preprocessing pipeline.
- Performing five-fold cross-validation.

## Results

| Metric | Result |
| --- | ---: |
| Initial test MAE | $50,551.75 |
| Initial test RMSE | $69,839.39 |
| Initial test R² | 0.628 |
| Five-fold cross-validation MAE | $49,658.90 |

The initial test scores describe the first model. Cross-validation evaluates the later pipeline on training data.

## Files
- `01_California_Housing_Linear_Regression.ipynb`: analysis, explanations and outputs.
- `data/housing.csv`: dataset input.
- `requirements.txt`: required Python packages.
- `.gitignore`: files excluded from Git tracking.

## How to run
1. Download this repository and open its folder in VS Code.
2. Install the Microsoft Python and Jupyter extensions.
3. Create a virtual environment in the project folder:

   ```powershell
   python -m venv .venv
   ```

4. Install the required packages:

   ```powershell
   .\.venv\Scripts\python.exe -m pip install -r requirements.txt
   ```

5. Place the original dataset CSV at `data/housing.csv` if it is not included.
6. Open the notebook and select the `.venv` Python kernel.
7. Run the cells from top to bottom.

## Limitations
- Historical data does not establish performance on current prices.
- House values are capped around $500,000, recorded as $500,001.
- There are very few island examples.
- Some predictions are negative or have large errors.
- Random splits do not measure performance in entirely new regions.

This is an educational project, not a property valuation service.