# 🤖 LLM-Powered EDA Web Application

An **AI-powered Exploratory Data Analysis (EDA) web application** built with **Python, Gradio, Pandas, Matplotlib, Seaborn, and Ollama**.

The application allows users to upload a CSV dataset and automatically generates:

*  Dataset summary
*  Missing-value analysis
*  AI-generated data insights using **Gemma 2B**
*  Histograms for numerical columns
*  Correlation heatmap
*  Interactive web interface using Gradio

---

##  Project Overview

Exploratory Data Analysis is an important step in understanding a dataset before applying statistical analysis or machine learning.

This project automates the initial EDA process. Users simply upload a **CSV file**, and the application processes the dataset, performs basic data cleaning, generates visualizations, and uses a Large Language Model (LLM) to provide insights.

The application uses **Ollama with the Gemma 2B model** to generate AI-powered observations from the dataset summary.

---

##  Features

### 1.  CSV File Upload

Users can upload a CSV dataset directly through the Gradio interface.

The application reads the uploaded file using Pandas.

### 2.  Automated Missing-Value Handling

The application handles missing values automatically:

* **Numerical columns:** Missing values are replaced with the median.
* **Categorical columns:** Missing values are replaced with the mode.

### 3. Automated Dataset Summary

The application generates a statistical summary of the dataset using:

```python
df.describe(include='all')
```

This provides information about the dataset's numerical and categorical variables.

### 4.  Missing-Value Analysis

The application calculates missing values for each column using:

```python
df.isnull().sum()
```

This allows users to inspect the missing-value status of the dataset.

### 5.  AI-Powered Insights

The project uses **Ollama + Gemma 2B** to analyze the dataset summary and generate natural-language insights.

The summary is passed to the model through a prompt, and the generated response is displayed in the EDA report.

### 6. Automatic Data Visualization

The application automatically creates:

#### Histograms

Histograms are generated for numerical columns to understand their distributions.

#### Correlation Heatmap

A correlation heatmap is generated for numerical variables to visualize relationships between features.

### 7.  Gradio Web Interface

The application provides a simple web interface where users can upload their CSV file and receive the EDA report and visualizations.

The interface contains an **EDA Report** section and a **Data Visualization** gallery.

---

## 🛠️ Technologies Used

| Technology | Purpose                        |
| ---------- | ------------------------------ |
| Python     | Core programming language      |
| Pandas     | Data loading and preprocessing |
| Matplotlib | Data visualization             |
| Seaborn    | Statistical visualization      |
| Gradio     | Web interface                  |
| Ollama     | Local LLM execution            |
| Gemma 2B   | AI-powered data insights       |

---

##  Project Structure

```text
LLM-EDA-Web-Application/
│
├── LLM EDA web application project.py
├── README.md
├── requirements.txt
│
└── generated visualizations/
    ├── *_distribution.png
    └── correlation_heatmap.png
```

> Visualization files are generated automatically when the application processes a dataset.

---

##  Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/LLM-EDA-Web-Application.git
```

```bash
cd LLM-EDA-Web-Application
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

If PowerShell blocks script execution, activate using Command Prompt instead:

```cmd
.venv\Scripts\activate.bat
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

##  Install Ollama

This project requires **Ollama** to run the local Gemma model.

After installing Ollama, download the Gemma 2B model:

```bash
ollama pull gemma:2b
```

Make sure Ollama is running before launching the application.

---

##  requirements.txt

Create a file named `requirements.txt` containing:

```text
gradio
pandas
matplotlib
seaborn
ollama
```

---

## Run the Application

Run:

```bash
python "LLM EDA web application project.py"
```

The Gradio application will launch in your browser.

The project uses:

```python
demo.launch(share=True)
```

to launch the application and create a shareable Gradio link.

---

##  How It Works

```text
              CSV Dataset
                   │
                   ▼
           Upload through Gradio
                   │
                   ▼
              Pandas
                   │
                   ▼
        Data Cleaning & Processing
                   │
          ┌────────┴────────┐
          ▼                 ▼
   Statistical EDA      Missing Values
          │
          ▼
     Dataset Summary
          │
          ▼
       Ollama + Gemma 2B
          │
          ▼
     AI-Generated Insights
          │
          ▼
     Data Visualizations
          │
          ▼
       Gradio Dashboard
```

---

## Example Output

After uploading a CSV file, the application generates an EDA report containing:

```text
Data Loaded Successfully!

Summary:
<Dataset statistical summary>

Missing Values:
<Missing value information>

AI Insights:
<AI-generated observations>
```

It also generates visualizations including:

* Distribution plots
* Correlation heatmap

---

## Use Cases

This project can be useful for:

* Data Science beginners
* Automated exploratory data analysis
* Machine learning preprocessing
* Healthcare datasets
* Business datasets
* Academic/research datasets
* Quick dataset profiling
* AI-assisted data analysis

---

## Future Improvements

Potential improvements include:

*  Interactive Plotly visualizations
*  Automatic data-quality report
*  Support for additional LLMs
*  Excel file support
*  Advanced statistical analysis
*  Automated ML model recommendations
*  Feature importance analysis
*  Outlier detection
*  Improved file handling
*  Downloadable EDA reports
*  Interactive dashboard
*  Healthcare-specific analytics

---

## Skills Demonstrated

This project demonstrates practical knowledge of:

**Python • Pandas • Data Cleaning • Exploratory Data Analysis • Data Visualization • Statistics • Seaborn • Matplotlib • Generative AI • LLM Integration • Ollama • Gemma • Gradio • Data Science**

---

##Author

**Rutuja C.**

B.Tech Biotechnology | Data Science & AI/ML Enthusiast

### Areas of Interest

* Data Science
* Data Analytics
* Artificial Intelligence
* Machine Learning
* Healthcare Analytics
* Generative AI
* LLM Applications

---

##  If You Like This Project

If you find this project useful, consider giving the repository a ⭐ on GitHub!

---
