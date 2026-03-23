# 🧠 PROMPT 3 — QUIZ INTERACTIF QUARTO AVEC QUIZDOWN

Tu es un expert en pédagogie, évaluation des compétences et création de quiz interactifs avec Quarto.

Je vais te fournir un document Quarto (`chX.qmd`) contenant un cours complet (sauf si tu as déjà généré le cours complet dans cette discussion !)

Tu dois générer un fichier Quarto (`.qmd`) contenant un **quiz interactif complet** permettant d’évaluer les compétences acquises, en utilisant **Quizdown**.

---

# ⚠️ TECHNOLOGIE OBLIGATOIRE

Tu dois utiliser la syntaxe du projet :

👉 Quizdown

GitHub : [https://github.com/parmsam/quarto-quizdown](https://github.com/parmsam/quarto-quizdown)

---

# ⚠️ CONTRAINTE CRITIQUE

* Utiliser UNIQUEMENT la syntaxe **Quizdown**
* Ne PAS utiliser `{.quiz}` (interdit)
* Respecter STRICTEMENT le format Quizdown Markdown
* Aucune syntaxe inventée

---

# ⚠️ FRONTMATTER (OBLIGATOIRE)

```yaml
---
title: "Titre du chapitre — Quiz"
filters:
  - quizdown
---
```

---

Nom du fichier : chXq.qmd

---

# 🎯 OBJECTIF : ÉVALUATION RÉELLE DES COMPÉTENCES

* Tester la compréhension (pas la récitation)
* Couvrir toutes les notions importantes
* Varier difficulté et types de réflexion

---

# 🧠 TYPES DE QUESTIONS (OBLIGATOIRE)

---

## 1. QCM (single et multiple)

### Exemple Quizdown (OBLIGATOIRE À RESPECTER) :

```markdown
### Question

Quelle est la bonne définition du surapprentissage (overfitting) ?

- [ ] Un modèle trop simple
- [x] Un modèle qui s’adapte trop aux données d’entraînement
- [ ] Un modèle aléatoire
- [ ] Une erreur de compilation

> 💡 Explication :
> Le surapprentissage correspond à une mémorisation excessive des données.
```

---

## 2. Vrai / Faux

```markdown
### Question

Le surapprentissage améliore la généralisation.

- [ ] Vrai
- [x] Faux

> ❌ Faux :
> Il dégrade la capacité à généraliser.
```

---

## 3. Questions ouvertes (réponse libre)

```markdown
### Question

Explique le concept de biais (bias).

> ✅ Réponse attendue :
> Le biais correspond à ...
```

---

## 4. Questions de raisonnement

```markdown
### Cas pratique

Un modèle a 100% de précision sur le train et 60% sur le test.

Que se passe-t-il ?

- [ ] Sous-apprentissage
- [x] Surapprentissage
- [ ] Bon modèle
- [ ] Données équilibrées

> 💡 Analyse :
> Cela indique un problème de généralisation.
```

---

# 📊 STRUCTURE DU QUIZ

## 🟢 Niveau 1 — Fondamentaux

* Définitions
* Concepts clés

## 🟡 Niveau 2 — Compréhension

* Relations
* Interprétation

## 🔴 Niveau 3 — Maîtrise

* Cas pratiques
* Raisonnement

---

# 📏 NOMBRE DE QUESTIONS

* Minimum : 15
* Idéal : 20–30

---

# ✍️ STYLE

* Clair
* Sans ambiguïté
* Pas de pièges inutiles

---

# 🌍 TERMINOLOGIE

Toujours :

* Français (Anglais)

---

# 🧠 CORRECTIONS (OBLIGATOIRE)

Chaque question DOIT inclure :

* Explication claire avec :

```
> 💡 Explication :
```

ou

```
> ✅ Réponse :
```

---

# ⚠️ QUALITÉ

INTERDIT :

* Questions triviales
* Copier-coller du cours

OBLIGATOIRE :

* Réflexion
* Vrais distracteurs
* Cas réalistes

---

# 🧪 AUTO-VÉRIFICATION

Avant de répondre :

* Syntaxe Quizdown correcte
* Toutes les notions importantes couvertes
* Réponses justes
* Explications présentes

---

# ⚠️ RÈGLE CRITIQUE FINALE

Si la syntaxe Quizdown est incorrecte → réponse invalide.

---

# 📌 SORTIE

* Fournir UNIQUEMENT le fichier `chXq.qmd`
* Aucun texte autour

---

# 📥 INPUT

Je vais maintenant te fournir le cours (`chX.qmd`)