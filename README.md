# ✈️ Flight Delay Prediction using Big Data and Machine Learning

This project uses **Apache Spark** and **Gradient Boosted Trees (GBT)** to predict flight delays using historical weather and flight data. It leverages PySpark for distributed processing and applies data visualization, feature engineering, model training, and scalability testing on large-scale datasets.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Spark](https://img.shields.io/badge/Spark-PySpark%203.x-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

---

## 🚀 Project Features

- 📊 **EDA** with Spark + Seaborn + Matplotlib
- 🧠 **ML modeling** using Spark’s `GBTClassifier`
- 📈 **Visualizations**: Line plots, bar plots, scatter plots, heatmaps
- 🧪 **Model evaluation**: Accuracy, F1-score, confusion matrix, classification report
- ⚙️ **Feature importance** analysis
- ⚡ **Scalability testing** across different dataset sizes using Spark

---

## 📁 Project Structure

```

Big\_Data\_Project/
├── Big\_Data\_Project.ipynb   # Jupyter notebook with complete pipeline
├── requirements.txt         # Python dependencies
├── README.md                # Project overview
└── LICENSE                  # MIT License

````

---

## 📊 Data Sources & Features

This project uses flight and weather data with features such as:

- **PRCP**: Precipitation
- **SNOW**, **SNWD**: Snow indicators
- **AWND**: Wind speed
- **SEGMENT_NUMBER**: Number of flights a plane made that day
- **PART_OF_DAY**: Encoded time of departure (morning, evening, etc.)
- **DEP_DEL15**: Target (1 = delayed, 0 = not delayed)

> Location-specific identifiers and carrier codes are excluded for model generalizability.

---

## 📉 ML Pipeline Highlights

- Data preprocessing using Spark DataFrame transformations
- Feature vectorization with `VectorAssembler`
- Model: `GBTClassifier` with 50 iterations
- Evaluation Metrics:
  - **Accuracy**: ~81.28%
  - **F1 Score**: ~73.79%
  - **Precision/Recall** per class
  - Confusion matrix
  - Feature importance analysis

---

## ⚡ Scalability Results

The model was trained on increasing data fractions (20% → 100%) to evaluate Spark’s efficiency.

| Data Fraction | Training Time (s) | Accuracy |
|---------------|-------------------|----------|
| 0.20          | ~63s              | ~81%     |
| 1.00          | ~485s             | ~81%     |

> ✔️ Training time scales linearly while accuracy remains stable, showcasing Spark’s big data capability.

---



## 📦 Dependencies


* `pyspark`
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `bokeh`
* `folium`
* `scikit-learn`

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 👩‍💻 Author

**Anushka Garg**
GitHub: [@anushkagarg-30](https://github.com/anushkagarg-30)

```
