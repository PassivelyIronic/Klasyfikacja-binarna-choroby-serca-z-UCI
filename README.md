# Klasyfikacja binarna choroby serca (UCI Heart Disease)

Projekt uczenia maszynowego mający na celu przewidywanie obecności choroby serca u pacjentów na podstawie ich danych klinicznych. Analiza opiera się na popularnym zbiorze danych [UCI Heart Disease Data](https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data).

## O projekcie
Cały kod i proces analityczny znajdują się w głównym notatniku Jupyter: `zmum_project.ipynb`. 

Projekt przechodzi przez pełen cykl Data Science:
* **Analiza i czyszczenie danych (Preprocessing):** Obsługa brakujących danych przy użyciu `SimpleImputer` oraz `KNNImputer`, a także radzenie sobie z wartościami odstającymi (outlierami) za pomocą winsoryzacji.
* **Inżynieria cech (Feature Engineering):** Tworzenie nowych wskaźników bazujących na wiedzy medycznej (np. wskaźnik ryzyka sercowo-naczyniowego `cv_risk_score`, tolerancja wysiłku, rezerwa tętna) oraz kodowanie zmiennych kategorycznych (Ordinal i One-Hot Encoding).
* **Modelowanie:** Trening i ewaluacja wielu algorytmów klasyfikacyjnych, w tym m.in.: Logistic Regression, Decision Tree, Random Forest, SVM, XGBoost, LightGBM oraz modeli zespołowych (Stacking, Voting).
* **Optymalizacja i Auto-ML:** Wybór optymalnych cech (RFE) oraz dostrajanie hiperparametrów z wykorzystaniem metod takich jak Grid Search, Optuna oraz biblioteki FLAML.

## Użyte technologie
Projekt został zrealizowany w języku Python. Główne wykorzystane biblioteki to:
* `pandas`, `numpy` (przetwarzanie danych)
* `scikit-learn` (modele ML, preprocessing, metryki)
* `xgboost`, `lightgbm` (algorytmy gradient boosting)
* `optuna`, `flaml` (optymalizacja parametrów)
* `matplotlib`, `seaborn` (wizualizacja wyników)

## Jak uruchomić projekt
1. Sklonuj repozytorium na swój dysk.
2. Upewnij się, że posiadasz zainstalowanego Pythona (wersja 3.x) oraz zainstaluj niezbędne pakiety:
   ```bash
   pip install pandas numpy scikit-learn xgboost lightgbm optuna flaml matplotlib seaborn
