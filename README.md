# AI-Powered Dashboard – Customer Intelligence bancaire

**TP de Master | Prompt Engineering + Data Analytics + Data Visualization**

> Objectif : utiliser l'IA générative comme copilote pour concevoir, réaliser et auditer un tableau de bord de Customer Intelligence bancaire avec **Looker Studio ou Tableau Public**. L'IA aide à raisonner et à documenter ; l'étudiant reste responsable des calculs, des choix visuels et de la validation métier.

## 1. Mission

Vous êtes analyste data dans une banque. La direction souhaite mieux comprendre son portefeuille clients, l'activité transactionnelle, les crédits et les retours clients. À partir du dataset fourni, vous devez produire un dashboard décisionnel et démontrer comment le Prompt Engineering a contribué à sa conception et à son amélioration.

**Question directrice :** quelles informations fiables et actionnables un responsable de la relation client peut-il tirer de ces données ?

## 2. Compétences visées

- Formuler des prompts contextualisés, précis et itératifs.
- Explorer un jeu de données et expliciter sa granularité.
- Définir des KPI avec des formules vérifiables.
- Choisir des visualisations adaptées à des questions métier.
- Traduire un cahier de conception en dashboard dans Looker Studio ou Tableau Public.
- Auditer les agrégations, la lisibilité, les filtres et les limites d'interprétation.
- Documenter les décisions, les prompts, les réponses IA et les corrections humaines.

## 3. Outils

- **Obligatoire :** ChatGPT ou un autre assistant IA génératif.
- **Au choix :** Looker Studio **ou** Tableau Public.
- **Préparation facultative :** Excel, Google Sheets ou Python/pandas.

Aucun code Python n'est exigé pour réaliser le dashboard. Le travail porte d'abord sur la maîtrise du prompting et de l'outil de datavisualisation.

## 4. Données et précautions

Fichier : `data/banking_dataset_anonymized.csv` (version d'exercice anonymisée).

Le fichier comporte des informations relatives aux clients, comptes, transactions, prêts, cartes et feedbacks. **Ne supposez pas que chaque ligne représente un client unique.** Avant tout calcul, identifiez la granularité réelle et recherchez les répétitions liées aux transactions, prêts ou cartes.

Points de vigilance :
- Comptez les clients avec un identifiant distinct, pas avec le nombre de lignes.
- Ne sommeez pas un solde de compte répété sur plusieurs transactions.
- Ne sommeez pas un montant de prêt répété sur plusieurs lignes.
- Distinguez les montants transactionnels des soldes après transaction.
- Vérifiez les valeurs manquantes, doublons, dates et catégories.
- Les données sont synthétiques/d'exercice : ne tirez aucune conclusion sur une banque réelle.
- Ne cherchez pas à réidentifier les personnes et ne réintroduisez aucune donnée personnelle.

## 5. Déroulement du TP (8 à 10 heures)

| Étape | Travail | Durée indicative | Livrable |
|---|---|---:|---|
| 1 | Explorer les données avec l'IA | 1 h | Diagnostic et dictionnaire |
| 2 | Définir et vérifier les KPI | 1 h | Catalogue KPI |
| 3 | Concevoir les visualisations | 1 h | Storyboard |
| 4 | Générer le cahier de conception | 1 h | Spécifications du dashboard |
| 5 | Construire le dashboard | 3 à 4 h | Dashboard publié ou captures |
| 6 | Auditer et améliorer avec l'IA | 1 h | Rapport d'audit |
| 7 | Présenter les résultats | 30 min | Soutenance de 10 min |

## 6. Dashboard attendu

Construire un dashboard de **3 pages/onglets** :

### Page 1 – Vue exécutive
- Nombre de clients distincts (si l'identifiant permet bien de les distinguer).
- Nombre de transactions.
- Montant total des transactions (après validation de la granularité).
- Répartition des types de comptes.
- Évolution des transactions dans le temps.
- Filtres pertinents : période, type de compte, agence si disponible.

### Page 2 – Customer Intelligence
- Répartition des clients par tranche d'âge.
- Répartition par ville ou genre si ces dimensions sont exploitables et pertinentes.
- Comparaison des soldes par type de compte, avec une agrégation qui évite les doubles comptes.
- Segments clients construits et documentés (pas de segmentation arbitraire présentée comme vérité).
- Filtres : ville, type de compte, segment.

### Page 3 – Crédits & relation client
- Répartition des prêts par type et statut.
- Montants de prêts selon une méthode de déduplication explicitée.
- Répartition des feedbacks par type et statut de résolution.
- Indicateurs de délais de résolution uniquement si les dates sont cohérentes.
- Filtres : type de prêt, statut, type de feedback.

**Exigence :** chaque page doit répondre à une question métier. Évitez les graphiques décoratifs et les KPI impossibles à interpréter.

## 7. Workflow de prompting

Utilisez les six prompts du dossier `prompts/` dans l'ordre. Pour chaque étape :
1. Joignez le dataset ou un extrait non sensible à l'assistant.
2. Donnez le contexte métier et l'objectif.
3. Demandez un résultat structuré et vérifiable.
4. Vérifiez les réponses à l'aide des données et de l'outil.
5. Reformulez le prompt si le résultat est vague ou erroné.
6. Conservez le prompt initial, la réponse utile et votre correction humaine.

Les prompts sont des points de départ : personnalisez-les et montrez vos itérations.

## 8. Livrables obligatoires

Déposez dans votre dépôt :
- `livrables/diagnostic_donnees.md`
- `livrables/catalogue_kpi.md`
- `livrables/storyboard.md`
- `livrables/cahier_conception.md`
- `livrables/journal_prompting.md` : prompts, réponses sélectionnées, itérations et vérifications.
- `livrables/rapport_audit.md`
- `livrables/lien_dashboard.md` : URL publique ou captures si publication impossible.
- `livrables/analyse_metier.md` : 5 constats maximum, chacun appuyé par un KPI/graphique.
- `captures/` : captures des trois pages et des filtres.
- `README.md` complété avec les noms du groupe, outil choisi et procédure de reproduction.

## 9. Évaluation (/20)

| Critère | Points |
|---|---:|
| Qualité du diagnostic et analyse de granularité | 3 |
| Qualité des prompts et des itérations documentées | 3 |
| Pertinence et vérifiabilité des KPI | 3 |
| Storyboard et choix des visualisations | 2 |
| Maîtrise de Looker Studio ou Tableau Public | 4 |
| Interactivité, lisibilité et ergonomie | 2 |
| Audit critique et améliorations | 2 |
| Présentation et interprétation métier | 1 |
| **Total** | **20** |

## 10. Règles de qualité

- Une réponse de l'IA n'est jamais une preuve : vérifiez les formules et les résultats.
- Ne demandez pas à l'IA de « faire un beau dashboard » sans contexte, public, questions et contraintes.
- Un KPI doit avoir une définition, une formule, une unité, une granularité et une limite.
- Une visualisation doit servir une question métier.
- N'affichez pas de données personnelles.
- Le dashboard doit rester compréhensible sans explication orale.

## 11. Démarrage rapide

1. Clonez ou téléchargez ce dépôt.
2. Lisez les six prompts dans `prompts/`.
3. Importez le CSV dans Google Sheets/Looker Studio ou Tableau Public.
4. Complétez les modèles du dossier `templates/`.
5. Construisez les trois pages, puis réalisez l'audit.

Voir les guides : `guides/looker_studio.md` et `guides/tableau_public.md`.
# AI-Powered-Dashboard-Customer-Intelligence
