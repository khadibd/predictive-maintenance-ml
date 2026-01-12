🟡 Predictive Maintenance System using Machine Learning

📌 Project Overview



This project implements a Predictive Maintenance System using Machine Learning to predict machine failure before it occurs, based on sensor data.

The system is built using the NASA Turbofan Engine Degradation Dataset, a well-known industrial dataset widely used in aerospace, automotive, and manufacturing applications.

The objective is to classify whether an engine is close to failure (1) or operating normally (0).





🎯 Problem Statement



Unexpected machine failures can lead to:

High maintenance costs

Production downtime

Safety risks



This project aims to anticipate failures in advance by analyzing sensor measurements and operating conditions, enabling early maintenance decisions.





📊 Dataset Description



Dataset: NASA CMAPSS Turbofan Engine Dataset (FD001)

Type: Time-series sensor data

Engines: Multiple engines run until failure

Each row represents: One engine at one operational cycle



Dataset contains:



Engine ID

Cycle number (time step)

3 operational settings

21 sensor measurements



⚠️ The dataset does not include a failure label.

This label is engineered using Remaining Useful Life (RUL).





🔵 Remaining Useful Life (RUL)

RUL (Remaining Useful Life) represents the number of cycles remaining before engine failure.

It is calculated as:


```bash
RUL = Maximum Cycle of Engine − Current Cycle
```




A binary failure label is created as follows:



Failure = 1 → RUL ≤ 30 (engine close to failure)

Failure = 0 → RUL > 30 (engine operating normally)



This transforms the problem into a binary classification task.





⚙️ Machine Learning Approach



Algorithm: Logistic Regression



Why Logistic Regression?

Suitable for binary classification

Interpretable

Widely used in industrial applications



Pipeline:



Data loading and cleaning

Feature selection

RUL computation

Failure label creation

Train/Test split

Feature scaling

Model training

Model evaluation





📈 Model Evaluation



The model is evaluated using:



Accuracy

Precision

Recall

F1-score



Typical accuracy achieved: 85% – 95%, depending on data split.





🧪 Technologies Used



Python

Pandas

NumPy

Scikit-learn





📁 Project Structure


```bash
predictive\_maintenance\_ml/

│

├── data/

│   └── turbofan\_train.txt

│

├── predictive\_maintenance.py

└── README.md
```




▶️ How to Run the Project



1. Clone the repository:


```bash
git clone https://github.com/khadibd/predictive-maintenance-ml
```


2. Navigate to the project folder:


```bash
cd predictive\_maintenance\_ml
```




3. Run the script:


```bash
python predictive\_maintenance.py
```




👩‍💻 Author

Eng. Khadija Bouadi


📧 Contact

For any queries, reach out to:

GitHub: @khadibd

Email:  khadijabouadi00@gmail.com 
