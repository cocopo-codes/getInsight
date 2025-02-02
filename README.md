# getInsight: Mars Weather Data Exploration

## Overview
getInsight is a collection of Jupyter notebooks that allows you to retrieve and analyze the latest Mars Weather data from NASA's Insight Weather Service API using a demo key.

## Prerequisites
- Python 3.10 or higher
- pip (Python package manager)
- Git

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/getInsight.git
cd getInsight
```

### 2. Create a Virtual Environment
```bash
# For macOS/Linux
python3 -m venv marsenv

# Activate the virtual environment
source marsenv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Install Jupyter Kernel
```bash
python -m ipykernel install --user --name=marsenv --display-name "Python (marsenv)"
```

## Available Notebooks

### 1. grab-mars-api-no-auth.ipynb
- **Purpose**: Retrieve and display the latest Mars Weather API response
- **Features**: 
  - Fetches data using NASA's demo key
  - Prints raw API response
  - No data export

### 2. excel-grab-mars-insight-data-demokey.ipynb
- **Purpose**: Retrieve Mars Weather data and export to Excel
- **Features**:
  - Fetches data using NASA's demo key
  - Exports data to an Excel spreadsheet
  - Filename includes current date

## Understanding the Excel Output

### Excel Sheet Structure
The exported Excel file contains multiple sheets to help you understand the Mars Weather data:

#### 1. Summary Sheet
- **Purpose**: Provides an overview of the dataset
- **Columns**:
  - `Total Sols Recorded`: Number of Martian days in the dataset
  - `Average Temperature (°F)`: Mean temperature across recorded sols
  - `Average Wind Speed (mph)`: Mean wind speed
  - `Most Common Wind Direction`: Predominant wind direction

#### 2. Sol-by-Sol Data Sheet
- **Purpose**: Detailed information for each Martian day (sol)
- **Key Columns**:
  - `Sol`: Martian day number
  - `Earth Date`: Corresponding Earth date
  - `Temperature High (°F)`: Maximum temperature for the sol
  - `Temperature Low (°F)`: Minimum temperature for the sol
  - `Wind Speed (mph)`: Average wind speed
  - `Wind Direction`: Predominant wind direction
  - `Pressure (Pa)`: Atmospheric pressure

### Data Interpretation Tips
- **Sol**: A Martian day, slightly longer than an Earth day (24 hours, 39 minutes)
- **Temperature**: Recorded in Fahrenheit
- **Wind Speed**: Measured in miles per hour
- **Pressure**: Measured in Pascals (Pa)

### Common Observations
- Martian temperatures can vary dramatically between day and night
- Wind directions can change frequently
- Atmospheric pressure is much lower than on Earth

### Visualization Suggestions
- Use Excel's built-in charting tools to create:
  - Temperature trends over time
  - Wind speed variations
  - Pressure changes

### Limitations
- Data is based on NASA's Insight Lander location
- Represents local conditions at the landing site
- May not reflect global Martian weather patterns

## Running the Notebooks

1. Start Jupyter Notebook
```bash
jupyter notebook
```

2. In the Jupyter interface:
   - Select the notebook you want to run
   - Ensure the kernel is set to "Python (marsenv)"
   - Run cells sequentially using Shift+Enter

## Troubleshooting
- **Module Not Found Errors**: Ensure you've activated the virtual environment and installed all dependencies
- **Kernel Issues**: Verify the marsenv kernel is installed and selected
- **API Limitations**: NASA's demo key has request rate limits

## Contributing
Contributions are welcome! Please submit a pull request or open an issue.

## Disclaimer
This project uses NASA's Mars Weather API demo key. For extensive use, consider obtaining a personal API key from NASA.
