# Data Analysis Application

This repository contains a Python script (`execute.py`) for analyzing sales data.

## Files:

*   `data.csv`: The input sales data in CSV format.
*   `execute.py`: A Python script that performs the following analysis:
    *   Calculates total revenue per transaction.
    *   Counts the total number of rows.
    *   Counts the number of distinct regions.
    *   Identifies the top 3 products by total revenue.
    *   Computes the last 7-day rolling average of daily revenue for each region.
*   `.github/workflows/ci.yml`: GitHub Actions workflow for continuous integration and deployment.

## How to Run Locally:

1.  Ensure you have Python 3.11+ installed.
2.  Install dependencies:
    ```bash
    pip install pandas ruff
    ```
3.  Run the analysis script:
    ```bash
    python execute.py
    ```
    The script will print a JSON output to the console.

## CI/CD Pipeline:

A GitHub Actions workflow is configured in `.github/workflows/ci.yml` that runs on every push to the `main` branch:

1.  **Lints code** using `ruff`.
2.  **Executes `execute.py`** and pipes its output to `result.json`.
3.  **Publishes `result.json`** to GitHub Pages, making the analysis results publicly accessible.