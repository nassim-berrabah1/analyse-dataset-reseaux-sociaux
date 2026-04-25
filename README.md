# 📱 Analyse d'un dataset de 5 000 utilisateurs — Réseaux sociaux
> Nettoyage, exploration statistique et visualisation d'un dataset de 5 000 utilisateurs d'un réseau social, décrit par 39 variables (qualitatives, quantitatives et dérivées). Le projet met en évidence des comportements utilisateurs souvent contre-intuitifs.

**Outils** : Python · Pandas · Matplotlib · Jupyter Notebook

---

## 📌 Contexte

**SAÉ Administration des Données** — BUT Informatique, Sciences des Données  
IUT de Villetaneuse, Université Sorbonne Paris Nord — février 2026  
Réalisé par : **Nassim Berrabah**, Aissatou Wade, Sara Younga

---

## ❓ Problématiques analysées

- Un utilisateur très engagé est-il forcément un utilisateur fidèle ?
- La consommation de vidéos varie-t-elle selon l'âge ?
- Les profils démographiques diffèrent-ils entre l'Europe et l'Asie ?

---

## 🧹 Nettoyage des données

Le dataset brut présentait plusieurs anomalies traitées avec Pandas :

| Problème | Solution |
|---|---|
| Âges aberrants (ex : 400 ans au lieu de 40) | Division par 10 |
| Caractères spéciaux dans les colonnes numériques (`###`, `???`) | Nettoyage via regex |
| Valeurs négatives dans les likes et messages | Suppression |
| Valeurs manquantes (NaN) | Conservées pour ne pas biaiser les stats |

---

## 📊 Visualisations & résultats

### 1. Distribution des âges — Europe vs Asie

<img width="1203" height="586" alt="Distribution des âges Europe vs Asie" src="https://github.com/user-attachments/assets/64d9b3ab-ff17-4581-9676-cf32c09a323a" />

- Les **18–44 ans** dominent en Europe
- Les **45 ans et plus** sont surreprésentés en Asie
- → Deux marchés aux profils démographiques opposés

---

### 2. Engagement vs risque d'abandon (churn)

<img width="1180" height="457" alt="Engagement vs churn" src="https://github.com/user-attachments/assets/b8b86d9e-e2e0-4b99-9914-5d35085e925e" />

- **Fort engagement ≠ fidélité assurée**
- Des "Power Users" très actifs présentent un risque de churn élevé
- → Suggère des bugs, limites du modèle gratuit ou fatigue publicitaire

---

### 3. Vidéos vues par tranche d'âge — Diagramme en violon

<img width="808" height="419" alt="Violon vidéos vues par tranche d'âge" src="https://github.com/user-attachments/assets/ac231499-820a-43f7-8f0e-6cdfec0e473e" />

- Les **55+** sont les plus gros consommateurs de vidéos
- Les **18–24 ans** ont la distribution la plus resserrée sur les faibles valeurs
- → Inversion des idées reçues sur les usages numériques

---

### 4. 🎉 Bonus — Easter egg caché dans les données

<img width="975" height="572" alt="Easter egg LEVEL" src="https://github.com/user-attachments/assets/ae3c8aba-c035-434d-9573-b3c14ba3925e" />

> Les coordonnées GPS (`geo_lat` / `geo_long`) des utilisateurs, tracées en nuage de points, forment le mot **"LEVEL"** — easter egg intentionnellement encodé par le professeur dans le dataset.

---

## 🔍 Conclusion

Ce projet montre que les comportements utilisateurs sont souvent à l'opposé des idées reçues : les plus engagés ne sont pas les plus fidèles, et ce sont les **seniors** qui consomment le plus de vidéos.

---

## 📁 Contenu du repo

```
📦 analyse-dataset-reseaux-sociaux/
 ┣ 📄 notebook.ipynb    ← Analyse complète (nettoyage + visualisations)
 ┣ 📄 rapport.pdf       ← Rapport de SAÉ
 ┗ 📄 README.md
```
