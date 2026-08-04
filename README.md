# Predykcja defaultu karty kredytowej

Projekt klasyfikacyjny oparty na danych 30 000 tajwańskich klientów kart kredytowych.  
Cel: przewidzieć czy klient nie spłaci zobowiązania w następnym miesiącu.

**Dane:** [UCI - Default of Credit Card Clients](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients)

---

## Wyniki

| Model | ROC-AUC | Recall (próg 0.4) |
|---|---|---|
| LightGBM ✅ | ~0.78 | ~73% |
| XGBoost | ~0.78 | ~71% |
| Random Forest | ~0.77 | ~68% |
| Regresja Logistyczna | ~0.76 | ~67% |

Najlepszy model: **LightGBM z progiem decyzyjnym 0.4** — zapisany jako `model_lgbm.pkl`.

---

## Stack

`Python` `pandas` `scikit-learn` `LightGBM` `XGBoost` `matplotlib` `seaborn`

---

## Uruchomienie

```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost lightgbm joblib openpyxl xlrd
```

Otworzyć `projekt.ipynb` i uruchomić komórki po kolei.  
Plik `default_of_credit_card_clients.xls` musi być w tym samym folderze co notebook.