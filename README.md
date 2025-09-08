# Analyse de Portefeuille et Optimisation du Ratio de Sharpe

Ce projet applique des techniques de finance quantitative et de data science afin d analyser la performance de plusieurs actions technologiques (AAPL, MSFT, GOOGL, AMZN, TSLA) et d optimiser un portefeuille selon le ratio de Sharpe.

---

## Fonctionnalites

* Telechargement automatique des donnees boursieres via `yfinance`
* Nettoyage et transformation des donnees (Close, Open, Volume)
* Integration des jours feries US pour filtrer les donnees de marche
* Calculs financiers :

  * Rendements simples et logarithmiques
  * Rendement cumule
  * Volatilite annualisee (fenetre mobile de 30 jours)
  * Ratio de Sharpe par action
* Optimisation du portefeuille avec `scipy.optimize` :

  * Maximisation du ratio de Sharpe
  * Contraintes de ponderation (somme = 1, pas de vente a decouvert)
* Visualisations avec `matplotlib` :

  * Performance normalisee des actions (base 100)
  * Rendements cumules
  * Volatilite annualisee
  * Bar chart du ratio de Sharpe

---

## Technologies utilisees

* Python 3.x
* yfinance
* pandas
* numpy
* matplotlib
* scipy
* holidays

---

## Ameliorations possibles

* Ajouter d autres actions ou secteurs pour diversifier l analyse
* Tester differentes frequences (hebdomadaire, mensuelle)
* Comparer l optimisation avec d autres methodes (ex. Markowitz classique)
* Integrer une interface interactive (Dash, Streamlit)

---

## Avertissement

Ce projet est realise a des fins educatives.
Il ne constitue en aucun cas une recommandation d investissement.

---
