# Assurance vie : Travailleurs du BTP

Projet réalisé dans le cadre du Master 2 IRFA (Ingénierie Financière, Risque et Assurance) à l'Université Paris 1 Panthéon-Sorbonne  cours *Assurance vie*, année 2025-2026.

## Objectif

Mesurer le biais de tarification induit par l'utilisation de tables de mortalité standard (TH 00-02, TGH 05) pour une population à surmortalité structurelle : les travailleurs du BTP. Deux produits sont étudiés : une **assurance temporaire décès** et une **rente viagère différée**.

## Structure du projet

```
├── Life_Insurance.ipynb   # Code Python (modélisation, tarification, provisionnement)
└── Life_insurance.pdf     # Rapport complet
```

## Méthodologie

1. **Modélisation de la mortalité** : ajustement d'un modèle de Gompertz (µ(x) = B·cˣ) par régression log-linéaire sur des taux ajustés par des facteurs de surmortalité λₓ décroissants avec l'âge.

2. **Construction des tables** : tables complètes (âges 40–90) pour la population standard et BTP, avec courbes de survie comparées.

3. **Tarification** : calcul des VAP et primes nettes/brutes (chargement 12 %, taux technique r = 2,5 %) pour les deux contrats souscrits à 40 ans.

4. **Provisionnement & rentabilité** : provision mathématique par récurrence, décomposition du profit annuel (marge financière + chargement), VAN au taux i = 4 %.

## Stack technique

Python 3 · `numpy` · `pandas` · `matplotlib` · `sklearn` (régression linéaire)

## Auteurs

Reda Allab · Thibaud Collet · Ethan Bennady
