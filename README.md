# Attack-Defend-SyncUp

## Overview

**Attack-Defend-SyncUp** is a comprehensive project aimed at bridging the gap between known cybersecurity vulnerabilities (CVEs) and automated defense mechanisms (playbooks). This repository provides tools and data for analyzing over 250,000 CVEs and 1,200 defense playbooks, offering valuable insights into the interplay between cyber threats and defensive strategies.

## Features

- **Extensive CVE Dataset**: Over 250,000 CVEs with detailed descriptions, scores, and associated attack techniques.
- **Defense Playbooks**: Collection of 1,200 playbooks in standardized formats for various mitigation techniques.
- **Mapping and Analysis Tools**: Jupyter Notebook for mapping CVEs to defense playbooks and analyzing their effectiveness.
- **Visualization and Reporting**: Generate visual reports to better understand threat landscapes and defense mechanisms.

### Usage

1. **Launch Jupyter Notebook**:
    ```bash
    jupyter notebook
    ```

2. **Open the notebook**:
    Navigate to the  `attack_defend_syncup.ipynb`.

3. **Explore and analyze the data**:
    Follow the steps in the notebook to explore, process, and analyze the CVE and playbook data. The notebook includes:
    - Data loading and preprocessing
    - Mapping CVEs to playbooks
    - Visualizing relationships and insights


## Kaggle Dataset

We have published the data used in this project on Kaggle for easy access and further analysis. You can find the dataset [here](https://www.kaggle.com/philipempl/attacker-data).

### Download Attacker Data from Kaggle

To download and use the dataset, follow these steps:

1. **Install Kaggle API**:
    ```bash
    pip install kaggle
    ```

2. **Download the dataset**:
    ```python
    import os
    import zipfile

    dataset_identifier = 'philipempl/attacker-data'  # Replace with your dataset identifier
    os.makedirs('kaggle_dataset', exist_ok=True)
    !kaggle datasets download -d {dataset_identifier} -p kaggle_dataset --force

    # List all downloaded files
    downloaded_files = os.listdir('kaggle_dataset')

    # Extract all zip files in the directory
    for file_name in downloaded_files:
        if file_name.endswith('.zip'):
            with zipfile.ZipFile(os.path.join('kaggle_dataset', file_name), 'r') as zip_ref:
                zip_ref.extractall('kaggle_dataset')
    ```

3. **Load the data**:
    ```python
    import pandas as pd

    df = pd.read_csv('kaggle_dataset/results.csv')
    df.head()
    ```

## Contributions

We welcome contributions from the community! Feel free to fork the repository, create a branch, and submit a pull request with your improvements. Please ensure your code adheres to our coding standards and includes relevant tests.

