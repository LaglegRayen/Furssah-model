# UNSW-NB15 Dataset Analysis and Model Training

## Dataset Description
The **UNSW-NB15** dataset is a modern network intrusion detection dataset created by the **Cyber Range Lab, UNSW Canberra**. It is designed to simulate a hybrid of real-world normal activities and synthetic contemporary attack behaviors. The dataset includes **49 features** and a **class label** that identifies whether a record is normal or an attack.

### Key Details:
- **Source**: The raw network packets were generated using the **IXIA PerfectStorm tool**.
- **Capture Tool**: The traffic was captured using the **Tcpdump tool**, resulting in 100 GB of raw traffic (Pcap files).
- **Attack Families**: The dataset includes **nine attack families**:
  - Fuzzers
  - Analysis
  - Backdoors
  - DoS (Denial of Service)
  - Exploits
  - Generic
  - Reconnaissance
  - Shellcode
  - Worms
- **Feature Extraction**: Tools like **Argus** and **Bro-IDS** were used, along with 12 custom algorithms, to extract 49 features.
- **Files**:
  - The dataset is split into four main CSV files: `UNSW-NB15_1.csv`, `UNSW-NB15_2.csv`, `UNSW-NB15_3.csv`, and `UNSW-NB15_4.csv`.
  - Ground truth is stored in `UNSW-NB15_GT.CSV`.
  - Event list is stored in `UNSW-NB15_LIST_EVENTS`.
  - Partitioned training and testing sets:
    - Training set: `UNSW_NB15_training-set.csv` (175,341 records)
    - Testing set: `UNSW_NB15_testing-set.csv` (82,332 records)

### Dataset Link
You can download the dataset from the following link:  
[UNSW-NB15 Dataset](https://research.unsw.edu.au/projects/unsw-nb15-dataset)

---

## Project Overview
This project focuses on analyzing the **UNSW-NB15** dataset and building a machine learning pipeline to classify network traffic as normal or malicious. The pipeline includes:
1. **Feature Selection**: Dropping features with low correlation to the target variable (correlation < 0.03).
2. **Preprocessing**:
   - Scaling numerical features using `StandardScaler`.
   - Encoding categorical features using `OneHotEncoder`.
3. **Model Training**: Using a **Random Forest Classifier** to achieve high accuracy.

---

## Results
The pipeline achieves **high accuracy** on the testing set, demonstrating its effectiveness in detecting network intrusions. The model is trained and evaluated using the following steps:
1. **Training Set**: 175,341 records.
2. **Testing Set**: 82,332 records.
3. **Model**: Random Forest Classifier with 100 estimators.

### Key Metrics:
- **Accuracy**: Achieved high accuracy on the testing set, ensuring reliable detection of attacks.

---

## How to Use
1. Clone the repository:
   ```bash
   git clone <repository-url>
