# NBA 3-Point Analysis and Prediction

This project uses NBA game data to analyze the evolution and impact of three-point shooting on game outcomes. By leveraging machine learning, the project identifies playstyle trends and evaluates game performance across different NBA eras.

## Project Overview

- **Data Analysis**: Visualizes trends in three-point attempts and shooting accuracy over time.
- **Machine Learning Models**: Predicts game outcomes based on in-game statistics, split by pre-2014 and post-2014 data to capture different playstyles.
- **Playstyle Simulation**: Assesses the adaptability of traditional versus modern NBA playstyles.

## Features

- **Three-Point Shot Trends**: Highlights the growth in three-point attempts and stability in shooting accuracy over seasons.
- **Outcome Prediction Models**: Trains machine learning models to predict game outcomes based on various in-game statistics.
- **Playstyle Adaptability Analysis**: Compares how old-school and new-school playstyles perform when applied across different NBA eras.

## Installation

To run this project, clone the repository and install the required dependencies:

```bash
git clone https://github.com/yourusername/NBA-3-Point-Analysis.git
cd NBA-3-Point-Analysis
```

Install dependencies with:

```bash
pip install -r requirements.txt
```

## Dataset

Data files:
- **Game Details** (`games_details.csv`): Contains detailed in-game statistics.
- **Seasons Data** (`games.csv`): Metadata on each game, including season and game IDs.

Place these datasets in the appropriate directory and adjust file paths as needed.

## Usage

### Data Cleaning and Preparation

1. **Data Preprocessing**: Duplicates and null values are removed, and game statistics (e.g., field goal percentage, free throw percentage) are calculated.
2. **Label Creation**: Each game is labeled with a win/loss outcome, making it suitable for supervised learning.

### Exploratory Data Analysis (EDA)

- **Three-Point Trends by Season**: Visualizes the increase in three-point shot attempts by season.
- **Shooting Accuracy Analysis**: Compares shooting percentages between winning and losing teams.
- **Shot Attempt Correlation**: Shows the relationship between attempted shots and points scored.

### Machine Learning: Predicting Game Outcomes

1. **Model Setup**:
   - **Random Forest Classifiers**: Used to predict game outcomes based on key in-game metrics, such as three-point attempts, rebounds, assists, and more.
   - **Era-Specific Splits**: The data is split into two periods (2003-2013 and 2014-2020) to capture unique gameplay patterns before and after the NBA’s three-point revolution around 2014.

2. **Training and Testing**:
   - Each era is separately trained using a **70/30 train-test split**.
   - The models are evaluated on **accuracy, precision, recall,** and **F1-score** to measure predictive effectiveness.
   
3. **Results**:
   - Both models achieved approximately **81% accuracy**, indicating reliable predictive power in distinguishing between winning and losing game outcomes.
   - The feature importance analysis shows that shooting accuracy, particularly three-point percentage, plays a significant role in the model's predictions.

4. **Optimal Playstyle Analysis**:
   - By generating data variations with different three-point attempt values, the model determines the optimal three-point shooting frequency for maximizing win probability.
   - **Partial Dependence Plots**: These plots show how win probability changes as three-point shot attempts increase, offering insights into shooting strategies over time.

### Playstyle Simulation: Old-School vs. Modern

- **Era Comparison**:
   - The models simulate how an old-school (2003-2013) team would perform in the modern era and vice versa.
   - Results suggest that a **modern NBA playstyle** (high three-point focus) has higher adaptability and effectiveness in both old and new eras compared to traditional styles.
   - For example, old-school teams have a lower predicted win rate in modern settings (around 41%), while modern teams playing in the past NBA achieve a higher hypothetical win rate (around 58%).

### Visualization

- **Partial Dependence Plot**: Visualizes the relationship between three-point shot attempts and win probability.
- **Histograms**: Illustrate the optimal range for three-point attempts in each era for maximizing win chances.

## Conclusion

The analysis indicates that the modern NBA playstyle, emphasizing three-point shooting, is better suited for success across different eras. The machine learning models provide consistent predictive power, and the visualizations offer clear insights into how playstyles have evolved and impacted game outcomes.
