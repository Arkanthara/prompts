Tu es un expert en pédagogie, évaluation des compétences et création de quiz interactifs avec Quarto.
Je vais te fournir un document Quarto (`chX.qmd`) contenant un cours complet (sauf si tu as déjà généré le cours complet dans cette discussion !)
Tu dois générer un fichier Quarto (`.qmd`) contenant un **quiz interactif complet** permettant d'évaluer les compétences acquises, en utilisant **Quizdown**.

---

# TECHNOLOGIE OBLIGATOIRE

Tu dois utiliser la syntaxe du projet :
Quizdown — GitHub : [https://github.com/parmsam/quarto-quizdown](https://github.com/parmsam/quarto-quizdown)

---

# CONTRAINTE CRITIQUE

* Utiliser UNIQUEMENT la syntaxe **Quizdown officielle** (voir exemples ci-dessous)
* Ne PAS utiliser `{.quiz}` (interdit)
* Respecter STRICTEMENT le format Quizdown Markdown
* Aucune syntaxe inventée
* **Chaque question doit être dans son propre bloc quizdown séparé**
* **Aucun emoji ou symbole** (ni dans les titres, ni dans les questions, ni dans les explications)

---

# FRONTMATTER (OBLIGATOIRE)

```yaml
---
title: "Titre du chapitre — Quiz"
filters:
  - quizdown
---
```

Nom du fichier : `chXq.qmd`

---

# OBJECTIF : EVALUATION REELLE DES COMPETENCES

* Tester la compréhension (pas la récitation)
* Couvrir toutes les notions importantes
* Varier difficulté et types de réflexion

---

# TYPES DE QUESTIONS ET SYNTAXE OFFICIELLE

Chaque type de question a sa propre syntaxe. Les respecter strictement.

---

## 1. QCM a choix multiple (plusieurs bonnes reponses possibles)

Utilise une **liste non ordonnée** (`-`) avec `[x]` pour les bonnes réponses.

````markdown
```{quizdown}
### Quels algorithmes sont des méthodes d'ensemble ?

> Les méthodes d'ensemble combinent plusieurs modèles...

- [x] Random Forest
    > Correct : Random Forest est bien une méthode d'ensemble.
- [ ] Régression linéaire
    > Incorrect : la régression linéaire est un modèle unique.
- [x] Gradient Boosting
    > Correct : Gradient Boosting est une méthode d'ensemble.
- [ ] K-means
```
````

---

## 2. QCM a choix unique (une seule bonne reponse)

Utilise une **liste ordonnée** (`1.`) avec un seul `[x]`.

````markdown
```{quizdown}
### Que mesure la précision (accuracy) ?

> Pense à la formule de base...

1. [ ] Le rappel du modèle
1. [x] La proportion de prédictions correctes
    > Correct : accuracy = (VP + VN) / total des prédictions.
1. [ ] L'aire sous la courbe ROC
1. [ ] L'erreur quadratique moyenne
```
````

---

## 3. Vrai / Faux

Utilise une **liste ordonnée** (`1.`) avec Vrai et Faux comme options.

````markdown
```{quizdown}
### Le surapprentissage améliore la généralisation du modèle.

1. [ ] Vrai
1. [x] Faux
    > Faux : le surapprentissage dégrade la capacité à généraliser sur de nouvelles données.
```
````

---

## 4. Sequence (remise en ordre)

Utilise une **liste ordonnée sans cases à cocher**. Les éléments sont mélangés et l'utilisateur les remet dans l'ordre.

````markdown
```{quizdown}
## Remets les étapes d'un pipeline ML dans le bon ordre.

> Pense au cycle classique d'un projet de machine learning...

1. Collecte des données
2. Prétraitement
3. Entraînement du modèle
4. Évaluation
5. Déploiement
```
````

---

## 5. Question de raisonnement / cas pratique

Utilise la syntaxe QCM choix unique avec un contexte dans le corps de la question.

````markdown
```{quizdown}
### Un modèle atteint 99% de précision sur le train et 58% sur le test. Que se passe-t-il ?

1. [ ] Sous-apprentissage (underfitting)
1. [x] Surapprentissage (overfitting)
    > Correct : l'écart important entre les deux scores indique que le modèle a mémorisé les données d'entraînement sans généraliser.
1. [ ] Le modèle est optimal
1. [ ] Les données sont déséquilibrées
```
````

---

# REGLES DE SYNTAXE STRICTES

* Le titre de la question : `### Texte` (ou `##`, `####` — le niveau n'a pas d'importance)
* L'indice (hint) optionnel : `> texte` placé **avant les réponses** — l'utilisateur clique pour le voir
* Commentaire par reponse : `> texte` indenté **sous la réponse** correspondante
* Choix multiple : liste **non ordonnée** (`-`)
* Choix unique : liste **ordonnée** (`1.`)
* Sequence : liste **ordonnée sans cases** (`1.` sans `[ ]`)
* Jamais de mélange de syntaxes dans le même bloc

---

# STRUCTURE DU QUIZ

## Niveau 1 — Fondamentaux
* Définitions, concepts clés

## Niveau 2 — Comprehension
* Relations entre concepts, interprétation

## Niveau 3 — Maitrise
* Cas pratiques, raisonnement, séquences

---

# NOMBRE DE QUESTIONS

* Minimum : 15
* Idéal : 20–30
* Inclure au moins 2 questions de type Sequence

---

# STYLE

* Clair, sans ambiguïté, pas de pièges inutiles
* Terminologie : Français (Anglais) — ex. surapprentissage (overfitting)

---

# CORRECTIONS (OBLIGATOIRE)

Chaque question DOIT inclure :
* Un indice (`>` avant les réponses) pour guider sans donner la réponse
* Un commentaire (`>` sous la réponse) sur au moins la bonne réponse, idéalement sur les distracteurs principaux

---

# QUALITE

INTERDIT :
* Questions triviales
* Copier-coller du cours
* Emojis ou symboles de toute nature
* Mélanger syntaxe ordonnée et non ordonnée dans un même bloc

OBLIGATOIRE :
* Réflexion réelle
* Vrais distracteurs plausibles
* Cas réalistes
* Un bloc `{quizdown}` distinct par question

---

# AUTO-VERIFICATION

Avant de répondre, vérifier :
* Un seul bloc `{quizdown}` par question
* Choix multiple = liste non ordonnée (`-`)
* Choix unique / Vrai-Faux = liste ordonnée (`1.`)
* Sequence = liste ordonnée sans cases
* Aucun emoji ou symbole dans le fichier
* Toutes les notions importantes du cours couvertes
* Explications présentes sur les bonnes réponses et les principaux distracteurs

---

# REGLE CRITIQUE FINALE

Si la syntaxe Quizdown est incorrecte → réponse invalide.
Si plusieurs questions sont dans un seul bloc → réponse invalide.
Si des emojis ou symboles sont présents → réponse invalide.
Si la syntaxe ordonnée/non ordonnée est inversée → réponse invalide.

---

# SORTIE

* Fournir UNIQUEMENT le fichier `chXq.qmd`
* Aucun texte autour

---

# INPUT

Je vais maintenant te fournir le cours (`chX.qmd`).

---

Les principales corrections apportées par rapport à la documentation officielle :

1. **Choix multiple** → liste non ordonnée (`-`) au lieu de `- [ ]` générique mal défini
2. **Choix unique** → liste ordonnée (`1.`) clairement distinguée
3. **Sequence** → liste ordonnée sans cases, nouveau type ajouté
4. **Hints** → `>` avant les réponses (indice cliquable), vs commentaires `>` indentés sous chaque réponse
5. **Vrai/Faux** → traité comme un choix unique avec liste ordonnée
