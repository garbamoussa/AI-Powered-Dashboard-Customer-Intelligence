# Prompt 1 – Explorer et qualifier les données

## Objectif
Obtenir un diagnostic structuré sans laisser l'IA inventer la signification des champs.

## Prompt à adapter

Tu es un data analyst senior spécialisé en Customer Intelligence bancaire.

Contexte :
- Projet : conception d'un dashboard décisionnel pour une direction de la relation client.
- Public cible : responsables marketing, relation client et pilotage.
- Fichier : `banking_dataset_anonymized.csv`.
- Les données peuvent contenir plusieurs lignes par client en raison des transactions, prêts, cartes ou feedbacks.

Analyse le fichier fourni et produis :

1. Une synthèse du nombre de lignes et de colonnes.
2. Un dictionnaire des variables : nom, type apparent, rôle possible, valeurs/exemples et précautions.
3. Une hypothèse de granularité de la table, avec les indices qui la soutiennent.
4. Les identifiants candidats et les tests à effectuer pour mesurer les doublons.
5. Les variables utiles pour analyser clients, comptes, transactions, crédits et feedbacks.
6. Les valeurs manquantes, incohérences de dates, catégories rares et valeurs atypiques que tu peux réellement constater.
7. Les risques de double comptage pour les soldes, montants de prêts et clients.
8. Les questions auxquelles les données ne permettent pas de répondre.

Présente les constats dans un tableau. Distingue explicitement :
- constat observé dans les données ;
- hypothèse à vérifier ;
- recommandation.

N'invente ni définition métier ni résultat statistique. Si tu ne peux pas calculer une information, indique le test ou la formule nécessaire.

## Itération attendue
Après la première réponse, demande à l'IA de détailler les risques de double comptage et propose une méthode de vérification reproductible dans l'outil choisi.

## Vérification humaine
- Comparer les nombres de lignes/colonnes avec le fichier.
- Vérifier le nombre d'identifiants clients distincts.
- Examiner quelques identifiants présents plusieurs fois.
- Confirmer la granularité avant les agrégations.
