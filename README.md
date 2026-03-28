#  RNN & LSTM & GRU — Prédiction de Séries Temporelles

Implémentation et comparaison de trois architectures de réseaux de neurones récurrents
(RNN, LSTM, GRU) appliquées à la prédiction du prix de l'action Apple (AAPL).

---

##  Objectif

Explorer et comparer les performances des modèles RNN, LSTM et GRU sur une tâche
de prédiction de séries temporelles financières, en mettant en évidence leurs
avantages et limitations respectifs.

---

##  Dataset

- **Source** : Yahoo Finance via `yfinance`
- **Ticker** : AAPL (Apple Inc.)
- **Période** : 01/01/2010 — 31/12/2023
- **Fréquence** : Quotidienne
- **Variable cible** : Prix de clôture (`Close`)

---
##  Résultats comparatifs

| Modèle | Paramètres | Val Loss finale | Vanishing Gradient | Vitesse |
|--------|-----------|-----------------|-------------------|---------|
| RNN (1 couche) | 2 651 | 0.0049 |  Oui |  Très rapide |
| RNN (2 couches) | 4 041 | 0.0073 |  Oui |  Rapide |
| LSTM (1 couche) | 10 451 | 0.0102 |  Non |  Lent |
| LSTM (2 couches) | 16 101 | 0.0143 |  Non |  Très lent |
| GRU (1 couche) | 8 001 | 0.0072 |  Non |  Rapide |
| GRU (2 couches) | ~23 000 | 0.0061 |  Non |  Moyen |

>  **Meilleur compromis : GRU (1 couche)** — Val Loss de 0.0072 avec seulement
> 8 001 paramètres, sans vanishing gradient et avec une vitesse d'entraînement rapide.


---

##  Technologies utilisées

- Python 3.12
- TensorFlow / Keras
- yfinance
- scikit-learn
- Matplotlib
- NumPy / Pandas

---

##  Lancer le projet
```bash
pip install tensorflow yfinance scikit-learn matplotlib numpy pandas
```

Ouvrir le notebook :
```bash
jupyter notebook RNN_LSTM_GRU.ipynb
```

Ou directement sur Google Colab :

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](VOTRE_LIEN_COLAB)

---

##  Auteure

**Zineb El Ouardi** — Étudiante M2 en Intelligence Artificielle  

