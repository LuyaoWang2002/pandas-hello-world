# Sensor Data Analysis

A simple pandas project that reads Excel sensor data, fills missing temperatures, and exports the processed data to Excel.

## Installation

Use a current Python 3 version. Tested with Python 3.14.

From the project folder:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

On Windows, activate with `.venv\Scripts\activate` instead.

## Usage

With the environment activated, run from the project folder:

```bash
python process_sensor_data.py
```

The script reads the first worksheet in `sensor_data.xlsx` and creates `sensor_data_analyzed.xlsx`, with a worksheet named `Analysis`. Open the output in Excel to view the results.

## Files

- `sensor_data.xlsx`: Excel input supplied by the course.
- `sensor_data.csv`: Original warmup input, retained for reference.
- `process_sensor_data.py`: Data analysis script.
- `sensor_data_analyzed.xlsx`: Generated output, ignored by Git.
- `requirements.txt`: Python dependencies.
- `.gitignore`: Excludes generated outputs and local environment files.

## What It Does

1. Loads the Excel input.
2. Prints the first rows, column information, and statistics.
3. Fills missing temperatures with the average available temperature.
4. Prints average temperatures by equipment and counts of each status.
5. Adds `Needs_Check` for temperatures above 50 degrees Celsius.
6. Exports the cleaned data to Excel without an extra index column.

The Excel output contains the cleaned rows and the new column. Group summaries are printed in the terminal. Output files are generated locally and not committed; the input workbook remains in the repository.

## Requirements

- Python 3
- pandas
- openpyxl
