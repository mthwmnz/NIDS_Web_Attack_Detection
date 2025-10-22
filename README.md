# Network Intrusion Detection System (NIDS)

## Project Summary & Results 🏆

This project implemented a high-performance **Network Intrusion Detection System (NIDS)** pipeline using PyCaret and LightGBM. The model successfully handled over 456K highly imbalanced network flows from the CIC-IDS2017 dataset.

* **Champion Model:** **Light Gradient Boosting Machine (LightGBM)**
* **F1 Score:** **0.9974** (Best balance of Precision and Recall for attack detection).
* **Training Method:** SMOTE and CPU Parallelism (Used to address extreme class imbalance).

***

## 🛠️ Repository Contents

The repository is structured to enable quick deployment and full review:

* **`NIDS_LightGBM_Final_Model.pkl`**: The completed machine learning pipeline, including all data cleaning and the final trained LightGBM model.
* **`Thursday-WorkingHours-Morning-WebAttacks.pcap_ISCX.csv`**: The subset of the raw dataset used for training.
* **`Network_Intrusion_Detection.ipynb`**: The Jupyter Notebook containing all code, model comparisons, and visualizations.
* **`requirements.txt`**: The exact list of dependencies for environment setup.

***

## ⚙️ Reproduction and Setup

### Prerequisites

* **Operating System:** Windows 10/11 or Linux.
* **Environment Manager:** Anaconda / Miniconda (recommended).
* **Python Version:** **3.10** or **3.11** (Required for PyCaret compatibility).

### Installation Steps

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/YourUsername/NIDS_Web_Attack_Detection.git](https://github.com/YourUsername/NIDS_Web_Attack_Detection.git)
    cd NIDS_Web_Attack_Detection
    ```
2.  **Create & Activate Environment**
    ```bash
    conda create -n nids_env python=3.11
    call conda activate nids_env
    ```
3.  **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

### Using the Final Model for Prediction

Once the environment is set up, you can load the model in a new script or notebook to make predictions on new, unseen network data:

```python
from pycaret.classification import load_model, predict_model
import pandas as pd

# Load the saved model pipeline
loaded_pipeline = load_model('NIDS_LightGBM_Final_Model') 

# Example: Predict on a new DataFrame of unseen network flows
# predictions = predict_model(loaded_pipeline, data=new_network_data)
