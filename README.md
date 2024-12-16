
# Engineering Thesis: Prediction of energy production in photovoltaic infrastructure based on weather and geographical conditions
This repository contains the implementation of the engineering thesis project focused on **data scraping**, **model development** and **visualization**. The project demonstrates the use of modern programming techniques and tools to solve real-world problems, showcasing the application of theoretical knowledge in a practical context.

---

## 🚀 Features
- Data scraping of weather data and combining it with dataset
- Integration of statistical models for data analysis.
- Data visualizations.
- Modular and scalable codebase for ease of extension.

The project does not provide data for training and testing the models. The user is expected to provide the data in the required format.

---

## 📦 Installation

### Prerequisites
1. **Python 3.8+** installed on your system.
2. Recommended: Create a virtual environment to manage dependencies.

### Steps
1. Clone this repository:
   ```bash
   git clone https://github.com/Iriide/Engineering-Thesis.git
   cd Engineering-Thesis
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## 🛠 Usage

### Running the Application
1. Prepare your input data files and place them in the appropriate directory. The input data should be in CSV format, with the first row containing column names:
    - **data/filtered_installations.csv**: Contains the dataset of installations
   
| Column Name | Description                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| id_licznika | Unique identifier for the meter.                                                                        |
| index       | Index of city in source database.                                                                       |
| moc         | Power measurement in watts.                                                                             |
| dlugosc     | Longitude coordinate for geographical data.                                                             |
| szerokosc   | Latitude coordinate for geographical data.                                                              |
| data        | Date of the observation or measurement in \"YYYY-MM-DD HH:mm:SS\" format. Have to be aggregated hourly. |
| dpv         | Counter increment from the previous measurement                                                         |
| efekt       | Calculated efficiency of the system.                                                                    |
    
   - **data/filtered_installations_with_weather.csv**: Contains the dataset of installations with weather data used for model training

| Column Name   | Description                                                   |
|---------------|---------------------------------------------------------------|
| longitude     | Longitude coordinate for geographical data.                   |
| latitude      | Latitude coordinate for geographical data.                    |
| temperature   | Ambient temperature at the time of measurement (in °C).       |
| humidity      | Relative humidity percentage.                                 |
| wind_speed    | Speed of the wind (in meters per second or km/h).             |
| cloudiness    | Percentage of cloud cover in the sky.                         |
| month         | Month of the year (as a numerical value).                     |
| hour          | Hour of the day (24-hour format).                             |
| efficiency    | Output efficiency of the system, used as the target variable. |

2. The scripts are written as a Jupyter notebook, which can be run in a Jupyter environment. There are three main sections in the notebook:
    - **scrape_data.ipynb**: Contains the code for scraping weather data and aligning it to the installation dataset.
    - **models_experiments.ipynb**: Contains the code for training and evaluating the statistical models.
    - **DL.ipynb**: Contains the code for training and evaluating the deep learning model.
3. Output results, including processed data and visualizations, will be visible as a part of the notebook.
---
## 📝 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---
